---
title: Typography
date: 1000-01-06
---

{% include shortcodes/chapter, text: 'Theming', color: 'teal' %}

### Font Family Chart

Use the following chart as the reference for the `font-family` property. Each font family also has fall-back options set.

<table class="table">
  <thead class="uppercase font-xs font-600 tracking-1 color-black">
    <tr>
      <th>
        Variant
      </th>
      <th>
        Value
      </th>
      <th>
        Preview
      </th>
    </tr>
  </thead>
  <tbody class="font-sm">
    <tr>
      <td>sans</td>
      <td>sans-serif</td>
      <td class="font-sans">
        Hello World
      </td>
    </tr>
    <tr>
      <td>serif</td>
      <td>serif</td>
      <td class="font-serif">
        Hello World
      </td>
    </tr>
    <tr>
      <td>mono</td>
      <td>monospace</td>
      <td class="font-mono">
        Hello World
      </td>
    </tr>
  </tbody>
</table>

---

### Font Size Chart

Use the following chart as the reference for the `font-size` property.

<table class="table">
  <thead class="uppercase font-xs font-600 tracking-1 color-black">
    <tr>
      <th>
        Variant
      </th>
      <th>
        Value
      </th>
      <th>
        Preview
      </th>
    </tr>
  </thead>
  <tbody class="font-sm">
    <tr>
      <td>2xs</td>
      <td>10px</td>
      <td class="font-2xs">
        Hello World
      </td>
    </tr>
    <tr>
      <td>xs</td>
      <td>12px</td>
      <td class="font-xs">
        Hello World
      </td>
    </tr>
    <tr>
      <td>sm</td>
      <td>14px</td>
      <td class="font-sm">
        Hello World
      </td>
    </tr>
    <tr>
      <td>md</td>
      <td>16px</td>
      <td class="font-md">
        Hello World
      </td>
    </tr>
    <tr>
      <td>lg</td>
      <td>18px</td>
      <td class="font-lg">
        Hello World
      </td>
    </tr>
    <tr>
      <td>xl</td>
      <td>20px</td>
      <td class="font-xl">
        Hello World
      </td>
    </tr>
    <tr>
      <td>2xl</td>
      <td>24px</td>
      <td class="font-2xl">
        Hello World
      </td>
    </tr>
    <tr>
      <td>3xl</td>
      <td>28px</td>
      <td class="font-3xl">
        Hello World
      </td>
    </tr>
    <tr>
      <td>4xl</td>
      <td>32px</td>
      <td class="font-4xl">
        Hello World
      </td>
    </tr>
    <tr>
      <td>5xl</td>
      <td>36px</td>
      <td class="font-5xl">
        Hello World
      </td>
    </tr>
    <tr>
      <td>6xl</td>
      <td>40px</td>
      <td class="font-6xl">
        Hello World
      </td>
    </tr>
    <tr>
      <td>7xl</td>
      <td>48px</td>
      <td class="font-7xl">
        Hello World
      </td>
    </tr>
    <tr>
      <td>8xl</td>
      <td>56px</td>
      <td class="font-8xl">
        Hello World
      </td>
    </tr>
    <tr>
      <td>9xl</td>
      <td>64px</td>
      <td class="font-9xl">
        Hello World
      </td>
    </tr>
    <tr>
      <td>10xl</td>
      <td>72px</td>
      <td class="font-10xl">
        Hello World
      </td>
    </tr>
  </tbody>
</table>

---

### Line-Height Chart

All default Uniform `line-height` values are unitless by default. Use the following chart as the reference for the `leading` property.

