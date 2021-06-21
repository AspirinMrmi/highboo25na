## 1. 快速查看NPM、yarn全局安装过的包

NPM

```bash
npm list -g --depth=0
```

Yarn

```bash
yarn global list --depth=0
```

如果有些包我们只用一次，或者只是想尝试一下，并不想安装到全局，也不想作为当前项目到以来，可以尝试使用npx

npx是npm 5.2+ 版本后自带的工具，能够帮助我们更加高校的执行npm仓库里的安装包

- 更方便的执行当前项目中的可执行工具

```bash
# 在没有 npx 之前
node ./node_modules/.bin/mocha

# 使用 npx
npx mocha
```

- 也可以执行那些不在当前项目，也没有在全局安装过的npm工具包，比如: create-react-app

```bash
npx create-react-app my-app

# 执行以上这条命令 npx 会按以下顺序工作：
# 1. 先查看当前项目有没 create-react-app
# 2. 如果当前项目找不到，会去全局查找 create-react-app
# 3. 如果全局还找不到，会帮我们临时从 npm 包仓库安装 create-react-app，不会污染到当前项目，也不会装到全局
```

## 2. NPM 查看源和切换源

```bash
npm config get registry 

npm config set registry https://registry.npm.taobao.org/
```

## 3. Yarn 查看源和切换源

```bash
yarn config get registry

**yarn config set registry https://registry.npm.taobao.org/**
```

## 4. Node版本管理工具 n

```bash
# 安装
npm install -g n

# 利用 n 下载所需node
n 版本号

# 下载最新版本
n latest

# 下载lts版本
n lts

# 切换版本
n

# 删除某个版本
n rm 版本号

# 以指定的版本号执行脚本
n use 7.4.0 index.js
```

## 5. 杀掉所有运行端口

```bash
pkill -9 node
```
