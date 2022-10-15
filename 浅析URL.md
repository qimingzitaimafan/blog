本篇记录一下我接触学习URL的一些重要知识和一些心得体会

URL(Uniform Resource Locator)是统一资源定位器, 由李爵士发明，是万维网的重要组成部分，用来表示网页的地址
## URL的结构
* 协议

HTTP(Hyper Text Transfer Protocol)超文本传输协议，作用是在浏览器与服务器间传送文档；

HTTPS，在HTTP的基础上加强了文件传输的安全性
* 域名 

用于代替复杂的IP地址，从而方便用户访问网站
* 端口 

用于定位设备上的服务
* 路径 

用于请求不同的页面
* 查询参数

用于在相同页面中查询不同的内容
* 锚点

用于查看相同查询结果中的不同内容要素

## DNS
DNS（Domain Name System）域名系统。是一种可以将域名和IP地址相互映射的层次结构的分布式数据库系统

（在命令行中输入nslookup+域名，可以得到域名对应的IP）

## IP
IP（Internet Protocal）互联网协议，作用是定位设备

（在在命令行中输入ping+域名，可以得到域名对应的IP)
## 域名
Domain Name，由一连串字符组成，指向某一个IP地址

域名种类：

* com 一级域名
* baidu.com 二级域名（俗称一级域名）
* www.baidu.com 三级域名（俗称二级域名）
