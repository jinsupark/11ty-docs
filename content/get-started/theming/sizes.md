---
title: Sizes
date: 1000-01-05
---

{% include shortcodes/chapter, text: 'Theming', color: 'pink' %}

### Size Variant Chart

Uniform provides 27 sizing units for size and spacing related properties such as `heights` and `margins`.

Each size also has an negative equivalent. You can access the negative variants by appending `n` to the beginning of each variant e.g. `n10`.

<div class="shadow-1 h-25 radius-sm overflow-hidden overflow-y-auto">
<table class="table table-colors shadow-none radius-0 relative">
  <thead class="uppercase font-xs font-600 tracking-1 color-black">
    <tr>
      <th class="sticky bg-white t-npx">
        Scale
      </th>
      <th class="sticky bg-white t-npx align-right">
        Pixel
      </th>
      <th class="sticky bg-white t-npx align-right">
        Rem
      </th>
    </tr>
  </thead>
  <tbody class="font-sm">
    <tr><td>1</td><td class="color-teal-700 align-right">4px</td><td class="color-gray-200 align-right">0.25rem</td>
    <tr><td>2</td><td class="color-teal-700 align-right">8px</td><td class="color-gray-200 align-right">0.5rem</td>
    <tr><td>3</td><td class="color-teal-700 align-right">12px</td><td class="color-gray-200 align-right">0.75rem</td>
    <tr><td>4</td><td class="color-teal-700 align-right">16px</td><td class="color-gray-200 align-right">1rem</td>
    <tr><td>5</td><td class="color-teal-700 align-right">20px</td><td class="color-gray-200 align-right">1.25rem</td>
    <tr><td>6</td><td class="color-teal-700 align-right">24px</td><td class="color-gray-200 align-right">1.5rem</td>
    <tr><td>7</td><td class="color-teal-700 align-right">28px</td><td class="color-gray-200 align-right">1.75rem</td>
    <tr><td>8</td><td class="color-teal-700 align-right">32px</td><td class="color-gray-200 align-right">2rem</td>
    <tr><td>9</td><td class="color-teal-700 align-right">36px</td><td class="color-gray-200 align-right">2.25rem</td>
    <tr><td>10</td><td class="color-teal-700 align-right">40px</td><td class="color-gray-200 align-right">2.5rem</td>
    <tr><td>11</td><td class="color-teal-700 align-right">44px</td><td class="color-gray-200 align-right">2.75rem</td>
    <tr><td>12</td><td class="color-teal-700 align-right">48px</td><td class="color-gray-200 align-right">3rem</td>
    <tr><td>13</td><td class="color-teal-700 align-right">56px</td><td class="color-gray-200 align-right">3.5rem</td>
    <tr><td>14</td><td class="color-teal-700 align-right">64px</td><td class="color-gray-200 align-right">4rem</td>
    <tr><td>15</td><td class="color-teal-700 align-right">72px</td><td class="color-gray-200 align-right">4.5rem</td>
    <tr><td>16</td><td class="color-teal-700 align-right">80px</td><td class="color-gray-200 align-right">5rem</td>
    <tr><td>17</td><td class="color-teal-700 align-right">88px</td><td class="color-gray-200 align-right">5.5rem</td>
    <tr><td>18</td><td class="color-teal-700 align-right">96px</td><td class="color-gray-200 align-right">6rem</td>
    <tr><td>19</td><td class="color-teal-700 align-right">128px</td><td class="color-gray-200 align-right">8rem</td>
    <tr><td>20</td><td class="color-teal-700 align-right">160px</td><td class="color-gray-200 align-right">10rem</td>
    <tr><td>21</td><td class="color-teal-700 align-right">192px</td><td class="color-gray-200 align-right">12rem</td>
    <tr><td>22</td><td class="color-teal-700 align-right">256px</td><td class="color-gray-200 align-right">16rem</td>
    <tr><td>23</td><td class="color-teal-700 align-right">320px</td><td class="color-gray-200 align-right">20rem</td>
    <tr><td>24</td><td class="color-teal-700 align-right">384px</td><td class="color-gray-200 align-right">24rem</td>
    <tr><td>25</td><td class="color-teal-700 align-right">512px</td><td class="color-gray-200 align-right">32rem</td>
    <tr><td>26</td><td class="color-teal-700 align-right">640px</td><td class="color-gray-200 align-right">40rem</td>
    <tr><td>27</td><td class="color-teal-700 align-right">768px</td><td class="color-gray-200 align-right">48rem</td>
    <tr><td>screen-xs</td><td class="color-teal-700 align-right">896px</td><td class="color-gray-200 align-right">56rem</td>
    <tr><td>screen-sm</td><td class="color-teal-700 align-right">1024px</td><td class="color-gray-200 align-right">64rem</td>
    <tr><td>screen-md</td><td class="color-teal-700 align-right">1152px</td><td class="color-gray-200 align-right">72rem</td>
    <tr><td>screen-lg</td><td class="color-teal-700 align-right">1280px</td><td class="color-gray-200 align-right">80rem</td>
    <tr><td>screen-xl</td><td class="color-teal-700 align-right">1536px</td><td class="color-gray-200 align-right">96rem</td>
  </tbody>
