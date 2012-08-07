# simplex-noise.js

simplex-noise.js is a fast simplex noise implementation in Javascript.

## Requirements

It requires typed arrays, if you want to use it in browsers without support
you will need to use a polyfill like [typedarray.js](http://www.calormen.com/polyfill/typedarray.js).

## Usage

```javascript
// initializing a simplex instance
// do this only once it's relatively expensive
var simplex = new SimplexNoise(),
    value2d = simplex.noise2D(x, y),
    value3d = simplex.noise3D(x, y, z),
    value4d = simplex.noise2D(x, y, z, w);
```

You can also pass an alternative random function to the constructor that is
used to build the permutation table:

```javascript
var simplex = new SimplexNoise(Math.random),
    value2d = simplex.noise2D(x, y);
```

## Benchmarks

- [Comparison between 2D and 3D noise](http://jsperf.com/simplex-noise)
- [Comparison with simplex implementation in three.js](http://jsperf.com/simplex-noise-comparison)

## Changelog

### 1.0.0
- Initial Release

## Credits

This is mostly a direct javascript port of the [Java implementation](http://webstaff.itn.liu.se/~stegu/simplexnoise/SimplexNoise.java)
by Stefan Gustavson and Peter Eastman.
