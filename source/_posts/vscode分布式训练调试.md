---
title: vscode分布式训练调试
catalog: true
date: 2022-06-29 16:47:53
tags: [vscode, 分布式训练, 调试]
categories: 深度学习
---

<!-- 
title: 文章标题
catalog: 是否显示段落目录
date: 文章日期
subtitle: 子标题
header-img: 顶部背景图片
top: 是否置顶
tags: 标签
categories: 分类 
-->

## 解决torch.distributed训练时需要Debug问题
### 正常运行命令
```
CUDA_VISIBLE_DEVICES=0 python -m torch.distributed.launch --nproc_per_node 1  main.py
```

### VSCODE调试
在VS Code中想要调试Python脚本很简单，只需要创建一个launch.json文件即可。
```
{
    // 使用 IntelliSense 了解相关属性。 
    // 悬停以查看现有属性的描述。
    // 欲了解更多信息，请访问: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Python: Current File",
            "type": "python",
            "request": "launch",
            "program": "xxx/lib/python3.6/site-packages/torch/distributed/launch.py",
            "console": "integratedTerminal",
            "justMyCode": true,
            "cwd": "${workspaceFolder}/xxx/xxx",
            "args": [
                "--nproc_per_node","1",
                "main.py"
            ],
            "env": {"CUDA_VISIBLE_DEVICES":"0"}
        }
    ]
}
```

