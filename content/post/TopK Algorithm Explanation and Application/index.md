---
title: TopK Algorithm Explanation and Application
date: 2023-02-07T10:24:36.983Z
summary: What is the TopK algorithm? To put it simply, it is to find the first K largest (of course, it can also be the first K smallest) number in a bunch of data.

This question is also a very classic algorithm question, whether it is in an interview or in actual development, it is very typical. Do you know how to solve this problem?
draft: false
featured: true
authors:
  - kevin
tags:
  - Algorithm
  - Sort
categories:
  - Algorithm
image:
  filename: featured.png
  focal_point: Smart
  preview_only: false
links:
  - name: Read More
    url: "https://ifree.love/topk-algorithm-explanation-and-application/"
---

## 前言

什么是 TopK 算法？简单来说就是在一堆数据里面找到前 K 大（当然也可以是前 K 小）的数。

这个问题也是十分经典的算法问题，不论是面试中还是实际开发中，都非常典型。面对这种问题，你知道怎么解决吗？

## 最经典的方法之堆

面对 Top K 问题，最经典的解法是利用**堆**。（堆是**数据结构**里的知识，学习算法的一个重要前提需要了解常用的数据结构，既然大胆点开了算法文章，这里默认大家对前提知识已经了解，在此就不多做介绍，不懂请自行搜索，后期有时间我再写相关文章。）

这里简单给大家介绍一下堆，以防陷入知识盲区的旁友。

堆（数据结构）：堆可以被看成是一棵树【树就不用多说了吧，对，就是你家门外的那棵树 （手动滑稽）】

最大堆（也叫大根堆、大顶堆）：根结点的键值是所有堆结点键值中最大者，且每个结点的值都比其孩子的值大。

最小堆（也叫小根堆、小顶堆）：根结点的键值是所有堆结点键值中最小者，且每个结点的值都比其孩子的值小。

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228225040487.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2NDUyNTg0,size_16,color_FFFFFF,t_70)

点击[阅读更多](https://ifree.love/topk-algorithm-explanation-and-application/)看全文。
