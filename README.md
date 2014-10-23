## Usage
Swipe 简单的模式。这里有一个例子:

``` html
<div id='slider' class='swipe'>
  <div class='swipe-wrap'>
    <div></div>
    <div></div>
    <div></div>
  </div>
</div>
```

以上所需的初始结构,一系列元素包装在两个容器中。项目中任何你想要的内容。包含div将需要传递功能一样:

``` js
window.mySwipe = Swipe(document.getElementById('slider'));
```

样式

``` css
.swipe {
  overflow: hidden;
  visibility: hidden;
  position: relative;
}
.swipe-wrap {
  overflow: hidden;
  position: relative;
}
.swipe-wrap > div {
  float:left;
  width:100%;
  position: relative;
}
```

## 参数



- **startSlide** Integer *(default:0)* - 开始滚动的位置

-	**speed** Integer *(default:300)* - 动画滚动的间隔（秒数）

- **auto** Integer - 开始自动幻灯片（以毫秒为单位幻灯片之间的时间）

- **continuous** Boolean *(default:true)* - 创建一个无限的循环（当滑动到所有动画结束时是否循环滑动）

- **disableScroll** Boolean *(default:false)* - 当滚动滚动条时是否停止幻灯片滚动

- **stopPropagation** Boolean *(default:false)* - 是否停止事件冒泡
 
-	**callback** 幻灯片运行中的回调函数

- **transitionEnd** 动画运行结束的回调函数

### Example

``` js

window.mySwipe = new Swipe(document.getElementById('slider'), {
  startSlide: 2,
  speed: 400,
  auto: 3000,
  continuous: true,
  disableScroll: false,
  stopPropagation: false,
  callback: function(index, elem) {},
  transitionEnd: function(index, elem) {}
});

```

## Swipe API

Swipe exposes a few functions that can be useful for script control of your slider.

`prev()` 上一页

`next()` 下一页

`getPos()` 返回当前幻灯片索引位置

`getNumSlides()`获取当前索引位置

`slide(index, duration)` 获取所有滑块总数



## Who's using Swipe
<img src='http://swipejs.com/assets/swipe-cnn.png' width='170'>
<img src='http://swipejs.com/assets/swipe-airbnb.png' width='170'>
<img src='http://swipejs.com/assets/swipe-nhl.png' width='170'>
<img src='http://swipejs.com/assets/swipe-htc.png' width='170'>
<img src='http://swipejs.com/assets/swipe-thinkgeek.png' width='170'>
<img src='http://swipejs.com/assets/swipe-snapguide.png' width='170'>



