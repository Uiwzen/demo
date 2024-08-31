# 超市销售系统

超市管理系统

包含推荐功能，按照订单进行推荐  
多用户，一个给后台管理，一个给用户

## 快速开始

强烈建议统一使用`pnpm`作为包管理器

安装 pnpm

```
npm -g pnpm
```

进入项目后，运行以下指令安装相关依赖

```
pnpm i
```

## 使用 git 进行团队协作

首先需要有一个 github 账号  
请给出自己的 github 账号以便于我将各位添加到项目中

下载项目请使用

```
git clone https://github.com/Uiwzen/demo.git
```

在每次开始你的编辑前，请在项目的根目录中重新拉取一遍项目，确保你的项目应用了最新的更改

```
git pull
```

在结束完你的编辑之后，请提交

```
git add .
git commit -m "这里写提交的注释信息"
```

此时你的更改会暂存到本地，接下来使用以下进行同步（最好尽可能频繁地同步）

```
git push -u origin main
```

## 技术栈

#### 前端

- Vuejs
- Vite
- [elementPlus](https://element-plus.org/zh-CN/)
- [echarts](https://echarts.apache.org/zh/index.html)

#### 后台

- Python
- flask

#### 数据库

- mysql 放本地  
  存商品相关信息：商品名、商品 ID、商品价格、商品类型  
  用户信息： 用户 ID、用户密码  
  订单： 订单编号、商品编号、数量

## 功能与页面描述

### 登录页面

包含登录和注册  
管理员和用户直接用同一个登录页面，区别只在于账户和密码

### 前台

前台根据 ID 和密码进行登录  
用户认证这些直接不搞了，安全直接不管  
账户密码正确，直接跳到对应的 URL

- 首页：展示全部产品信息，含有筛选、搜索等功能
- 购物车： 查看在购物车中的订单（有哪些商品）、结算（含推荐的商品）
- 我的：会员信息、 历史订单信息

### 后台

固定的账户密码和 URL

- 订单信息：用户提交的订单
- 统计信息：用图标展示一下销售情况（销售额、哪些商品销售最多，反正就画几张图），推荐下月的热销产品
