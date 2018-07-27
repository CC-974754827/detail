# html
一种标记语言(超文本标记语言)
```
<!doctype html>
<!--html:根(root)标签-->
<!--lang="en" 用处不大，可忽略-->
<html lang="en">
<head>
    <meta charset="UTF-8"><!--字符集-->
    <title>标题</title>

    <!--SEO 搜索引擎优化-->
    <meta name="keywords" content="内容"/>
    <meta name="description" content="内容"/>
</head>
<body>
    <!--标题h1~h6-->
    <h1></h1>

    <!--有序列表-->
    <ol>
        <li></li>
    </ol>
    <!--无序列表-->
    <ul>
        <li></li>
    </ul>

    <!--链接-->
    <a href="" target="_blank"></a>  <!--target="_blank" 在新窗口打开网页-->

    <!--图片-->
    <img src="" alt="" title=""/>
    <!--alt 当图片加载失败时，显示其中内容
        title 当鼠标放在图片上时，显示其中内容 -->
   
    <form action="提交的地址">
        <label for="1">名字: </label>
        (获得焦点)(失去焦点)
        <input type="text" id="1"> 文本
        属性：outline:none;外边框样式
        <input type="password">  密码
        <input type="radio" name="1"> 单选 
        <input type="checkbox" name="2"> 多选
        <select name="" id=""> 下拉列表
            <option value=""></option>
        </select>
        <textarea name="" id="" cols="30" rows="10"></textarea> 备注
            属性：resize: none; 不能拉动
        <input type="reset">重置
        <input type="submit" value="名字"> 提交
    </form>
    
    <p>段落</p>
    
    <br>换行

    <!--表格-->
    <table border="1">  <!--border 边框-->
        <!--行-->
        <tr>
            <!--列-->
            <td colspan="2">  <!--跨列-->
                11
            </td>
            <td rowspan="2"> <!--跨行-->
                22
            </td>
        </tr>
        <tr>
            <td>
                33
            </td>

        </tr>
    </table>
 

    <!--框架-->
    <!--布局 div+css-->
    <div>div1</div>
    <div>div2</div>

    <span>span1</span>
    <span>span2</span>
    <!--
    重点!!!
        块级元素 block:可以设计宽高
            自己占一行
            h1~h6
            ol ul li
            table
            div
            p
        行级元素 inline:不能设计宽高
            行级元素与行级元素会在一行显示
            a  span
        行块级元素:
            img input
    -->

</body>
</html>
```
  
