# Graphify Case Study: Exploring the Seismic Foundation Model

## Overview
This repository contains a case study developed for a doctoral-level course. It investigates the practical application of **Graphify**—an AI-powered knowledge graph and reasoning tool—to extract structured technical knowledge from a complex machine learning codebase. 

The primary target of this analysis is the [**Seismic Foundation Model (SFM)**](https://arxiv.org/abs/2309.02791) (arXiv: 2309.02791), specifically focusing on mapping the data flow and architectural components of its downstream **Seismic Denoising** task.

## Objectives
* Trace the complete data flow of the denoising task, from the Dataloader to the final regression head [3, 4].
* Understand the specific architecture and loss functions employed during fine-tuning.
* Critically evaluate the trade-offs, strengths, and limitations of using Graphify for codebase navigation and reasoning.

## Core Architectural Findings: The Denoising Pipeline

Through iterative querying and manual cross-referencing, we mapped the complete end-to-end data flow for the SFM Denoising task:

### 1. Initialization and Dataloader
* **Trigger:** The pipeline is activated via the `finetune-Denoise.sh` script, which selects the `vit_base_patch16` backbone.
* **Data Processing:** The `DenoiseSet` class reads raw `.dat` binary files (in `float32`) from the `seismic` and `label` directories. 
* **Batching:** The data is reshaped and packaged by the DataLoader into batches of spatial tensors structured as `[B, 1, 224, 224]`.

### 2. Model Architecture and Head
* **Vision Transformer:** The batches are fed into the `VisionTransformer` class (located in `models_Regression.py`).
* **Feature Extraction:** The `forward_features` function processes the input through the patch embedding, transformer blocks, and a decoder.
* **Segmentation Head:** The output is routed to the `segmentation_head`, which compresses the extracted features into a single channel (1D), producing a dense prediction that maintains the exact spatial resolution of the input image.

### 3. Crucial Insight: Residual Noise Learning
The most significant architectural finding relates to how the model actually learns to denoise:
* **Training Phase:** The model's raw prediction is evaluated by the `forward_loss` function, which optimizes the network using an equally weighted mix (0.5 / 0.5) of **MSE** and **MSSSIM** metrics.
* **Evaluation Phase:** During validation (`evaluateRegression`), the output is mathematically redefined as `output = images - output`.
* **Conclusion:** The model **does not** learn to predict the clean seismic image directly. Instead, it acts as a residual learner, estimating the **noise component** itself. The clean signal is reconstructed by subtracting this predicted noise from the original input image.

## Graphify Evaluation & Trade-offs

While Graphify proved to be a powerful assistant, its usage in an academic/technical context comes with clear trade-offs:

### Strengths
* **Search Space Reduction:** Significantly accelerated initial comprehension by pinpointing the exact classes (`DenoiseSet`, `segmentation_head`) and scripts involved.
* **Visual Artifacts:** Successfully recovered and correctly described relationship graphs from the repository.

### Limitations
* **High Token Cost:** Processing the repository consumed approximately 45,000 tokens.
* **Formatting Friction:** Required manual intervention to normalize the JSON graph structure (changing `edges` to `links`) before the query mode could function.
* **Fragmented Systemic View:** The tool initially isolated responsibilities but failed to connect the end-to-end logic autonomously. The crucial "residual learning" insight was only discovered because human expertise guided the cross-referencing between the training script (`main_finetune.py`) and the evaluation loop (`engine_finetune.py`).


## How to Obtain the Results
To replicate this analysis and query the codebase, follow these steps:

1. **Install Prerequisites:** Install the **Graphify** extension in VSCode to be used alongside the GitHub Copilot extension.
2. **Clone the Repository:** Clone the target SFM codebase to your local machine.
   ```bash
   git clone https://github.com/shenghanlin/SeismicFoundationModel
   ```
3. **Create the Knowledge Graph:** Use Graphify to ingest the repository and generate the Knowledge Graph representing the codebase's architecture. (Note: If you encounter query errors, ensure the generated `graph.json` uses `links` instead of `edges`).
4. **Run Queries:** Open the Copilot chat in VSCode and use the `/graphify query` command to ask technical questions. For example:
   > `/graphify` query "Explique, passo a passo, como o dado flui na tarefa Denoise, desde a entrada no dataloader até a saída final do modelo."

## Conclusion
Graphify does not replace meticulous technical reading, but it acts as a highly effective academic co-pilot. It creates navigable investigation trails out of scattered codebases, allowing researchers to focus their cognitive effort on deep architectural logic rather than getting lost in file directories.