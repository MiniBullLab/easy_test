easy_sample_mark库测试
==================

## 测试概述

### 目的

### 测试范围

## 测试计划执行情况

### 测试环境与配置

| 资源名称 | 配置 | 备注 |
| :------: | :------ | :------ | 
| window10 |  | |

### 测试用例表格

| 测试用例标识符 | 测试用例名称 | 详细说明 | 备注 |
| :------: | :------ | :------ |  :------ | 
| mark_case001 | 检测任务标注 | 标注数据[饺子数据](http://118.31.19.101:8080/dataset/det/denet_dumpling_1class_bmp_xml.zip)（1类，jpg格式），对图片中的饺子进行拉框操作，标注后结果正确保存到Annotations文件夹中。| |
| mark_case002 | 分割任务标注 | 标注数据[易拉罐底部气泡数据](http://118.31.19.101:8080/dataset/seg/segnet_can_2class_jpg.zip)（2类，jpg格式），对易拉罐底部的气泡进行多边形标注操作，标注后结果正确保存到Annotations文件夹中。| |
| mark_case003 | OCR任务标注 | 标注数据[集装箱数据](http://118.31.19.101:8080/dataset/seg/segnet_can_2class_jpg.zip)（jpg格式），对集装箱字符多边形标注操作，并注释字符内容，标注后结果正确保存到Annotations文件夹中。| |
| mark_case004 | 分割图生成 | 分割标注后的结果生成mask图片，结果保存在SegmentLabel文件夹中。| |
| mark_case005 | 视频转化为图片 | | |
| mark_case006 | 图片格式转换 | | |