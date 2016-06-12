---
title: learn-C-04
date: 2016-06-12 17:59:27
tags:
  - C
---


`#include<stdio.h>`
    int main(void){
      printf("This C stuff is easy!\n");
      return(0);
    }

<!-- more -->
## main函数 ##

- C语言中，所有命令和预定义函数应该使用小写字母；
- C程序由至少一个函数构成；
- 每个程序必须且只能包含一个main()函数。
- 函数名后面带有括号。

![](http://ww3.sinaimg.cn/large/691a3013gw1f4r8mgkbc0j20at02vmx3.jpg)

**警告**：calcIt()含有一个大写字母。当一个名称有多个部分，如doReportPrint()，通常把每个分隔词以大写字母开头，这样可以提高可读性（**函数名中不允许出现空格**）。但是不能把单词全部用大写，可用大写1、2个字母。

### 字符 ###

- 电脑能识别256个不同的字符，详见ASCII表；如下列：

![](http://ww2.sinaimg.cn/large/691a3013gw1f4r8zejlhuj207q012q2p.jpg)

- C语言的所有字符数据都括在**''**中，单个字符放在''中有效。如：

![](http://ww3.sinaimg.cn/large/691a3013gw1f4r95pzvolj20ap039mx4.jpg)

- 多个字符的组合，即字符串，放在**""**间，如："C is fun to learn."

### 数字 ###

- C程序必须有一种存储数字的方式：整型，浮点型。
- 浮点型占用的内存是整型的2倍
- 尽量使用整型，不要让整型以0开头，除非整型是0本身。

## 练习： ##

*打印3行消息，每行数据类型为：字符（B），整型（87）和浮点型（85.9）。*

![](http://ww3.sinaimg.cn/large/691a3013gw1f4s53dcecfj20d805u3zm.jpg)

输出结果为：

![](http://ww3.sinaimg.cn/large/691a3013gw1f4s54495esj206k01qjrj.jpg)

错误在于：87，85.9 写了单引号''。如下正确：

![](http://ww1.sinaimg.cn/large/691a3013gw1f4s55ytoytj20c505u0tn.jpg)

![](http://ww2.sinaimg.cn/large/691a3013gw1f4s56fyqwvj206v01z3yo.jpg)

