---
layout: post
title:  "rails 评论提交hotkeys"
date:   2016-07-25 08:53:48 +0800
---
往往，我们聊天或输入评论可以按快捷键直接发送，通常是`Ctrl`+`Enter`，以此为例，用到js的jquery.hotkeys库来实现该功能。
（1）通过wget命令把js文件添加进源码

```
$ wget https://raw.githubusercontent.com/jeresig/jquery.hotkeys/master/jquery.hotkeys.js
```

（2）在application.js文件中添加如下代码：

```
//= require vendor/jquery.hotkeys
```

其中（1）中的文件放在了app/assets/javascript/vendor/ 目录下

（3）在评论框的view层代码尾部添加如下代码：

```
<script>
  $(".reply textarea#comment_content").keydown(function(e) {
    if ((e.ctrlKey||e.metaKey) && e.keyCode == 13) {
      $(".reply input[type=submit]").click();
    }
  });
</script>
```