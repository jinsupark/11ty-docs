---
title: Breakpoints
date: 1000-01-01
---

### Breakpoint Variant Chart

Use the following chart as the reference for any breakpoint related property.

<table>
  <thead>
    <tr>
      <th>
        Variant
      </th>
      <th>
        Value
      </th>
    </tr>
  </thead>
  <tbody>
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
        <code class="color-gray-600">1440px</code>
      </td>
    </tr>
  </tbody>
</table>

---

### Basic Usage

The following example showcases how the variants can be applied.

<section class="radius-lg bg-gray-100 p-6">
  <div class="bg-black sm.bg-gray-1000 md.bg-red-500 lg.bg-blue-500 color-white align-center p-4">
    Adjust your browser width to see the background change
  </div>
</section>

```html
<div class="bg-black sm.bg-gray-1000 md.bg-red-500 lg.bg-blue-500 color-white align-center p-4">
	Adjust your browser width to see the background change
</div>
```

---

### Extending Core Variants

You can extend the core breakpoints by adding key value pairs to the `$breakpoints` map.

```scss
@use "uniform" as * with (
  $breakpoints: (
    xs: 640px
  )
);
```

---

### Replacing Core Variants

You can replace the core breakpoints by adding key value pairs to the `$core-breakpoints` map.

```scss
@use "uniform" as * with (
  $core-breakpoints: (
    ...
  )
);
```

---

### API Functions

The color API functions allow you to query and pull values from maps. You can also pluralize the function name to pull all values, this can be helpful for when you need to loop through all the values using the `@each` rule.

```bash
screen()
breakpoints()
```

```scss
.element {
  border-breakpoint: screen(md);
}

@each $breakpoint, $breakpoint-value in breakpoints() {
  // for each breakpoint, do the following
}
```
