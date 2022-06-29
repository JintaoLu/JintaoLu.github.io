---
title: vscode分布式训练调试
date: 2022-06-29 16:47:53
tags:
---

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

