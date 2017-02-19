---
layout: post
title:  "rails 在view层显示carrierwave文件名"
date:   2016-08-01 09:00:43 +0800
---
#介绍三种方法
不妨设，数据库表名为page，列名为form
（1）

```
<%= File.basename(@page.form.path) %>
```

（2）

```
<%= @page.form.file.filename %>
```

（3）使用carrierwave时，在数据库中新建一字段 : original_filename  
在controller的update和create方法中，进行如下方式存储：

```
page.file_name = page.original_filename
```

在view层，调用file_name即可：

```
<%= @page.file_name %>
```