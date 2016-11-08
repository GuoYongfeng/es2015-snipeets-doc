## 箭头函数 Arrow Function

- 箭头函数是使用=>符号对函数定义的简写，它支持两种写法：表达式（Expression bodies）和函数体（Statement bodies）。
- 值得注意的是，与一般的函数不同，函数体内的this对象，指向的是绑定定义时所在的对象，而不是使用时所在的对象。即：**共享父作用域的关键字this。**

```
var fn  = p => p

var fn1 = () => "无参数输入的箭头函数"

var fn3 = ( a, b ) => a + b

console.log( fn3( 1, 4 ));

var fn4 = ( a, b) => {
  var m = a + 2

  // 显式return
  return m * b
}

// 20
alert( fn4(2, 5) );



var obj = {
  name: "yongfeng",
  courses: ["react", "nodejs", "mongodb"],
  getMessage: function(){
    this.courses.forEach((item) => {
      console.log(this.name + " tech us" + item);
    })
  }
}

obj.getMessage();

```
