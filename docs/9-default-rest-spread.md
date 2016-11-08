
## 默认参数（Default） + 任意参数（Rest） + 扩展运算符（Spread）

> 他们给js函数带来的改变

- 调用具有默认参数的函数，可以很好的保证函数的容错性，并减少代码逻辑
- 任意参数 rest 让我们不再需要arguments，并且更直接地解决了一些常见的问题。
- 扩展运算符 spread，逻辑清晰，代码精简


```


// function Person( name, age ){
//
//   if(typeof name === 'undefined') name = name || "guoyongfeng"
//   if(typeof age === 'undefined') age = age || "18"
//
//   return name + ' ' + age
// }

// default

// var Person = ( name="guoyongfeng", age="18" ) => name + ' ' + age
//
//
// console.log( Person("guoyongfeng") )


// keys 任意参数
// function agrv(obj, ...keys){
//   var res = Object.create(null)
//
//   for (var i = 0; i < keys.length; i++) {
//     res[keys[i]] = obj[keys[i]]
//   }
//
//   return res
// }
//
// var data = { title: "es6", name: "name"}
//
// var msg = agrv(data, "title", "name")
//
// console.log( msg.title )


var arr = [18,232,33,5]

var newArr = [...arr, 100, 10000]

console.log( newArr )

console.log(Math.max(...newArr))

```
