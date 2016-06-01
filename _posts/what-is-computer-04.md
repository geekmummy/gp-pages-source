---
title: what-is-computer-04
date: 
tags:computer
  - default

---

# 熟练使用内存 #

## 内存的物理机制很简单 ##

![](http://ww1.sinaimg.cn/large/691a3013gw1f4ebd9rxuoj20gu0aqtag.jpg)

<!-- more -->

![](http://ww3.sinaimg.cn/large/691a3013gw1f4ebeafinsj20bv0fmack.jpg)

## 数据类型 ##

从内存看，就是占用的内存大小的意思。

    char，表示1字节的长度；
    short，表示2字节的长度；
    long，表示4字节的长度。

![](http://ww4.sinaimg.cn/large/691a3013gw1f4fr96reclj20er09hgn1.jpg)

## 指针 ##

一种变量，表示的是存储着数据的内存的地址。

通过使用指针，可以对任意指定地址的数据进行读写。

## 数组是高效使用内存的基础 ##

- 数组是指多个同样数据类型的数据在内存中连续排列的形式。
- 索引，作为数组元素的各个数据会通过连续的编号被区分开来。这个编号称为索引（index）。

## 栈(LIFO)和列队(FIFO) ##

![](http://ww1.sinaimg.cn/large/691a3013gw1f4friz8g2bj206k05fwes.jpg)    ![](http://ww4.sinaimg.cn/large/691a3013gw1f4frkl9tozj206905fq3a.jpg)

## 列队 ##

类似排队的机制

以环状缓冲区的方式来实现。

![](http://ww4.sinaimg.cn/large/691a3013gw1f4froh477rj20er08tta4.jpg)
 
> 从数组的起始位置开始有序地存储数据；
> 
> 再按照存储时的顺序把数据读出。
> 
> 在数组的末尾写入数据后，后一个数据就会被写入数组的起始位置。
> 
> 数组的写入和读出就循环起来。
> 

## 链表 ##

数据的值和下一个元素的索引组合在一起，就构成了数组的一个元素。

![](http://ww2.sinaimg.cn/large/691a3013gw1f4frtp7fjwj20en08et9w.jpg)

若需要追加或删除数据，使用链表更高效：

![](http://ww4.sinaimg.cn/large/691a3013gw1f4fruxgh3rj20eo07ygms.jpg)

![](http://ww1.sinaimg.cn/large/691a3013gw1f4frvc3sjqj20eu08ngmy.jpg)

## 二叉查找树使数据搜索更有效 ##

- 指在链表的基础上往数组中追加元素时，考虑到数据的大小关系，将其分成左右两个方向的表现形式。
- 第一个数值50 放到数组，第二个数值若比先前数值大，放到右边；反之若小，放到左边。
- 实际的内存不分两方向，这是在程序逻辑上实现的。

![](http://ww4.sinaimg.cn/large/691a3013gw1f4fs31sqy0j20er04udgf.jpg)

![](http://ww2.sinaimg.cn/large/691a3013gw1f4fs3nt4plj20ek0d1wgc.jpg)




