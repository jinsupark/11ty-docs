---
title: Breakpoints
date: 1000-01-01
---

{% include shortcodes/chapter, text: 'Theming', color: 'blue' %}

### Breakpoint Variant Chart

By default, Uniform provides **4 breakpoints** for any responsive properties. Use the following chart as the reference for any breakpoint related property.

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
      <td><code class="color-teal-500">sm</code></td>
      <td>
        <code class="color-gray-600">768px</code>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">md</code></td>
      <td>
        <code class="color-gray-600">1024px</code>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">lg</code></td>
      <td>
        <code class="color-gray-600">1280px</code>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">xl</code></td>
      <td>
        <code class="color-gray-600">1536px</code>
      </td>
    </tr>
  </tbody>
</table>

---

### Basic Usage

The following example showcases how the variants can be applied.

<section class="radius-sm bg-silver-100 p-6">
  <div class="bg-black sm.bg-teal-500 md.bg-red-500 lg.bg-blue-500 color-white align-center py-8">
    Adjust your browser to see change
  </div>
</section>

```html
<div class="bg-black sm.bg-teal-500 md.bg-red-500 lg.bg-blue-500">
	Adjust your browser to see change
</div>
```

---

#### Extending Core Variants

You can extend the core breakpoints by adding key value pairs to the `$screens` map. Note, if you pass in a key that already exists, the original will be overwritten with the latest variant.

```scss
@use "uniform" as * with (
  $screens: (
    xs: 640px
  )
);
```

---

#### Replacing Core Variants

You can replace the default variants entirely by adding key value pairs to the `$core-screens` map.

```scss
@use "uniform" as * with (
  $core-screens: (
    ...
  )
);
```

---

#### API Functions

The screen API functions allow you to query and pull values from maps. You can also pluralize the function name to pull all values, this can be helpful for when you need to loop through all the values using the `@each` rule.

```bash
screen()
screens()
```

```scss
.element {
  max-width: screen(md);
}

@each $screen, $screen-value in screens() {
  // for each breakpoint, do the following
}
```
