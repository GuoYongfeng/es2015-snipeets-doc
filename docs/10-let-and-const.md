## Let（局部变量） + Const（常量）

- 新增块级作用域，使用let定义。
- const是用于定义常量，单赋值（仅允许被赋值一次）。
- 没有变量提升，静态限制（Static restrictions ）阻止变量在赋值前被使用。

```

console.log( a )


let a = "2"

const b = 2

b = 3

```
