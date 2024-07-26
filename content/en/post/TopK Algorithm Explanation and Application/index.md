---
title: TopK Algorithm Explanation and Application
date: 2023-02-04T10:24:36.983Z
summary: What is the TopK algorithm? To put it simply, it is to find the first K largest (of course, it can also be the first K smallest) number in a bunch of data.
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

## Introduction

What is the TopK algorithm? Simply put, it is used to find the top K largest (or the top K smallest) numbers in a set of data.

This is a classic algorithmic problem, both commonly encountered in interviews and in practical development. Do you know how to solve it?

## The Classic Approach: Heap

For the Top K problem, the most classic solution involves using a **heap**. (A heap is a **data structure**, and understanding common data structures is a fundamental prerequisite for learning algorithms. Since you’ve ventured into an algorithm article, it's assumed that you're familiar with these prerequisites. If not, please search for more information, and I’ll cover this in future articles.)

Here’s a brief introduction to heaps to prevent knowledge gaps.

Heap (Data Structure): A heap can be viewed as a tree [and we won't go into details about trees here; yes, that tree outside your house (sarcastic smile)].

Max Heap (also known as a Large Root Heap or Max-Heap): The root node's key is the largest among all heap nodes, and each node's value is greater than the values of its children.

Min Heap (also known as a Small Root Heap or Min-Heap): The root node's key is the smallest among all heap nodes, and each node's value is smaller than the values of its children.

![Insert image description here](https://img-blog.csdnimg.cn/20200228225040487.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2NDUyNTg0,size_16,color_FFFFFF,t_70)

Click [Read More](https://ifree.love/topk-algorithm-explanation-and-application/) for the full article.
