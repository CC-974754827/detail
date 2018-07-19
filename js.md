```
js操作html、css
    document.write('<h1></h1>') 输出
    alert(''); 弹出框
    var msg = window.prompt("请输入","默认值")；
        输入框
    
    console.log(a);  后台打印日志
    console.log(typeof a); 数据类型
        js弱类型语言(不区分小数、整数...)
        typeof返回值是string字符串
    
    var 变量；赋值（从右向左）(未定义undefined)
        不能以数字开头；
        不建议包含中文； 
        非法的-，可用_，建议驼峰式(首字母小写)，
        eg:productName；
        不能定义var var;
        变量名称区分大小写；
    数据类型：number,string,boolean,underfined,null
    ①var a;
    ②var a = 5;c   /*--number*/
    ③var c = '字符串';
        console.log(typeof(c)); /*--string字符串*/
    ④var d = true;   /*true 1 ; false 0*/
        console.log(typeof(d)); /*--boolean*/
    ⑤var e;
        console.log(typeof(e)); /*undefined*/
    
    str1 = str1 + str2; <=> str1 += str2;
    console.log(a++);   后自增，先运算后加1
    console.log(++a);   先自增，先加1后运算
    
    
    eg: 'a' - 3   输出NaN  (not a number)
    eg：'5' - 3   输出2
    eg: '6' / 3   输出2
    eg: '5' /0    输出infinity  (无限的)
    
    
    5 == 5  -> true
    5 == '5'  -> true   ==只判断值
    5 === '5' ->false   ===表示严格判断(值、类型)
    5 != 5   ->false
    5 !== 5  ->false  
    
    
判断
    ①
    if('ab'){
        console.log(true);
        
    }else{
        console.log(false);
        
    }   -> true   (非空字符串)
    
    if(''){
        console.log(true);
        
    }else{
        console.log(false);
        
    }     -> false  (空字符串)
    if('null/undefined'){
    console.log(true);
        
    }else{
    console.log(false);
        
    }-> false 
    ②三元运算符
    null ? console.log(true):console.log(false);
    ③isNaN()  判断是否为NaN
    ③分支
    switch(a){
        case 1: 
            console.log(1);
            break;
        case a:
        case A:
            console.log(2);
            break;
        default:         /*默认值*/
            console.log(未匹配);
    }
循环
    ①for(var i=1; i<100; i++){
        console.log(i);
    }
    ②while先判断后执行
    var i=0;
    while(i<100){
        console.log(i);
        i++; 
    }
    ③do{}while 先执行后判断
    var i=0;
    do{
        console.log(i);
        i++;
    }while(i<100);
    ④for( in)
    for(var p in a){
            console.log(p);//输出a的属性名
            
            console.log(a[p]);
            //循环遍历a的对象
        }
    
函数function
    function name(){
        
    }   /*函数声明*/
    name();    /*函数调用*/
  
    /*eg:
    function name(x, y){   形参
        console.log(x + y);
    }
    name(3, 4);  实参
    */
    
    /*return问题
    ①function name(x, y){   
       var result= x * y;
       return result;   
       //返回值
       //将局部变量变成全局变量
    }
    console.log(result * 2);
    
    ②return 之后的代码不会执行
    */
    
    function name(){
        
    }  
    name();  
    //函数先调用后声明也可以
    var a = function(){
    
    }   //将函数赋给变量
    //这种函数不可以先调用后声明
    
数组array
    var arr = [];  /*arr.length*/
    console.log(arr[0]);
    
    var arr = new Array();
    arr[0] = 1;
    arr[1] = 2;
        /*当 Array(1)  只一个数字时，表示长度*/
        
    方法
    插入push()  返回新长度
    eg:
        var arr = [1, 2, 3];
        arr.push(4);
        
        var len = arr.push(4);
        console.log(len);
    
对象object
    var a = {属性、方法};
    //属性key唯一
    eg:
        var a = {
          name: '',
          age: '',
          coding: function(){}
        };
        //查看对象内某个元素
        ①console.log(a.name); //对固定值
        ②console.log(a['name']);
        //查找是否有该属性
        ③a.coding();  //调用对象方法
        
        for(var p in a){
            console.log(p);//输出a的属性名
            
            console.log(a[p]);
            //循环遍历对象
        }
    var obj = new Object();
    obj.name = '';
    obj.age = '';
```
