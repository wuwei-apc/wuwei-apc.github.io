---
title: 部署Blog(Hexo)
date: 2023-11-29
tags: 部署
categories: hexo
cover:  https://mygithubcdn.educatedtest.eu.org/gh/mycodeoen/MyPicture@main/blog/202409021145034.jpg
---

> [配置](https://redefine-docs.ohevan.com/footer#%E8%BF%90%E8%A1%8C%E6%97%B6%E9%97%B4)

### 1.一键部署

#### （1）在_config.yml中配置github仓库和分支
```yml
deploy:
  type: git
  repository:  # 仓库地址
  branch:  # 分支
```
![image-20240902030612843](https://mygithubcdn.educatedtest.eu.org/gh/mycodeoen/MyPicture@main/blog/202409020306519.png)

#### （2）执行部署命令

```bash
hexo clean # 解决缓存问题
hexo g -d #一键部署
```

![image-20240902025912694](https://mygithubcdn.educatedtest.eu.org/gh/mycodeoen/MyPicture@main/blog/202409020259919.png)

## 启动自动化脚本部署

```shell
# 执行 app.exe
填写信息
# `ctrl+s`触发
```

![image-20240902224734605](https://mygithubcdn.educatedtest.eu.org/gh/mycodeoen/MyPicture@main/blog/202409022247671.png)

## 成功😂





