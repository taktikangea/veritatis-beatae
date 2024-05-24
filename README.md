# @taktikangea/veritatis-beatae <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![dependency status][5]][6]
[![dev dependency status][7]][8]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Is this value a JS Typed Array? This module works cross-realm/iframe, does not depend on `instanceof` or mutable properties, and despite ES6 Symbol.toStringTag.

## Example

```js
var isTypedArray = require('@taktikangea/veritatis-beatae');
var assert = require('assert');

assert.equal(false, isTypedArray(undefined));
assert.equal(false, isTypedArray(null));
assert.equal(false, isTypedArray(false));
assert.equal(false, isTypedArray(true));
assert.equal(false, isTypedArray([]));
assert.equal(false, isTypedArray({}));
assert.equal(false, isTypedArray(/a/g));
assert.equal(false, isTypedArray(new RegExp('a', 'g')));
assert.equal(false, isTypedArray(new Date()));
assert.equal(false, isTypedArray(42));
assert.equal(false, isTypedArray(NaN));
assert.equal(false, isTypedArray(Infinity));
assert.equal(false, isTypedArray(new Number(42)));
assert.equal(false, isTypedArray('foo'));
assert.equal(false, isTypedArray(Object('foo')));
assert.equal(false, isTypedArray(function () {}));
assert.equal(false, isTypedArray(function* () {}));
assert.equal(false, isTypedArray(x => x * x));
assert.equal(false, isTypedArray([]));

assert.ok(isTypedArray(new Int8Array()));
assert.ok(isTypedArray(new Uint8Array()));
assert.ok(isTypedArray(new Uint8ClampedArray()));
assert.ok(isTypedArray(new Int16Array()));
assert.ok(isTypedArray(new Uint16Array()));
assert.ok(isTypedArray(new Int32Array()));
assert.ok(isTypedArray(new Uint32Array()));
assert.ok(isTypedArray(new Float32Array()));
assert.ok(isTypedArray(new Float64Array()));
assert.ok(isTypedArray(new BigInt64Array()));
assert.ok(isTypedArray(new BigUint64Array()));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@taktikangea/veritatis-beatae
[npm-version-svg]: https://versionbadg.es/inspect-js/@taktikangea/veritatis-beatae.svg
[deps-svg]: https://david-dm.org/inspect-js/@taktikangea/veritatis-beatae.svg
[deps-url]: https://david-dm.org/inspect-js/@taktikangea/veritatis-beatae
[dev-deps-svg]: https://david-dm.org/inspect-js/@taktikangea/veritatis-beatae/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@taktikangea/veritatis-beatae#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@taktikangea/veritatis-beatae.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@taktikangea/veritatis-beatae.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@taktikangea/veritatis-beatae.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@taktikangea/veritatis-beatae
[codecov-image]: https://codecov.io/gh/inspect-js/@taktikangea/veritatis-beatae/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@taktikangea/veritatis-beatae/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@taktikangea/veritatis-beatae
[actions-url]: https://github.com/taktikangea/veritatis-beatae/actions
