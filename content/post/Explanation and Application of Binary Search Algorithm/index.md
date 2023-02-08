---
title: Explanation and Application of Binary Search Algorithm
date: 2023-02-07T10:24:36.983Z
summary: Binary search has the advantages of fast search speed and good average performance, but only when the list is **ordered**, binary search works. It is often tested in interviews. This article will explain the binary search algorithm.
draft: false
featured: true
authors:
  - kevin
tags:
  - Algorithm
  - Search
categories:
  - Algorithm
image:
  filename: featured.png
  focal_point: Smart
  preview_only: false
links:
  - name: Read More
    url: "https://ifree.love/explanation-and-application-of-binary-search-algorithm/"
---

二分查找有着查找速度快，平均性能好等优点，但仅当列表是**有序**的时候，二分查找才管用。面试中比较常考，这篇文章来讲解一下二分查找算法。

### 我们先从一个场景开始了解吧

有一天，小明心血来潮去图书馆借了 N 本书，结果出图书馆的时候，警报响了，于是门卫大爷把小明拦下，要检查一下哪本书没有登记出借。小明正准备把每一本书在报警器下过一下，以找出引发警报的书，但是大爷露出不屑的眼神：你连二分查找都不会吗？于是大爷把书分成两堆，让第一堆过一下报警器，报警器响；于是再把这堆书分成两堆…… 最终，检测了 logN 次之后，大爷成功的找到了那本引起警报的书，露出了得意和嘲讽的笑容。于是小明背着剩下的书走了，心想：大爷果然还是我大爷！

是不是觉得二分查找很简单？！其实思想是很简单，但是有不少细节需要注意。正如 Knuth 大佬（发明 KMP 算法的那位）所说：

> Although the basic idea of binary search is comparatively straightforward, the details can be surprisingly tricky...

大致意思就是：**思路很简单，细节是魔鬼。**

接下来我就带大家来分析需要注意的细节，以及二分查找的巧妙运用。

点击[阅读更多](https://ifree.love/explanation-and-application-of-binary-search-algorithm/)看全文。
