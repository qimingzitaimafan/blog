## 声明对象
声明对象有两种方法：
* `let obj = { 'name': 'Ivor', 'age': 24 }`
* `let obj = new Object({'name': 'Ivor'})`

第一种方法更便捷,第二种方法更规范

其中，'name'是属性名（键key)，'Ivor'是属性值，二者合称键值对


值得注意的是，所有的属性名会自动变成字符串
```JS
let obj = {
  1: 'a',
  3.2: 'b',
  1e2: true,
  1e-2: true,
  .234: true,
  0xFF: true
};
Object.keys(obj)
=> ["1", "100", "255", "3.2", "0.01", "0.234"]

```
而且可以用变量做属性名
```JS
let p1 = 'name'
let obj = { [p1] : 'frank' } //这样写，属性名为 'name'

```
## 对象属性的增删查改
**删除属性**
删除属性有两种方法：
* 

## 判断属性是否属于对象的方法
