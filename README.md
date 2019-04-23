# scrollTopFixed

> js

## 滚动吸顶，适用于移动端和pc端
> 获取需要固定的元素（简称nav）距离顶部的位置，监听屏幕滚动事件，滚动高度 大于 nav距顶部高度 就为nav 添加固定属性fixed，纯js+css实现

```bash
 install dependencies
var tit = document.getElementById("nav");
    //获取距离页面顶端的距离
    var titleTop = tit.offsetTop;
    //滚动事件
    document.onscroll = function() {
        //获取当前滚动的距离
        var btop = document.body.scrollTop || document.documentElement.scrollTop;
        //如果滚动距离大于导航条据顶部的距离
        if(btop > titleTop) {
            //为导航条设置fix类名
            tit.className = "clearfix fix";
        } else {
            //移除fixed
            tit.className = "clearfix";
        }
    }
```

> 实例可见文件