# loaders-by-extension

[![NPM version][npm-image]][npm-url]

> A mirror library from webpack/react-starter


## Install

```
$ npm install loaders-by-extension
```


## Usage

```js
var loadersByExtension = require('loaders-by-extension');

var loaders = {
	"jsx": options.hotComponents ? ["react-hot-loader", "babel-loader?stage=0"] : "babel-loader?stage=0",
	"js": {
		loader: "babel-loader?stage=0",
		include: path.join(__dirname, "app")
	},
	"json": "json-loader",
	"coffee": "coffee-redux-loader",
	"json5": "json5-loader",
	"txt": "raw-loader",
	"png|jpg|jpeg|gif|svg": "url-loader?limit=10000",
	"woff|woff2": "url-loader?limit=100000",
	"ttf|eot": "file-loader",
	"wav|mp3": "file-loader",
	"html": "html-loader",
	"md|markdown": ["html-loader", "markdown-loader"]
};


//=> loaders: loadersByExtension(loaders)
```

[npm-image]: https://img.shields.io/npm/v/loaders-by-extension.svg?style=flat-square
[npm-url]: https://npmjs.org/package/loaders-by-extension
