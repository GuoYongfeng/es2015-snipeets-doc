## 如何定义一个类 class

- ES2015的类只是一个语法糖，通过class关键字让语法更接近传统的面向对象模式，本质上还是基于原型的。
- 使用单一便捷的声明格式，使得类使用起来更方便，也更具互操作性。
- 类支持基于原型的继承，调用父类的构造函数，生成实例，静态方法和构造函数。

```
// function Animal(name, age){
//   this.name = name
//   this.age = age
// }
//
// Animal.prototype = {
//   getMessage: function(){
//     console.log(this.name + ' is ' + this.age + ' years old')
//   }
// };
//
// var cat = new Animal("cat", "1")
//
// cat.getMessage()

class Animal {
  constructor(name, age){
    this.name = name
    this.age = age
  }
  getMessage(){
    console.log(this.name + ' is ' + this.age + ' years old')
  }
  static showInfo(){
    console.log('show info~!')
  }
}

class Cat extends Animal {
  constructor(name, age, color){
    super(name, age)
    this.color = color
  }
  getName(){
    console.log(this.name + ' , color is ' + this.color)
  }
}

var cat = new Cat("cat", "1", "red")

cat.getMessage()

cat.getName()

// Animal.showInfo()


```
