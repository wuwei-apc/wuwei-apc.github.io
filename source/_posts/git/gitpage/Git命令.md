---
title:  Git命令
date: 2023-11-30
tags: git教程
categories:  Git命令
---

### 1.基本命令

![Untitled](/images/Git命令/Untitled.png)

### 2.初始化本地库

```bash
# 在项目目录下执行此命令
git init
```

![Untitled](/images/Git命令/Untitled%201.png)

### 3.查看本地库状态

```bash
git status
```

![Untitled](/images/Git命令/Untitled%202.png)

### 4.添加到暂存区

```bash
# . 代表把所有修改文件添加到暂存区域
git add .
```

![Untitled](/images/Git命令/Untitled%203.png)

```bash
#查看当前状态,修改的文件都变为绿色代表添加到暂存区成功
git status 
```

![Untitled](/images/Git命令/Untitled%204.png)

```bash
# 删除工作区文件
git rm --cached <file>
```

### 5.提交本地库

```bash
git commit -m "日志信息" 文件名
```

![Untitled](/images/Git命令/Untitled%205.png)

### 6.查看日志信息

```bash
git reflog
# 或者
git log
```

![Untitled](/images/Git命令/Untitled%206.png)

![Untitled](/images/Git命令/Untitled%207.png)

### 7.历史版本切换

```bash
git reset --hard <版本号>
```

![Untitled](/images/Git命令/Untitled%208.png)