```
//鼠标移入移出
.hover(function(){},function(){});

//前者不冒泡
mouseenter ---- mouseover
mouseleave ---- mouseout
```

target
```
eg:
<ul id="ul">
    <li>001</li>
</ul>

（1）原生js：
点击li时
e.target :事件源  ---><li>001</li>
this :当前事件的引用  ---><ul><li>001</li></ul>
//e.currentTarget === this

点击ul时
e.target :事件源  ---><ul><li>001</li></ul>
this :当前事件的引用  ---><ul><li>001</li></ul>

（2）jQuery
//针对li绑定事件
$('#ul').on('click','li',function(){
    console.log(e.target); //<li>001</li>
    console.log(e.currenttarget); //<li>001</li>
});

<!--if(e.tarfet.tagName === 'LI'){-->
<!--    console.log();-->
<!--}-->
```
