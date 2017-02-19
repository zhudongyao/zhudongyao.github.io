---
layout: post
title:  "rails partial"
date:   2016-06-23 06:29:27 +0800
---
partial文件名必须以下划线开头，例： _issue_list.html.erb

可使用render来渲染partial文件，并可传递参数，例如：

```
<%= render partial: 'issue_list',locals: {issues: @issues} %>
```