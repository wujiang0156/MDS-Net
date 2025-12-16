# MDS-Net

MDS-Net： An Image-Text Enhanced Multimodal Dual-Branch Siamese Network for Remote Sensing Change Detection
## Introduction

In this work, we propose a new change detection framework, CLIPFormer, which leverages pretraining knowledge from CLIP and the Swin transformer. 

<img width="1230" height="669" alt="image" src="https://github.com/user-attachments/assets/232e3dc4-153e-40fe-a665-46c4edf9c7d1" />

## Install
- First, you need to download mmsegmentation and install it on your server.
- Second, Place clipformer.py, swinclip, cswin_text_head.py, and other .py files in the corresponding directory of mmsegmentation..
- Third, train according to the training strategy of mmsegmentation and the training parameters in our paper.

## Pretrained Weights of Backbones

[CLIP-pretrain](https://github.com/OpenAI/CLIP)
[Swin-Trnasformer-pretrain](https://download.openmmlab.com/mmsegmentation/)


## Data Preprocessing

Download the datasets from the official website and split them yourself.



**LEVIR-CD**
[LEVIR-CD](https://justchenhao.github.io/LEVIR/)

**LEVIR-CD+**
[LEVIR-CD+](https://github.com/S2Looking/Dataset)

**WHUCD**
[WHUCD](https://study.rsgis.whu.edu.cn/pages/download/building_dataset.html)

**CDD**
[CDD](https://paperswithcode.com/sota/change-detection-for-remote-sensing-images-on)

**SYSU-CD**
[SYSU-CD](https://github.com/liumency/SYSU-CD)


## Training

You can refer to **mmsegmentation document** (https://mmsegmentation.readthedocs.io/en/latest/index.html).


## Results and Logs for CLIPformer
Here we only present the test results of our model. For detailed test results, please refer to our paper.

### TABLE I
COMPARISONS OF DETECTION PERFORMANCE ON LEVIR-CD DATASET
| Model | Backbone | OA | IoU | F1 | Prec | Rec | log |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| CLIPformer(ViT-B/16) | Swin-T | 99.22 | 85.60 | 92.24 | 93.60 |  90.92 | [log](https://github.com/wujiang0156/CLIPformer/blob/main/log/20240413_094938.log) |

### TABLE II
COMPARISONS OF DETECTION PERFORMANCE ON LEVIR-CD+ DATASET
| Model | Backbone | OA | IoU | F1 | Prec | Rec | log |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| CLIPformer(RN50) | Swin-T | 98.87 | 76.81 | 86.89 | 88.51 |  85.32 | [log](https://github.com/wujiang0156/CLIPformer/blob/main/log/20240414_161022.log) | 

### TABLE III
COMPARISONS OF DETECTION PERFORMANCE ON WHUCD DATASET
| Model | Backbone | OA | IoU | F1 | Prec | Rec | log |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| CLIPformer(ViT-B/16) | Swin-T | 99.54 | 89.55 | 94.49 | 96.38 |  92.66 | [log](https://github.com/wujiang0156/CLIPformer/blob/main/log/20240418_065021.log) | 

### TABLE IV
COMPARISONS OF DETECTION PERFORMANCE ON CDD DATASET
| Model | Backbone | OA | IoU | F1 | Prec | Rec | log |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| CLIPformer(RN50) | Swin-T | 99.33 | 94.51 | 97.18 | 97.03 |  97.32 | [log](https://github.com/wujiang0156/CLIPformer/blob/main/log/20240416_221124.log) | 

### TABLE V
COMPARISONS OF DETECTION PERFORMANCE ON SYSU-CD DATASET.
| Model | Backbone | OA | IoU | F1 | Prec | Rec | log |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| CLIPformer(ViT-B/16) | Swin-T | 99.62 | 71.77 | 83.57 | 88.02 |  79.54 | [log](https://github.com/wujiang0156/CLIPformer/blob/main/log/20240602_084845.log) | 

## Visualization on remote sensing change detection datasets
Here we present the visualization results on the LEVIR-CD dataset. For detailed qualitative analysis and visualization results on other datasets (LEVIR-CD+, WHUCD, CDD, and SYSU-CD), please refer to our paper.
<div>
<img src="https://github.com/wujiang0156/CLIPformer/blob/main/fig/fig%203%20levir.jpg" width="100%"/>
</div>

## Cite
@ARTICLE{10989581,
  author={Wang, Tao and Bai, Tiecheng and Xu, Chao and Zhang, Erlei and Liu, Bin and Zhao, Xining and Zhang, Hongming},
  journal={IEEE Journal of Selected Topics in Applied Earth Observations and Remote Sensing}, 
  title={MDS-Net: An Image-Text Enhanced Multimodal Dual-Branch Siamese Network for Remote Sensing Change Detection}, 
  year={2025},
  volume={18},
  number={},
  pages={12421-12438},
  keywords={Feature extraction;Transformers;Remote sensing;Semantics;Computational modeling;Visualization;Adaptation models;Accuracy;Context modeling;Training;Change detection;multimodal learning;remote sensing image;Siamese network;transformer},
  doi={10.1109/JSTARS.2025.3567508}}

## Acknowledgement
 Many thanks the following projects's contributions to **CLIPFormer**.
- [MACT-UNet](https://github.com/open-mmlab/mmsegmentation)
- [mmsegmentation](https://github.com/open-mmlab/mmsegmentation)
- [DenseCLIP](https://github.com/raoyongming/DenseCLIP)
- [CLIP](https://github.com/OpenAI/CLIP)
- [ChangeCLIP](https://github.com/dyzy41/ChangeCLIP)
