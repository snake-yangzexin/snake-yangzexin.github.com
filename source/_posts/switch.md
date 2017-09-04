---
title: switch
date: 2017-09-04 16:05:23
categories: vue-snake-ui
tags: switch
---




``` html
<SNSwitch v-model="snswitch"></SNSwitch>

```


``` javascript
  export default {
      data(){
          return{
              snswitch:false
          }
      }
  }
```

v-model需要接受一个boolean类型的变量。true为选中状态，false为未选中状态。


    