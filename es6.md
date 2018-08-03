```
兼容性问题
ES6标准入门
```
var问题
```
①
var a = 1;  //局部变量
a = 1;      //全局变量

②
console.log(a);  //变量提升
var a = 1;           --->undefined
===
var a;
console.log(a);
a = 1;

③
console.log(a);      --->error

④没有块级作用域
for(var i = 0;i < 5;i++){
    console.log(i);  --->0 1 2 3 4
}
console.log(i);    --->5

⑤
if(false){
    var a = 5;
}
console.log(a);    --->undefined
```
es6使用let定义变量
```
let定义变量，解决var的问题
①不存在变量提升；
②不可重复声明；
③块级作用域；
④暂时性死区
eg:
    function foo(){
        console.log(a);
        let a = 1;
    }
    foo();      --->error
⑤闭包  //内存泄漏
var aLi = document.querySelectorAll('#nav li');
for(var i = 0;i <aLi.length;i++){
    (function(idx){
        aLi[i].onclick = function(){
            console.log(idx);  
        };
    })(i);   //函数立即调用
}
外部函数引用内部函数变量

function fn1(){
    return function fn2(){
        var a = 5;
        renturn a;
    }
}
console.log(fn1()());
⑥ let  //自动生成闭包
var aLi = document.querySelectorAll('#nav li');
for(let i = 0;i <aLi.length;i++){
        aLi[i].onclick = function(){
            console.log(i);  
        };
}
```
const
只读变量，内存地址改变
```
①
const a = 5;
a = 6;          --->5

② 
const obj = {
    name: 'zs',
    age: 18
}
//Object.freeze(obj);  冻结
obj.age = 30;       --->30
console.log(obj)

const obj = {
    name: 'zs',
    age: 18
}
obj = {
    age:20
}               --->18
//等同于开辟另一个内存空间

```
```
基本数据类型(存于栈)  eg： var a =5 ; var obj;  
引用数据类型(存于堆)  eg:数组 对象
```
```
//污染全局变量
var aa = 5;
console.log(window.aa);      --->5

let aa = 5;
console.log(window.aa);      --->undefined
```
eg:
```
console.log('1==' + a);
var a =1;
function a(){
    console('2==' + a);
}
a();
console.log('3==' + a);

--->
1== function a(){
    console('2==' + a);
}
2== error
    a(); 不是一个函数,取的是var a = 5;

```
方法提升
方法比变量级别更高
```
foo();
function foo(){
    console.log(123);  --->123
}

foo();           //不可以 等同于undefined();
var foo = function(){
    console.log(123);
}
```
