# <p align="center"> Logo-2K+:A Large-Scale Logo Dataset for Scalable Logo Classiﬁcation </p>

## Logo-2k+ Dataset
![example](logo/example.png)\

## Logo-2k+ Dataset Description
In this work, we construct a large scale logo dataset, Logo-2K+, which covers a diverse range of logo classes from real-world logo images.
Our resulting logo dataset contains `167,140` images with 10 root categories and `2,341` categories. \
The statistic comparison of 10 root categories from Logo-2K+ is shown as follows. 

| Root Category        | Logos           | Images  |
| ------------- |:-------------:| -----:|
| Food          |    769        | 54,507 |
| Clothes       |    286        | 20,413 |
| Institution   |    238        | 17,103 |
| Accessories   |    210        | 14,569 |
|Transportation |    203        | 14,719 |
|Electronic     |    191        | 13,972 |
|Necessities    |    182        | 13,205 |
|Cosmetic       |    115        |  7,929 |
|Leisure        |    99         |  7,338 |
|Medical        |    48         |  3,385 |
|Total          |    2,341      |167,140 | 

# DRNA-Net

This is a PyTorch implementation of the AAAI2020 paper "Logo-2K+: A Large-Scale Logo Dataset for Scalable Logo Classification".

## Requirements

- Python >= 3
- PyTorch >= 0.4 Install PyTorch >=0.4 with GPU (code are GPU-only), refer to official website
- Install cupy, you can install via pip install cupy-cuda80 or(cupy-cuda90,cupy-cuda91, etc).
- Install other dependencies: pip install -r requirements.txt

## Datasets
Download the Logo-2K+(https://github.com/msn199959/Logo-2k-plus-Dataset) datasets and put it in the root directory. You can also try other classification datasets.

## Training on Logo-2K+ dataset:
Download the training, testing data. Since the program loading the data in ``drna_master/data`` by default, you can set the data path as following.
- cd drna_master
- mkdir data
- cd data
- ln -s $ dataset path

Then you can set some hyper-parameters in ``drna_master/config.py``.
If you want to train the DRNA-Net, just run ``python train.py``. During training, the log file and checkpoint file will be saved in ``save_dir`` directory. 

## Test the model
If you want to test the DRNA-Net, just run ``python test.py``. You need to specify the ``test_model`` in ``config.py`` to choose the checkpoint model for testing.

## Logo-2k+ Dataset download
Logo-2k+ Dataset website: \
http://www.victor.sdnu.edu.cn/datasets/Logo2K.htm \
Baidu drive download link: \
https://pan.baidu.com/s/1NuwYPKkZoR0BksFANDJGKQ  password: zxf0 \
Google drive download link: \
https://drive.google.com/open?id=1PTA24UTZcsnzXPN1gmV0_lRg3lMHqwp6  

## Reference
If you are interested in our work and want to cite it, please acknowledge the following paper:

```
@inproceedings{Wang2020Logo2K,
author={Jing Wang, and Weiqing Min, and Sujuan Hou, and Shengnan Ma, and Yuanjie Zheng, and Haishuai Wang, and Shuqiang Jiang},
booktitle={AAAI Conference on Artificial Intelligence. Accepted},
title={{Logo-2K+:} A Large-Scale Logo Dataset for Scalable Logo Classification},
year={2020}
}
@inproceedings{Yang2018Learning,
author = {Yang, Ze and Luo, Tiange and Wang, Dong and Hu, Zhiqiang and Gao, Jun and Wang, Liwei},
year = {2018},
title = {Learning to Navigate for Fine-grained Classification},
booktitle = {European Conference on Computer Vision},
pages ={438-454}
}
@article{Hu2019See,
author = {Tao Hu and Honggang Qi and Qingming Huang and Yan Lu},
title = {See Better Before Looking Closer: Weakly Supervised Data Augmentation Network for Fine-Grained Visual Classification},
booktitle = {CoRR Computing Research Repository},
year = {2019},
journal = {arXiv:1901.09891}
}

```
