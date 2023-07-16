# 动手学深度学习

## 0. 相关问题

### 0.1 在安装miniconda和jupyter时产生的问题

- jupyter_client版本和pyzmq版本不匹配，需要下调后者版本，卸载jupyter_client然后安装查看支持的其最低版本的pyzmq，然后挨个尝试。本次将jupyter_client版本下降至7.4.4(当前版本最低需要)，pyzmq版本降低至24.0.1 ，产生的问题解决
- 涉及到的命令
  - pip list
  - pip install xx==version
  - pip uninstall xx==version

## 1. 简介

### 介绍深度学习经典和最新模型

- LeNet,ResNet,LSTM,BERT

### 机器学习基础

- 损失函数、目标函数、过拟合、优化

### 优化

- Pytorch
- 算法

### 内容

- 深度学习基础
- 卷积神经网络
- 循环神经网络
- 注意力机制---Transformer
- 优化算法
- 高性能计算
- 计算机视觉
- 自然语言处理

### 其它

- What 有哪些技术
- How 如何实现和调参
- Why 背后的原因（直觉、数学）

## 2. 深度学习介绍

- 感知：自然语言处理
- 推理：计算机视觉和自然语言处理的结合
- 知识：深度学习
- 规划

**--广告点击--根据用户的输入给出广告**

触发--点击率预估（模型）--根据价格排序

**预测与训练**

- 特征提取
- 模型预测
- 点击率预测
- 将用户点击数据进行训练
- 特性和用户点击
- 优化模型

### 安装

需要安装的包

```shell
sudo apt install build-essential
sudo apt install python-3.8
#minicaonda安装
wget link
bash xxxx.sh
#bash进入conda环境（base）
#安装jupyter torch
pip install jupyter d2l torch torchvision
#启动jupyter 然后将服务器端口映射到本地
ssh -L8888:localhost:8888 ubantu@ip

```

## 3. 数据操作+数据预处理

### N维度数组

- 0-d 标量
- 1-d 向量：特征向量[1,2,3.0]
- 2-d 矩阵 [[1,2],[3.0,4.0]]
- 3-d RGB图片等
- 4-d RGB图片的批量
- 5-d 在上面的基础上加上时间--视频

### 创建数组

### 访问元素

- 一个元素 [1,2]
- 一行 [1:]
- 一列[:1]
- 子区域[1:3,1:]
- 子区域[::3,::2] 间隔访问 相当于每个3行访问  每隔2列访问

### 数据操作
