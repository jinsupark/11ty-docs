---
title: Naming Principles
date: 1000-01-09
---

{% include shortcodes/chapter, text: 'Fundamentals', color: 'yellow' %}

### Naming Principles

Utility classes function in an immutable way by nature, therefore we want its name to be just as durable and future-proof. Every CSS property name and its variants follow a strict and scalable naming convention. The following is a list of principles Uniform follows when considering how properties and variants should be named.

---

<div class="mb-10"></div>

<h4><span class="w-6 h-6 mr-2 inline-flex align-items-center justify-content-center font-sm font-600 leading-none bg-blue-500 leading-1 color-white radius-round">1</span> Make use of verbose values</h4>

If the property values are verbose and self explanatory, then use the value to define keyword provided the value name does not cause any confusion or conflict with other properties.

```scss
.block {display: block;}
.ease-in-out {transition-timing-function: ease-in-out;}
.underline {text-decoration: underline;}
...
```

<div class="mb-10"></div>

<h4><span class="w-6 h-6 mr-2 inline-flex align-items-center justify-content-center font-sm font-600 leading-none bg-blue-500 leading-1 color-white radius-round">2</span> Truncate property names when possible</h4>

If the property name include words that can be shortened without confusion, shorten it.

```scss
.bg-black: {background-color: black;}
.bg-white: {background-color: white;}
...
```

<div class="mb-10"></div>

<h4><span class="w-6 h-6 mr-2 inline-flex align-items-center justify-content-center font-sm font-600 leading-none bg-blue-500 leading-1 color-white radius-round">3</span> Remove redundant hyphenation</h4>

If the word is hyphenated but can be elegantly combined, remove hyphenation e.g. `wordbreak` and `whitespace` instead of `word-break` and `white-space`.

```scss
.wordbreak-normal: {word-break: normal;}
.whitespace-normal: {white-space: normal;}
...
```

<div class="mb-10"></div>

<h4><span class="w-6 h-6 mr-2 inline-flex align-items-center justify-content-center font-sm font-600 leading-none bg-blue-500 leading-1 color-white radius-round">4</span>Use single-letter keywords conservatively</h4>

Single-characters are only reserved for directions and the `width`, `height`, `margin`, and `padding` properties e.g. `w`, `h`, `m`, `p`. For single letter properties, don't separate direction using a delimiter. For example, use `mr` for margin right instead of `m-r`.

```scss
.w-1: {width: 0.25rem;}
.p-2: {padding: 0.5rem;}

.mr-1: {margin-right 0.25rem;}
.mb-1: {margin-bottom 0.25rem;}
...
```

<div class="mb-10"></div>

<h4><span class="w-6 h-6 mr-2 inline-flex align-items-center justify-content-center font-sm font-600 leading-none bg-blue-500 leading-1 color-white radius-round">5</span> Use single-characters for directions</h4>

Common directional properties such as `top`, `right`, `bottom`, and `left` are represented with the first letter of the direction e.g. `border-t` for `border-top` etc. For more than one direction, combine the direction letters e.g. `tr` for `top-right`.

```scss
.radius-tl-sm: {border-top-left-radius: 0.25rem;}
.radius-tr-sm: {border-top-right-radius: 0.25rem;}
...
```

<div class="mb-10"></div>

<h4><span class="w-6 h-6 mr-2 inline-flex align-items-center justify-content-center font-sm font-600 leading-none bg-blue-500 leading-1 color-white radius-round">6</span> Simplify properties names</h4>

Simplify the property name to its most essential and ideal denominator of the word provided it does not cause confusion or conflict with others properties in the same family.

```scss
.font-700: {font-weight: 700;}
.font-xl: {font-size: 1.25rem;}
...
```

When dealing with multi-word properties such as `line-height`, simplifying it to just `height` or `line` would misrepresent the meaning and cause confusion. In this case, use a different industry term such as `leading` instead.

<div class="mb-10"></div>

<h4><span class="w-6 h-6 mr-2 inline-flex align-items-center justify-content-center font-sm font-600 leading-none bg-blue-500 leading-1 color-white radius-round">7</span> Append unit as alphabetical characters</h4>

Over qualify the unit by appending an abbreviated characters that represent the unit only if it causes conflict without. All negative values are suffixed have `n` (negative) at the beginning of the variant name. Append units to avoid conflicts with similarly numbered variants.


```scss
50p: 50%,
n50p: -50%,
100p: 100%,   // p for percent
n100p: -100%,

100vw: 100vw, // vw for viewport width
100vh: 100vh, // vw for viewport width
...
```

<div class="mb-10"></div>

<h4><span class="w-6 h-6 mr-2 inline-flex align-items-center justify-content-center font-sm font-600 leading-none bg-blue-500 leading-1 color-white radius-round">8</span> Be consistent about how property scales</h4>

Pixel based variants follow the `px`, `2px`, `3px...` pattern. General sizing follow the `sm`, `md`, `lg` pattern. Custom user-defined scales such as sizing and line-height properties follow the numerical `1`, `2`, `3` pattern.

```scss
// Pixel based scaling
px: 1px,
2px: 2px,
3px: 3px,
4px: 4px,
...
```

```scss
// XY based scaling
...
3xs: 2px,
2xs: 3px,
xs: 4px,
sm: 6px,
md: 8px,
lg: 10px,
xl: 12px,
2xl: 14px,
3xl: 16px,
...
```

```scss
// Used-defined scaling
0: 0,
1: rem(4),
2: rem(8),
3: rem(12),
4: rem(16),
5: rem(20),
6: rem(24),
...
```