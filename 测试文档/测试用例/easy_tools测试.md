easy_tools库测试
==================

## 测试概述

### 目的
测试easy_tools中的所有功能运行正常。

### 测试范围
测试涉easy_docker(1.0)以及easy_ai（0.1）的测试，其中包含ClassNet, DeNet, SegNet等网络训练，界面化训练，界面化测试。

### 测试流程
#### 1. 安装软件
确保环境中安装好easy_workspace的镜像，如未安装，请参考easy_docker环境编译：[docker镜像编译及制作流程](https://github.com/MiniBullLab/easy_docker/blob/master/docs/docker%E9%95%9C%E5%83%8F%E7%BC%96%E8%AF%91%E5%8F%8A%E5%88%B6%E4%BD%9C%E6%B5%81%E7%A8%8B.md)。

进入镜像后会在home目录下生成easy_data目录，将easy_ai工程clone到easy_data目录下，并切换到test分支。

#### 2. 软件使用方法


## 测试计划执行情况

### 测试环境与配置

| 资源名称 | 配置 | 备注 |
| :------: | :------ | :------ | 
| 已经安装好easy_workspace环境的带有gpu的服务器 | Ubuntu18.04,4T硬盘,128G内存,12G独显 | |

### 测试用例表格

| 测试用例标识符 | 测试用例名称 | 详细说明 | 备注 |
| :------: | :------ | :------ |  :------ | 
| tools_case001 | ClassNet训练 | 训练数据集为[花朵数据](http://118.31.19.101:8080/dataset/cls/classnet_flower_17class_jpg.zip)（17类，jpg格式），进入easy_ai目录下，运行./easy_tools/ClassNet.sh path/to/ImageSets/train.txt path/to/ImageSets/val.txt。 |  |
| tools_case002 | ClassNet断点训练 | 训练数据集为[花朵数据](http://118.31.19.101:8080/dataset/cls/classnet_flower_17class_jpg.zip)（17类，jpg格式），进入easy_ai目录下，运行./easy_tools/ClassNet.sh path/to/ImageSets/train.txt path/to/ImageSets/val.txt。 |  |
| tools_case003 | DeNet训练 | 训练数据集为[水果数据](http://118.31.19.101:8080/dataset/det/denet_fruit_4class.zip)（4类，混合格式（jpg,png,bmp）），进入easy_ai目录下，运行./easy_tools/DeNet.sh path/to/ImageSets/train.txt path/to/ImageSets/val.txt 。 |  |
| tools_case004 | DeNet断点训练 | 训练数据集为[水果数据](http://118.31.19.101:8080/dataset/det/denet_fruit_4class.zip)（4类，混合格式（jpg,png,bmp）），进入easy_ai目录下，运行./easy_tools/DeNet.sh path/to/ImageSets/train.txt path/to/ImageSets/val.txt 。 |  |
| tools_case005 | SegNet训练 | 训练数据集为[螺母数据](http://118.31.19.101:8080/dataset/seg/segnet_nut_2class.zip)（2类，混合格式（jpg,png,bmp）），进入easy_ai目录下，运行./easy_tools/SegNet.sh path/to/ImageSets/train.txt path/to/ImageSets/val.txt。 |  |
| tools_case006 | SegNet断点训练 | 训练数据集为[螺母数据](http://118.31.19.101:8080/dataset/seg/segnet_nut_2class.zip)（2类，混合格式（jpg,png,bmp）），进入easy_ai目录下，运行./easy_tools/SegNet.sh path/to/ImageSets/train.txt path/to/ImageSets/val.txt。 |  |
| tools_case007 | ClassNet界面训练 | 训练数据集为[花朵数据](http://118.31.19.101:8080/dataset/cls/classnet_flower_17class_jpg.zip)（17类，jpg格式），运行python3 train_gui.py。| |
| tools_case008 | DeNet界面训练 | 训练数据集为[水果数据](http://118.31.19.101:8080/dataset/det/denet_fruit_4class.zip)（4类，混合格式（jpg,png,bmp）），运行python3 train_gui.py。| |
| tools_case009 | SegNet界面训练 | 训练数据集为[螺母数据](http://118.31.19.101:8080/dataset/seg/segnet_nut_2class.zip)（2类，混合格式（jpg,png,bmp）），运行python3 train_gui.py。| |
| tools_case010 | ClassNet精度界面测试 | 运行python3 test_gui.py | |
| tools_case011 | DeNet精度界面测试 | 运行python3 test_gui.py | |
| tools_case012 | SegNet精度界面测试 | 运行python3 test_gui.py | |