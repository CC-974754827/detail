    
逻辑运算符 & | ！
&&
    当&&前为false时，后面的语句不执行
    var a = 5;
    false && (a = 6);
    console.log(a);
    -->a = 5
||
    当||前为true时，后面的语句不执行
    var a = 5;
    true || (a = 6);
    console.log(a);
    -->a = 5

    
    
    
函数嵌套
    ①function foo1(){
        console.log('foo1');
        function foo2(){
            console.log('foo2');
        }
        foo2();
    }
    foo1();
    
    ②function foo1(){
        console.log('foo1');
        return function foo2(){
            console.log('foo2');
        }
       
    }
    var fn = foo1();
    fn();
    
    ③function foo1(){
        console.log('foo1');
        return function foo2(){
            console.log('foo2');
        }
       
    }
    fn()();
    
window:
    var a = 1;  //变量
    function aa(){   //函数
        
    }
    console.log(window);
    //console.log(window.a); 污染全局变量
    解决：函数直接调用
    (function (){
        var a = 1;
    var b = 2;
    console.log(window);
    })();
