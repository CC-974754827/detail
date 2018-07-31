原生js
```
//存储大小4K，不超过20条
//随着请求，从客户端传向服务端
var now = new Date();
now.setDate(now.getDate()+30);
//toUTCStrings 将时间转成字符串
？？？
document.cookie = 'name;expires='+now.toUTCString;
//默认session 会话
```
jQuery
```
expires:-1; //删除
```
