---
title: 部署Blog(Hexo)
date: 2023-11-29
tags: 部署
categories: hexo
cover: /images/bg1.png
---

> [配置](https://redefine-docs.ohevan.com/footer#%E8%BF%90%E8%A1%8C%E6%97%B6%E9%97%B4)

### 1.一键部署

#### （1）在_config.yml中配置github仓库和分支
```yml
deploy:
  type: git
  repository:  # 仓库地址
  branch:  # 分支
  # 测试
```
#### （2）执行部署命令
```bash
hexo g -d
```

