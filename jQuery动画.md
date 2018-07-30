```
动画
<!--消失、出现-->
<!--改变宽度、高度、透明度-->
.hide(1000); //display: none;
.show(1000); //display: block;

<!--切换-->
.toggle();

渐变
<!--淡入淡出-->
<!--改变透明度-->
.fadeIn(); //display: none;
.fadeOut(); //display: block;

滑动
<!--改变高度-->
.slideDown();
.slideUp();


自定义
.animate({css属性},1000,'linear/swing',function(){
});

$(#id:animate).css(); //动画未执行完时的操作

停止当前正在执行的动画
stop([是否取消队列动画false],[是否立即完成false]);
```
