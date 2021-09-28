easy_arm库测试
==================

## 测试概述

### 目的
测试easy_arm中的所有功能运行正常。

### 测试范围
测试涉easy_docker(1.0)以及easy_perception（0.1）的测试，其中包含ClassNet, DeNet, SegNet等网络部署。

### 测试流程
#### 1. 安装软件
确保环境中安装好easy_workspace的镜像，如未安装，请参考easy_docker环境编译：[docker镜像编译及制作流程](https://github.com/MiniBullLab/easy_docker/blob/master/docs/docker%E9%95%9C%E5%83%8F%E7%BC%96%E8%AF%91%E5%8F%8A%E5%88%B6%E4%BD%9C%E6%B5%81%E7%A8%8B.md)。

进入镜像后会在home目录下生成easy_data目录，将easy_perception工程clone到easy_data目录下，并切换到test分支。

easy_perception编译：[docker环境下编译](https://github.com/MiniBullLab/easy_perception/blob/develop/easy_arm/README.md)。

#### 2. 软件使用方法

## 测试计划执行情况

### 测试环境与配置

| 资源名称 | 配置 | 备注 |
| :------: | :------ | :------ | 
| 已经安装好easy_workspace环境的服务器 | Ubuntu18.04,4T硬盘,128G内存 | |
| 安霸cv22芯片 | linux系统内核4.6，RAM2G，ROM8G | |

### 测试用例表格说明

### 测试用例表格

| 测试用例标识符 | 测试用例名称 | 详细说明 | 备注 |
| :------: | :------ | :------ |  :------ | 
| arm_case001 | 分类任务部署 | 通过easy_perception编译生成classnet_test，将训练得到的classnet.bin以及测试图片一起放到sd卡中，插入AMBA的板子后，上电运行classnet_test，结果保存在cls_result.txt中。| |
| arm_case002 | 检测任务部署 | 通过easy_perception编译生成denet_test，将训练得到的denet.bin以及测试图片一起放到sd卡中，插入AMBA的板子后，上电运行denet_test，结果保存在det2d_result.txt中。| |
| arm_case003 | 分割任务部署 | 通过easy_perception编译生成segnet_test，将训练得到的segnet.bin以及测试图片一起放到sd卡中，插入AMBA的板子后，上电运行segnet_test，结果保存在seg_result.txt中。| |
| arm_case004 | 字符识别任务部署 | 通过easy_perception编译生成textnet_test，将训练得到的TextNet.bin以及测试图片一起放到sd卡中，插入AMBA的板子后，上电运行textnet_test，结果保存在text_result.txt中。| |
| arm_case005 | OneClass任务部署 | 通过easy_perception编译生成one_class_test，将训练得到的OneClassNet.bin以及测试图片一起放到sd卡中，插入AMBA的板子后，上电运行one_class_test，结果保存在one_class_result.txt中。| |
| arm_case006 | 车牌检测任务部署 | | |