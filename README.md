# metalsmith-clean-css [![Build Status](https://travis-ci.org/aymericbeaumet/metalsmith-clean-css.svg?branch=master)](https://travis-ci.org/aymericbeaumet/metalsmith-clean-css) [![NPM version](https://badge.fury.io/js/metalsmith-clean-css.svg)](http://badge.fury.io/js/metalsmith-clean-css)

A Metalsmith plugin to minify CSS files using
[clean-css](https://github.com/GoalSmashers/clean-css).

## Installation

```javascript
$ npm install metalsmith-clean-css
```

## Usage

### CLI

```javascript
{
  "plugins": {
    "metalsmith-clean-css": {
      "pattern": "src/**/*.css"
    }
  }
}
```

### JavaScript

```javascript
var MetalSmith = require('metalsmith');
var cleanCSS = require('metalsmith-clean-css');

Metalsmith(__dirname)
  .use(cleanCSS({
    files: "src/**/*.css",
    cleanCSS: {
      noRebase: true
    }
  }));
```

#### files
Type: `String`
Default: `**/*.css`

This define which files pattern are concerned by the minification. It is
directly passed to [minimatch](https://github.com/isaacs/minimatch).

#### cleanCSS
Type: `Object`
Default: `{}`

Allow you to directly manipulate the [CleanCSS
API](https://github.com/GoalSmashers/clean-css#how-to-use-clean-css-programmatically).
The configuration object will be passed as is.

## Changelog

* 0.0.1
  * Working plugin

## License

MIT © [Aymeric Beaumet](http://beaumet.me)