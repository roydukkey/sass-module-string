# sass-meta

[![Release Version](https://img.shields.io/npm/v/sass-string.svg)](https://www.npmjs.com/package/sass-string)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

This Sass module provides more advanced string functions.

## Install

### Requires

Install the package:

```bash
npm install sass-string
```

Use the package like any other Sass module:

```scss
@use 'sass-string';
```

Depending on your setup, you may need to configure `node_modules` as include path:

```js
const sass = require('sass');

sass.render({
  file: scss_filename,
  includePaths: ['node_modules']
});
```

## Public API

<dl>

  <dt><a href="//github.com/roydukkey/sass-module-string/tree/master/src/string/_from.sass"><code>from ( $value )</code></a></dt>
  <dd>Creates a string from the provided value.</dd>

</dl>

Don't see the function you're looking for? Request a [new feature](//github.com/roydukkey/sass-module-string/issues/new) describing a use case.

## Combined API

In order to avoid constantly declaring both the native 'sass:string' module and this library, the combined API has been added which merges the two.

```scss
// Rather than using both modules separately...
@use 'sass-string';
@use 'sass:string';

// ...this statement will accomplish the same thing.
@use 'sass-string/string';
```
