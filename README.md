# Divide-and-Conquer Predictor for Unbiased Scene Graph Generation

[![LICENSE](https://img.shields.io/badge/license-MIT-green)](https://github.com/KaihuaTang/Scene-Graph-Benchmark.pytorch/blob/master/LICENSE)
[![Python](https://img.shields.io/badge/python-3.8-blue.svg)](https://www.python.org/)
![PyTorch](https://img.shields.io/badge/pytorch-1.6.0-%237732a8)

Implement of paper [Divide-and-Conquer Predictor for Unbiased Scene Graph Generation](https://arxiv.org/abs/2104.00308).

## Contents

Overview

Installation

Dataset

Training

Pre-trained DCNet

Evaluation

## Overview

We divide the predicate prediction into a few sub-tasks with a Divide-and-Conquer Predictor (DC-Predictor).


## Installation

Check [INSTALL.md](INSTALL.md) for installation instructions.

## Dataset

Check [DATASET.md](DATASET.md) for instructions of dataset preprocessing.


## Training

### Prepare Faster-RCNN Detector

We adopted the pretrained Faster R-CNN provided by [Scene Graph Benchmark](https://github.com/KaihuaTang/Scene-Graph-Benchmark.pytorch).
You can download the [pretrained Faster R-CNN](https://onedrive.live.com/embed?cid=22376FFAD72C4B64&resid=22376FFAD72C4B64%21779870&authkey=AH5CPVb9g5E67iQ) and put it into the folder:
```
/home/username/checkpoints/pretrained_faster_rcnn
```

### Scene Graph Generation Model

This code include DCNet and other SGG methods.

There are three standard protocols: 1) Predicate Classification (PredCls). 2) Scene Graph Classification (SGCls), and 3) Scene Graph Detection (SGDet).
 
We use `MODEL.ROI_RELATION_HEAD.USE_GT_BOX` and `MODEL.ROI_RELATION_HEAD.USE_GT_OBJECT_LABEL` to select the protocols.

Test Example 1: (Neural Motifs, SGCls)

Test Example 2: (DCNet, PredCls)

Test Example 3: (DCNet, SGDet)

## Checkpoint DCNet

The checkpoint of are provided in this link. 

## Evaluation

Test Example: (SGCls)


## Citations

If you find this project helps your research, please kindly consider citing our papers in your publications.



## Acknowledgment
This repository is developed on top of the scene graph benchmarking framwork develped by [KaihuaTang](https://github.com/KaihuaTang/Scene-Graph-Benchmark.pytorch)