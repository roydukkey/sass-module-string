**Renamed!**
This package has been renamed to [`@sass-fairy/string`](https://github.com/roydukkey/sass-fairy/tree/master/packages/string#readme) and organised in a mono-repo for better maintainablity, an improved user experience, and [full documentation](https://sass-fairy.com/api/string). Explore more about the change at [sass-fairy.com](https://sass-fairy.com).

---

# sass-string

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

  <dt><a href="//github.com/roydukkey/sass-module-string/tree/master/src/string/_ends-with.sass"><code>ends-with ( $string, $substring [, $end-at] )</code></a></dt>
  <dd>Determines whether a string ends with the characters of a specified substring, returning true or false as appropriate.</dd>

  <dt><a href="//github.com/roydukkey/sass-module-string/tree/master/src/string/_from.sass"><code>from ( $value )</code></a></dt>
  <dd>Creates a string from the provided value.</dd>

  <dt><a href="//github.com/roydukkey/sass-module-string/tree/master/src/string/_includes.sass"><code>includes ( $string, $substring [, $start-at] )</code></a></dt>
  <dd>Determines whether a string includes the characters of a specified substring, returning true or false as appropriate.</dd>

  <dt><a href="//github.com/roydukkey/sass-module-string/tree/master/src/string/_index.sass"><code>index ( $string, $substring [, $start-at] )</code></a></dt>
  <dd>Returns the first index at which a specified substring can be found in a string; otherwise, 0 is returned, indicating the substring is not present.</dd>

  <dt><a href="//github.com/roydukkey/sass-module-string/tree/master/src/string/_last-index.sass"><code>last-index ( $string, $substring [, $end-at] )</code></a></dt>
  <dd>Returns the last index at which a specified substring can be found in a string; otherwise, 0 is returned, indicating the substring is not present. The string is searched forwards, ending at a given index when specified.</dd>

  <dt><a href="//github.com/roydukkey/sass-module-string/tree/master/src/string/_split.sass"><code>split ( $string [, $delimiter] [, $limit] [, $separator] [, $bracketed] )</code></a></dt>
  <dd>Divides a string into a list of substrings.</dd>

  <dt><a href="//github.com/roydukkey/sass-module-string/tree/master/src/string/_starts-with.sass"><code>starts-with ( $string, $substring [, $start-at] )</code></a></dt>
  <dd>Determines whether a string begins with the characters of a specified substring, returning true or false as appropriate.</dd>

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

*Note:* Since its functionality is enhanced by this library, the combined API hides the native `string.index()` function.
