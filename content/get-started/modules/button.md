---
title: Button
date: 1000-01-01
---

### Button Module

Button is an optional module that can be enabled in your configuration.

<section class="radius-lg bg-gray-100 p-6">
  <button class="btn">Button</button>
</section>

```html
<button class="btn">Button</button>
```

---

### Button Fills

There are four types of button fills available, `primary` is the default.

<section class="radius-lg bg-white border-px border-gray-200 p-6">
  <button class="btn btn-primary">Button</button>
  <button class="btn btn-secondary">Button</button>
  <button class="btn btn-tertiary">Button</button>
  <button class="btn btn-ghost">Button</button>
  <button class="btn btn-danger">Button</button>
</section>

```html
<button class="btn btn-primary">Button</button>
<button class="btn btn-secondary">Button</button>
<button class="btn btn-tertiary">Button</button>
<button class="btn btn-ghost">Button</button>
<button class="btn btn-danger">Button</button>
```

---

### Button Sizes

Buttons come in three sizes.

<section class="radius-lg bg-gray-100 p-6">
  <button class="btn btn-sm">Button</button>
  <button class="btn btn-md">Button</button>
  <button class="btn btn-lg">Button</button>
</section>

```html
<button class="btn btn-sm">Button</button>
<button class="btn btn-md">Button</button>
<button class="btn btn-lg">Button</button>
```

---

### Responsive Button Sizes

Button sizes can change based on breakpoint

<section class="radius-lg bg-gray-100 p-6">
  <button class="btn btn-lg sm.btn-md">Button</button>
</section>

```html
<button class="btn btn-lg sm.btn-md">Button</button>
```

---

### Button Groups

Buttons can be combined by wrapping with `btns` assigned container. Buttons can also have an `is-active` state.

<section class="radius-lg bg-gray-100 p-6">
  <div class="btns">
    <button class="btn">1</button>
    <button class="btn is-active">2</button>
    <button class="btn">3</button>
  </div>
</section>

```html
<div class="btns">
	<button class="btn">1</button>
	<button class="btn is-active">2</button>
	<button class="btn">3</button>
</div>
```

---

### How to Enable this Module

By default, all modules are disabled. To enable this button module, set the `$include-button-module` variable to `true`.

```scss
@use "uniform" as * with (
  $include-button-module: true
);
```
