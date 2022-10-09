## 结构
由外到内分别是：margin, border, padding, content

## 分类
* content-box (width里只包含content)
* border-box  (width里包含border, padding和content)
## margin合并问题
#### 阻止兄弟合并的方法
* 使用display: inline-block
#### 组织父子合并的方法
* 加border或者padding
* 加overflow: hidden
* 加display: flex
#### （注意：只有上下margin会合并，左右不会）
