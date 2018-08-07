Ajax 前端向后端发送
```
jquery

$.get('url',{参数},回调函数function(res){
    console.log(res.subjects);
    for(let item of res.subjects){
        let $li = `<li>${movie.title}</li>`;
        $list.append($li);
    }
}，json) 获取

<!--http://bird.ioliu.cn/v1?url=-->
<!--res=>{}箭头函数-->
$.post() 提交
```
```
原生js


```
promise
状态一旦改变，就不会再变
```
对异步操作进行管理
解决callback hill

new Promise((resolve,reject)=>{
    $.get('a.json',res=>(){
        console.log(res);
        resolve(res.a);
    })
}).then(()=>{
        //成功
    },()=>{
        //失败
    });
    
    
promise.all() //全部执行后再执行
promise.race  //有一个完成就全部完成

.then(res=>{
    
}).catch(err=>{
    
});
```
