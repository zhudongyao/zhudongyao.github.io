---
layout: post
title:  "Rails reverse_each"
date:   2016-05-31 02:54:15 +0800
---
对数组进行倒序排列
例子如下:

```
a = [ "a", "b", "c" ]
a.reverse_each {|x| print x, " " }
```

则输出：

```
c b a
```