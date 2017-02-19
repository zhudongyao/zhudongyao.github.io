---
layout: post
title:  "Aliyun采用MySQLdump将远程数据拉取到本地"
date:   2016-05-11 06:24:22 +0800
---
在本地命令行输入：

```
$ mysqldump -h [host] -u [UserName] -p --opt --default-character-set=utf8   --hex-blob [DatabaseName] --skip-triggers  > [FileName]
```