---
title: Go map and concurrency security issues
date: 2023-02-06T10:24:36.983Z
summary: It is not safe for code in different goroutines to read and write to the same map at the same time. The map value itself may be confused by these operations, and related programs may also have unpredictable problems.
draft: false
featured: true
authors:
  - kevin
tags:
  - Golang
  - Map
categories:
  - Golang
image:
  filename: featured.png
  focal_point: Smart
  preview_only: false
links:
  - name: Read More
    url: "https://ifree.love/go-map-and-concurrency-security-issues/"
---

在同一时间段内，让不同 goroutine 中的代码，对同一个`map`进行读写操作是不安全的。`map`值本身可能会因这些操作而产生混乱，相关的程序也可能会因此发生不可预知的问题。

我们可以用如下代码展示 `map` 的并发安全问题。

```Go
package main

func main() {
	m := make(map[int]int)

	go func() {
		for {
			_ = m[1]
		}
	}()

	go func() {
		for {
			m[2] = 2
		}
	}()

	select {}
}
```

错误信息是: `fatal error: concurrent map read and map write。`

如果你查看 Go 的源代码: [hashmap_fast.go#L118](https://github.com/golang/go/blob/master/src/runtime/hashmap_fast.go#L118),会看到读的时候会检查 `hashWriting` 标志， 如果有这个标志，就会报并发错误。

写的时候会设置这个标志: [hashmap.go#L542](https://github.com/golang/go/blob/master/src/runtime/hashmap.go#L542)

`h.flags |= hashWriting`

[hashmap.go#L628](https://github.com/golang/go/blob/master/src/runtime/hashmap.go#L628) 设置完之后会取消这个标记。

当然，代码中还有好几处并发读写的检查， 比如写的时候也会检查是不是有并发的写，删除键的时候类似写，遍历的时候并发读写问题等。

有时候，`map` 的并发问题不是那么容易被发现, 你可以利用`-race`参数来检查。

那么我们如何保证 `map` 的并发安全呢？

点击[阅读更多](https://ifree.love/go-map-and-concurrency-security-issues/)看全文。
