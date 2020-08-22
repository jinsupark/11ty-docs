---
title: Transitions
date: 1000-01-01
---

### Transition Variant Chart

Use the following chart as the reference for the `transition` property.

<table>
  <thead>
    <tr>
      <th class="w-3-12">
        Variant
      </th>
      <th>
        Value
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code class="color-teal-500">all-slow</code></td>
      <td><code class="color-gray-600">all 0.4s</code></td>
    </tr>
    <tr>
      <td><code class="color-teal-500">all-steady</code></td>
      <td><code class="color-gray-600">all 0.2s</code></td>
    </tr>
    <tr>
      <td><code class="color-teal-500">all-fast</code></td>
      <td><code class="color-gray-600">all 0.1s</code></td>
    </tr>
    <tr>
      <td><code class="color-teal-500">visuals-slow</code></td>
      <td><code class="color-gray-600">background-color 0.4s, border-color 0.4s, color 0.4s, fill 0.4s, stroke 0.4s, opacity 0.4s, box-shadow 0.4s, transform 0.4s</code></td>
    </tr>
    <tr>
      <td><code class="color-teal-500">visuals-steady</code></td>
      <td><code class="color-gray-600">background-color 0.2s, border-color 0.2s, color 0.2s, fill 0.2s, stroke 0.2s, opacity 0.2s, box-shadow 0.2s, transform 0.2s</code></td>
    </tr>
    <tr>
      <td><code class="color-teal-500">visuals-fast</code></td>
      <td><code class="color-gray-600">background-color 0.1s, border-color 0.1s, color 0.1s, fill 0.1s, stroke 0.1s, opacity 0.1s, box-shadow 0.1s, transform 0.1s</code></td>
    </tr>
  </tbody>
</table>

---

### Basic Usage

The following example showcases how the variant can be applied.

<section class="radius-lg bg-gray-100 p-6">
  <div class="bg-black hover.bg-blue-500 transition-visuals-slow radius-md p-4 color-white align-center cursor-pointer">
    Hover me
  </div>
</section>

```html
<div class="bg-black hover.bg-blue-500 transition-visuals-slow">
	Hover me
</div>
```

---

### Extending Core Variants

You can extend the core transitions by adding key value pairs to the `$transitions` map.

```scss
@use "uniform" as * with (
  $transitions: (
    all-extra-slow: all 2s,
  )
);
```

---

### Replacing Core Variants

You can replace the core transitions by adding key value pairs to the `$core-transitions` map.

```scss
@use "uniform" as * with (
  $core-transitions: (
    ...
  )
);
```

---

### API Functions

The transition API function allows you to query and pull values from the transition map. You can also pluralize the function name to pull all values, this can be helpful for when you need to loop through all the values using the `@each` rule.

```bash
transition()
transitions()
```

```scss
.element {
  transition: 200ms;
}

@each $transition, $transition-value in transitions() {
  // for each transition, do the following
}
```
