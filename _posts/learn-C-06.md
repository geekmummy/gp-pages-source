---
title: learn-C-06
date: 2016-06-13 16:30:54
tags:
  - C

---

# 操作空间 #

## 复合赋值 ##

计数器变量：当特定事件发生时，它的值增加1。

![](http://ww1.sinaimg.cn/large/691a3013gw1f4tor8rcuoj209q07ujst.jpg)

<!-- more -->

输出为：

![](http://ww1.sinaimg.cn/large/691a3013gw1f4torr3jwvj203u031wel.jpg)

### 复合赋值运算符 ###

    lossCount=lossCount+1; 等同于 lossCount +=1;

![](http://ww4.sinaimg.cn/large/691a3013gw1f4tseh4m5zj20g104st91.jpg)

- **复合赋值运算符**的优先级很低，

![](http://ww2.sinaimg.cn/large/691a3013gw1f4tsi20chvj208d03wq2y.jpg)

## 强制类型转换（typecast） ##

- 格式： (dataType)value

    int age; 把age转换成值为6.0的float (float)age;

## 练习

    int main(){
    	int age;
    	float dogAge;
    	printf("How old are you?\n ");
    	scanf(" %d", &age);
    	dogAge = (float)age / 7.0;
    	printf("If you were a dog, you'd only be %.1f years old!\n", dogAge);

    	return(0);
    }

# 关系运算符 #

**在C语言中，对关系运算符进行求值时，总产生数值1或0。为真-1，为假-0。**

    a=(4<10); // (4<10) is true, so a 1 is put in a
    b=(8==9); // (8==9) is false,so a 0 is put in b

![](http://ww2.sinaimg.cn/large/691a3013gw1f4tsvcnv17j20fq0573yp.jpg)

- 关系运算符两侧数据类型相同

## if ##

- 如果某事为真，就做一件事；否则，就做另外的事
- 格式：

        if (condition)
    { block of one or more C statements;}
    
- 如：

    if(age<18){
    	printf("You cannot vote yet\n");
    	yrs=18-age;
    	printf("You can vote in %d years.\n",yrs);
    }  


## else ##

    if (condition){ 
    	block of one or more C statements;
    }
    else{
    	block of one or more C statements;
    }

# 逻辑运算符 #

![](http://ww2.sinaimg.cn/large/691a3013gw1f4twd1zsjvj20ft0410su.jpg)

    if(age>=21){
    	if(age<=65){
    		printf("The age falls between 21 and 65.\n");
    	}
    }

以上代码的写法不直观，并且逻辑变得有些复杂。运用逻辑运算符更清晰：

    if((age>=21) && (age>=65)){
    	printf("The age falls between 21 and 65.\n");
    }

- && 两边的条件必须都为真
- || 一边条件为真
- ！ 将真或假的条件取反：即**真变假，假变真**

`if(!(sales<3000)) 等同于 if(sales>=3000)`

逻辑运算符把关系运算符连接起来

## 练习 ##

    int main(){
      char name[25];
      printf("What is your last name?\n");
      scanf(" %s", name);
    
      if ((name[0]>='P') && (name[0]<='S')){
    	printf("You must go to room 2432\n");
    	printf("for your tickets.\n");
      }
      else {
    	printf("You can get your tickets here.\n");
      }
      return(0);
    }
    
## 条件运算符 ##

- 唯一需要3个参数的C运算符；
- 格式：

`relation ? trueStatement : falseStatement;`
`(total <= 3850) ? (total *= 1.1) : (total *=1.0);`
`解析：total<=3850是否成立？如果成立，就做第一件事；否则，就做第二件事。`

- 几乎任何**if-else**语句都可以，写成条件语句。
- 条件运算符可以出现在if语句不能出现的地方。

### 递增++ 和 递减-- ###

`count++; ++count;    count--; --count;`
`前缀递增  后缀递增     前缀递减  后缀递减`

- 前缀运算符和后缀运算符独立使用时，会产生相同的结果。

`int i=2,j=5,n; (1) n=++i*j; (2) n=i++ *j;`
`解析：(1)先执行 i+1，再执行 *j。 (2)先执行 i*j，再执行 i+1。`

## 运算符sizeof() ##

用来查明存储任何类型的数据所占用的内存单元。如查明整型和浮点型占用的内存：

    i=sizeof(int);
    f=sizeof(float);

    char name[]="George Paul";
    int i=7;
    printf("The size of i is %d\n", sizeof(i));
    printf("The size of name is %d\n", sizeof(name));

输出为：

    The size of i is 2
    The size of name is 12