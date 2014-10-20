# gl-checker-texture

[![experimental](http://badges.github.io/stability-badges/dist/experimental.svg)](http://github.com/badges/stability-badges)

Creates a 2x2 checkered repeating WebGL texture. Useful for checkered backgrounds, dotted lines, etc.

```js
var Checker = require('gl-checker-texture')

var tex = Checker(gl)
tex.bind()
```

## Usage

[![NPM](https://nodei.co/npm/gl-checker-texture.png)](https://nodei.co/npm/gl-checker-texture/)

#### `createTexture(gl[, opt])`

Creates a new 2x2 texture with the given options:

- `colors` an array of two RGBA colors *in bytes*. Defaults to #ffffff and #cccccc. 

Example:

```js
var tex = createTexture(gl, { colors: [
    [0x50,0x50,0x50,0xff],
    [0x46,0x46,0x46,0xff]
]})
```

The new texture is set to `gl.REPEAT` wrap and `gl.NEAREST` filtering. 

## License

MIT, see [LICENSE.md](http://github.com/mattdesl/gl-checker-texture/blob/master/LICENSE.md) for details.
