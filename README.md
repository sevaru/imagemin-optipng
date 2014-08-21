# imagemin-optipng [![Build Status](https://travis-ci.org/kevvaimagemin/imagemin-optipng.svg?branch=master)](https://travis-ci.org/imagemin/imagemin-optipng)

> optipng image-min plugin


## Install

```sh
$ npm install --save imagemin-optipng
```


## Usage

```js
var Imagemin = require('image-min');
var optipng = require('imagemin-optipng');

var imagemin = new Imagemin()
	.src('foo.png')
	.dest('foo-optimized.png')
	.use(optipng({ optimizationLevel: 3 }));

imagemin.optimize();
```


## Options

### optimizationLevel

Type: `Number`  
Default: `3`

Select an optimization level between `0` and `7`.

> The optimization level 0 enables a set of optimization operations that require minimal effort. There will be no changes to image attributes like bit depth or color type, and no recompression of existing IDAT datastreams. The optimization level 1 enables a single IDAT compression trial. The trial chosen is what. OptiPNG thinks it’s probably the most effective. The optimization levels 2 and higher enable multiple IDAT compression trials; the higher the level, the more trials.

Level and trials:

1. 1 trial
2. 8 trials
3. 16 trials
4. 24 trials
5. 48 trials
6. 120 trials
7. 240 trials


## License

MIT © [imagemin](https://github.com/imagemin)
