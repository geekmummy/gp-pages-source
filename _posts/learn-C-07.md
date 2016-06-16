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

    do {block of oneor more C statements;}
while (condition)

- while 和 do-while 重复执行大括号中的所有代码；
- 二者的区别在于用来控制循环的关系测试所处的位置不同：while语句在循环的顶部测试
- do-while语句在循环的底部测试。
- 选择while 还是 do-while 通常不太重要：2种循环可以做相同的事情。

`int main(void) {
   int ctr=1;
	while (ctr<=20){
 	 printf("%d\n", ctr);
	 ctr++;
	}
	ctr=1;
	do {
		printf("%d\n",ctr);
 		ctr++;
	}while (ctr<=20);
	return 0;
}`


## for循环 ##

- 格式：

`for (startExpression; testExpression; countExpression)`
`{ block of oneor more C statements; }`

![](http://ww4.sinaimg.cn/large/691a3013gw1f4ws646kdej207r02amx3.jpg)

![](http://ww3.sinaimg.cn/large/691a3013gw1f4ws8l1800j206n04jjre.jpg)

用while语句实现相同功能：

![](http://ww4.sinaimg.cn/large/691a3013gw1f4wsbqmbirj207h02zt8n.jpg)

嵌套循环：

    for (outer=1; outer<=3; outer++){
    	for (inner=1; inner<=5; inner++) {
			printf("%d", inner);}
		printf("\n");}

- 外层循环从1到3，内层循环用于打印前5名顾客；
- 用于循环特定的次数，如 打印3张前5名顾客的列表（以上）

### break; ###

- 总是出现在循环中，用于终止当前的循环。
- break出现在循环主体中，break会立刻终止循环而程序的其他部分会继续执行。

![](http://ww2.sinaimg.cn/large/691a3013gw1f4wtlgtk24j20ch035t8s.jpg)

以上代码中的break，使循环在打印5个数字后就停止了。



    int main(void) {
      int numTest;
      float stTest,avg,total=0.0;
    
      for(numTest=0; numTest<25; numTest++){
    printf("what is the next student's test score?");
    scanf(" %f", &stTest);
    if (stTest < 0.0){
      break;
    }
    total+=stTest;
      }
      avg=total/numTest;
      printf("\nthe average is %.1f%%.\n", avg);
    
    	return 0;
    }

### continue ###

-break使循环提前跳出，与之相反，continue是强迫循环提前继续。

    int i;
      for (i=1;i<=10;i++){
    	if ((i%2)==1){
      printf("I'm rather odd...\n");
      continue;
    }
    printf("Even up!\n");
      }
    	return 0;
    }



的
