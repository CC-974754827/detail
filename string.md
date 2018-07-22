```
1.charAt() 返回指定位置的字符
    var str = 'abc';
//        for(var i = 0;i < str.length;i++){
//            console.log(str[i]);
////        console.log(str.charAt(i));
//        }
        console.log(str[3]);     //---> undefined
        console.log(str.charAt(3));  //---> 空
        
2.indexOf()
返回某个指定的字符串值在字符串中首次出现的位置
如果要检索的字符串值没有出现，则该方法返回 -1。
    var str = 'abc';
    console.log(str.indexOf('a'));
        
3.slice()
可提取字符串的某个部分，并以新的字符串返回被提取的部分。
    var str="Hello happy world!"
    document.write(str.slice(6))

---->happy world!

4.split() 方法用于把一个字符串分割成字符串数组。
    "2:3:4:5".split(":")	
    //将返回["2", "3", "4", "5"]
    "|a|b|c".split("|")	
    //将返回["", "a", "b", "c"]

5.substr() 
方法可在字符串中抽取从 start 下标开始的指定数目的字符。
    var str="Hello world!"
    document.write(str.substr(3))

--->lo world!


```
