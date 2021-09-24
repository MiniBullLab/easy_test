easy_arm库测试
==================

## 测试概述

### 目的

### 测试范围

## 测试计划执行情况

### 测试环境与配置

| 资源名称 | 配置 | 备注 |
| :------: | :------ | :------ | 
| amba下位机 |  | |

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