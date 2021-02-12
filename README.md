<img src="https://raw.githubusercontent.com/dreipol/chaestli/main/logo.png" width="50%"/>

# chaestli
Dreipol scss grid system

[![Build Status][travis-image]][travis-url]
[![NPM version][npm-version-image]][npm-url]
[![NPM downloads][npm-downloads-image]][npm-url]
[![MIT License][license-image]][license-url]

# Documentation

- [API](https://www.dreipol.dev/chaestli/)
- [Demo](https://www.dreipol.dev/chaestli/demo)

## Available mixins

Chaestli exports only 3 mixins (`chaestli.container`, `chaestli.grid`, `chaestli.column`) that combined together should be enough to scaffold your grid setup. For example:

```scss
@use 'node_modules/@dreipol/chaestli';

.grid {
    .grid__container {
        // a container having a max-with of 1024px with 16px lateral padding
        @include chaestli.container(( width: 1024px, edge: 16px ));
    }
   
    .grid__row {
        // a grid made of 12 columns with 8px lateral gutter
        @include chaestli.grid(( gutter: 8px, num-cols: 12 ));
    }

    .grid__small-col {
        // two columns over 12
        @include chaestli.column(2 span, 12 span);
    }

    .grid__medium-col {
        // for columns over 12
        @include chaestli.column(4 span, 12 span);
    }

    .grid__big-col {
        // eight columns over 12
        @include chaestli.column(8 span, 12 span);
    }
}
```

# Usage 

## Installation


```bash
npm i chaestli -S
```

[travis-image]:https://img.shields.io/travis/dreipol/chaestli.svg?style=flat-square
[travis-url]:https://travis-ci.org/dreipol/chaestli

[license-image]:http://img.shields.io/badge/license-MIT-000000.svg?style=flat-square
[license-url]:LICENSE

[npm-version-image]:http://img.shields.io/npm/v/chaestli.svg?style=flat-square
[npm-downloads-image]:http://img.shields.io/npm/dm/chaestli.svg?style=flat-square
[npm-url]:https://npmjs.org/package/chaestli
