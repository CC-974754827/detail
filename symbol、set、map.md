symbol
```
避免属性名重复，不产生冲突
let age = Symbol();
let obj = {
    [age] = 18 ;   //[age]代表变量
};

console.log(obj[age]);  //取值
```

set
```
①
//可去重
let s = new Set([1,2,3]);
//set内的数据不允许重复

//set的索引是自身的值
for(let [item,index] of s.entries()){
    console.log(item,index);
}
    
<!--let result = [];-->
<!--for(let [item,index] of arr.entries()){-->
<!--    if(!result.includes(item)){-->
<!--        result.push(item);-->
<!--    }-->
<!--}-->

②
添加：s.add();
删除：s.delete();
判断是否有这个成员：s.has();
清空：s.clear();
```
map (key唯一)
```
var m = new Map();
m.set('name','zs');
--->'name'=>'zs';

m.get('name');    //获取
```
