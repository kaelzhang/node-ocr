# ocr [![NPM version](https://badge.fury.io/js/ocr.png)](http://badge.fury.io/js/ocr) [![Build Status](https://travis-ci.org/kaelzhang/node-ocr.png?branch=master)](https://travis-ci.org/kaelzhang/node-ocr) [![Dependency Status](https://gemnasium.com/kaelzhang/node-ocr.png)](https://gemnasium.com/kaelzhang/node-ocr)

Optical character recognition for node.js

## Installation

```sh
npm install ocr
```

## Synopsis

```js
ocr
.language('arabic')
.recognize(path_to_image, function(err, text){
	if ( err ) {
        console.error(err);   
    } else {
        console.log(text);
    }
});
```

## Usage

### Custom Font-face

Define a custom font-face of a certain language to improve the accuracy.

```js
ocr
.language('chinese')
.fontFace(path_to_font_file)
.recognize(path_to_image, callback)
```