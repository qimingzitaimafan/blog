## 浏览器渲染原理
1. 根据HTML构建HTML树
2. 根据CSS构建CSS树
3. 将两棵树合并成一颗渲染树(render tree)
4. Layout布局(文档流、盒模型、计算大小和位置)
5. Paint绘制(画出边框颜色、文字颜色、阴影等)
6. Compose合成(根据层叠关系展示画面)
## CSS动画
#### 定义
动画是由许多静止的画面(帧)，以一定的速度连续播放时，肉眼因视觉残像产生错觉，而误以为是活动的画面
#### CSS动画的做法
* transition
transition: 属性名 时间 过渡方式 延迟
常用过渡方式：linear/ease/ease-in/ease-out
```CSS
transition: transform .5s ease-out 1s
```
* animation
1. 添加关键帧
```CSS
@keyframes xxx {
  0% {
     transform: translate(0);
  }
  50% {
    transform: translateX(100px);
  }
  100% {
    transform: translateX(100px) translateY(100px)
  }
}
```
2. 添加animation:
（属性名 时长 过渡方式 延迟 次数 方向 填充模式）
```CSS
animation: xxx .5s alternate 1s infinite;
```

#### CSS动画优化方法
* 将left改成transform（transform可以跳过布局和绘制这两步）
* 使用will-change或translate
* JS用requestAnimationFrame代替setTimeout或setInerval