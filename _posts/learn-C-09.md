---
title: learn-C-09
date: 2016-06-19 08:53:54
tags:
  - C

---

    char input[81];    //holds a string as long as 80 characters 
    char *iptr=input;  //also could have done this: char *iptr=&input[0];
    gets(iptr);       //makes sure that iptr points to the string typed by the user.

<!-- more -->

## 指针 ##

### 内存地址 ###

- 内存地址，从0开始，并逐渐增加
- 每个地址就是不同的下标，每个内存位置就是不同的数组元素

### 定义指针变量 ###

- 定义指针变量，要理解以下 指针运算符

![](http://ww2.sinaimg.cn/large/691a3013gw1f52m9wbzcoj20g502zwei.jpg)

    int *pNum;     // 指针变量名可随意定义。许多程序员喜欢以p(pointer,指针)开头
    float *pValue;

- 指针变量存放了其他变量的地址。这是指针的主要用途
- 用取址运算符**&**，把一个变量的地址赋给一个指针。且指针未被初始化，不能用它们做任何事。

 `int age=19; int *pAge=&age; //定义整型变量age,并存储19。再定义指针变量pAge,并使它指向age.`

![](http://ww1.sinaimg.cn/large/691a3013gw1f52nhwgnnbj20bd06zq39.jpg)

- 在指针定义时，用*表示这个变量是一个指针
- 在把一个变量的地址赋给指针变量时不用*，除非在同时定义这个指针。

- 当把一个指针指向另一个变量后，可通过对指针取值来处理另一个值，用*取值运算符。
- 如上2条语句，有两种修改age值的方法：

    age=25; *pAge=25;

- 打印age值的两种方法：

        printf("the age is %d.\n", age);
`printf("the age is %d.\n", *pAge;`

# 数组和指针 #

- 数组是特殊类型的指针
- 可用指针符号(*)来获取数组的值，也可用数组符号([])来访问指针指向的值

## 数组名是指针 ##

- 数组名是指向第一个数组元素的指针。是指针常量。
- 如： int vals[5]={10,20,30,40,50};
- 当你定义并初始化vals时，C语言设置一个指向数组的指针并命名为vals。

![](http://ww4.sinaimg.cn/large/691a3013gw1f52rsheom2j209s07nmxg.jpg)

- 如打印数组的第一个值：

![](http://ww1.sinaimg.cn/large/691a3013gw1f52rtg7ahoj20dc04t74r.jpg)

## 在数组中取值 ##

![](http://ww1.sinaimg.cn/large/691a3013gw1f52run33dtj20dj06edgw.jpg)

## 字符和指针 ##

- 两条语句在内存中设置了几乎相同的内容。
- 唯一不同的是：第2条语句是指针变量。

![](http://ww1.sinaimg.cn/large/691a3013gw1f52rw5iv89j20d901gq2w.jpg)


## 指针数组 ##

一个包含25个整型指针的数组；一个包含25个字符型指针的数组

![](http://ww1.sinaimg.cn/large/691a3013gw1f52zf55pncj20ba01jdft.jpg)

字符数组，在数组中存储字符串的列表。即指向不同的字符串。如下程序：

    int main(){
    	int i;
    	char *names[5]={"Joe Swadley", "Richard Wikert", "Keith Miller", "Dean Davenport", "Stacy Wiquet"};
    
    	for(i=0;i<5;i++) {
    		printf("Name %d: %s\n", i, names[i]);
    	}
    return 0;
    }

![](http://ww4.sinaimg.cn/large/691a3013gw1f52zmiulfaj206h03jt8q.jpg)

每一个元素只不过是一个字符型指针，包含了不同人名的地址。names不存放字符串，它只存放指向字符串的指针。

![](http://ww1.sinaimg.cn/large/691a3013gw1f52zn96he1j208q04kdfy.jpg)

把字符型指针存储在nemes中就可以使程序表现得像names是一个字符串数组一样。












