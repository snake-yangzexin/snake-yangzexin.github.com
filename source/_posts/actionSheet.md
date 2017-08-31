---
title: actionSheet
date: 2017-08-31 15:23:35
categories: vue-snake-ui
tags: actionSheet
---




``` javascript
this.SNActionSheet(
    ...
     title:'我来组成头部',
    ...
)
```

arguments

参数名| 意义 |类型
---|---|---
title | 头部提示|string
btnList | [{'key':'a','value':'按钮a'}] key为按钮对应的id，value为按钮上的文字 |array 
key | 按钮id对应的映射 |string
value | 按钮文字对应的映射 |string
success | 点击选项按钮后的回掉函数，会将按钮对应的id传回| function
cancel | 点击返回按钮后的回掉函数 | function


    