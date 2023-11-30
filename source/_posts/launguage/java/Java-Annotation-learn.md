---
title: Java-Annotation-learn
date: 2023-11-30 16:10:19
tags: [Java]
categories: [Java-Annotation-learn,Java-Base]
excerpt: "注解（Annotation），也叫[元数据](https://baike.baidu.com/item/元数据/1946090?fromModule=lemma_inlink)。一种代码级别的说明。它是JDK1.5及以后版本引入的一个特性，与类、接口、枚举是在同一个层次。它可以声明在包、类、字段、方法、[局部变量](https://baike.baidu.com/item/局部变量/9844788?fromModule=lemma_inlink)、方法参数等的前面，用来对这些元素进行说明，注释。"
cover: "/images/bg1.png"
---

> Java注解学习笔记 

## 1. 注解基础:

###  1.1 概念: 说明程序给计算机看的

### 1.2 注释: 文字描述程序,给程序员看

### 1.3 定义：

  注解（Annotation），也叫[元数据](https://baike.baidu.com/item/元数据/1946090?fromModule=lemma_inlink)。一种代码级别的说明。它是JDK1.5及以后版本引入的一个特性，与类、接口、枚举是在同一个层次。它可以声明在包、类、字段、方法、[局部变量](https://baike.baidu.com/item/局部变量/9844788?fromModule=lemma_inlink)、方法参数等的前面，用来对这些元素进行说明，注释。

#### 1.3.1 作用分类：

1. 编写文档：通过代码里标识的元数据生成文档【生成文档[doc](https://baike.baidu.com/item/doc/364715?fromModule=lemma_inlink)文档】

2. 代码分析：通过代码里标识的元数据对代码进行分析【使用反射】

3. 编译检查：通过代码里标识的元数据让[编译器](https://baike.baidu.com/item/编译器/8853067?fromModule=lemma_inlink)能够实现基本的编译检查

#### 1.3.2 JDK中预定义的注解

* @Override: 检测被该注解标注的方法是否是继承自父类（接口）的
* @Deprecated：该注解标注内容是否已过时
* @SuppressWarnings： 压制警告
  * 一般传参all  `@SuppressWarnings("all")`

#### 1.3.3 自定义注释

##### 1、格式：

元注解：`public @interface 注解名称 `

##### 2、本质:

> 注解本质是一个接口，该接口默认继承Annotation接口

  `public interface MyAnnotation extends java.lang.annotation.Annotation {
  }`

##### 3 、属性:

> 注解中可以定义的抽象（成员）方法

##### 4、要求

1. 返回值类型:
   * 基本数据类型
   * String 
   * 枚举
   * 注解
   * 以上类型数组
 2. 定义了属性，使用时需要给属性赋值
       1. 如果定义属性时，使用default关键字默认初始化值，则不需要传值
       2. 如果只有一个属性需要赋值，属性名为value,则直接定义值
       3. 数组赋值时,值使用{}包裹，如果数组只有一个值则直接写值

##### 5、元注解:

> 用于描述注解的注解  

* @Target: 描述注解能够作用的位置
   *  ElementType取值:
        * TYPE: 可以作用于类上
        * METHOD:  可以作用于方法上
        * FIELD:  可以作用于成员变量上
   * @Retention: 描述注解被保留的阶段
     * @Retention(RetentionPolicy.RUNTIME)： 当前被描述的注解，会保留到class 字节码文件中，并被JVM读取到
   * @Documented： 描述注解是否被抽取到API文档中
   * @Inherited: 描述注解是否被子类继承

##### 6、 在程序中使用解析注解： 获取注解中定义的属性值

 1. 获取注解定义位置的对象(Class Method Field)

 2. 获取指定的注解

     * getAnnotation(Class)
     *  其实就是在内存中生成一个该注释接口的子类实现对象
        ```java
        public propertiesImpl implments   Properties
              {
                public String className(){
                    return "com.zpc.demo2";
                }
                public String methodName(){
                    return "show";
                }
        
               }
        ```

  3. 调用注解中的抽象方法获取配置文件的属性值

## 2. 注解实战

