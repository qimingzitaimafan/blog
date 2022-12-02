## 获取元素
使用jQuery的第一步，往往就是将一个选择表达式放进构造函数jQuery（）（简写为$)，然后得到被选中的元素。
选择表达式一般是CSS选择器：
```
$(document) //选择整个文档对象

$('#myId') //选择ID为myId的网页元素

$('div.myClass') // 选择class为myClass的div元素

```
## jQuery的链式操作
jQuery的重要设计思想之一就是最终选中网页元素以后，可以对它进行一系列操作，并且对它进行一系列操作，而且所有操作可以连接在一起，以链条的形式写出来，比如：
```
$('div').find('h3').addClass('red').addClass('blue')
```
分解开来，就是下面这样：
```
$('div') //找到div元素

.find('h3') //选择其中的h3元素

.addClass('red') //给h3元素添加red class

.addClass('blue') //继续给h3元素添加blue class
```
它的原理在于每一步jQuery操作返回的都是一个jQuery对象，所以不同操作可以连在一起
## 创建元素

## 移动元素

## 修改元素属性
