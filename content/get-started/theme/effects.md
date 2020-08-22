---
title: Effects
date: 1000-01-01
---

### Effect Variant Chart

Use the following chart as the reference for the `box-shadow` property.

<table>
  <thead>
    <tr>
      <th>
        Variant
      </th>
      <th>
        Preview
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code class="color-teal-500">none</code></td>
      <td>
        <div class="shadow-none w-8 h-8"></div>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">sm</code></td>
      <td>
        <div class="shadow-1 w-8 h-8"></div>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">md</code></td>
      <td>
        <div class="shadow-1 w-8 h-8"></div>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">lg</code></td>
      <td>
        <div class="shadow-3 w-8 h-8"></div>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">focus</code></td>
      <td>
        <div class="shadow-focus w-8 h-8"></div>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">valid</code></td>
      <td>
        <div class="shadow-valid w-8 h-8"></div>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">error</code></td>
      <td>
        <div class="shadow-error w-8 h-8"></div>
      </td>
    </tr>
  </tbody>
</table>

---

### Basic Usage

The following example showcases how the variants can be applied.

<section class="radius-lg bg-gray-100 p-6">
  <div class="w-100p p-5 bg-white align-center shadow-3">
    This container has a large shadow
  </div>
</section>

```html
<div class="w-100p p-5 bg-white align-center shadow-3">
	This container has a large shadow
</div>
```

---

### Extending Core Variants

You can extend the core effects by adding key value pairs to the `$effects` map.

```scss
@use "uniform" as * with (
  $effects: (
    custom-effect: (0 1px 4px 0 rgba(0, 0, 0, 0.5))
  )
);
```

---

### Replacing Core Variants

You can replace the core effects by adding key value pairs to the `$core-effects` map.

```scss
@use "uniform" as * with (
  $core-effects: (
    ...
  )
);
```

---

### API Functions

The color API functions allow you to query and pull values from maps. You can also pluralize the function name to pull all values, this can be helpful for when you need to loop through all the values using the `@each` rule.

```bash
effect()
effects()
```

```scss
.element {
  box-shadow: effect(md);
}

@each $effect, $effect-value in effects() {
  // for each effect, do the following
}
```
