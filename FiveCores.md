## 入口
```javascript
module.exports = {
  entry: ''
}
```
告诉webpack我们的应用从哪个js开始

## 输出
```javascript
module.exports = {
  output: {
    path: ''
    filename: ''
  }
}
```
告诉webpack最终你打包出来的名字是什么，路径是什么

## loader
```javascript
module.exports = {
  module: {
    rules: [
      { test: /\.txt$/, use: 'raw-loader' }
    ]
  }
}
```
e.g. 处理一些静态的资源文件；比如说我们需要webpack去拥有对于一些高阶语法的支持、对图片字体等资源文件的支持等等。
这些loader就提供了webpack这种扩展能力和处理资源的能力


## 插件
```javascript
module.exports = {
  plugins: [
    new HtmlWebpackPlugin({template: './src/index.html'})
  ]
}
```
支持loader无法实现的一些功能，webpack官方提供了很多优秀的插件，从打包优化到压缩等等。
插件赋予了webpack无限扩展的一种能力。

## 模式/兼容性
* development
* production
