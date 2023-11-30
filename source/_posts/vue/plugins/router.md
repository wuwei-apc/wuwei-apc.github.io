---
title: vue-router 配置
date: 2023-11-29 
tags: 前端
categories: vue-router
cover: /images/bg1.png
---

### 一、npm安装vue-router插件

         ```shell
         在项目文件夹下的命令行输入以下命令:
           npm install vue-router
         ```

### 二、在vue3cli项目下的src文件夹中创建router包并配置

####      1.创建router包

####      2.创建index.js输入以下代码基本配置

```js

 import { createRouter, createWebHashHistory } from 'vue-router'
 
 const router = createRouter({
   history: createWebHashHistory(),
   routes: [
     //...
   ],
 })
```



### 三、main.js中引入router包中的index.js

```js
配置如下：
import { createApp } from 'vue'
import App from './App.vue'
import router from './route'

const app = createApp(App)
app.use(router)
app.mount('#app')
```

