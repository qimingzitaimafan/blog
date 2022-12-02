## 获取元素
使用jQuery的第一步，往往就是将一个选择表达式放进构造函数jQuery（）（简写为$)，然后得到被选中的元素。
选择表达式可以是CSS选择器：
```
$(document) //选择整个文档对象

$('#myId') //选择ID为myId的网页元素

$('div.myClass') // 选择class为myClass的div元素

```
也可以是jQuery特有的表达式：
```
　　$('a:first') //选择网页中第一个a元素

　　$('tr:odd') //选择表格的奇数行

　　$('#myForm :input') // 选择表单中的input元素

　　$('div:visible') //选择可见的div元素

　　$('div:gt(2)') // 选择所有的div元素，除了前三个

　　$('div:animated') // 选择当前处于动画状态的div元素
```

## jQuery的链式操作

## 创建元素

## 移动元素

## 修改元素属性
