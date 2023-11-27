colors-named
===

[![Buy me a coffee](https://img.shields.io/badge/Buy%20me%20a%20coffee-048754?logo=buymeacoffee)](https://jaywcjlove.github.io/#/sponsor)
[![Build & Deploy](https://github.com/jaywcjlove/colors-named/actions/workflows/ci.yml/badge.svg)](https://github.com/jaywcjlove/colors-named/actions/workflows/ci.yml)
[![Open in unpkg](https://img.shields.io/badge/Open%20in-unpkg-blue)](https://uiwjs.github.io/npm-unpkg/#/pkg/colors-named/file/README.md)
[![npm version](https://img.shields.io/npm/v/colors-named.svg)](https://www.npmjs.com/package/colors-named)
[![Coverage Status](https://jaywcjlove.github.io/colors-named/badges.svg)](https://jaywcjlove.github.io/colors-named/lcov-report/)

A array with color names. Based on https://www.w3.org/TR/css-color-4/#named-colors

## Installation

This package is [ESM only](https://gist.github.com/sindresorhus/a39789f98801d908bbc7ff3ecc99d99c): Node 12+ is needed to use it and it must be import instead of require.

```bash
npm install colors-named
```

If you still want to use in CommonJS, you can use dynamic `import()` to load.

```js
const named = await import('colors-named');

// Fix compiling in typescript.
// https://github.com/microsoft/TypeScript/issues/43329#issuecomment-922544562
const named = await (Function('return import("colors-named")')()) as Promise<typeof import("colors-named")>;
```

## Usage

```js
import named from "colors-named";

console.log(named)                   // => ['aliceblue', 'antiquewhite', 'aqua', ... ]
console.log(named.includes('red'))   // => true
console.log(named.length)            // => 148
```

```js
'colors-named'                'colors-named-hex'          'colors-named-decimal'
===============              ===================         =====================
const named = [                const hexs = [             const hexs = [
  'aliceblue',         ->        '#F0F8FF',       ->        [240, 248, 255],
  'antiquewhite',      ->        '#FAEBD7',       ->        [250, 235, 215],
  'aqua',              ->        '#00FFFF',       ->        [0, 255, 255],
  'aquamarine',        ->        '#7FFFD4',       ->        [127, 255, 212],
  'azure',             ->        '#F0FFFF',       ->        [240, 255, 255],
  'beige',             ->        '#F5F5DC',       ->        [245, 245, 220],
  'bisque',            ->        '#FFE4C4',       ->        [255, 228, 196],
  'black',             ->        '#000000',       ->        [0, 0, 0],
  'blanchedalmond',    ->        '#FFEBCD',       ->        [255, 235, 205],
  'blue',              ->        '#0000FF',       ->        [0, 0, 255],
  'blueviolet',        ->        '#8A2BE2',       ->        [138, 43, 226],
  'brown',             ->        '#A52A2A',       ->        [165, 42, 42],
  ...                  ->        ...              ->        ...
];                             ];                         ];
```

```js
import hexs from "colors-named-hex";
import named from "colors-named";
import decimal from "colors-named-decimal";

decimal[named.indexOf('aliceblue')] // => [240, 248, 255]
decimal[named.indexOf('red')]       // => [255, 0, 0]
decimal[named.indexOf('black')]     // => [0, 0, 0]

hexs[named.indexOf('aliceblue')] // => #F0F8FF
hexs[named.indexOf('red')]       // => #FF0000
hexs[named.indexOf('black')]     // => #000000
```

## API

```ts
/**
 * A array with color names. Based on https://www.w3.org/TR/css-color-4/#named-colors
 */
declare const names: readonly ["aliceblue", "antiquewhite", "aqua", "aquamarine", "azure", "beige", "bisque", "black", "blanchedalmond", "blue", "blueviolet", "brown", "burlywood", "cadetblue", "chartreuse", "chocolate", "coral", "cornflowerblue", "cornsilk", "crimson", "cyan", "darkblue", "darkcyan", "darkgoldenrod", "darkgray", "darkgreen", "darkgrey", "darkkhaki", "darkmagenta", "darkolivegreen", "darkorange", "darkorchid", "darkred", "darksalmon", "darkseagreen", "darkslateblue", "darkslategray", "darkslategrey", "darkturquoise", "darkviolet", "deeppink", "deepskyblue", "dimgray", "dimgrey", "dodgerblue", "firebrick", "floralwhite", "forestgreen", "fuchsia", "gainsboro", "ghostwhite", "gold", "goldenrod", "gray", "green", "greenyellow", "grey", "honeydew", "hotpink", "indianred", "indigo", "ivory", "khaki", "lavender", "lavenderblush", "lawngreen", "lemonchiffon", "lightblue", "lightcoral", "lightcyan", "lightgoldenrodyellow", "lightgray", "lightgreen", "lightgrey", "lightpink", "lightsalmon", "lightseagreen", "lightskyblue", "lightslategray", "lightslategrey", "lightsteelblue", "lightyellow", "lime", "limegreen", "linen", "magenta", "maroon", "mediumaquamarine", "mediumblue", "mediumorchid", "mediumpurple", "mediumseagreen", "mediumslateblue", "mediumspringgreen", "mediumturquoise", "mediumvioletred", "midnightblue", "mintcream", "mistyrose", "moccasin", "navajowhite", "navy", "oldlace", "olive", "olivedrab", "orange", "orangered", "orchid", "palegoldenrod", "palegreen", "paleturquoise", "palevioletred", "papayawhip", "peachpuff", "peru", "pink", "plum", "powderblue", "purple", "rebeccapurple", "red", "rosybrown", "royalblue", "saddlebrown", "salmon", "sandybrown", "seagreen", "seashell", "sienna", "silver", "skyblue", "slateblue", "slategray", "slategrey", "snow", "springgreen", "steelblue", "tan", "teal", "thistle", "tomato", "turquoise", "violet", "wheat", "white", "whitesmoke", "yellow", "yellowgreen"];
export default names;
```

## Related

- [`colors-named-hex`](https://jaywcjlove.github.io/colors-named-hex) A array with color name -> Hex rgb.
- [`colors-named-decimal`](https://github.com/jaywcjlove/colors-named-decimal) A array with color name -> decimal rgb.

## Contributors

As always, thanks to our amazing contributors!

<a href="https://github.com/jaywcjlove/colors-named/graphs/contributors">
  <img src="https://jaywcjlove.github.io/colors-named/CONTRIBUTORS.svg" />
</a>

Made with [action-contributors](https://github.com/jaywcjlove/github-action-contributors).

## License

Licensed under the MIT License.
