---
layout: post
title: "面试问题1-百度"
category: [baidu]
tags: [interview]
published: false
---
{% include JB/setup %}

一面：

第一道很简单，问程序在内存有几个数据区，堆和栈区有啥区别

&gt;&gt; 堆和栈区有啥区别？

刚才在看thinking in java，刚好看到书里这样解释，所以就写下来。

For maximum run-time speed, the storage and lifetime can be determined while the program is being written, by placing the objects on the stack (these are sometimes called automatic or scoped variables) or in the static storage area.

The second approach is to create objects dynamically in a pool of memory called the heap, you don't know until run time how many objects you need, what their lifetime is, or what their exact type is.

第二道是两个有序数组（可能升序或降序），要求合并到一个大数组中，使其仍然有序，讲了大体思路，并用C简单写了实现代码

第三道是给出int型的x、 y两个数，要求不借助第三个变量交换x和y的值。

第四题有1.txt、2.txt。。。。n.txt的n个文件，要求查出含有字符串“love”的文件，并返回文件名。

第五道题，测试一台自动售货机。

死锁的四个条件、进程通信的方式，宕机测试

二面：

第一道，给出两个集合A和B，其中集合A={name}，集合B={age、sex、scholarship、address、...}，要求：问 题1、根据集合A中的name查询出集合B中对应的属性信息；问题2、根据集合B中的属性信息（单个属性，如age&lt;20等），查询出集合A中对应 的name

第二道，给出一个文件，里面包含两个字段{url、size}，即url为网址，size为对应网址访问的次数，要求：问题1、利用Linux  Shell命令或自己设计算法，查询出url字符串中包含“baidu”子字符串对应的size字段值；问题2、根据问题1的查询结果，对其按照size 由大到小的排列。（说明：url数据量很大，100亿级以上）

第三道，测试一部手机（手机是普通手机，除了系统软件外，可能已经安装了某些应用软件）

第四道，根据我简历上的项目经历，选出了其中的一个“Gloss搜索推荐系统”项目，让我介绍其架构以及我负责的工作

第五道，询问了是否比较熟悉的编程语言（C/C++/C#）、VS2008以及对Linux Shell、Python认识等

先放着，一道道做出来。。。挺有趣的。