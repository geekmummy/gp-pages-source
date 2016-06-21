---
title: learn-C-08
date: 2016-06-17 22:52:36
tags:
  - C

---

```#include <stdio.h> #include <stdlib.h>
int main(void) {
  char letters[50];
  char userInit;
  int ctr,n1,numInits=0;
  for(ctr=0;ctr<50;ctr++){
    letters[ctr]=65+(rand()%26);
  }
  printf("What is your first initial?\n");
  userInit=getchar();
  n1=getchar();
  for(ctr=0;ctr<50;ctr++){
    if(letters[ctr]==userInit){
      numInits++;
    }
  }
  printf("\nIn the array, there were %d of your initials.\n", numInits);
  return 0;
}
```

<!-- more -->

## 数组 ##

- 定义数组： 

`int i[25]；`    
`char name[6]="Italy";  // leave room for the null`

- 在变量名后面加上方括号[]，并指定可能存放的最大元素个数。
- 元素，指数组包含的值。
- 如果初始的数值需要比要赋的初值大，就在定义数组时指定一个更大的数值大小，如：

`char name[80]="Italy";`

- 在定义数组时，可以通过把数组的数据放在大括号里并在数组名后面跟上等号来初始化数组。如下，既定义了一个整型数组又用5个值进行了初始化：

int vals[5]={10,40,70,90,120}

![](http://ww2.sinaimg.cn/large/691a3013gw1f4ymiyve96j206x05zt8s.jpg)

## 填充数组 ##

- 赋值：char name[6]="Italy
- 用户数据输入；
- 磁盘文件。

int main(void) {
  int ctr;
  int idSearch;
  int found =0;
  int custID[10]={313,453,502,101,892,475,792,912,343,633};
  float custBal[10]={0.00,45.43,71.23,301.56,9.08,192.41,389.00,229.67,18.31,59.54};

  printf("\n\n***Customer Balance Lookup ***\n");
  printf("What is the customer number?\n ");
  scanf(" %d",&idSearch);

  for (ctr=0;ctr<10;ctr++){
    if(idSearch==custID[ctr]){
      found=1;
      break;
    }
  }

  if(found){
    if(custBal[ctr]>100.00){
      printf("\n** That customer's balance is $%.2f.\n", custBal[ctr]);
      printf("No credit!\n");
    }
    else {
      printf("\n** The customer's credit is good!\n");
    }
  }

  else {
    printf("** You must have typed an incorrect customer ID.");
    printf("\n ID %3d was not found in list.\n", idSearch);
  }

  return 0;
}

- 该程序定义两个数组，称并行数组。并用顾客ID号和匹配的欠款初始化。
- 变量found 通常称为标记变量，它为程序的其他部分做标记，表明顾客ID是否找到。
- 这里的程序搜索是顺序搜索；更高级的搜索技术叫二分搜索(binary search)和斐波那契搜索(Fibonacci search)。

## 排序 ##

冒泡排序-bubble sort

- 在排序过程中，每一遍扫描都使较小的值“浮”到列表的上端。

![](http://ww1.sinaimg.cn/large/691a3013gw1f507duxqdpj20od0bv0ue.jpg)

- 冒泡排序只不过是嵌套的for循环：
- 内层循环扫描列表，并把不按任何符合顺序的一对数字进行交换
- 外层循环控制内层循环执行次数，为列表中的每个元素执行一次








