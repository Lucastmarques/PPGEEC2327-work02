# Graph Report - SeismicFoundationModel  (2026-04-27)

## Corpus Check
- Corpus is ~49,217 words - fits in a single context window. You may not need a graph.

## Summary
- 502 nodes · 814 edges · 33 communities detected
- Extraction: 80% EXTRACTED · 20% INFERRED · 0% AMBIGUOUS · INFERRED: 164 edges (avg confidence: 0.71)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- [[_COMMUNITY_Community 0|Community 0]]
- [[_COMMUNITY_Community 1|Community 1]]
- [[_COMMUNITY_Community 2|Community 2]]
- [[_COMMUNITY_Community 3|Community 3]]
- [[_COMMUNITY_Community 4|Community 4]]
- [[_COMMUNITY_Community 5|Community 5]]
- [[_COMMUNITY_Community 6|Community 6]]
- [[_COMMUNITY_Community 7|Community 7]]
- [[_COMMUNITY_Community 8|Community 8]]
- [[_COMMUNITY_Community 9|Community 9]]
- [[_COMMUNITY_Community 10|Community 10]]
- [[_COMMUNITY_Community 11|Community 11]]
- [[_COMMUNITY_Community 12|Community 12]]
- [[_COMMUNITY_Community 13|Community 13]]
- [[_COMMUNITY_Community 14|Community 14]]
- [[_COMMUNITY_Community 15|Community 15]]
- [[_COMMUNITY_Community 16|Community 16]]
- [[_COMMUNITY_Community 17|Community 17]]
- [[_COMMUNITY_Community 18|Community 18]]
- [[_COMMUNITY_Community 19|Community 19]]
- [[_COMMUNITY_Community 20|Community 20]]
- [[_COMMUNITY_Community 22|Community 22]]
- [[_COMMUNITY_Community 23|Community 23]]
- [[_COMMUNITY_Community 24|Community 24]]
- [[_COMMUNITY_Community 25|Community 25]]
- [[_COMMUNITY_Community 26|Community 26]]
- [[_COMMUNITY_Community 27|Community 27]]
- [[_COMMUNITY_Community 28|Community 28]]
- [[_COMMUNITY_Community 29|Community 29]]
- [[_COMMUNITY_Community 30|Community 30]]
- [[_COMMUNITY_Community 31|Community 31]]
- [[_COMMUNITY_Community 32|Community 32]]
- [[_COMMUNITY_Community 33|Community 33]]

## God Nodes (most connected - your core abstractions)
1. `SynchronizedBatchNorm2d` - 22 edges
2. `main()` - 21 edges
3. `SyncMaster` - 20 edges
4. `MaskedAutoencoderViT` - 19 edges
5. `DRN` - 16 edges
6. `MetricLogger` - 14 edges
7. `SegmentationMetric` - 12 edges
8. `VisionTransformer` - 11 edges
9. `Block` - 11 edges
10. `_SynchronizedBatchNorm` - 11 edges

## Surprising Connections (you probably didn't know these)
- `main()` --calls--> `interpolate_pos_embed()`  [INFERRED]
  /mnt/c/Users/Lucas Torres/Documents/Acadêmico/Doutorado/Tópicos Especiais em Deep Learning/SeismicFoundationModel/SFM-Finetune/main_finetune.py → /mnt/c/Users/Lucas Torres/Documents/Acadêmico/Doutorado/Tópicos Especiais em Deep Learning/SeismicFoundationModel/SFM-Finetune/util/pos_embedtest.py
- `Constructs a ResNet-101 model.     Args:         pretrained (bool): If True, ret` --uses--> `SynchronizedBatchNorm2d`  [INFERRED]
  /mnt/c/Users/Lucas Torres/Documents/Acadêmico/Doutorado/Tópicos Especiais em Deep Learning/SeismicFoundationModel/SFM-Finetune/modules/modeling/backbone/resnet.py → /mnt/c/Users/Lucas Torres/Documents/Acadêmico/Doutorado/Tópicos Especiais em Deep Learning/SeismicFoundationModel/SFM-Finetune/modules/modeling/sync_batchnorm/batchnorm.py
- `Modified Alighed Xception` --uses--> `SynchronizedBatchNorm2d`  [INFERRED]
  /mnt/c/Users/Lucas Torres/Documents/Acadêmico/Doutorado/Tópicos Especiais em Deep Learning/SeismicFoundationModel/SFM-Finetune/modules/modeling/backbone/xception.py → /mnt/c/Users/Lucas Torres/Documents/Acadêmico/Doutorado/Tópicos Especiais em Deep Learning/SeismicFoundationModel/SFM-Finetune/modules/modeling/sync_batchnorm/batchnorm.py
- `evaluate()` --calls--> `accuracy()`  [INFERRED]
  /mnt/c/Users/Lucas Torres/Documents/Acadêmico/Doutorado/Tópicos Especiais em Deep Learning/SeismicFoundationModel/SFM-Finetune/engine_finetune.py → /mnt/c/Users/Lucas Torres/Documents/Acadêmico/Doutorado/Tópicos Especiais em Deep Learning/SeismicFoundationModel/SFM-Finetune/util/tools.py
