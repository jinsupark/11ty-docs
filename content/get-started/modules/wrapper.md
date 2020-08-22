---
title: Wrapper
date: 1000-01-01
---

### Wrapper Module

Wrapper is an optional module that provides set of `max-width` properties based on various breakpoints. This module is useful for design layouts that have a fixed width.

<table>
  <thead>
    <tr>
      <th>
        Breakpoint
      </th>
      <th>
        Property
      </th>
      <th>
        Padding Applied
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <code class="color-teal-500">sm</code>
      </td>
      <td>
        <code>max-width: 768px</code>
      </td>
      <td>
        <code class="color-gray-600">1.5rem</code>
      </td>
    </tr>
    <tr>
      <td>
        <code class="color-teal-500">md</code>
      </td>
      <td>
        <code>max-width: 1024px</code>
      </td>
      <td>
        <code class="color-gray-600">1.5rem</code>
      </td>
    </tr>
    <tr>
      <td>
        <code class="color-teal-500">lg</code>
      </td>
      <td>
        <code>max-width: 1280px</code>
      </td>
      <td>
        <code class="color-gray-600">5rem</code>
      </td>
    </tr>
    <tr>
      <td>
        <code class="color-teal-500">xl</code>
      </td>
      <td>
        <code>max-width: 1440px</code>
      </td>
      <td>
        <code class="color-gray-600">0</code>
      </td>
    </tr>
  </tbody>
</table>

```html
<div class="wrapper">
  ...
</div>
```

---

### How to Enable this Module

By default, all modules are disabled. To enable this wrapper module, set the `$include-wrapper-module` variable to `true`.

```scss
@use "uniform" as * with (
  $include-wrapper-module: true
);
```