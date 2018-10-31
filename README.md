
**BEST PRACTICES 👉 https://github.com/webpack/webpack/issues/5493#issuecomment-321705298**

# noop-webpack-plugin
[![npm](https://img.shields.io/npm/v/noop-webpack-plugin.svg)](https://www.npmjs.com/package/noop-webpack-plugin)

> Webpack plugin that does nothing

## Installation
```shell
npm i noop-webpack-plugin -D
```

## Usage
```javascript
var webpack = require('webpack')
var noop = require('noop-webpack-plugin')
var isProd = process.env.NODE_ENV === 'production'

module.exports = {
  entry: './src/entry.js',
  output: {
    path: './dist',
    filename: '[name].js'
  },
  plugins: [
    isProd ? new webpack.optimize.UglifyJsPlugin() : noop()
  ]
}
```

## License
MIT
