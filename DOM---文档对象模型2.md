```
DOM 0 非标准浏览器
DOM 1 标准浏览器
一个网页即一个文档 document

1.
(1)通过id获取元素
var p = document.getElementById('id')
eg:当id重复时，js取第一个，css全部获取

(2)通过标签获取元素
返回的是HTML collection集合
①获得全部标签(集合)
    var aLi = document.getElementsByTagName('Tag');
②获得某个对象的标签(集合)
    var aLi = p.getElementsByTagName('Tag');
③获得某个具体对象的标签
    var aLi = p.getElementsByTagName('Tag')[0];

(3)通过class获取元素
var a = document.getElementsByClassName('class');
    //兼容性问题，只在标准浏览器可用
    
    封装方法(能力检测)
function getByClass(clsName){
    if(document.getElementsByClassName){
        return document.getElementsByClassName(clsName);
    }else{
        var allElems = docunment.getElementsByTagName('*');
        var result = [];
        for(var i = 0;i<allElems.length;i++){
//  eg:clsName xx   if(allElems[i].className.indexOf(clsName) != -1)
//  匹配不完整，用正则表达式
            if(allElems[i].className == clsName){
                result.push(allElems[i]);
            }
        }return result;
    }
}

//两种返回值
//htmlconnection
//NodeList

(4)获得name
eg:
    <form action="">
        <label for="username">名</label>
        <input type="text" id="username" name="uname"/>
    </form>
var uname = document.getElementsByName('uname');

(5)querySelector查询选择器(支持css/css3选择器)
    //一个对象
    document.querySelector('#id'); 
    //多个对象
    document.querySelectorAll('#id 。class'); 
    
(5)直接获取child
console.log(object.children);
``` 
```
①创建
var oMenu = docunment.querySelector('#menu');
var oLi = document.createElement('li');//创建
oLi.innerHTML = Math.random();
oMenu.appendChild(oLi); //增加
②任意位置插入
oMenu.insertBefore(onew新元素,oold旧元素);
③替换
oMenu.replaceChild(onew新元素,oold旧元素);
④删除
oMenu.removeChild(元素)
```
```
①子节点
var child = object.childNodes; 
eg：text、结点、text

②结点类型
child[i].nodeType;
<!--文本结点text类型：3-->
<!--元素结点类型：1-->

③第一个元素结点
object.firstElementChild; //早期IE不支持

④下一个兄弟结点
object.nextSibling;

⑤下一个兄弟元素结点
object.nextElementSibling; //早期IE不支持


封装方法
//找到元素结点的兄弟
function next(elem){
    do{
        elem = elem.nextSibling;
    }while(elem && elem.nodeType != 1);
    //只有一个元素并且元素的类型不等于文本类型
    return elem;
}

//找到第一个元素结点孩子
<!--传入父结点作为elem-->
function first(elem){
    elem = elem.firstChild;
    if(elem === null){
        return null;
    }
    return elem.nodeType == 1 ? elem:next(elem);
}

```
