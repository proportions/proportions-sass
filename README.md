# Proportions for Sass 📐

[![npm module](https://badge.fury.io/js/proportions-sass.svg)](https://www.npmjs.org/package/proportions-sass)

> Organic, Mechanical and Musical Proportions

From *The Elements of Typographic Style* by Robert Bringhurst.

Install using `npm` or `yarn`:

```
[npm|yarn] install proportions-sass
```

Import using [webpack](https://github.com/webpack/webpack)'s [sass-loader](https://github.com/webpack-contrib/sass-loader):

```js
@import '~proportions-sass'
```

Or the more verbose way in a vanilla Sass environment:

```scss
@import './node_modules/proportions-sass/proportions-sass.scss';
```

The proportions are implemented in a map. This way the global scope is not polluted width too many variables:

```scss
$proportions: (
  doubleSquare: 2,
  tallOctagon: 1.924,
  tallHexagon: 1.866,
  octagon: 1.848,
  hexagon: 1.732,
  tallPentagon: 1.701,
  goldenSection: 1.618,
  pentagon: 1.539,
  shortPentagon: 1.376,
  tallHalfOctagon: 1.307,
  halfOctagon: 1.207,
  truncatedPentagon: 1.176,
  turnedHexagon: 1.155,
  tallCrossOctagon: 1.082,
  turnedPentagon: 1.051,
  square: 1,
  broadPentagon: 0.951,
  broadCrossOctagon: 0.924,
  broadHexagon: 0.866,
  fullCrossOctagon: 0.829,
  iso: 1.414,
  octave: 2,
  majorSeventh: 15 / 8,
  minorSeventh: 16 / 9,
  majorSixth: 5 / 3,
  minorSixth: 8 / 5,
  fifth: 3 / 2,
  diminishedFifth: 1.414,
  augmentedFourth: 1.414,
  fourth: 4 / 3,
  majorThird: 5 / 4,
  minorThird: 6 / 5,
  majorSecond: 9 / 8,
  minorSecond: 16 / 15,
  unison: 1
);
```

Use [`map-get`](http://sass-lang.com/documentation/Sass/Script/Functions.html#map_get-instance_method) to fetch the desired proportion:

```scss
body {
  line-height: map-get($proportions, goldenSection);
}
```
