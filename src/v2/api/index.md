---
type: api
---

## 快速开始


### 安装
 ```shell
 npm install vue-snake-ui -S
 ```
### 快速开始
``` javascript
import Vue from 'vue'
import Snake from 'vue-snake-ui'

Vue.use(Snake)

```

## Basic

### img
- **类型**：`component`
- **用法**：

``` html
<SNImg src="https://cn.vuejs.org/images/logo.png" class="img"></SNImg>

```
- **arguments**：

参数名| 意义 |类型
---|---|---
src | 图片的src地址 |String
-**说明**-：
同一父组件下的 SNImg 点击可以查看详情，左右滑动可以查看兄弟图片组件详情

### button
- **类型**：`component`
- **用法**：

``` html
<SNButton type="success" size="large" text="成功"></SNButton>

```
- **arguments**：

参数名| 意义 |类型|可选值
---|---|---|---
type | 按钮的类型 |String|'success'、'error'、'warn'、'default'
text | 按钮的文字 |String|''
size | 按钮的大小 |String|'large'、'middle'、'mini'


## Form

### buttonTab
- **类型**：`component`
- **用法**：

``` html
<SNButtonTab v-model="btnTab">
    <SNButtonTabItem>文章</SNButtonTabItem>
    <SNButtonTabItem>商品</SNButtonTabItem>
    <SNButtonTabItem>照片</SNButtonTabItem>
</SNButtonTab>

```

``` javascript
  export default {
      data(){
          return{
              btnTab:0
          }
      }
  }
```

-**说明**-：
v-model需要接受一个Number类型的变量。为buttonTab选中的index。

### switch
- **类型**：`component`
- **用法**：

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
- **arguments**：

参数名| 意义 |类型|可选值
---|---|---|---
size | switch大小 |String|'mini'、'large'、''
-**说明**-：
v-model需要接受一个boolean类型的变量。true为选中状态，false为未选中状态。




### radio
- **类型**：`component`
- **用法**：

``` html
<SNRadio :list="checkBoxList" v-model="radioResult" str="name" keys="id"></SNRadio>

```

``` javascript
  export default {
      data(){
          return{
              checkBoxList: [
                 {name: "示例1", id: "1", checked: false, disabled: false},
                 {name: "示例2", id: "2", checked: true, disabled: false},
                 {name: "示例3", id: "3", checked: false, disabled: false}
              ]
          }
      }
  }
```
- **arguments**：

参数名| 意义 |类型|默认值
---|---|---|---
list | 列表数据 |Array|[]
str |  列表数据中文字映射  |String| 'name'
keys | 列表数据中逻辑值映射 |String| 'id'
-**说明**-：
v-model为选中项的逻辑值，默认为id，如果有需要更改请更改组件调用时的参数 'keys'。


### checkBox
- **类型**：`component`
- **用法**：

``` html
<SNCheckBox :list="checkBoxList" v-model="result" str="name" keys="id"></SNCheckBox>

```
``` javascript
  export default {
      data(){
          return{
              checkBoxList: [
                 {name: "示例1", id: "1", checked: false, disabled: false},
                 {name: "示例2", id: "2", checked: true, disabled: false},
                 {name: "示例3", id: "3", checked: false, disabled: false}
              ]
          }
      }
  }
```
- **arguments**：

参数名| 意义 |类型|默认值
---|---|---|---
list | 列表数据 |Array|[]
str |  列表数据中文字映射  |String| 'name'
keys | 列表数据中逻辑值映射 |String| 'id'

-**说明**-：
v-model为选中项的逻辑值，默认为id，如果有需要更改请更改组件调用时的参数 'keys'。


### datePicker
- **类型**：`component`
- **用法**：
``` html
<SNDatePicker placeholder="请选择日期" format="yyyy-MM-dd" v-model="datePickerStr"></SNDatePicker>

```

``` javascript
  export default {
      data(){
          return{
              datePickerStr:''
          }
      }
  }
```
- **arguments**：

参数名| 意义 |类型|默认值
---|---|---|---
placeholder | 组件默认展示文字 |String|'请选择日期'
format |  时间格式  |String| 'yyyy-MM-dd'

-**说明**-：
v-model目前是单向数据流，选择时间完毕之后会按照 format 的格式传出字符串。



## Notice


### toast
- **类型**：`Function`
- **用法**：
    - **基础**：
        ``` javascript
            this.SNToast('这是一条toast');
        ```
    - **success**：
        ``` javascript
        this.SNToast.success();
        this.SNToast.success('成功');
        ```
    - **error**：
        ``` javascript
        this.SNToast.error();
        this.SNToast.error('失败');
        ```
    - **loading-toast**：
        ``` javascript
        this.SNToast.loading.show();
        ```
        loading图标最长10s消失，如果想消失请调用
        ``` javascript
        this.SNToast.loading.hide();
        ```
    - **other**：
        ``` javascript
        this.SNToast({
            ...
            msg:'已完成'，
            ...
        });
        ```

- **arguments**：

参数名| 意义 |类型
---|---|---
msg | 普通消息提示  |string
successmsg | 成功消息提示  |string
errormsg | 失败消息提示  |string
loadingmsg | loading消息提示  |string
loadingmsg | loading消息提示  |string
type | totas类型 msg、success、error、loading  |string
remain | 消息存在时间,默认1s,loading默认10s  |string

### alert
- **类型**：`Function`
- **用法**：
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
- **arguments**：

参数名| 意义 |类型
---|---|---
msg | 展示信息|string
btn | [{str:'确定',callback:()=>{}}] str为按钮对应的文字，callback为按钮点击的回掉函数 |array 

### actionSheet
- **类型**：`Function`
- **用法**：
``` javascript
    this.SNActionSheet({
        title: '我来组成头部',
        btnList: arr,
        success: (num) => {
            this.SNToast('我点击按钮' + num);
        },
        cancel: () => {
            this.SNToast('我点击返回');
        },
        key: 'key',
        value: 'value'
    });
```
- **arguments**：

参数名| 意义 |类型|默认值
---|---|---|---
title | 头部描述文字 |String| ''
btnList |  按钮数组  |Array| []
key |  按钮数组逻辑值  |String| 'key'
value |  按钮数组文字展示  |String| 'value'
success |  点击按钮的回调  |Function| es6
cancel |  按钮数组文字展示  |Function| es6


## Qrcode

### Qrcode
- **类型**：`component`
- **用法**：

``` html
<SNQrcode v-model="qrcode"  :size="size" :colorDark="colorDark" :colorLight="colorLight"></SNQrcode>
```
- **arguments**：

参数名| 意义 |类型|默认值
---|---|---|---
size | 二维码图片的大小 |Number|180
colorDark | 二维码图片颜色|String|'#000000'
colorLight | 二维码图片背景色 |String|'#ffffff'

-**说明**-：
v-model为二维码的值