## 声明对象
#### 声明对象有两种方法：
* `let obj = { 'name': 'Ivor', 'age': 24 }`
* `let obj = new Object({'name': 'Ivor'})`

第一种方法更便捷,第二种方法更规范

其中，'name'是属性名（键key)，'Ivor'是属性值，二者合称键值对


#### 值得注意的是，所有的属性名会自动变成字符串
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
#### 而且可以用变量做属性名
```JS
let p1 = 'name'
let obj = { [p1] : 'frank' } //这样写，属性名为 'name'

```
#### 对象的隐藏属性
JS 中每一个对象都有一个隐藏属性，这个隐藏属性储存着其共有属性组成的对象的地址，这个共有属性组成的对象叫做原型，也就是说，隐藏属性储存着原型的地址

## 对象属性的增删查改
### 删除属性
#### 删除属性有两种方法：
* `delete obj['xxx']`
* `delete obj.xxx`
#### 这里要注意区分“属性值为undefined”和“不含属性名”
“不含属性名”是这这样的：
```JS
'xxx' in obj === false
```
“含有属性名，但是值为undefined”是这样的：
```JS
'xxx' in obj && obj.xxx === undefined
```

### 查看属性
* 查看自身所有属性

  `Object.keys(obj)`
* 查看自身属性和共有属性

  `console.dir(obj)`

  `Object.keys(obj)+Object.keys(obj.__proto__)`

* 判断一个属性是自身的还是共有的

  `obj.hasOwnProperty('toString')`
  
### 修改和增加属性
**修改属性有两种方式，分别是直接赋值和批量赋值，具体如下：**

* 直接赋值
1. `obj['name'] = 'Ivor' `
2. `obj.name = 'Ivor'`
3. `obj['na'+'me'] = 'Ivor'`
4. `let key = 'name'; obj[key] = 'Ivor'`
* 批量赋值

  `Object.assign(obj, {age: 18, gender: 'man'})`
  
**除此之外还可以修改或增加原型上的属性：**
  
1. `obj.__proto__.toString = 'xxx'`
2. `Object.prototype.toString = 'xxx' `

不过一般来说，不要修改原型，会引起很多问题

**修改隐藏属性：**
```JS
let obj = Object.create(common)
obj.name = 'Ivor'
```
以上操作可以形成一个原型链

**（增加属性和修改属性的操作一样，已有属性就修改，没有属性就增加）**
  
  ## 判断属性是否属于对象的方法
判断属性是否属于对象有两种方法，具体如下
1. `'xxx' in obj`
2. `obj.hasOwnProperty('xxx')`

二者的区别在于第一种方法可以判断一个对象的所有属性，而第二种方法只能判断对象的自有属性