- `evaluateRegression()` --calls--> `msssim()`  [INFERRED]
  /mnt/c/Users/Lucas Torres/Documents/Acadêmico/Doutorado/Tópicos Especiais em Deep Learning/SeismicFoundationModel/SFM-Finetune/engine_finetune.py → /mnt/c/Users/Lucas Torres/Documents/Acadêmico/Doutorado/Tópicos Especiais em Deep Learning/SeismicFoundationModel/SFM-Finetune/util/msssim.py

## Hyperedges (group relationships)
- **he_pretrain_pipeline** — file_main_pretrain_py, file_engine_pretrain_py, file_models_mae_py, file_readme_pretrain_md_data [INFERRED]
- **he_finetune_utils** — file_metrics_py, file_misc_py, file_msssim_py, file_pos_embed_py, file_pos_embedtest_py, file_tools_py [INFERRED]
- **he_data_documentation** — file_readme_denoise_md, file_readme_facies_md, file_readme_geobody_md, file_readme_interpolation_md, file_readme_inversion_md, file_readme_pretrain_md_data [INFERRED]

## Communities

### Community 0 - "Community 0"
Cohesion: 0.0
Nodes (25): Attention_block, AttU_Net, ContractiveBlock, conv_block, conv_block_nested, ConvolutionBlock, ExpansiveBlock, NestedUNet (+17 more)

