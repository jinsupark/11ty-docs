---
title: Radius
date: 1000-01-03
---

{% include shortcodes/chapter, text: 'Theming', color: 'cyan' %}

### Radius Variant Chart

By default, Uniform provides **5 border radiuses** . Use the following chart as the reference for any `border-radius` related property.

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
      <td><code class="color-teal-500">xs</code></td>
      <td><code class="color-gray-600">4px</code></td>
      <td>
        <div class="radius-sm bg-black w-12 h-12"></div>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">sm</code></td>
      <td><code class="color-gray-600">8px</code></td>
      <td>
        <div class="radius-sm bg-black w-12 h-12"></div>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">md</code></td>
      <td><code class="color-gray-600">12px</code></td>
      <td>
        <div class="radius-md bg-black w-12 h-12"></div>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">lg</code></td>
      <td><code class="color-gray-600">16px</code></td>
      <td>
        <div class="radius-lg bg-black w-12 h-12"></div>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">xl</code></td>
      <td><code class="color-gray-600">20px</code></td>
      <td>
        <div class="radius-lg bg-black w-12 h-12"></div>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">round</code></td>
      <td><code class="color-gray-600">9999px</code></td>
      <td>
        <div class="radius-round bg-black w-12 h-12"></div>
      </td>
    </tr>
  </tbody>
</table>

---

### Basic Usage

The following example showcases how the variants can be applied.

<section class="radius-sm bg-silver-100 p-6">
  <div class="w-100p p-5 bg-white align-center shadow-3 radius-lg">
    This container has a large radius
  </div>
</section>

```html
<div class="radius-lg">
	This container has a large radius
</div>
```

---

#### Extending Core Variants

You can extend the core radius by adding key value pairs to the `$radius` map.

```scss
@use "uniform" as * with (
  $radius: (
    custom: 10px
  )
);
```

```css
/* styles.css */
.radius-custom {
  border-radius: 10px;
}
```

---

#### Replacing Core Variants

You can replace the default variants entirely by adding key value pairs to the `$core-radius` map.

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

---

#### Root Variables

If you are using the basic configuration setup of Uniform, use the following set of root variables to override default values.

<div class="bg-black radius-sm h-25 overflow-auto">
{% highlight css %}
:root {
  --radius-xs: 0.25rem;
  --radius-sm: 0.5rem;
  --radius-md: 0.75rem;
  --radius-lg: 1rem;
  --radius-xl: 1.25rem;
  --radius-round: 9999px;
}
{% endhighlight %}
</div>