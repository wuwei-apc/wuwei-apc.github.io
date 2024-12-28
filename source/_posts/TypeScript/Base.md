---
title: TypeScript快速学习
date: 2024-12-13
tags: TypeScript
categories: TypeScript
cover:  https://mygithubcdn.educatedtest.eu.org/gh/mycodeoen/MyPicture@main/blog/202409021145034.jpg
---

## 一、 TypeScript简介

> TypeScript和JavaScript关系图
>
> ![image-20241116183048480](https://mygithubcdn.educatedtest.eu.org/gh/mycodeoen/MyPicture@main/blog/202411161830530.png)

1. `TypeScript`由微软开发，基于`JavaScript`的一个扩展语言

2. `TypeScript` 包含了`JavaScript`的所有特性

3. 因为`TypeScript`在`JavaScript`的基础之上增加了新的特性:

   - 静态类型检查
   - 接口
   - 泛型

   等当前主流的开发特性,所以更适合大型的项目开发

4. 但是`TypeScript`最终还是需要通过编译转换为`JavaScript`,然后再交给浏览器或其他`JavaScript`的运行环境中运行

## 二、 为什么需要`TypeScript`呢?

### 2.1 `JavaScript`中的编程困扰

1. 不清楚的数据类型

   ```javascript
   let welcome = 'hello'
   welcome() // 此行报错: TypeError: welcome is not a function
   ```

   

2. 有逻辑漏洞

3. 访问不存在的属性

1. 低级的拼写错误

## 三、编译TypeScript

> 浏览器不能直接运行`TypeScript`代码,需要编译为`JavaScript`在交由浏览器解析执行

### 3.1 命令行编译

#### 3.1.1 安装编译器

```bash
npm install typescript -g
```

#### 3.1.2 编译

```bash
tsc 以.ts结尾的文件名
```

![image-20241117131748215](https://mygithubcdn.educatedtest.eu.org/gh/mycodeoen/MyPicture@main/blog/202411171317300.png)



### 3.2 自动化编译

#### 3.2.1 生成ts配置文件

```bash
tsc --init
```

![image-20241117132116317](https://mygithubcdn.educatedtest.eu.org/gh/mycodeoen/MyPicture@main/blog/202411171321477.png)

#### 3.2.2 监视ts文件的变化

```bash
tsc --watch # 如果不写具体的文件名，则监视当前目录下所有的文件
```

![image-20241117132613106](https://mygithubcdn.educatedtest.eu.org/gh/mycodeoen/MyPicture@main/blog/202411171326173.png)

![image-20241117132820734](https://mygithubcdn.educatedtest.eu.org/gh/mycodeoen/MyPicture@main/blog/202411171328776.png)

## 四、类型声明

```typescript
let a: string
let b: number
let c: boolean


a = 'Tom' 
b = 20
c = false
console.log('a: '+a + ' b:' + b + ' c: ' + c);

function count(x:number,y:number) {
    return x + y
}

let result = count(2, 3)
console.log(result);
```

## 五、类型推断

> `TypeScript`可以自动推断类型，可以不用写类型声明，但建议写上类型声明。

## 六、类型总览

`JavaScript`类型

| 类型      | 类型名                                       |
| --------- | -------------------------------------------- |
| string    | 字符串                                       |
| number    | 数字                                         |
| boolean   | 布尔                                         |
| null      | 空值                                         |
| undefined | 未定义                                       |
| bigint    | 大数                                         |
| symbol    |                                              |
| object    | 对象类型包含：Array、Function、Date、Error等 |

`TypeScript`数据类型

> `TypeScript`除包含`JavaScript`中的所有类型外还新增了其他的类型

| any            |
| -------------- |
| unknown        |
| never          |
| void           |
| tuple          |
| enum           |
| 自定义类型方式 |
| type           |
| interface      |