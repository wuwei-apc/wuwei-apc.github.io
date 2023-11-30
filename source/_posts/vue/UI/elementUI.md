---
title: Vue3 Element-plus配置    
date: 2023-11-29
tags: 前端
categories: Element-plus
---

##                                

### 一、npm 安装element-plus

```shell
在vue3cli 项目更目录下的命令行中输入以下代码
npm install element-plus --save
```

### 二、main.js中全局引入

```js
在mian.js 中加入以下代码
import ElementPlus from 'element-plus'
import 'element-plus/dist/index.css'
app.use(ElementPlus)
```

