---
title: totat
date: 2017-08-31 15:02:00
categories: vue-snake-ui
tags: toast
---

# toast
``` javascript
    this.SNToast('这是一条toast');
```

# success-toast
``` javascript
this.SNToast.success();
this.SNToast.success('成功');
```

# error-toast
``` javascript
this.SNToast.error();
this.SNToast.error('失败');
```

# loading-toast
``` javascript
this.SNToast.loading.show();
```
##### loading图标最长10s消失，如果想消失请调用;
``` javascript
this.SNToast.loading.hide();
```

---
以上为简单调用，完整api如下


``` javascript
this.SNToast({
    ...
    msg:'已完成'，
    ...
});
```

arguments

参数名| 意义 |类型
---|---|---
msg | 普通消息提示  |string
successmsg | 成功消息提示  |string
errormsg | 失败消息提示  |string
loadingmsg | loading消息提示  |string
loadingmsg | loading消息提示  |string
type | totas类型 msg、success、error、loading  |string
remain | 消息存在时间,默认1s,loading默认10s  |string


    