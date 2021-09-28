easy_sample_mark库测试
==================

## 测试概述
测试标注工具easy_sample_mark使用无误。

### 目的
测试涉及easy_docker(1.0)以及easy_sample_mark（0.1）的标注功能，工具中的一些基础功能。

### 测试流程

#### 1. 安装软件
确保环境中安装好easy_workspace的镜像，如未安装，请参考easy_docker环境编译：[docker镜像编译及制作流程](https://github.com/MiniBullLab/easy_docker/blob/master/docs/docker%E9%95%9C%E5%83%8F%E7%BC%96%E8%AF%91%E5%8F%8A%E5%88%B6%E4%BD%9C%E6%B5%81%E7%A8%8B.md)。

进入镜像后会在home目录下生成easy_data目录，将easy_sample_mark工程clone到easy_data目录下，并切换到test分支。

easy_sample_mark编译与运行：[docker环境下编译与运行](https://github.com/MiniBullLab/easy_sample_mark/blob/develop/docs/docker%E7%8E%AF%E5%A2%83%E4%B8%8B%E7%BC%96%E8%AF%91%E4%B8%8E%E8%BF%90%E8%A1%8C.md)。

#### 2. 软件使用方法
easy_sample_mark的使用方式参见百度网盘中easyai标注软件视频。

### 测试范围

## 测试计划执行情况

### 测试环境与配置

| 资源名称 | 配置 | 备注 |
| :------: | :------ | :------ | 
| 已经安装好easy_workspace环境的服务器 | Ubuntu18.04,4T硬盘,128G内存 | |

### 测试用例表格

| 测试用例标识符 | 测试用例名称 | 详细说明 | 备注 |
| :------: | :------ | :------ |  :------ | 
| mark_case001 | 检测任务标注 | 标注数据[饺子数据](http://118.31.19.101:8080/dataset/det/denet_dumpling_1class_bmp_xml.zip)（1类，jpg格式），对图片中的饺子进行拉框操作，标注后结果正确保存到Annotations文件夹中。| |
| mark_case002 | 分割任务标注 | 标注数据[易拉罐底部气泡数据](http://118.31.19.101:8080/dataset/seg/segnet_can_2class_jpg.zip)（2类，jpg格式），对易拉罐底部的气泡进行多边形标注操作，标注后结果正确保存到Annotations文件夹中。| |
| mark_case003 | OCR任务标注 | 标注数据[集装箱数据](http://118.31.19.101:8080/dataset/seg/segnet_can_2class_jpg.zip)（jpg格式），对集装箱字符多边形标注操作，并注释字符内容，标注后结果正确保存到Annotations文件夹中。| |
| mark_case004 | 分割图生成 | 分割标注后的结果生成mask图片，结果保存在SegmentLabel文件夹中。| |
| mark_case005 | 视频转化为图片 | | |
| mark_case006 | 图片转化为视频 | | |
| mark_case007 | 图片格式转换 | | |