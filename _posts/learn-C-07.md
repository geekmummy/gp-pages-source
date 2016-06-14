---
title: learn-C-07
date: 2016-06-14 08:27:14
tags:
  - C

---




<!-- more -->

# 保持控制 #

## while 循环 ##

- 总是出现在循环的开始或结尾
- 格式：

`while (condition){
block of one or more C statements;
}`

- 只要condition为真，while语句的主体就会一直重复执行。
- if和while 的共同点和不同点：

![](http://ww1.sinaimg.cn/large/691a3013gw1f4ujjs5yhfj20dg0833z8.jpg)

    wrongVal++;的作用：改变condition中的变量，最终结束while 语句。

### 利用while清屏 ###

`void dispTitle(void){
	int i=0;
	while(i<25){
		printf("\n");
		i++;
	}
	printf("\n\n*step right up to the Blackjack tables*\n\n");
	return;
}
`

## do-while ##

- 与while循环一样：

`do {
	block of oneor more C statements;
}
while (condition)
`

