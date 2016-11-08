## 模块（Modules）

- ES6的Class只是面向对象编程的语法糖，升级了ES5的构造函数的原型链继承的写法，并没有解决模块化问题。Module功能就是为了解决这个问题而提出的。
- 为了方便定义模块，从语言层面对模块进行了支持。编写方式借鉴了流行的JavaScript模块加载器（AMD, CommonJS）。
- 使用webpack将模块打包

```
$ npm install webpack babel-loader --save-dev
$ touch webpack.config.js
```

配置webpack.config.js文件

```


var path = require('path')
var webpack = require('webpack')

var config = {
  entry: path.resolve(__dirname, "./src/index.js"),
  output: {
    path: path.resolve(__dirname, "./dist"),
    filename: "index.js"
  },
  module: {
    loaders: [
      {
        test: /\.js$/,
        loader: 'babel',
        exclude: /node_modules/
      }
    ]
  }
}

module.exports = config

```

配置packages.json中的scripts字段

```
"scripts": {
  "dev": "babel src -d dist -w",
  "build": "webpack -w --progress --colors"
}
```

新建一个模块

```
$ touch ./src/module.js
```

编辑module.js

```
export var a = 1
export let b = 2
export function fn(){

}
```

编辑index.js

```
import { a, b, fn } from './module'

console.log( a )
console.log( b )
console.log( fn )

```
