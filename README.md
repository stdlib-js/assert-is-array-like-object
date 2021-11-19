<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# isArrayLikeObject

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Test if a value is an array-like object.

<section class="installation">

## Installation

```bash
npm install @stdlib/assert-is-array-like-object
```

</section>

<section class="usage">

## Usage

```javascript
var isArrayLikeObject = require( '@stdlib/assert-is-array-like-object' );
```

#### isArrayLikeObject( value )

Tests if a value is an [array-like][array-like] `object`.

<!-- eslint-disable object-curly-newline -->

```javascript
var bool = isArrayLikeObject( [] );
// returns true

bool = isArrayLikeObject( { 'length': 10 } );
// returns true
```

If provided a `string`, the function returns `false`.

```javascript
var bool = isArrayLikeObject( 'beep' );
// returns false
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint-disable object-curly-newline, object-curly-spacing, no-empty-function, no-restricted-syntax -->

<!-- eslint no-undef: "error" -->

```javascript
var Float64Array = require( '@stdlib/array-float64' );
var isArrayLikeObject = require( '@stdlib/assert-is-array-like-object' );

var bool = isArrayLikeObject( { 'length': 10 } );
// returns true

bool = isArrayLikeObject( [] );
// returns true

bool = isArrayLikeObject( new Float64Array( 10 ) );
// returns true

bool = (function test() {
    return isArrayLikeObject( arguments );
})();
// returns true

bool = isArrayLikeObject( 'beep' );
// returns false

bool = isArrayLikeObject( null );
// returns false

bool = isArrayLikeObject( void 0 );
// returns false

bool = isArrayLikeObject( 5 );
// returns false

bool = isArrayLikeObject( true );
// returns false

bool = isArrayLikeObject( {} );
// returns false

bool = isArrayLikeObject( function noop() {} );
// returns false
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/assert/is-array`][@stdlib/assert/is-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array.</span>
-   <span class="package-name">[`@stdlib/assert/is-array-like`][@stdlib/assert/is-array-like]</span><span class="delimiter">: </span><span class="description">test if a value is array-like.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/assert-is-array-like-object.svg
[npm-url]: https://npmjs.org/package/@stdlib/assert-is-array-like-object

[test-image]: https://github.com/stdlib-js/assert-is-array-like-object/actions/workflows/test.yml/badge.svg
[test-url]: https://github.com/stdlib-js/assert-is-array-like-object/actions/workflows/test.yml

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/assert-is-array-like-object/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/assert-is-array-like-object?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/assert-is-array-like-object.svg
[dependencies-url]: https://david-dm.org/stdlib-js/assert-is-array-like-object/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/assert-is-array-like-object/main/LICENSE

[array-like]: http://www.2ality.com/2013/05/quirk-array-like-objects.html

<!-- <related-links> -->

[@stdlib/assert/is-array]: https://github.com/stdlib-js/assert-is-array

[@stdlib/assert/is-array-like]: https://github.com/stdlib-js/assert-is-array-like

<!-- </related-links> -->

</section>

<!-- /.links -->
