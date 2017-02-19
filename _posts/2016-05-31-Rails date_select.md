---
layout: post
title:  "Rails date_select"
date:   2016-05-31 03:00:16 +0800
---
欲实现一个日期选择框，且默认显示日期为当天，且月份为数字，输入以下代码即可：


```
<%= f.date_select :date,  { :use_month_numbers => true }  %>
```