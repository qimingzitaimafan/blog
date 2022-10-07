## a标签的用法
### href取值

1.网址

* https://google.com
* http://google.com
//google.com
2. 路径
* /a/b/c或者a/b/c
* index.html
3. 伪协议
* javascript伪协议（可以用于创建一个点了没反应的按键，代码如下）
```javascript
<a href="javascript:;">点这里</a>
```
* mailto:邮箱
* tel: 电话
4. id
* href="#xxx"（可以跳转到一个名称是xxx的页面）
### target取值
* _blank (新开一个页面显示网页）
* _self (在当前页面显示网页）
* _top （在顶层页面打开网页）
* _parent (在父级页面打开网页）

## img标签的用法
### 属性
* src (source)
* alt （图片加载失败时显示alt里的内容）
* height（长和宽是同步变化的，如果两个一起调整图片可能会变形）
* width
### 事件
* onload
* onerror
记录图片是否加载成功，代码如下
```javascript
<script>
   xxx.onload = function() {
     console.log("图片加载成功");
   };
   xxx.onerror = function() {
     console.log("图片加载失败");
   };
</script>
```
## table标签的用法
### 语法
* thead 表头
* tbody 表格主体
* tfoot 表尾
* tr 创建表格里的一行
* th (table head)表头
* td (table data)表格数据
### 样式
* table-layout (fixed代表列宽固定；auto代表列宽随字数增加而增加)
* border-spacing （边框间距）
* border-collapse (合并边框）
