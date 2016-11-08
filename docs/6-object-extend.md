##增强的对象字面量

- 扩展后的对象字面量，允许在结构中设置原型，简化了类似 `foo: foo` 这样的赋值、定义方法和父级调用。
- 这使对象字面量更接近**类的声明**，并使得基于对象的设计更加方便。

````
var others = { data: "other data" }

var obj = {
  __proto__: others,
  name: "guoyongfeng",
  getName(){
    console.log(this.name)
  }
}

var a = 1
var b = "2"
var fn = ( m, n ) => console.log( m + n )

var objAnother = { a, b, fn }

console.log( objAnother.fn(1, 4) )

```
