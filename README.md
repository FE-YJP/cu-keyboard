### 属性参数
|       属性 |  类型   | 默认值  |             说明             |
| ---------: | :-----: | :-----: | :--------------------------: |
| confirmText| String  | '付款' |           确认按钮的文本           |
|confirmStyle| Object |  `{backgroundColor:'#57BE6D'}`   |       确认按钮的样式       |
|   duration | Number  |   300   | 键盘弹起的动画时间 |
|  `</slot>` | HTML  |      -   |        键盘上部是一个插槽,可以自定义内容        |


### 事件方法
|       属性 |  类型   | 		说明  		|    	返回值    	|
| ---------: | :-----: | :-----: | :--------------------------: |
|   change   | Events |  数字改变时触发   	|   数字键盘的值  	|
|   confirm  | Events | 点击右下角确认按钮触发|   数字键盘的值  	|
|   hide  | Events | 点击非键盘位置时触发  |   	-		 	|

### 使用方法示例
在`template`中使用
```
<cu-keyboard ref="cukeyboard" @change="change" @confirm="confirm" @hide="hide"></cu-keyboard>
```
调用键盘显示的方法  
```
this.$refs.cukeyboard.open();
```
