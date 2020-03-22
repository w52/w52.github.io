---
layout: article
title: 数据结构(1) —— 数组
tags: 数据结构
aside:
  toc: true
---

本文对数据结构中最简单的线性结构 —— 数组进行数据

<!--more-->

## 数组定义

**数组** 是在一片连续的存储内存空间中存放的数据集合，其中每一个数据类型是相同的。

因此，数组中存储的是多个相同数据类型的数据项。

数组的结构如下示意图所示

![ds-array.png](/assets/images/ds-array.png)


数组的特点：

- 存储的数据类型相同

- 存储的内存空间连续

- 通过数组索引进行访问

## 数组实现

此处使用C语言实现数组的定义以及访问

在C语言中，数组的定义和访问如下图所示

![array-in-c-language.png](/assets/images/array-in-c-language.png)


代码实现如下

{% highlight C %}
#include <stdio.h> 
  
int main() 
{ 
    int arr[5]; 
    arr[0] = 6; 
    arr[1] = 8; 
    arr[4 / 2] = 10; // this is same as arr[2] = 2 
    arr[3] = arr[0]; 
  
    printf("%d %d %d %d", arr[0], arr[1], arr[2], arr[3]); 
  
    return 0; 
} 
{% endhighlight %}

输出结果为

```
6 8 10 6
```

## 参考

1. [Array Data Structure](https://www.geeksforgeeks.org/array-data-structure/)

2. [Introduction to Arrays](https://www.geeksforgeeks.org/introduction-to-arrays/)

3. [Arrays in C/C++](https://www.geeksforgeeks.org/arrays-in-c-cpp/)

4. [Difference between pointer and array in C](https://www.geeksforgeeks.org/difference-pointer-array-c/)


