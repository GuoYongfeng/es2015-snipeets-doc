# 轻松驾驭ES6


## 介绍

- ES6/7没有你想象的那么难，但不学习，也没有那么简单
- 学习前起码得把ES3/5的基础打牢
- 拥抱babel：Babel 是一个 JavaScript 编译器。
- 掌握常用的20%的ES6语法，其他的，看工作需要和自己兴趣了
- destroy one by one 每个知识点单点突破

## 搭建学习环境

- 基本环境
	- 全局nodejs & npm
	- git bash or terminal
	- 编辑器atom or others
	- chrome
- babel
	- babel-core@5  用于浏览器端直接引入
	- babel-cli 命令行工具
	- babel-preset-es2015 & babel-preset-es2015-loose 分别是normal和loose两种模式解析es5语法
	- babel-preset-stage-0 或者stage-1等
	- babel-preset-es2016
	- babel-register 用于在es6的文件里面直接引入，这样可以运行时解析
	- babel-polyfill 用于将一些es6的API做兼容处理
- npm scripts

```
mkdir es6-course
cd es6-course/
git init
touch .gitignore README.md
npm init -y
touch index.html
mkdir src dist
cd src/
touch index.js
cd ..
npm install babel-cli babel-preset-es2015 --save-dev
touch .babelrc
npm run dev
```
