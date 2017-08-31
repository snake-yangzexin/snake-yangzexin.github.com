---
title: alert
date: 2017-08-31 15:48:39
categories: vue-snake-ui
tags: alert
---

# alert
``` javascript
    this.SNAlert('这是一条alert');
```
---
以上为简单调用，完整api如下


``` javascript
this.SNAlert(
    ...
     msg:'我来组成头部',
    ...
)
```

arguments

参数名| 意义 |类型
---|---|---
msg | 展示信息|string
btn | [{str:'确定',callback:()=>{}}] str为按钮对应的文字，callback为按钮点击的回掉函数 |array 


    