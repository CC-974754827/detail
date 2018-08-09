```
<script src="vue.js"></script>
<script src="https://cdn.jsdeliver.net/npm/vue"></script>
```
MVC MVVM
```
视图view、控制器controller、模型model
V-C-M-C-V

vue属于MVVM型,数据驱动
```
CDN
```
内容分发网络
寻找距离最近的结点进行加载
```
语法
```
<script src="vue.js"></script>
<script>
    let vm = new Vue({
        el:'#app',
        data:{
            msg:'Hello World'
        }
    });
</script>
①
    v-if      //改变DOM结构，DOM结构消失,非频繁时用
    v-else
    v-else-if
    v-show    //切换display,频繁切换时用

②
    v-for
    循环对象、数组、数组里的对象
    
③
    v-on
    绑定事件
    
④
    v-model
    用于表单
    
```





















