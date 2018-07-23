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
①获得全部标签
    var aLi = document.getElementsByTagName('Tag');
②获得某个对象的标签
    var aLi = p.getElementsByTagName('Tag');

```
