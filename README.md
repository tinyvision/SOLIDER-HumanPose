# SOLIDER on [Human Pose]

This repo provides details about how to use [SOLIDER](https://github.com/tinyvision/SOLIDER) pretrained representation on human parsing task.
We modify the code from [mmpose](https://github.com/open-mmlab/mmpose), and you can refer to the original repo for more details.

## Installation and Datasets

Details of installation and dataset preparation can be found in [mmpose-installation](https://mmpose.readthedocs.io/en/latest/installation.html).

## Prepare Pre-trained Models
Step 1. Download models from [SOLIDER](https://github.com/tinyvision/SOLIDER), or use [SOLIDER](https://github.com/tinyvision/SOLIDER) to train your own models.

Steo 2. Put the pretrained models under the `pretrained` file, and rename their names as `./pretrained/solider_swin_tiny(small/base).pth`

## Training
Train with single GPU or multiple GPUs:

```shell
sh run_train.sh
```

## Performance

| Method | Model | COCO(AP/AR) |
| ------ | :---: | :---: | 
| SOLIDER | Swin Tiny | 74.4/79.6 | 
| SOLIDER | Swin Small | 76.3/81.3 | 
| SOLIDER | Swin Base | 76.6/81.5 | 

- We use the pretrained models from [SOLIDER](https://github.com/tinyvision/SOLIDER).
- The semantic weight we used in these experiments is 0.8.

## Citation

If you find this code useful for your research, please cite our paper

```
@inproceedings{chen2023beyond,
  title={Beyond Appearance: a Semantic Controllable Self-Supervised Learning Framework for Human-Centric Visual Tasks},
  author={Weihua Chen and Xianzhe Xu and Jian Jia and Hao Luo and Yaohua Wang and Fan Wang and Rong Jin and Xiuyu Sun},
  booktitle={The IEEE/CVF Conference on Computer Vision and Pattern Recognition},
  year={2023},
}
```

