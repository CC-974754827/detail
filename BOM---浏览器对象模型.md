```
1.
document.write('');
=== window.document.write('');

2.
窗体滚动轴
scrollBy(x,y);滚动
scrollTo(x,y);滚动到
窗体控制
移动
    moveBy();
    moveTo();移动到
大小
    resizeBy();
    resizeTo();
    
3.
alert();  //按钮：确定
=== window.alert();
confirm(); //按钮：确定、取消
prompt();


4.!!!定时器返回值类型:number
(1)
定时器serInterval
间隔指定的毫秒数
    var n= 1;
    setInterval(function(){
        console.log(n++);
    },1000);   //毫秒单位的时间
清除定时器clearInterval
    var n= 1;
    var timer = setInterval(function(){
        if(n >= 5){
            clearInterval(timer);
        }
        console.log(n++);
    },1000);   //毫秒单位的时间
    
(2)
定时器setTimeout
延迟指定的毫秒数，只执行一次
    var n = 1;
    setTimeout(function(){
        console.log(n++);
    },1000)
清除定时器clearTimeout

5.history
    <button id="back">绑定事件</button>
    <script>
        //事件
        var oBtn = document.getElementById('back')  //通过id获取元素
        oBtn.onclick = function(){     //绑定点击事件   //事件处理函数
            history.back();//前一个
            //history.forward();下一个
            //history.go(-1);上一个   //history.go(1);下一个
        }
    </script>
    
6.location
    location.href; //返回完整URL地址
    location.host; // 返回主机名和端口号
    location.port; //返回端口号
    location.protocal; //返回协议
    
7.navigator
navigator.userAgent;//当前浏览器信息
     if(navigator.userAgent.indexOf('iphone') != -1){
            location.href = '';
        }else{
            location.href = '';
        }
        
```
