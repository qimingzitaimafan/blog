### 1、什么是DOM事件
举例，click就是一个事件，可以在后面绑定函数执行功能。事件可以在文档(Document)结构的任何部分被触发，触发者可以是用户操作，也可以是浏览器本身。事件并不是只是在一处被触发和终止；他们在整个document中流动，拥有它们自己的生命周期。
### 2、DOM事件模型
DOM的结构是一个树形，每当HTML元素产生事件时，该事件就会在树的根节点和元素节点之间传播，所有经过的节点都会收到该事件。 DOM事件模型分为两类：一类是IE所使用的冒泡型事件（Bubbling）；另一类是DOM标准定义的冒泡型与捕获型（Capture）的事件
### 3、捕获与冒泡
举例释义，图中[td]被点击，其上节点[tr]到[window]都可以加上onclick事件去执行函数。函数执行顺序分两种，从[window]到[tr]定义为捕获，从[tr]到[window]定义为冒泡。

具体用哪种顺序，可以通过addEventListener的第三个参数控制

e.addEventLisenter('click',f2,true)   // true按捕获方向执行函数

e.addEventLisenter('click',f2,false)  //  false按冒泡方向执行函数
![opps](https://upload-images.jianshu.io/upload_images/1181204-f84073bad90a1e3c.png?imageMogr2/auto-orient/strip|imageView2/2/format/webp)
