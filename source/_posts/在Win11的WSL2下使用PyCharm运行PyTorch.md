---
title: 在Win11的WSL2下使用PyCharm运行PyTorch
top: false
cover: false
toc: true
mathjax: true
date: 2022-10-21 18:00:42
password:
summary:
tags: [Win11, WSL2, PyCharm, PyTorch]
categories: 深度学习
---

# 在Win11的WSL2下使用PyCharm运行PyTorch

## 一、配置WSL解释器
设置项目解释器
![](./在Win11的WSL2下使用PyCharm运行PyTorch/pycharm_interpreter.png)
设置System Interpreter 或 WSL2里的虚拟环境（已存在或新建）
![](./在Win11的WSL2下使用PyCharm运行PyTorch/pycharm_interpreter2.png)
![](./在Win11的WSL2下使用PyCharm运行PyTorch/pycharm_interpreter2_1.png)
配置完成
![](./在Win11的WSL2下使用PyCharm运行PyTorch/pycharm_interpreter3.png)
## 二、配置Terminal
设置终端Terminal,将Shell path改为wsl.exe
![](./在Win11的WSL2下使用PyCharm运行PyTorch/pycharm_interpreter4.png
## 三、正常运行
![](./在Win11的WSL2下使用PyCharm运行PyTorch/pycharm_wsl_demo.png)
## 四、调试
会弹出防火墙信息弹窗，点允许即可
![](./在Win11的WSL2下使用PyCharm运行PyTorch/pycharm_wsl_debug.png)