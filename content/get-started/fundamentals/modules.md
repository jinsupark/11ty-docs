---
title: Modules
date: 1000-01-07
---

{% include shortcodes/chapter, text: 'Fundamentals', color: 'blue' %}

### What are Modules?

Modules in Uniform are pre-built components for common UI elements such as buttons, forms, and tables. Uniform provides these modules to help avoid having to build these types of components from scratch.

Out of the box, Uniform includes modules for **buttons**, **responsive tables**, **form elements**, and **wrappers**.


---

### Button Module

The button module come in various types and supports multiple sizes. To learn more about using this module visit the dedicated modules page on <a class="hover.underline" href="/get-started/button/">buttons</a>.

<section class="radius-sm bg-silver-100 p-6 align-center">
  <button class="btn">Button</button>
</section>

```html
<button class="btn">Button</button>
```

**All modules are enabled by default**, to enable this module, pass in the setting `false`, to `$include-button-module` in your configuration.

```scss
@use "uniform" as * with (
  $include-button-module: false
);
```

---

### Form Module

The form module provides styling for basic form elements. To learn more about using this module visit the dedicated modules page on <a class="hover.underline" href="/get-started/form/">form</a>.

<section class="radius-sm bg-silver-100 p-6">
  <form>
    <div class="mb-6 last.mb-0">
      <label class="label mb-2">Email</label>
      <input class="input" placeholder="Email" value="john.titor@apple.com">
    </div>
    <div class="mb-6 last.mb-0">
      <label class="label mb-2">Username</label>
      <input class="input" type="text" placeholder="UniformCSS" value="@UniformCSS">
    </div>
    <div class="mb-6 last.mb-0">
      <label class="checkbox">
        <input type="checkbox" checked required />
        <div class="checkbox__checkmark"></div>
        Checkbox
      </label>
    </div>
    <div class="mb-6 last.mb-0">
      <label class="radio mr-4">
        <input type="radio" name="radio" checked />
        <div class="radio__checkmark"></div>
        Radio
      </label>
      <label class="radio">
        <input type="radio" name="radio" checked />
        <div class="radio__checkmark"></div>
        Radio
      </label>
    </div>
    <div class="mb-6 last.mb-0">
      <label class="toggle">
        <input type="checkbox" checked />
        <div class="toggle__switch"></div>
      </label>
    </div>
    <div class="mb-6 last.mb-0">
      <div class="select">
        <select>
          <option selected>Selected</option>
          <option>Option</option>
          <option>Option</option>
        </select>
        <div class="select__angle"></div>
      </div>
    </div>
  </form>
</section>

```html
<form>
  <div class="mb-6 last.mb-0">
    <label class="label mb-2">Email</label>
    <input class="input" placeholder="Email" value="john.titor@apple.com">
  </div>

  <div class="mb-6 last.mb-0">
    <label class="label mb-2">Username</label>
    <input class="input" type="text" placeholder="UniformCSS" value="@UniformCSS">
  </div>

  <div class="mb-6 last.mb-0">
    <label class="checkbox">
      <input type="checkbox" checked required />
      <div class="checkbox__checkmark"></div>
      Checkbox
    </label>
  </div>

  <div class="mb-6 last.mb-0">
    <label class="radio mr-4">
      <input type="radio" name="radio" checked />
      <div class="radio__checkmark"></div>
      Radio
    </label>
    <label class="radio">
      <input type="radio" name="radio" checked />
      <div class="radio__checkmark"></div>
      Radio
    </label>
  </div>

  <div class="mb-6 last.mb-0">
    <label class="toggle">
      <input type="checkbox" checked />
      <div class="toggle__switch"></div>
    </label>
  </div>

  <div class="mb-6 last.mb-0">
    <div class="select">
      <select>
        <option selected>Selected</option>
        <option>Option</option>
        <option>Option</option>
      </select>
      <div class="select__angle"></div>
    </div>
  </div>
</form>
```

**All modules are enabled by default**, to enable this module, pass in the setting `false`, to `$include-form-module` in your configuration.

```scss
@use "uniform" as * with (
  $include-form-module: false
);
```

---

### Table Module

The table module provides styling for the basic table element. To learn more about using this module visit the dedicated modules page on <a class="hover.underline" href="/get-started/table/">table</a>.

<section class="radius-sm bg-silver-100 p-6">
  <table class="table table-stack sm.table-unstack">
    <thead>
      <tr>
        <th>Column A</th>
        <th>Column B</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td data-table-label="Column A">1</td>
        <td data-table-label="Column B">2</td>
      </tr>
      <tr>
        <td data-table-label="Column A">1</td>
        <td data-table-label="Column B">2</td>
      </tr>
    </tbody>
  </table>
</section>

```html
<table class="table table-stack sm.table-unstack">
  <thead>
    <tr>
      <th>Column A</th>
      <th>Column B</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td data-table-label="Column A">1</td>
      <td data-table-label="Column B">2</td>
    </tr>
    <tr>
      <td data-table-label="Column A">1</td>
      <td data-table-label="Column B">2</td>
    </tr>
  </tbody>
</table>
```

All modules are disabled by default, to enable this module, pass in the value `true`, to `$include-table-module` in your configuration.

```scss
@use "uniform" as * with (
  $include-table-module: true
);
```

---

### Wrapper Module

The wrapper module is a container that provides set of `max-width` properties based on various breakpoints. To learn more about using this module visit the dedicated modules page on <a class="hover.underline" href="/get-started/wrapper/">wrapper</a>.

```html
<div class="wrapper">
  ...
</div>
```

All modules are disabled by default, to enable this module, pass in the value `true`, to `$include-wrapper-module` in your configuration.

```scss
@use "uniform" as * with (
  $include-wrapper-module: true
);
```