---
title: Customizing Properties
date: 1000-01-03
---

{% include shortcodes/chapter, text: 'Customization', color: 'teal' %}

### Customizing CSS Properties

You can customize almost every aspect of a CSS property. To customize a CSS property, simply pass property variables to the Uniform module configuration.

```scss
@use "uniform" as * with (
  // CSS property settings
);
```

---

#### Changing the Keyword

The `$<property>-keyword` variable sets the class name that will be used to represent this property.

```scss
// styles.scss
@use "uniform" as * with (
  $background-color-keyword: bg
);
```

```css
/* styles.css */
.bg-red-100 {background-color: #feefef;}
.bg-red-200 {background-color: #fee0e0;}
.bg-red-300 {background-color: #fdb0b0;}
...
```

---

#### Exempt Keywords

If the keyword variable is set as `exempt` then the variant name will be used as the class name to define the property.

```scss
// styles.scss
@use "uniform" as * with (
  $display-keyword: exempt
);
```

```css
/* styles.css */
.inline-block {display: inline-block;}
.block {display: block;}
...
```

---

#### Making a CSS property responsive

The `$<property>-responsive` variable controls wether the property will be responsive across breakpoints.

```scss
// styles.scss
@use "uniform" as * with (
  $display-responsive: true
);
```

```css
/* styles.css */
.block {display: block;}
...
@media (min-width: 768px) {
  .block {display: block;}
  ...
}
@media (min-width: 1024px) {
  .block {display: block;}
  ...
}
@media (min-width: 1280px) {
  .block {display: block;}
  ...
}
```

---

#### Responsive Pseudos

The `$<property>-responsive-pseudos` variable enables or disables responsiveness across pseudo variants.

```scss
// styles.scss
@use "uniform" as * with (
  $display-responsive-pseudo: true
);
```

```css
/* styles.css */
.hover\.block:hover {display: block;}
...
@media (min-width: 768px) {
  .hover\.block:hover {display: block;}
  ...
}
@media (min-width: 1024px) {
  .hover\.block:hover {display: block;}
  ...
}
@media (min-width: 1280px) {
  .hover\.block:hover {display: block;}
  ...
}
```

---

#### Customizing Variants

The `$<property>-variants` map sets the variant name and property value.

```scss
// styles.scss
@use "uniform" as * with (
  $max-height-variants: (
    100p: 100%,
    screen: 100vh
  )
);
```

```css
/* styles.css */
.max-h-100p {max-height: 100%;}
.max-h-screen {max-height: 100vh;}
...
```

---

#### Exempt Variants

If the variant key is set as `exempt` then the keyword will be used to define both the class name and variant.

```scss
// styles.scss
@use "uniform" as * with (
  $flex-grow-keyword: flex-grow,
  $flex-grow-variants: (
    exempt: 1,
    0: 0
  )
);
```

```css
/* styles.css */
.flex-grow {flex-grow: 1;}
.flex-grow-0 {flex-grow: 0;}
...
```

---

#### Pseudos

The `$<property>-pseudos` controls which pseudo interaction will be activated for the given property.

```scss
// styles.scss
@use "uniform" as * with (
  $opacity-pseudos: (hover, active)
);
```

```css
/* styles.css */
.hover\.opacity-0:hover {opacity: 0;}
.hover\.opacity-10:hover {opacity: 0.1;}
...

.active\.opacity-0:active {opacity: 0;}
.active\.opacity-10:active {opacity: 0.1;}
...
```





























---

### Customizing your Build

By default, Uniform has default settings already set, however almost every aspect of this framework can be overwritten. To customize, simply load the Uniform module with `with: (<variable>: <value>, <variable>: <value>)`.

```scss
// styles.scss
@use "uniform" as * with (
  $important: true,
  $prefix: 'myPrefix-',
  $colors: (
    custom-color-1: '#000000',
    custom-color-2: '#ffffff'
  ),
  // chain as many variable overrides as you like here
);
```

```css
/* styles.css */
.myPrefix-block {display: block !important;}
.myPrefix-bg-custom-red {background-color: red !important;}
.myPrefix-bg-custom-blue {background-color: blue !important;}
...
```

---

### Extending CSS Property Variants

If you find yourself wanting an extra variant for a particular CSS property that is not available in the default set, simply add key value pairs to the `$<property-name>-variants` map in your module configuration.

```scss
// styles.scss
@use "uniform" as * with (
  $font-size-variants: (
    big: 72px,
    small: 14px,
  ),
  $height-variants: (
    tall: 100px,
    short: 14px,
  ),
  $background-color-variants: (
    sunset: 'red',
    bloodorange: 'orange',
  )
);
```

```css
/* styles.css */
.font-big {font-size: 72px;}
.font-small {font-size: 14px;}
...

.height-tall {height: 100px;}
.height-short {height: 14px;}
...

.bg-sunset {background-color: red;}
.bg-bloodorange {background-color: orange;}
...
```

---

### Replacing Default CSS Property Variants

You can reduce the number of default variants and even remove them by overriding the core variant set. To do this, add key value pairs to the `$<property-name>-core-variants` map in your module configuration.

```scss
// styles.scss
@use "uniform" as * with (
  $font-size-core-variants: (
    big: 72px,
    small: 14px,
  ),
  $height-core-variants: (
    tall: 100px,
    short: 14px,
  ),
  $background-color-core-variants: (
    sunset: 'red',
    bloodorange: 'orange',
  )
);
```

```css
/* styles.css */
.font-big {font-size: 72px;}
.font-small {font-size: 14px;}
/* no other variants available */

.height-tall {height: 100px;}
.height-short {height: 14px;}
/* no other variants available */

.bg-sunset {background-color: red;}
.bg-bloodorange {background-color: orange;}
/* no other variants available */
```