</table>
</div>

---

### Basic Usage

The following example showcases how the variants can be applied. You can also apply negative sizes by appending `n` to the beginning of your variant e.g. `w-n10 h-n10` etc.

<section class="radius-sm bg-silver-100 p-6 flex">
  <div class="flex align-items-center justify-content-center bg-black color-white font-600 w-8 h-8 radius-round mr-6">
    8
  </div>
  <div class="flex align-items-center justify-content-center bg-black color-white font-600 w-10 h-10 radius-round mr-6">
    10
  </div>
  <div class="flex align-items-center justify-content-center bg-black color-white font-600 w-12 h-12 radius-round">
    12
  </div>
</section>

```html
<div class="w-8 h-8"></div>
<div class="w-10 h-10"></div>
<div class="w-12 h-12"></div>
```

---

#### Extending Core Variants

There are two types of size maps that can be extended. The `$positive-sizes` map contains positive size values, and the `$negative-sizes` map contain negative values. You can extend each of these variant sets by adding key value pairs to each map.

```scss
@use "uniform" as * with (
  $positive-sizes: (
    31: 1600px
  ),
  $negative-sizes: (
    n31: -1600px
  )
);
```

```css
/* styles.css */
.h-31 {
  height: 1600px;
}
.h-n31 {
  height: -1600px;
}
```

---

#### Replacing Core Variants

You can replace the core sizes by adding key value pairs to the `$core-positive-sizes` or `$core-negative-sizes` map.

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

#### API Functions

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

#### Querying Multiple Sizes

Unlike other API Functions the `sizes()` function can query multiple sizes. This is particulary useful for shorthand properties such as `margin` or `padding`.

```scss
// INPUT
.element {
  padding: size(5, 6, 7, 8);
}

// OUTPUT
.element {
  padding: 1.25rem 1.5rem 1.75rem 2rem;
}
```

---

#### Root Variables

If you are using the basic configuration setup of Uniform, use the following set of root variables to override default values.

<div class="bg-black radius-sm h-25 overflow-auto">
{% highlight css %}
:root {
  --size-0: 0;
  --size-1: 0.25rem;
  --size-2: 0.5rem;
  --size-3: 0.75rem;
  --size-4: 1rem;
  --size-5: 1.25rem;
  --size-6: 1.5rem;
  --size-7: 1.75rem;
  --size-8: 2rem;
  --size-9: 2.25rem;
  --size-10: 2.5rem;
  --size-11: 2.75rem;
  --size-12: 3rem;
  --size-13: 3.5rem;
  --size-14: 4rem;
  --size-15: 4.5rem;
  --size-16: 5rem;
  --size-17: 5.5rem;
  --size-18: 6rem;
  --size-19: 8rem;
  --size-20: 10rem;
  --size-21: 12rem;
  --size-22: 16rem;
  --size-23: 20rem;
  --size-24: 24rem;
  --size-25: 32rem;
  --size-26: 40rem;
  --size-27: 48rem;
  --size-n1: -0.25rem;
  --size-n2: -0.5rem;
  --size-n3: -0.75rem;
  --size-n4: -1rem;
  --size-n5: -1.25rem;
  --size-n6: -1.5rem;
  --size-n7: -1.75rem;
  --size-n8: -2rem;
  --size-n9: -2.25rem;
  --size-n10: -2.5rem;
  --size-n11: -2.75rem;
  --size-n12: -3rem;
  --size-n13: -3.5rem;
  --size-n14: -4rem;
  --size-n15: -4.5rem;
  --size-n16: -5rem;
  --size-n17: -5.5rem;
  --size-n18: -6rem;
  --size-n19: -8rem;
  --size-n20: -10rem;
  --size-n21: -12rem;
  --size-n22: -16rem;
  --size-n23: -20rem;
  --size-n24: -24rem;
  --size-n25: -32rem;
  --size-n26: -40rem;
  --size-n27: -48rem;
}
{% endhighlight %}
</div>