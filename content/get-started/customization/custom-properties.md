---
title: Custom Properties
date: 1000-01-05
---

{% include shortcodes/chapter, text: 'Customization', color: 'teal' %}

### Extending Uniform

All of the most common and popular CSS properties are already built in and supported out of the box. If you need to add properties that Uniform does not yet support, you can do so by following the steps below.

---

### Adding new CSS properties

<div class="mb-10"></div>

#### Step 1.  Use the boilerplate template

Use the following boilerplate template to add in details about the CSS property you would like to support.

```scss
// customProperty.scss
@use "uniform/_core" as *;
@use "sass:map";

$keyword: customProperty !default;
$responsive: false !default;
$responsive-pseudos: false !default;

$properties: (css-property) !default;

$core-variants: (
  key-1: red,
  key-2: blue
) !default;

$variants: () !default;

$final-variants: map.merge($core-variants, $variants) !default;

$core-pseudos: () !default;
$pseudos: () !default;
$final-pseudos: list.join($core-pseudos, $pseudos) !default;

@include constructor(
  $keyword,
  $responsive,
  $responsive-pseudos,
  $properties,
  $final-variants,
  $final-pseudos
);

```

This example template will generate the following CSS.

```css
/* styles.css */
.customProperty-key-1 {
  css-property: red;
}
.customProperty-key-2 {
  css-property: blue;
}
```

<div class="mb-10"></div>

#### Step 2. Register your new custom property

To register your new custom property simply include it in your Sass stylesheet.

```scss
// styles.scss
@use "uniform" as *;
@use "customProperty";
...
```