<table class="table">
  <thead class="uppercase font-xs font-600 tracking-1 color-black">
    <tr>
      <th>
        Variant
      </th>
      <th>
        Value
      </th>
    </tr>
  </thead>
  <tbody class="font-sm">
    <tr>
      <td>1</td>
      <td>1</td>
    <tr>
      <td>2</td>
      <td>1.125</td>
    </tr>
    <tr>
      <td>3</td>
      <td>1.25</td>
    </tr>
    <tr>
      <td>4</td>
      <td>1.375</td>
    </tr>
    <tr>
      <td>5</td>
      <td>1.5</td>
    </tr>
    <tr>
      <td>6</td>
      <td>1.625</td>
    </tr>
    <tr>
      <td>7</td>
      <td>1.75</td>
    </tr>
    <tr>
      <td>8</td>
      <td>1.875</td>
    </tr>
    <tr>
      <td>9</td>
      <td>2</td>
    </tr>
    <tr>
      <td>10</td>
      <td>2.125</td>
    </tr>
    <tr>
      <td>11</td>
      <td>2.25</td>
    </tr>
    <tr>
      <td>12</td>
      <td>2.375</td>
    </tr>
    <tr>
      <td>13</td>
      <td>2.5</td>
    </tr>
  </tbody>
</table>

---

### Basic Usage

The following example showcases how typography variants can be applied.

<section class="radius-sm bg-silver-100 p-6">
  <div class="bg-white shadow-3 p-4 py-8 font-h5 md.font-2xl font-600 leading-8 align-center radius-xs">
    Hello World
  </div>
</section>

```html
<div class="font-h5 md.font-2xl font-600 leading-8">
	Hello World
</div>
```

---

#### Extending Core Variants

You can extend the various typography related maps to enable more variant options. Note, if you pass in a key that already exists, the original will be overwritten with the latest variant.

```scss
@use "uniform" as * with (
  $font-families: (
    helvetica: Helvetica
  ),
  $font-sizes: (
    huge: 72px,
    tiny: 8px
  ),
  $leadings: (
    tall: 3
  )
);
```

```css
/* styles.css */
.font-helvetica {
  font-family: Helvetica;
}
.font-huge {
  font-size: 72px;
}
.font-tiny {
  font-size: 8px;
}
.font-tall {
  line-height: 3;
}
```

---
#
### Replacing Core Variants

You can replace the default variants entirely by adding key value pairs to each of the maps.

```scss
@use "uniform" as * with (
  $core-font-families: (
    ...
  ),
  $core-font-sizes: (
    ...
  ),
  $core-font-weights: (
    ...
  ),
  $core-leadings: (
    ...
  )
);
```

---

#### API Functions

The screen API functions allow you to query and pull values from maps. You can also pluralize the function name to pull all values, this can be helpful for when you need to loop through all the values using the `@each` rule.

```bash
font-family()
font-families()

font-size()
font-sizes()

font-weight()
font-weights()

leading()
leadings()
```

```scss
.element {
  font-family: font-family(sans);
  font-size: font-size(6xl);
  font-weight: 700;
  line-height: leading(8);
}

@each $font-size, $font-size-value in font-sizes() {
  // for each font-size, do the following
}
```

---

#### Root Variables

If you are using the basic configuration setup of Uniform, use the following set of root variables to override default values.

<div class="bg-black radius-sm h-25 overflow-auto">
{% highlight css %}
:root {
  --font-sans: sans-serif;
  --font-serif: serif;
  --font-mono: monospace;

  --font-10xl: 4.5rem;
  --font-9xl: 4rem;
  --font-8xl: 3.5rem;
  --font-7xl: 3rem;
  --font-6xl: 2.5rem;
  --font-5xl: 2.25rem;
  --font-4xl: 2rem;
  --font-3xl: 1.75rem;
  --font-2xl: 1.5rem;
  --font-xl: 1.25rem;
  --font-lg: 1.125rem;
  --font-md: 1rem;
  --font-sm: 0.875rem;
  --font-xs: 0.75rem;
  --font-2xs: 0.625rem;

  --leading-1: 1;
  --leading-2: 1.125;
  --leading-3: 1.25;
  --leading-4: 1.375;
  --leading-5: 1.5;
  --leading-6: 1.625;
  --leading-7: 1.75;
  --leading-8: 1.875;
  --leading-9: 2;
  --leading-10: 2.125;
  --leading-11: 2.25;
  --leading-12: 2.375;
  --leading-13: 2.5;

  --tracking-n3: -0.075em;
  --tracking-n2: -0.05em;
  --tracking-n1: -0.025em;
  --tracking-0: 0;
  --tracking-1: 0.025em;
  --tracking-2: 0.05em;
  --tracking-3: 0.075em;
}
{% endhighlight %}
</div>