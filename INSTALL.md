# 环境准备

## 一、安装 node.js
首先下载稳定版 Node.js：https://nodejs.org/en/download/。
安装选项全部默认，一路点击 Next。

在 Windows PowerShell 中输入：
```angular2html
node -v
npm -v
```

### 添加国内镜像源
如果没有梯子的话，可以使用阿里的国内镜像进行加速。
```angular2html
npm config set registry https://registry.npm.taobao.org
```

## 二、安装Git
Git官网地址： https://git-scm.com/download/

## 三、安装Hexo
安装完后输入hexo -v验证是否安装成功。
```angular2html
npm install -g hexo-cli

hexo -v
```

## 四、下载git代码
```angular2html
git clone https://github.com/JintaoLu/JintaoLu.github.io.git -b hexo Blog

cd Blog
```

## 五、安装必备组件
npm install安装必备的组件
```angular2html
npm install
```

## 六、本地查看博客
输入hexo g生成静态网页，然后输入hexo s打开本地服务器，然后浏览器打开http://localhost:4000/
```angular2html
hexo g
hexo s
```