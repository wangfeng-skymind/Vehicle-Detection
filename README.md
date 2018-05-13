# 实战 车辆检测及型号识别

## 简介
车辆检测及型号识别广泛应用于物业，交通等的管理场景中。通过在停车场出入口，路口，高速卡口等位置采集的图片数据，对车辆的数量型号等进行识别，可以以较高的效率对车型，数量信息等进行采集。通过采集的数据，在不同的场景中可以辅助不同的业务开展。如商场停车位的规划，路况规划，或者公安系统追踪肇事车辆等等。

在第七周的作业中，学员们已经掌握了使用slim框架来对植物进行分类识别。

在第八周的作业中，学员们已经掌握使用slim物体检测框架来进行物体的检测和识别。

本项目中，将会综合第七周作业内容和第八周的作业内容,实现一个车辆检测的工业级系统。

## 作业内容

学员需要利用tensorflow提供的slim图片分类框架和物体检测框架实现一个可以对任意图片进行车辆检测的系统。

## 评价标准

### 成果1, 一整套可以运行的系统
包含代码和详细的文档。文档要求可操作。能够按照文档的描述搭建系统并运行。文档不全者不予及格。

系统要求能检测任意图片并给出合理的输出。

### 成果2, 提供一个演示视频
视频内容：从任意图片网站上，随机下载一张有汽车在内的图片，送入系统进行检测。可以输出并显示图片中车辆的位置和型号等信息。没有车辆的图片可以给出没有检测到的提示。

## 数据集

本作业提供一个车辆分类的数据集。

本作业提供的数据集分类参考数据集中的labels.txt文件：

共48856张图片
其43971张作为训练集，4885张作为验证集。

数据已经预先打包成tfrecord格式，数据格式与第七周作业相同，第七周的代码可以直接使用。请联系课程管理人员获取训练数据。


## 要点提示

- 系统的输入输出不做要求，能够正常演示即可。
    - 推荐的输入方式有：
        - 命令行直接指定待识别文件
        - 搭建一个web系统，使用表单方式上传文件
        - 搭建一个native程序，使用pyqt等GUI框架搭建GUI界面
    - 推荐的输出方式：
        - 将检测结果写入文件
        - 使用matplotlib显示检测结果
        - 搭建一个web系统，在web页上显示结果
        - 搭建一个native程序，使用pyqt等GUI框架搭建GUI界面
- 训练数据集为分类数据，在1080Ti显卡上，以inceptionv4网络，0.001的学习率，利用google提供的预训练模型，在6～8个小时的训练后可以得到top1 80%的准确率。经过24个小时的训练后，top1可以达到88%。