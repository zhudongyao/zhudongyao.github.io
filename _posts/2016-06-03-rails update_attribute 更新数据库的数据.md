---
layout: post
title:  "rails update_attribute 更新数据库的数据"
date:   2016-06-03 07:51:34 +0800
---
对数据库中的一条或多条数据进行更新，更新一条数据用update_attribute

```
[DatabaseTableName].update_attribute(:[ColumnName],[Data])
```


对数据库中的一条或多条数据进行更新，更新多条数据用update_attributes

```
[DatabaseTableName].update_attribute(:[Column1Name] => [Data1],:[Column2Name] => [Data2],...:[ColumnXName] => [DataX],)
```

示例一：

```
DecoratingCaseImage.find(needs_to_be_added_id).update_attributes({:is_shown => true})
```

示例二：

```
decoratingcase =Decoratingcase.find_by_id(params[:id]).
   update_attributes :longitude => params[:longitude],:latitude => params[:latitude]
```