### Community 1 - "Community 1"
Cohesion: 0.0
Nodes (33): _BatchNorm, Compute the mean and standard-deviation with sum and square-sum. This method, r"""Applies Synchronized Batch Normalization over a 2d or 3d input that is seen, r"""Applies Batch Normalization over a 4d input that is seen as a mini-batch, sum over the first and last dimention, r"""Applies Batch Normalization over a 5d input that is seen as a mini-batch, add new dementions at the front and the tail, Reduce the sum and square-sum, compute the statistics, and broadcast it. (+25 more)

### Community 2 - "Community 2"
Cohesion: 0.0
Nodes (27): evaluate(), evaluateRegression(), evaluateRegressionold(), train_one_epoch(), train_one_epoch(), adjust_learning_rate(), Decay the learning rate with half-cycle cosine after warmup, main() (+19 more)

### Community 3 - "Community 3"
Cohesion: 0.0
Nodes (11): RandomResizedCrop, RandomResizedCrop for matching TF/TPU implementation: no for-loop is used.     T, build_dataset(), build_transform(), DenoiseSet, FacesSet, InterpolationSet, ReflectSet (+3 more)

### Community 4 - "Community 4"
Cohesion: 0.0
Nodes (18): mae_vit_base_patch16_dec256d4b(), mae_vit_base_patch16_dec512d8b(), mae_vit_huge_patch14_dec512d8b(), mae_vit_large_patch16_dec256d4b(), mae_vit_large_patch16_dec512d8b(), mae_vit_small_patch16_dec512d8b(), MaskedAutoencoderViT, x: (N, L, patch_size**2 *3)         imgs: (N, 3, H, W) (+10 more)

### Community 5 - "Community 5"
Cohesion: 0.0
Nodes (15): BasicBlock, Bottleneck, conv3x3(), DRN, DRN_A, drn_a_50(), drn_c_26(), drn_c_42() (+7 more)

### Community 6 - "Community 6"
Cohesion: 0.0
Nodes (10): build_backbone(), Bottleneck, Constructs a ResNet-101 model.     Args:         pretrained (bool): If True, ret, ResNet, ResNet101(), AlignedXception, Block, fixed_padding() (+2 more)

### Community 7 - "Community 7"
Cohesion: 0.0
Nodes (13): Conv2dReLU, DecoderBlock, DecoderCup, mae_vit_small_patch16(), MLAHead, Vision Transformer with support for global average pooling, Vision Transformer with support for patch or hybrid CNN input stage, SegmentationHead (+5 more)

### Community 8 - "Community 8"
Cohesion: 0.0
Nodes (18): get_init_file(), get_shared_folder(), main(), parse_args(), Trainer, accuracy(), backup_code(), list_files() (+10 more)

### Community 9 - "Community 9"
Cohesion: 0.0
Nodes (6): ASPP, _ASPPModule, build_aspp(), build_decoder(), Decoder, DeepLab

### Community 10 - "Community 10"
Cohesion: 0.0
Nodes (10): Conv2dReLU, DecoderBlock, DecoderCup, mae_vit_small_patch16(), Vision Transformer with support for global average pooling, SegmentationHead, VisionTransformer, vit_base_patch16() (+2 more)

### Community 11 - "Community 11"
Cohesion: 0.0
Nodes (9): forward_loss(), imgs: [N, 3, H, W]         pred: [N, L, p*p*3]         mask: [N, L], 0 is keep,, create_window(), gaussian(), msssim(), PSNR, # TODO: store window between calls if possible, # TODO: store window between calls if possible (+1 more)

### Community 12 - "Community 12"
Cohesion: 0.0
Nodes (5): refer to https://github.com/jfzhang95/pytorch-deeplab-xception/blob/master/utils, Mean Pixel Accuracy(MPA，均像素精度)：是PA的一种简单提升，计算每个类内被正确分类像素数的比例，之后求所有类的平均。         :, 同FCN中score.py的fast_hist()函数,计算混淆矩阵         :param imgPredict:         :param img, FWIoU，频权交并比:为MIoU的一种提升，这种方法根据每个类出现的频率为其设置权重。         FWIOU =     [(TP+FN)/(TP+FP, SegmentationMetric

### Community 13 - "Community 13"
Cohesion: 0.0
Nodes (14): Finetune Engine, Main Finetune Script, Regression Models, Segmentation Models, MAE Models, UNet Models, ASPP Module, Model Backbones (ResNet, MobileNet, Xception, DRN) (+6 more)

### Community 14 - "Community 14"
Cohesion: 0.0
Nodes (6): get_args_parser(), get_init_file(), get_shared_folder(), main(), parse_args(), Trainer

### Community 15 - "Community 15"
Cohesion: 0.0
Nodes (4): conv_bn(), fixed_padding(), InvertedResidual, MobileNetV2

### Community 16 - "Community 16"
Cohesion: 0.0
Nodes (9): SFM-Pretrain/engine_pretrain.py, SFM-Pretrain/main_pretrain.py, SFM-Finetune/util/misc.py, SFM-Pretrain/models_mae.py, SFM-Finetune/util/pos_embed.py, SFM-Pretrain/README.md, Data/README-Pretrain.md, SFM-Pretrain/submitit_pretrain.py (+1 more)

### Community 17 - "Community 17"
Cohesion: 0.0
Nodes (5): get_1d_sincos_pos_embed_from_grid(), get_2d_sincos_pos_embed(), get_2d_sincos_pos_embed_from_grid(), grid_size: int of the grid height and width     return:     pos_embed: [grid_siz, embed_dim: output dimension for each position     pos: a list of positions to be

### Community 18 - "Community 18"
Cohesion: 0.0
Nodes (3): LARS, LARS optimizer, no rate scaling or weight decay for parameters <= 1D., step()

### Community 19 - "Community 19"
Cohesion: 0.0
Nodes (4): get_layer_id_for_vit(), param_groups_lrd(), Parameter groups for layer-wise lr decay     Following BEiT: https://github.com/, Assign a parameter with its layer id     Following BEiT: https://github.com/micr

### Community 20 - "Community 20"
Cohesion: 0.0
Nodes (3): Network Architecture Image, README.md, requirements.txt

### Community 22 - "Community 22"
Cohesion: 0.0
Nodes (1): Crop Utils

### Community 23 - "Community 23"
Cohesion: 0.0
Nodes (1): LARS Optimizer Utils

### Community 24 - "Community 24"
Cohesion: 0.0
Nodes (1): SFM-Finetune/util/metrics.py

### Community 25 - "Community 25"
Cohesion: 0.0
Nodes (1): SFM-Finetune/util/msssim.py

### Community 26 - "Community 26"
Cohesion: 0.0
Nodes (1): SFM-Finetune/util/pos_embedtest.py

### Community 27 - "Community 27"
Cohesion: 0.0
Nodes (1): Data/README-Denoise.md

### Community 28 - "Community 28"
Cohesion: 0.0
Nodes (1): Data/README-Facies.md

### Community 29 - "Community 29"
Cohesion: 0.0
Nodes (1): Data/README-Geobody.md

### Community 30 - "Community 30"
Cohesion: 0.0
Nodes (1): Data/README-Interpolation.md

### Community 31 - "Community 31"
Cohesion: 0.0
Nodes (1): Data/README-Inversion.md

### Community 32 - "Community 32"
Cohesion: 0.0
Nodes (1): SFM-Finetune/Application/README.md

### Community 33 - "Community 33"
Cohesion: 0.0
Nodes (1): SFM-Finetune/README.md

## Knowledge Gaps
- **52 isolated node(s):** `Masked Autoencoder with VisionTransformer backbone`, `imgs: (N, 3, H, W)         x: (N, L, patch_size**2 *3)`, `x: (N, L, patch_size**2 *3)         imgs: (N, 3, H, W)`, `Perform per-sample random masking by per-sample shuffling.         Per-sample sh`, `imgs: [N, 3, H, W]         pred: [N, L, p*p*3]         mask: [N, L], 0 is keep,` (+47 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **Thin community `Community 22`** (1 nodes): `Crop Utils`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 23`** (1 nodes): `LARS Optimizer Utils`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 24`** (1 nodes): `SFM-Finetune/util/metrics.py`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 25`** (1 nodes): `SFM-Finetune/util/msssim.py`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 26`** (1 nodes): `SFM-Finetune/util/pos_embedtest.py`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 27`** (1 nodes): `Data/README-Denoise.md`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 28`** (1 nodes): `Data/README-Facies.md`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 29`** (1 nodes): `Data/README-Geobody.md`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 30`** (1 nodes): `Data/README-Interpolation.md`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 31`** (1 nodes): `Data/README-Inversion.md`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 32`** (1 nodes): `SFM-Finetune/Application/README.md`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 33`** (1 nodes): `SFM-Finetune/README.md`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.