---
title: pyinstaller打包之后的windows程序无法正常运行多进程
top: false
cover: false
toc: true
mathjax: true
date: 2022-07-05 14:16:15
password:
summary:
tags: [python, pyinstaller, 多进程]
categories: python
---

## pyinstaller打包之后的windows程序无法正常运行多进程

### 错误日志
<!-- ![pyinstaller_err](/source/imgs/pyinstaller_err.png)  -->
![pyinstaller_err](./pyinstaller打包之后的windows程序无法正常运行多进程/pyinstaller_err.png)

### 解决方案
在 if __name__ == '__main__':的方法下面添加 multiprocessing.freeze_support()
```
from multiprocessing import freeze_support
if __name__ == '__main__':
    freeze_support()
```
