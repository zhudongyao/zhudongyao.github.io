---
layout: post
title:  "Html document"
date:   2016-06-04 07:30:24 +0800
---
Document对象定义：每个载入浏览器的 HTML 文档

Document 对象使我们可以从脚本中对 HTML 页面中的所有元素进行访问

提示：Document 对象是 Window 对象的一部分，可通过 window.document 属性对其进行访问。

比如：
（1）Find an element by element id

```
document.getElementById(id)
```

（2）Find elements by tag name

```
document.getElementsByTagName(name)	
```


（3）Find elements by class name

```
document.getElementsByClassName(name)
```