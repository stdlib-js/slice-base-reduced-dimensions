<!--

@license Apache-2.0

Copyright (c) 2023 The Stdlib Authors.

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


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# reducedDimensions

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Return a list of reduced dimensions in an un-normalized [`MultiSlice`][@stdlib/slice/multi] object.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

In a multi-axis indexing expression (e.g., '1,:,2,:,0:10:1'), a non-reduced dimension corresponds to a dimension which is retained in the slice result. Only integer indexing expressions (e.g., only the first and third dimensions in '1,:,2,:,0:10:1') result in dimension reduction; slices always retain respective dimensions, even if a slice is empty or only selects a single element.

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

```javascript
import reducedDimensions from 'https://cdn.jsdelivr.net/gh/stdlib-js/slice-base-reduced-dimensions@deno/mod.js';
```
The previous example will load the latest bundled code from the deno branch. Alternatively, you may load a specific version by loading the file from one of the [tagged bundles](https://github.com/stdlib-js/slice-base-reduced-dimensions/tags). For example,

```javascript
import reducedDimensions from 'https://cdn.jsdelivr.net/gh/stdlib-js/slice-base-reduced-dimensions@v0.0.1-deno/mod.js';
```

<a name="main"></a>

#### reducedDimensions( slice )

Return a list of reduced dimensions in an un-normalized [`MultiSlice`][@stdlib/slice/multi] object.

```javascript
import MultiSlice from 'https://cdn.jsdelivr.net/gh/stdlib-js/slice-multi@deno/mod.js';
import Slice from 'https://cdn.jsdelivr.net/gh/stdlib-js/slice-ctor@deno/mod.js';

var s = new MultiSlice( 1, null, 2, void 0, new Slice( 0, 10, 1 ) );
// returns <MultiSlice>

var indices = reducedDimensions( s );
// returns [ 0, 2 ]
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

<!-- eslint-disable new-cap -->

```javascript
import S from 'https://cdn.jsdelivr.net/gh/stdlib-js/slice-ctor@deno/mod.js';
import MultiSlice from 'https://cdn.jsdelivr.net/gh/stdlib-js/slice-multi@deno/mod.js';
import reducedDimensions from 'https://cdn.jsdelivr.net/gh/stdlib-js/slice-base-reduced-dimensions@deno/mod.js';

var s = new MultiSlice( null, S(), -1 );
var out = reducedDimensions( s );
console.log( '%s => [%s]', s.toString(), out.join( ',' ) );

s = new MultiSlice( null );
out = reducedDimensions( s );
console.log( '%s => [%s]', s.toString(), out.join( ',' ) );

s = new MultiSlice( S( -1, null, -1 ), 3 );
out = reducedDimensions( s );
console.log( '%s => [%s]', s.toString(), out.join( ',' ) );

s = new MultiSlice( 2, S( -10, -2, 2 ), 3, null );
out = reducedDimensions( s );
console.log( '%s => [%s]', s.toString(), out.join( ',' ) );

s = new MultiSlice( S( 1, 20, 2 ), S( null, null, -1 ) );
out = reducedDimensions( s );
console.log( '%s => [%s]', s.toString(), out.join( ',' ) );
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2023. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/slice-base-reduced-dimensions.svg
[npm-url]: https://npmjs.org/package/@stdlib/slice-base-reduced-dimensions

[test-image]: https://github.com/stdlib-js/slice-base-reduced-dimensions/actions/workflows/test.yml/badge.svg?branch=v0.0.1
[test-url]: https://github.com/stdlib-js/slice-base-reduced-dimensions/actions/workflows/test.yml?query=branch:v0.0.1

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/slice-base-reduced-dimensions/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/slice-base-reduced-dimensions?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/slice-base-reduced-dimensions.svg
[dependencies-url]: https://david-dm.org/stdlib-js/slice-base-reduced-dimensions/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/slice-base-reduced-dimensions/tree/deno
[umd-url]: https://github.com/stdlib-js/slice-base-reduced-dimensions/tree/umd
[esm-url]: https://github.com/stdlib-js/slice-base-reduced-dimensions/tree/esm
[branches-url]: https://github.com/stdlib-js/slice-base-reduced-dimensions/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/slice-base-reduced-dimensions/main/LICENSE

[@stdlib/slice/multi]: https://github.com/stdlib-js/slice-multi/tree/deno

</section>

<!-- /.links -->
