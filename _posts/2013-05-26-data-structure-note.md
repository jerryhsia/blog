---
author: Jerry Hsia
title: 数据结构小记
excerpt:
layout: post
views:
  - 100
category:
  - 数据结构
tags:
  - 
post_format: [ ]
---

## 1 线性表

### 1.2 顺序存储

- 用一段连续的存储单元(通常为数组)依次存储数据元素
- 需要预分配存储空间，分大了浪费，分小了容易溢出，元素个数受限

- 查找：O(1)
- 插入与删除：O(n)

### 1.2 单链表

- 采用链式存储结构，用一组任意的存储单元存放元素
- 不需要分配存储空间，只要有就可以分配，元素个数不受限制
- 链表第一个节点为头结点
- 头指针指向第一个数据节点的存储位置
- 每个节点有数据域和指针域，指针域指向下一个节点，指针为NULL，链表结束

- 查找：O(n)
- 插入与删除：O(1)

### 1.3 静态链表

- 没有指针的高级语言用数组实现链表，由于使用数组，元素个数受到限制
- 数组最后一个元素游标指向链表第一个元素在数组中的位置，0表示链表为空
- 数组第一个元素游标指向下一个可用的数组位置，0表示链表已满
- 数据的元素为链表的节点，包含数据域和游标，游标指向下一个链表元素在数组中的位置，0表示链表结束

### 1.4 循环链表

- 在单链表的基础上引入尾指针的概念(rear)，指向头结点
- list->rear->next == head，代表链表为空
- 其他和单链表一致

### 1.5 双向链表