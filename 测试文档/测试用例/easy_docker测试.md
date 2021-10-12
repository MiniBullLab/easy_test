easy_docker库测试
==================

## 测试概述

### 目的
测试docker环境正常无误。

### 测试范围
测试涉及easy_docker(1.0), easy_sample_mark（0.1）, easy_ai（0.1）, easy_perception（0.1）的整体测试。

### 测试流程

#### 1. 安装软件
easy_docker环境编译：[docker镜像编译及制作流程](https://github.com/MiniBullLab/easy_docker/blob/master/docs/docker%E9%95%9C%E5%83%8F%E7%BC%96%E8%AF%91%E5%8F%8A%E5%88%B6%E4%BD%9C%E6%B5%81%E7%A8%8B.md)。

#### 2. 软件使用方法
easy_docker使用方式：[docker镜像使用流程](https://github.com/MiniBullLab/easy_docker/blob/master/docs/docker%E9%95%9C%E5%83%8F%E4%BD%BF%E7%94%A8%E6%B5%81%E7%A8%8B.md)。

进入镜像后会在home目录下生成easy_data目录，对于ai_runtime的镜像测试，需要将easy_sample_mark, easy_perception分别clone到easy_data目录下。
对于ai_workspace的镜像测试需要将easy_sample_mark, easy_ai, easy_perception分别clone到easy_data目录下。

easy_sample_mark编译与运行：[docker环境下编译与运行](https://github.com/MiniBullLab/easy_sample_mark/blob/develop/docs/docker%E7%8E%AF%E5%A2%83%E4%B8%8B%E7%BC%96%E8%AF%91%E4%B8%8E%E8%BF%90%E8%A1%8C.md)。

easy_perception编译：[docker环境下编译](https://github.com/MiniBullLab/easy_perception/blob/develop/easy_arm/README.md)。

## 测试计划执行情况

### 测试环境与配置

| 资源名称 | 配置 | 备注 |
| :------: | :------ | :------ | 
| 带有gpu的服务器 | Ubuntu18.04,4T硬盘,128G内存,12G独显 | |

### 测试用例表格

| 测试用例标识符 | 测试用例名称 | 详细说明 | 备注 |
| :------: | :------ | :------ |  :------ | 
| docker_case001 | ai_runtime镜像编译 | 参照1.安装软件：easy_docker环境编译中的编译镜像。  |  |
| docker_case002 | ai_runtime镜像启动 | 参照2. 软件使用方法：easy_docker使用方式中的启动docker镜像。 |  |
| docker_case003 | ai_runtime镜像进入 | 参照2. 软件使用方法：easy_docker使用方式中的进入docker镜像。 |  |
| docker_case004 | ai_runtime镜像打包 |  参照1.安装软件：easy_docker环境编译中的docker镜像打包。 |  |
| docker_case005 | ai_runtime镜像ClassNet.sh脚步测试 |  训练数据集为[花朵数据](http://118.31.19.101:8080/dataset/cls/classnet_flower_17class_jpg.zip)（17类，jpg格式），直接运行ClassNet.sh path/to/ImageSets/train.txt path/to/ImageSets/val.txt。 |  |
| docker_case006 | ai_runtime镜像DeNet.sh脚步测试 | 训练数据集为[水果数据](http://118.31.19.101:8080/dataset/det/denet_fruit_4class.zip)（4类，混合格式（jpg,png,bmp）），直接运行DeNet.sh path/to/ImageSets/train.txt path/to/ImageSets/val.txt 。 |  |
| docker_case007 | ai_runtime镜像SegNet.sh脚步测试 |  训练数据集为[螺母数据](http://118.31.19.101:8080/dataset/seg/segnet_nut_2class.zip)（2类，混合格式（jpg,png,bmp）），直接运行SegNet.sh path/to/ImageSets/train.txt path/to/ImageSets/val.txt。 |  |
| docker_case008 | ai_workspace镜像编译 |  参照1.安装软件：easy_docker环境编译中的编译镜像。  |  |
| docker_case009 | ai_workspace镜像启动 |  参照2. 软件使用方法：easy_docker使用方式中的启动docker镜像。 |  |
| docker_case010 | ai_workspace镜像进入 | 参照2. 软件使用方法：easy_docker使用方式中的进入docker镜像。 |  |
| docker_case011 | ai_workspace镜像打包 | 参照1.安装软件：easy_docker环境编译中的docker镜像打包。 |  |
| docker_case012 | ai_workspace镜像ClassNet.sh脚步测试 | 训练数据集为[花朵数据](http://118.31.19.101:8080/dataset/cls/classnet_flower_17class_jpg.zip)（17类，jpg格式），进入easy_ai目录下，运行./easy_tools/ClassNet.sh path/to/ImageSets/train.txt path/to/ImageSets/val.txt。 |  |
| docker_case013 | ai_workspace镜像DeNet.sh脚步测试 |  训练数据集为[水果数据](http://118.31.19.101:8080/dataset/det/denet_fruit_4class.zip)（4类，混合格式（jpg,png,bmp）），进入easy_ai目录下，运行./easy_tools/DeNet.sh path/to/ImageSets/train.txt path/to/ImageSets/val.txt 。 |  |
| docker_case014 | ai_workspace镜像SegNet.sh脚步测试 |  训练数据集为[螺母数据](http://118.31.19.101:8080/dataset/seg/segnet_nut_2class.zip)（2类，混合格式（jpg,png,bmp）），进入easy_ai目录下，运行./easy_tools/SegNet.sh path/to/ImageSets/train.txt path/to/ImageSets/val.txt。 |  |
| docker_case015 |  ai_workspace镜像中easy_sample_mark编译 | 参照2. 软件使用方法：easy_sample_mark编译与运行。 |  |
| docker_case016 |  ai_workspace镜像中easy_sample_mark运行 | 参照2. 软件使用方法：easy_sample_mark编译与运行。 |  |
| docker_case017 |  ai_workspace镜像中easy_perception编译 | 参照2. 软件使用方法：easy_perception编译。  |  |

