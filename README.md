## Convolutional neural network model for automatic recognitionand classification of pancreatic cancer cell based on analysis of lipid droplet on unlabeled sample by 3D optical diffraction tomography

> Computer Methods and Programs in Biomedicine, 2024. (IF: 6.1, JCR 13.1%)

## Contents
1. [Overview](#Overview)
2. [Introduction](#Introduction)
3. [Dataset composition](#Dataset-composition)

4. [Getting started](#Getting-started)
5. [Setup](#Setup)
6. [Training](#Training)
    - [Single Task Setting](#Printing3DModel)
    - [Multi-view Task Setting](#Printing3DModel)
    - [Multi-Task Setting](#DataBase)
    - [Modal-Task Setting(meta-data)](#Transfer-Learning)
    - [Final Task Setting(multi-view, multi-task, meta-data)](#Live-Object-Detection)
    
7. [Evaluating](#Training)
    - [Single Task Setting](#Printing3DModel)
    - [Multi-view Task Setting](#Printing3DModel)
    - [Multi-Task Setting](#DataBase)
    - [Modal-Task Setting(meta-data)](#Transfer-Learning)
    - [Final Task Setting(multi-view, multi-task, meta-data)](#Live-Object-Detection)
8.  [Citation](#Citation)

## Overview
![스크린샷 2024-02-05 171501](https://github.com/tmdrn9/Medical-Identification_of_pancreatic_cancer/assets/77779116/26649b96-d580-48da-9e79-62919cc48ae2)

> This study proposed an automatic pancreatic cancer cell recognition system utilizing a deep convolutional neural network and quantitative images of lipid droplets (LDs) from stain-free cytologic samples through optical diffraction tomography. We retrieved 3D refractive index tomograms, reconstructing 37 optical images per cell. Additionally, we employed various machine learning techniques within a single image-based prediction model to enhance the computer-aided diagnostic system's performance.

## Introduction
> Pancreatic cancer cells generally accumulate large numbers of lipid droplets (LDs), which regulate lipid storage. To promote rapid diagnosis, an automatic pancreatic cancer cell recognition system based on a deep convolutional neural network was proposed in this study using quantitative images of LDs from stain-free cytologic samples by optical diffraction tomography.
## Dataset composition

    ${POSE_ROOT}
     `-- cell
         |-- cancer
         |    |-- BxPc-3
         |    |    `-- cell ID
         |    |           |-- Num.1 cell
         |    |           |     |-- image
         |    |           |     |     |-- BxPc-3-001_1.jpg
         |    |           |     |     |-- BxPc-3-001_2.jpg
         |    |           |     |     |-- BxPc-3-001_3.jpg
         |    |           |     |     |-- ...
         |    |           |     |     `-- BxPc-3-001_37.jpg
         |    |           |     |
         |    |           |     `-- meta data
         |    |           |           |-- Cell volume         
         |    |           |           |-- Cell surface area      
         |    |           |           |-- Projected area        
         |    |           |           |-- Mean RI         
         |    |           |           |-- Protein concentration        
         |    |           |           |-- Dry mass
         |    |           |           |-- Sphericity
         |    |           |           |-- Lipid droplet volume
         |    |           |           |-- Lipid droplet count
         |    |           |           `-- ...         
         |    |           |                  
         |    |           |-- Num.2 cell
         |    |           |-- Num.3 cell
         |    |           `-- Num.n cell
         |    |-- Capan-2
         |    `-- PSN-1
         |
         `-- normal
              `-- H6c7


## Getting started

## Setup
- Python 3.8
- CUDA Version 12.4
- cuDNN Version 8.9.7

1. Nvidia driver, Anaconda install

2. Install pytorch

        pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121

3. Install various necessary packages in requirements.txt

        pip install -r requirements.txt
 
## Training

## Evaluating

## Citation

> If you want to cite our paper and code, you can use a bibtex code here:

        @article{hong2024convolutional,
          title={Convolutional neural network model for automatic recognition and classification of pancreatic cancer cell based on analysis of lipid droplet on unlabeled sample by 3D optical diffraction tomography},
          author={Hong, Seok Jin and Hou, Jong-Uk and Chung, Moon Jae and Kang, Sung Hun and Shim, Bo-Seok and Lee, Seung-Lee and Park, Da Hae and Choi, Anna and Oh, Jae Yeon and Lee, Kyong Joo and others},
          journal={Computer Methods and Programs in Biomedicine},
          volume={246},
          pages={108041},
          year={2024},
          publisher={Elsevier}
        }
