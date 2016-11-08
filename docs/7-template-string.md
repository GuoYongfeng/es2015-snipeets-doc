## 模板字符串 tempalte strings

- 模板字符串提供了构建字符串的语法糖，类似于像Perl，Python等语言中的字符串插值。
- 也可以构建一个自定义标签，避免注入攻击或用字符串内容构建更高层次的数据结构。

```
var name = "cat"
var age = "1"

var str = name + " is " + age + " years old."

// 痛点 1
var temStr = `${name} is ${age} years old.`

// console.log( str )
console.log( temStr )

var htmlStr = '<div><div>' + name + '</div>' +
  '<h1>' + age + '</h1></div>'

// 痛点 2
var htmlTemStr = `<div>
                    <div>${name}</div>
                    <h1>${age}</h1>
                  </div>`


console.log(htmlStr)
console.log(htmlTemStr)

```
