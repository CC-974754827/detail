```
function People(name,age){
    this.name = name;
    this.age = age;
}
People.prototype.showName = function(){
    console.log(this.name);
};

let p = new People('zs',19);
console.log(p);
p.showName();

//基于原型的继承
//继承
function Coder(name,age,company){
    People.call(this,name,age);
    this.company = company;
}
//继承父类的属性
Coder.prototype = new People();
//继承父类的方法
```

```
//这类方法属于静态方法
Math.random();

```


es6
```
class People{
    constructor(name,age){
        this.name = name;
        this.age = age;
    }
    showName(){
        console.log(this.name);
    }
}

//继承
//继承父类的属性与方法
class Coder extends People{
    constructor(name,age,company){
        super(name,age);
        this.company = company;
    }
}

//静态方法
static foo(){
}
```
