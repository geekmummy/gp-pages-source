---
title: learn-C-05
date: 2016-06-13 08:41:56
tags:
  - C

---

## 预处理指令 ##

- **#include<filename>**，或者 #include"filename"(自己写的头文件格式)。一个文件合并命令。
- 如下图，#include<addr.h>

![](http://ww4.sinaimg.cn/large/691a3013gw1f4tebu4zgjj20b6084js6.jpg)

- #include<stdio.h> 头文件，放在main()之前。

<!-- more -->

- **#define** 预处理指令，用来定义常量（constant）

`#define CONSTANT constantDefiniton`

- 该指令告诉C：把程序中CONSTANT出现的每个地方都用constantDefiniton替换。

## 输出 printf() ##

![](http://ww4.sinaimg.cn/large/691a3013gw1f4teugg0y8j20bq0663yr.jpg)

- 格式：

    printf(controlString [, data]);

    printf("I am %d", 16); /* controlString="I am %d"部分; data =16,可选部分 */

![](http://ww4.sinaimg.cn/large/691a3013gw1f4su3nnfm2j20gb04lglr.jpg)

    printf("Read a lot\n");/* \n换行符 */

![](http://ww4.sinaimg.cn/large/691a3013gw1f4su0zju53j20fu0543ym.jpg)

![](http://ww3.sinaimg.cn/large/691a3013gw1f4tf3778zcj20bm04xq36.jpg)

## 输入 scanf()##

![](http://ww1.sinaimg.cn/large/691a3013gw1f4tetf3onhj20af07m74q.jpg)

- 格式：

    scanf(controlString [, data]);

- 每个scanf()前面都要有printf()。

    printf("What is the amount?");
    scanf(" %d", **&**age); /* 变量age将存放 用户在按下Enter前输入的任何值。*/

- **&**  如果要输入整数、浮点数、字符、双精度数或其他任何一个变量组合，就要在scanf()中的变量名前加**&**。如果输入字符串到一个字符数组中，就不用在数组名前加&。

- & 不能放在指针（pointer）变量前面。

- **scanf()只能一次读取一个单词，如要读取多个单词，就得用多个scanf()。**

## 数学运算 ##

运算符的优先级

![](http://ww2.sinaimg.cn/large/691a3013gw1f4tnfc1ajyj20c608374l.jpg)

- **乘，/,% ** 同一级别，从左到右，先于**+，-**

- 可用 **（）**改变优先级

### 多重赋值 ###

![](http://ww2.sinaimg.cn/large/691a3013gw1f4tnwlb6n5j20fk04yjrs.jpg)

- 如果你想让很多变量的值为0，可以通过**多重赋值**来实现。

`total = cost * numberBought;`

    sTax = .08 * total;
    grandTotal = total + sTax;
    

