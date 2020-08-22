---
title: Sizes
date: 1000-01-01
---

### Size Variant Chart

Uniform features 21 sizing units to handle various size and spacing related properties such as `heights` and `margins`.

Each size also has an negative equivalent. You can access the negative variants by appending `n` to the beginning of each variant e.g. `n10` would be the negative equivalent of the `10` size variant.

<div class="shadow-1 w-100p overflow-auto">
  <table class="shadow-none">
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
      <tr><td>0</td><td>0</td><td><div class="h-4 w-0 bg-gray-300"></div></td></tr>
      <tr><td>1</td><td>4px</td><td><div class="h-4 w-1 bg-gray-300"></div></td></tr>
      <tr><td>2</td><td>8px</td><td><div class="h-4 w-2 bg-gray-300"></div></td></tr>
      <tr><td>3</td><td>12px</td><td><div class="h-4 w-3 bg-gray-300"></div></td></tr>
      <tr><td>4</td><td>16px</td><td><div class="h-4 w-4 bg-gray-300"></div></td></tr>
      <tr><td>5</td><td>20px</td><td><div class="h-4 w-5 bg-gray-300"></div></td></tr>
      <tr><td>6</td><td>24px</td><td><div class="h-4 w-6 bg-gray-300"></div></td></tr>
      <tr><td>7</td><td>32px</td><td><div class="h-4 w-7 bg-gray-300"></div></td></tr>
      <tr><td>8</td><td>40px</td><td><div class="h-4 w-8 bg-gray-300"></div></td></tr>
      <tr><td>9</td><td>48px</td><td><div class="h-4 w-9 bg-gray-300"></div></td></tr>
      <tr><td>10</td><td>64px</td><td><div class="h-4 w-10 bg-gray-300"></div></td></tr>
      <tr><td>11</td><td>80px</td><td><div class="h-4 w-11 bg-gray-300"></div></td></tr>
      <tr><td>12</td><td>96px</td><td><div class="h-4 w-12 bg-gray-300"></div></td></tr>
      <tr><td>13</td><td>128px</td><td><div class="h-4 w-13 bg-gray-300"></div></td></tr>
      <tr><td>14</td><td>160px</td><td><div class="h-4 w-14 bg-gray-300"></div></td></tr>
      <tr><td>15</td><td>192px</td><td><div class="h-4 w-15 bg-gray-300"></div></td></tr>
      <tr><td>16</td><td>256px</td><td><div class="h-4 w-16 bg-gray-300"></div></td></tr>
      <tr><td>17</td><td>320px</td><td><div class="h-4 w-17 bg-gray-300"></div></td></tr>
      <tr><td>18</td><td>384px</td><td><div class="h-4 w-18 bg-gray-300"></div></td></tr>
      <tr><td>19</td><td>512px</td><td><div class="h-4 w-19 bg-gray-300"></div></td></tr>
      <tr><td>20</td><td>640px</td><td><div class="h-4 w-20 bg-gray-300"></div></td></tr>
      <tr><td>21</td><td>768px</td><td><div class="h-4 w-21 bg-gray-300"></div></td></tr>
    </tbody>
  </table>
</div>

---

### Basic Usage

The following example showcases how the variants can be applied.

<section class="radius-lg bg-gray-100 p-6 flex justify-content-center gap-x-sm">
  <div class="bg-black w-8 h-8 radius-round">
  </div>
  <div class="bg-black w-10 h-10 radius-round">
  </div>
  <div class="bg-black w-12 h-12 radius-round">
  </div>
</section>

```html
<div class="bg-black w-8 h-8 radius-round"></div>
<div class="bg-black w-10 h-10 radius-round"></div>
<div class="bg-black w-12 h-12 radius-round"></div>
```

You can also apply negative sizes by appending `n` to the beginning of your variant e.g. `w-n10 h-n10` etc

---

### Extending Core Variants

There are two types of size maps that can be extended. The `$positive-sizes` map contains positive size values, and the `$negative-sizes` map contain negative values.

```scss
@use "uniform" as * with (
  $positive-sizes: (
    22: 1000px
  ),
  $negative-sizes: (
    n22: -1000px
  )
);
```

---

### Replacing Core Variants

You can replace the core sizes by adding key value pairs to the `$core-sizes` map.

```scss
@use "uniform" as * with (
  $core-positive-sizes: (
    ...
  ),
  $core-negative-sizes (
    ...
  )
);
```

---

### API Functions

The color API functions allow you to query and pull values from maps. You can also pluralize the function name to pull all values, this can be helpful for when you need to loop through all the values using the `@each` rule.

```bash
positive-size()
positive-sizes()
negative-size()
negative-sizes()
size()
sizes()
```

```scss
.element {
  padding: size(5);
}

@each $size, $size-value in sizes() {
  // for each size, do the following
}
```

---

### Querying Multiple Sizes

Unlike other API Functions the `sizes()` function can query multiple sizes. This is particulary useful for shorthand properties such as `margin` or `padding`.

```scss
// INPUT
.element {
  padding: size(5, 6, 7, 8);
}

// OUTPUT
.element {
  padding: 1.25rem 1.5rem 2rem 2.5rem;
}
```
