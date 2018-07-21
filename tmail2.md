```
1、重点!!!
块级元素 block:
    自己占一行
    h1~h6
    ol ul li
    table
    div
    p
行级元素 inline:
    行级元素与行级元素会在一行显示
    a  span
行块级元素:
    img

块级元素：
    未设置宽高时，
    宽充满它的父元素，高是内容撑开的

盒模型：
    margin【border【padding【内容】】】
    
    border自带8px的外边距margin
    p自带16px的上外边距与下外边距
    ul自带40px的左内边距
    
    样式重置
    *{
        margin:0;
        padding:0;
    }
    
p里面不能嵌套块级元素，一般嵌套行级元素


2、css 选择器
    1. 标签/元素 选择器 div{}
    2. id选择器: 唯一  #id{}
    3. class选择器 可重复 .class{}
    4. 后代选择器 #uli1 li{}
    5. 亲子代选择器  #uli1 > li{}  IE6不支持
    6. 分组选择器 #1,#2,#3{}
    7. 伪类选择器 
        #id a:hover{} 当鼠标移上，发生改变
    8. 多类选择器 div.a{}

3、权重值(优先级)
!important > 内联 > id100 > class10 > tag1(标签) 
!important 使权重值最高
选择器的权重值可以叠加
权重值相同情况下，后定义的会把先定义的覆盖
eg:
.1 .2 .3 .4 .5 .6 .7 .8 .9 .10 .11{}
#1{}
实现#1{}的属性
选择器是从右向左的进行检查
eg：
<div id="aa" class="cc">
    <div class="bb" id="dd"></div>
</div>
#aa .bb{}
.cc #dd{}
权重值一样，实现.cc #dd{}属性

4、
eg:
<style>
        #1{
            margin-bottom: 100px;
        }
        #2{
            margin-top: 100px;
        }
    </style>
<div id="1">1</div>
<div id="2">2</div>
当两个元素为兄弟时，1加下边距与2加上边距，元素合并，取两者之间的最大值

eg：
<style>
    #3{
        width: 100px;
        height: 100px;
        background: #000;
    }
    #4{
        width: 200px;
        height: 200px;
        background: #fff;
        <!--
            float:left;
            overflow:hidden; /*溢出隐藏*/
        -->
    }
</style>
<div id="3">
    <div id="4"></div>
</div>
当两个元素为父子时，给子元素加margin-top时，父元素会一起下落
若想父元素不变，子元素下落，
设置float或者overflow(BFC解决方法)



```
```
outline: none;  /*外框*/
text-indent: 10px;  /*文本缩进*/
placeholder="" 
background:rgba(0,0,0,0.55); 最后一个透明度
```
```
行级元素可以设置padding，margin只能设置左右
```
