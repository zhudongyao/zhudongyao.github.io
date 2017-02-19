---
layout: post
title:  "Rails left join 多张表"
date:   2016-06-13 08:56:16 +0800
---
下面的这个例子为 left join 两张表，查两个条件：

```
@admin_tasks = Admin::Task
    .joins("left join decoratingcases on admin_tasks.decoratingcase_id = decoratingcases.id")
    .joins("left join householders on decoratingcases.householder_id = householders.id")
    .page(params[:page]).where(conditions.join(" and ")).order("occur desc, decoratingcase_id desc")
```