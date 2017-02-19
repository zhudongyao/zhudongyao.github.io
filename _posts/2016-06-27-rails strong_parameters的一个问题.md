---
layout: post
title:  "rails strong_parameters的一个问题"
date:   2016-06-27 09:45:27 +0800
---
rails的安全保护机制被触发时，往往需要加上如下代码：

```
private
  def issue_params
    params.require(:issue).permit(:title, :content)
  end
```

然后做如下引用：

```
Issue.create(issue_params)
```

问题：在private中定义的一个私有方法issue_params，为什么在后面像是一个变量来引用？感觉方法的调用不应该是这样的，就像是引用变量的感觉。