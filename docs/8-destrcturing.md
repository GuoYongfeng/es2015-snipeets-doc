
## 解构 Destructuring

- 解构允许**数组和对象**使用**模式匹配**进行绑定。
- 解构是以foo['foo']方式查找变量，当没有找到时返回undefined。

```
// 数组 array
// var arr = ["🐶", ["🐱", "🐮"]]

// console.log( dog )
// console.log( cat )
// console.log( bull )


// object 对象
var obj = {
  a: "1",
  b: ["🐶", ["🐱", "🐮"]],
  fn(){ console.log( this.a )}
}

var { a, b } = obj

console.log( b )



```
