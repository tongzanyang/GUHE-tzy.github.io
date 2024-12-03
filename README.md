
# 通过Hexo静态博客框架,快速搭建个人博客

[Hexo](https://hexo.io/)是一个快速、简洁且高效的静态博客框架，基于[Node.js](https://dev.nodejs.cn/)开发。它可以帮助你轻松地生成静态网站，并且支持[Markdown](https://markdown.com.cn/)语法，非常适合用于个人博客、项目文档等静态内容的生成。

# 2.部署前期准备
1. [Nodejs](https://dev.nodejs.cn)开源和跨平台的 JavaScript 运行时环境。
2. [Git](https://git-scm.com/downloads)版本控制工具。
3. [域名](https://wanwang.aliyun.com/domain/)可注册域名加速访问，非必要。
4. [Hexo](https://hexo.io/)主题库[Themes](https://hexo.io/themes/)。

# 3.安装Nodejs
1. 在[Node官网](https://dev.nodejs.cn/)选择下载合适的版本。
2. 以Ubuntu-v22.0.4操作系统为例，下载[node-v22.11.0-linux-x64.tar.xz](https://nodejs.org/en/download/prebuilt-binaries)。
3. 验证安装是否成功: node -v 和 npm -v
```bash
# 方法一
# 安装curl 和 bash
sudo apt install -y cur bash

# 在远程服务器上解压缩 Node.js 安装包
tar -xvf node-v22.11.0-linux-x64.tar.xz

# 创建 Node.js 命令的符号链接到系统的 bin 目录，使其全局可用
mv node-v22.11.0-linux-x64 /usr/local/lib/nodejs

# 创建 npm 命令的符号链接到系统的 bin 目录，使其全局可用
sudo ln -s /usr/local/lib/nodejs/bin/node /usr/local/bin/node

sudo apt install -y curl bash

# 添加 NodeSource 的 PPA（个人包存档）来获取最新的 Node.js 版本。
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -

# 安装nodejs
apt-get install -y node.js

# 验证安装是否成功
node -v
npm -v
```

# 4.安装 Git工具
1. [Git官网](https://git-scm.com/downloads)下载Git版本控制工具。
```bash

# 安装Git
sudo apt-get install git-core

# 查看git版本进行验证
git -v
```

# 5.安装并配置Hexo
1. 创建文件夹保存博客源码
```bash
mkdir ~/hexo
```
2. 设置npm镜像源
```bash
# 设置 npm 镜像源为华为镜像源
npm config set registry https://mirrors.huaweicloud.com/repository/npm/

# 设置 npm 镜像源为阿里镜像源
npm config set registry https://registry.npmmirror.com/
```
3. 所以必备应用程序安装完成后，使用npm安装Hexo。
```bash
# 安装Hexo
npm install -g hexo-cli && hexo -v
```
4. 设置环境变量
```bash
vim ~/.bashrc

export PATH="/usr/local/lib/nodejs/lib/node_modules/hexo-cli/bin:$PATH"

source ~/.bashrc
```
5. 使用 hexo -v 命令验证安装成功。
6. 启动项目
```bash
hexo cl && hexo s
```
7. 浏览器访问[https://localhost:4000](https://localhost:4000)进行查看。
![示例图片](https://cdn.jsdelivr.net/gh/tongzanyang/PicGo@main/hexo-test.png)

## 查看博客
1. 个人博客[天外天](https://guhe-tzy-github-io.pages.dev/)。
2. 进入[魔法信息包](https://blog.zetman.cn/article/hexo-1/)查看详细具体的教程。
