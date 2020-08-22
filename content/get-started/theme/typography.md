---
title: Typography
date: 1000-01-01
---

### Font Family Chart

Use the following chart as the reference for the `font-family` property. Each font family also has fall-back options set.

<table>
  <thead>
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
  <tbody>
    <tr>
      <td>sans</td>
      <td>system-ui</td>
      <td class="font-sans">
        Hello World
      </td>
    </tr>
    <tr>
      <td>serif</td>
      <td>Georgia</td>
      <td class="font-serif">
        Hello World
      </td>
    </tr>
    <tr>
      <td>mono</td>
      <td>Menlo</td>
      <td class="font-mono">
        Hello World
      </td>
    </tr>
  </tbody>
</table>

---

### Font Weight Chart

Use the following chart as the reference for the `font-weight` property.

<table>
  <thead>
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
  <tbody>
    <tr>
      <td>light</td>
      <td>300</td>
      <td class="font-light">
        Hello World
      </td>
    </tr>
    <tr>
      <td>regular</td>
      <td>400</td>
      <td class="font-400">
        Hello World
      </td>
    </tr>
    <tr>
      <td>medium</td>
      <td>500</td>
      <td class="font-500">
        Hello World
      </td>
    </tr>
    <tr>
      <td>semibold</td>
      <td>600</td>
      <td class="font-600">
        Hello World
      </td>
    </tr>
    <tr>
      <td>bold</td>
      <td>700</td>
      <td class="font-700">
        Hello World
      </td>
    </tr>
  </tbody>
</table>

---

### Font Size Chart

Use the following chart as the reference for the `font-size` property.

<table>
  <thead>
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
  <tbody>
    <tr>
      <td>h1</td>
      <td>56px</td>
      <td class="font-h1">
        Hello World
      </td>
    </tr>
    <tr>
      <td>h2</td>
      <td>48px</td>
      <td class="font-h2">
        Hello World
      </td>
    </tr>
    <tr>
      <td>h3</td>
      <td>36px</td>
      <td class="font-5xl">
        Hello World
      </td>
    </tr>
    <tr>
      <td>h4</td>
      <td>28px</td>
      <td class="font-4xl">
        Hello World
      </td>
    </tr>
    <tr>
      <td>h5</td>
      <td>24px</td>
      <td class="font-h5">
        Hello World
      </td>
    </tr>
    <tr>
      <td>h6</td>
      <td>22px</td>
      <td class="font-2xl">
        Hello World
      </td>
    </tr>
    <tr>
      <td>large</td>
      <td>18px</td>
      <td class="font-large">
        Hello World
      </td>
    </tr>
    <tr>
      <td>body</td>
      <td>16px</td>
      <td class="font-md">
        Hello World
      </td>
    </tr>
    <tr>
      <td>small</td>
      <td>14px</td>
      <td class="font-small">
        Hello World
      </td>
    </tr>
    <tr>
      <td>micro</td>
      <td>12px</td>
      <td class="font-xs">
        Hello World
      </td>
    </tr>
  </tbody>
</table>

---

### Line-Height Chart

Use the following chart as the reference for the `line-height` property.

<table>
  <thead>
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
  <tbody>
    <tr>
      <td>none</td>
      <td>1</td>
      <td class="leading-none">
        Line 1<br>
        Line 2<br>
        Line 3
      </td>
    </tr>
    <tr>
      <td>tighter</td>
      <td>1.25</td>
      <td class="leading-tighter">
        Line 1<br>
        Line 2<br>
        Line 3
      </td>
    </tr>
    <tr>
      <td>tight</td>
      <td>1.375</td>
      <td class="leading-tight">
        Line 1<br>
        Line 2<br>
        Line 3
      </td>
    </tr>
    <tr>
      <td>normal</td>
      <td>1.5</td>
      <td class="leading-normal">
        Line 1<br>
        Line 2<br>
        Line 3
      </td>
    </tr>
    <tr>
      <td>loose</td>
      <td>1.625</td>
      <td class="leading-loose">
        Line 1<br>
        Line 2<br>
        Line 3
      </td>
    </tr>
    <tr>
      <td>looser</td>
      <td>2</td>
      <td class="leading-looser">
        Line 1<br>
        Line 2<br>
        Line 3
      </td>
    </tr>
  </tbody>
</table>

---

### Basic Usage

The following example showcases how the variants can be applied.

<section class="radius-lg bg-gray-100 p-6 flex justify-content-center gap-x-sm">
  <div class="bg-white shadow-3 p-4 font-h5 md.font-2xl font-700 leading-none align-center">
    Hello World
  </div>
</section>

```html
<div class="bg-white shadow-3 p-4 font-h5 md.font-2xl font-700 leading-none align-center">
	Hello World
</div>
```

---

### Extending Core Variants

You can extend the various typographical maps.

```scss
@use "uniform" as * with (
  $font-families: (
    custom-font: Helvetica
  ),
  $font-sizes: (
    hero: 72px,
    hero-lg: 100px
  ),
  $font-weights: (
    thin: 200
  ),
  $line-heights: (
    tall: 3
  )
);
```

---

### Replacing Core Variants

You can replace the various typographical maps.

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
  $core-line-heights: (
    ...
  )
);
```

---

### API Functions

The color API functions allow you to query and pull values from maps. You can also pluralize the function name to pull all values, this can be helpful for when you need to loop through all the values using the `@each` rule.

```bash
font-family()
font-families()

font-size()
font-sizes()

font-weight()
font-weights()

line-height()
line-heights()
```

```scss
.element {
  font-family: font-family(sans);
  font-size: font-size(h1);
  font-weight: 700;
  line-height: line-height(snug);
}

@each $font-size, $font-size-value in font-sizes() {
  // for each font-size, do the following
}
```
