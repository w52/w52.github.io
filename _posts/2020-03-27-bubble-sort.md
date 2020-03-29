---
layout: article
title: 冒泡排序
tags: 数据结构
aside:
  toc: true
---

介绍冒泡排序算法的原理，以及代码实现

<!--more-->

## 原理

以[9, 1, 5, 8, 3, 7, 4, 6, 2]数据为例，介绍冒泡排序算法原理

当进行第一轮冒泡排序时， 流程如下图

![bubble_sort_1st.png](/assets/images/bubble_sort_1st.png)


当进行第二轮冒泡排序时， 流程如下图
![bubble_sort_2nd.png](/assets/images/bubble_sort_2nd.png)

以此类推，直到对所有数据完成排序。

## 实现

以下通过C语言实现冒泡排序

{% highlight C %}
#include <stdio.h>

#define MAXSIZE 10

typedef struct {
    int r[MAXSIZE + 1];
    int len;
} SqList;

void swap(SqList *l, int i, int j)
{
    int tmp = l->r[i];

    l->r[i] = l->r[j];
    l->r[j] = tmp;
}


void BubbleSort(SqList *l)
{
    int i;
    int j;

    for (i = 1; i < l->len; i++) {
        for (j = l->len - 1; j >= i; j--) {
            if (l->r[j - 1] > l->r[j]) {
                swap(l, j - 1, j);
            }
        }
    }
}

int main()
{
    SqList l;
    int arr[] = {9, 1, 5, 8, 3, 7, 4, 6, 2};
    int i;
    l.len = sizeof(arr) / sizeof(arr[0]);

    for (i = 0; i < l.len; i++) {
        l.r[i] = arr[i];
    }

    BubbleSort(&l);

    for (i = 0; i < l.len; i++) {
        printf("l.r[%d] = %d\r\n", i, l.r[i]);
    }

    return 0;
}
{% endhighlight %}
