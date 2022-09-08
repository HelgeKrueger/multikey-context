# Multikey Context for JavaScript _(@digitalbazaar/multikey-context)_

[![Build status](https://img.shields.io/github/workflow/status/digitalbazaar/multikey-context/Node.js%20CI)](https://github.com/digitalbazaar/multikey-context/actions?query=workflow%3A%22Node.js+CI%22)
[![Coverage status](https://img.shields.io/codecov/c/github/digitalbazaar/multikey-context)](https://codecov.io/gh/digitalbazaar/multikey-context)
[![NPM Version](https://img.shields.io/npm/v/@digitalbazaar/multikey-context.svg)](https://npm.im/@digitalbazaar/multikey-context)

> A Multikey context library for JavaScript.

## Table of Contents

- [Background](#background)
- [Install](#install)
- [Usage](#usage)
- [Commercial Support](#commercial-support)
- [License](#license)

## Background

See also (related specs):

* [Data Integrity v1.0](https://w3c.github.io/vc-data-integrity/)

## Install

Requires Node.js 16+

To install via NPM:

```
npm install @digitalbazaar/multikey-context
```

## Usage

```js
import multikeyContext from '@digitalbazaar/multikey-context';

multikeyContext.CONTEXT_URL
// 'https://w3id.org/security/multikey/v1'

// Codec term map value for CBOR-LD
multikeyContext.constants.CBORLD_CODEC_VALUE
// 0x31

// get context data for a specific context
multikeyContext.CONTEXT
// full context object
```

This package can be used with bundlers, such as [webpack][], in browser
applications.

## API

The library exports the following properties:
- `CONTEXT_URL`
- `CONTEXT`
- `constants`: A Object that maps constants to well-known context URLs. The
  main constant `CONTEXT_URL` may be updated from time to time to the
  latest context location.
- `contexts`: A `Map` that maps URLs to full context data.
- `appContextMap`: For use with `cborld` library.

## Developing

WARNING: The `.jsonld` in `contexts/` is auto-generated by the `npm run build` script,
each time you run the test suite.

DO NOT edit it directly (or your changes will be quickly overwritten).
Instead, make all context changes to `js/context.js`.

## Commercial Support

Commercial support for this library is available upon request from
Digital Bazaar: support@digitalbazaar.com

## License

- BSD 3-Clause © Digital Bazaar
- See the [LICENSE](./LICENSE) file for details.

[webpack]: https://webpack.js.org/
