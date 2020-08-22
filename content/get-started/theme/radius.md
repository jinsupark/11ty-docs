---
title: Radius
date: 1000-01-01
---

### Radius Variant Chart

Use the following chart as the reference for the `box-shadow` property.

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
      <td><code class="color-teal-500">0</code></td>
      <td><code class="color-gray-600">0</code></td>
      <td>
        <div class="radius-round bg-black w-8 h-8"></div>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">sm</code></td>
      <td><code class="color-gray-600">3px</code></td>
      <td>
        <div class="radius-sm bg-black w-8 h-8"></div>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">md</code></td>
      <td><code class="color-gray-600">4px</code></td>
      <td>
        <div class="radius-md bg-black w-8 h-8"></div>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">lg</code></td>
      <td><code class="color-gray-600">8px</code></td>
      <td>
        <div class="radius-lg bg-black w-8 h-8"></div>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">round</code></td>
      <td><code class="color-gray-600">9999px</code></td>
      <td>
        <div class="radius-round bg-black w-8 h-8"></div>
      </td>
    </tr>
  </tbody>
</table>

---

### Basic Usage

The following example showcases how the variants can be applied.

<section class="radius-lg bg-gray-100 p-6">
  <div class="w-100p p-5 bg-white align-center shadow-3 radius-lg">
    This container has a large radius
  </div>
</section>

```html
<div class="w-100p p-5 bg-white align-center shadow-3 radius-lg">
	This container has a large radius
</div>
```

---

### Extending Core Variants

You can extend the core radius by adding key value pairs to the `$radius` map.

```scss
@use "uniform" as * with (
  $radius: (
    custom-radius: 10px
  )
);
```

---

### Replacing Core Variants

You can replace the core radius by adding key value pairs to the `$core-radius` map.

```scss
@use "uniform" as * with (
  $core-radius: (
    ...
  )
);
```

---

### API Functions

The radius API function allows you to query and pull values from the radius map. You can also pluralize the function name to pull all values, this can be helpful for when you need to loop through all the values using the `@each` rule.

```bash
radius()
radiuses()
```

```scss
.element {
  border-radius: radius(md);
}

@each $radius, $radius-value in radiuses() {
  // for each radius, do the following
}
```
