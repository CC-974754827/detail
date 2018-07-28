提供DOM操作
```
<script src="jquery-1.12.4.js"> </script>
<script>
    $('#id').css('background','red');
    
    var $div = $('#div');  //命名以$开头
    
<!--jq对象 -> 原生对象-->
    $obj.get(0)    $obj.get[0]
<!--原生对象 -> jq对象-->
    $(oDiv1).css('background','red');
</script>
```

文档就绪函数
```
//文档就绪函数
    $(document).ready(function(){
        console.log($('#div1'));  
    });
    
    $(function(){
        console.log($('#div1'));
    });
//等到DOM加载完成后执行
    
//window.onload = function(){};
//等到资源加载完成并且DOM加载完成后执行
```

选择器
```
$(function(){
   $('#div1'); 
   
   $('.div1');   //不是集合
   
   $(':eq(0)'); //索引
   
   $(':even'); //偶数(从0开始)
   $(':odd');//奇数(从0开始)
   
   $(':first'); //第一个
   $(':last'); //最后一个
   
   $(':lt(1)'); //小于
   $(':gt(1)'); //大于
   
   $(':header'); //头部
   $(':root');  //根html
   
   $(':not(selector选择器)'); //除了
   
   $(':target');  //目标，锚点
});
```
内容
```
    $(':contains()'); //包含

    $(':empty');  //空
    $(':parent');  //非空
```

```
//原生属性
    设置属性
    object.id = '';
    object.setAttribute('');
    
    获取属性
    object.getAttribute('');
//jq
    $(function(){
    //两个参数赋值
       $('#id').prop('xx','yy');
    //一个参数取值
       $('#id').prop('xx');
    });

    //只一次
    $(function(){
    //两个参数赋值
       $('#id').attr('xx','yy');
    //一个参数取值
       $('#id').attr('xx');
    });
    
```
css
```
①$().addclass();

②   
    $().css('background','red');
    
    $().css({
        background: 'red',
        fontSize:10;
        //'font-size':10;
    });
    
    //经过计算而得的属性
    $().css('width',function(){
        return 200;
    });
    
    //获取
    $().css('color');

③$().toggleclass(); //切换

④!!!链式操作
$().css('background','red').attr('aa','bb');
完成一部分就返回jQuery对象

```
尺寸
```
width:内容
innerwidth:内容+padding
outerwidth:内容+padding+border
//outerwidth(true):内容+padding+border+margin
```
位置
```
.position:相对于父元素
.offset:相对于document
```
插入
```
$('#id').append('');
$('').appendTo('#id');
```
拷贝
```
.clone();
```
包裹
```
.wrap();
.wrapAll();
.wrapInner();
```
内部插入
```
$().html('<h1>hhh</h1>'); -->hhh //解析
$().text(<h1>hhh</h1>); --><h1>hhh</h1> //不解析
```

```
$('li').eq(2).css(); //先找出所有li
$('li:eq(2)').css(); //找出第2个li
```

```
绑定事件
$('#id').on('事件',function(){});

提取
$('input[name=""]');

循环遍历
.each(function(index,elem){});
<!--elem原生对象-->
<!--index下标-->
```

```
console.log(this.value);
console.log($(this).val());
```
