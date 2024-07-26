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

It is unsafe for code in different goroutines to read and write to the same `map` simultaneously. The `map` values themselves may become inconsistent due to these operations, and related programs may experience unpredictable issues.

We can demonstrate the concurrency safety problem with `map` using the following code:

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

The error message is: `fatal error: concurrent map read and map write.`

If you check the Go source code: [hashmap_fast.go#L118](https://github.com/golang/go/blob/master/src/runtime/hashmap_fast.go#L118), you'll see that during reads, the `hashWriting` flag is checked, and if this flag is set, a concurrency error is reported.

The flag is set during writes: [hashmap.go#L542](https://github.com/golang/go/blob/master/src/runtime/hashmap.go#L542)

`h.flags |= hashWriting`

After setting, the flag is cleared: [hashmap.go#L628](https://github.com/golang/go/blob/master/src/runtime/hashmap.go#L628)

There are also several other checks for concurrent read and write issues in the code, such as checking for concurrent writes, similar issues when deleting keys, and concurrency problems during iteration.

Sometimes, concurrency issues with `map` are not easily detected; you can use the `-race` flag to check.

So, how can we ensure concurrency safety for `map`?

Click [Read More](https://ifree.love/go-map-and-concurrency-security-issues/) for the full article.
