# Dynamic Neural Representational Decoders for High-Resolution Semantic Segmentation, NeurIPS'21

[arXiv paper](https://arxiv.org/abs/2107.14428)
or the [final published version](https://proceedings.neurips.cc/paper/2021/hash/912d2b1c7b2826caf99687388d2e8f7c-Abstract.html)

## Requirements

This repository needs [mmsegmentation](https://github.com/open-mmlab/mmsegmentation)

## Training

To train the model(s) in the paper, run this command:

```train
python tools/train.py ./configs/NRD/ade20k/NRD_r101_512x512_164k_ade20k.py
```

The batch size is 16 in this work. Please change the 'samples_per_gpu' in configs/_base_/datasets/.. accordingly

## Evaluation

To evaluate my model at single-scale inference, run:

```eval
python tools/eval.py ./configs/NRD/ade20k/NRD_r101_512x512_164k_ade20k.py  {path-to-checkpoint-file}   --eval mIoU
```

## Pre-trained Models


## Results

Our model achieves the following performance on :

### [Semantic segmentation results]

| Model name         |datasets| mIoU  | mIoU (ms) |
| ------------------ |--------------|---------------- | -------------- |
| NRD-r101   | ade20k (val) |   44.01         |      45.62       |
| NRD-x101   |ade20k (val) |  44.34         |      46.35       |
| NRD-r101   | pascal-context(val) |     52.31 (59 classes)       |      54.1 (59 classes)       |
| NRD-r101   | pascal-context(val) |     47.5  (60 classes)      |      40.9 (60 classes)       |
| NRD-r50   | Cityscapes (val) |   79.8         |      80.8       |
| NRD-r101   | Cityscapes (val) |   80.7         |      82.0      |

### BibTeX

```
@inproceedings{NEURIPS2021_Zhangbowen,
 author = {Bowen Zhang and Yifan liu and Zhi Tian and Chunhua Shen},
 booktitle = {Proc.\ Advances in Neural Information Processing Systems},
 title = {Dynamic Neural Representational Decoders for High-Resolution Semantic Segmentation},
 year = {2021}
}
```

## Contributing

This code is built upon mmsegmentation.

