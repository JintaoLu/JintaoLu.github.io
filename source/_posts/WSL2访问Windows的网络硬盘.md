---
title: WSL2访问Windows的网络硬盘
top: false
cover: false
toc: true
mathjax: true
date: 2023-03-30 11:14:17
password:
summary:
tags: [WSL2, Windows, 网络硬盘]
categories: [深度学习]
---

# WSL2访问Windows的网络硬盘

## 1、安装依赖
```angular2html
sudo apt-get update
sudo apt-get install cifs-utils
```

## 2、创建挂载点：
```angular2html
sudo mkdir /mnt/y
sudo mount -t drvfs Y: /mnt/y
```

## 3、 永久生效（启动后即生效）：
sudo vi /etc/fstab添加新一行
```angular2html
Y: /mnt/y drvfs defaults 0 0
```

## 4、查看挂载结果
至此挂载搞定，可像普通目录一样访问：
```angular2html
ll /mnt/y
```



参考：
https://madgd.github.io/2021/05/20/wsL2中挂载windows下的网络硬盘/