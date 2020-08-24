---
title: Shadows
date: 1000-01-04
---

{% include shortcodes/chapter, text: 'Theming', color: 'violet' %}

### Shadow Variant Chart

By default, Uniform provides 5 levels of shadows. Use the following chart as the reference for the `box-shadow` property.

<table class="table">
  <thead class="uppercase font-xs font-600 tracking-1 color-black">
    <tr>
      <th>
        Variant
      </th>
      <th>
        Preview
      </th>
    </tr>
  </thead>
  <tbody class="font-sm">
    <tr>
      <td><code class="color-teal-500">shadow-1</code></td>
      <td>
        <div class="shadow-1 w-8 h-8"></div>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">shadow-2</code></td>
      <td>
        <div class="shadow-2 w-8 h-8"></div>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">shadow-3</code></td>
      <td>
        <div class="shadow-3 w-8 h-8"></div>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">shadow-4</code></td>
      <td>
        <div class="shadow-4 w-8 h-8"></div>
      </td>
    </tr>
    <tr>
      <td><code class="color-teal-500">shadow-5</code></td>
      <td>
        <div class="shadow-5 w-8 h-8"></div>
      </td>
    </tr>
  </tbody>
</table>

---

### Basic Usage

The following example showcases how the variants can be applied.

<section class="radius-sm bg-silver-100 p-6">
  <div class="w-100p p-5 bg-white align-center shadow-2">
    This container has a large shadow
  </div>
</section>

```html
<div class="w-100p p-5 bg-white align-center shadow-2">
	This container has a large shadow
</div>
```

---

#### Extending Core Variants

You can extend the core effects by adding key value pairs to the `$effects` map.

```scss
@use "uniform" as * with (
  $effects: (
    custom-effect: (0 1px 4px 0 rgba(0, 0, 0, 0.5))
  )
);
```

---

#### Replacing Core Variants

You can replace default variants entirely by adding key value pairs to the `$core-shadows` map.

```scss
@use "uniform" as * with (
  $core-shadows: (
    ...
  )
);
```

---

#### API Functions

The color API functions allow you to query and pull values from maps. You can also pluralize the function name to pull all values, this can be helpful for when you need to loop through all the values using the `@each` rule.

```bash
shadow()
shadows()
```

```scss
.element {
  box-shadow: shadow(md);
}

@each $shadow, $shadow-value in shadows() {
  // for each effect, do the following
}
```

---

#### Root Variables

If you are using the basic configuration setup of Uniform, use the following set of root variables to override default values.

<div class="bg-black radius-sm">
{% highlight css %}
:root {
  --shadow-1: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
  --shadow-2: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);
  --shadow-3: 0 10px 20px rgba(0, 0, 0, 0.19), 0 6px 6px rgba(0, 0, 0, 0.23);
  --shadow-4: 0 14px 28px rgba(0, 0, 0, 0.25), 0 10px 10px rgba(0, 0, 0, 0.22);
  --shadow-5: 0 19px 38px rgba(0, 0, 0, 0.3), 0 15px 12px rgba(0, 0, 0, 0.22);
}
{% endhighlight %}
</div>