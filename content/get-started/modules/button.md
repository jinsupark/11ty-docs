---
title: Button
date: 1000-01-01
---

{% include shortcodes/chapter, text: 'Modules', color: 'yellow' %}

### Button Module

The Button module is an optional pre-built component that can be useful for handling call-to-actions.

<section class="radius-sm bg-silver-100 p-6 flex flex-wrap justify-content-center">
  <button class="btn">Button</button>
</section>

```html
<button class="btn">Button</button>
```

<div class="mb-10"></div>

#### Button root variables

To customize the look of your button, override the following root variables.

<div class="bg-black radius-sm h-24 overflow-auto">
{% highlight css %}
/* styles.css */
:root {
  --btn-height: ...;
  --btn-padding: ...;
  --btn-bg: ...;
  --btn-border: ...;
  --btn-shadow: ...;
  --btn-radius: ...;
  --btn-font-family: ...;
  --btn-font-size: ...;
  --btn-font-weight: ...;
  --btn-text-transform: ...;
  --btn-tracking: ...;
  --btn-color: ...;
  --btn-transition: ...;

  --btn-hover-bg: ...;
  --btn-hover-color: ...;
  --btn-hover-border: ...;
  --btn-hover-shadow: ...;

  --btn-focus-shadow: ...;

  --btn-active-bg: ...;
  --btn-active-color: ...;
  --btn-active-border: ...;
  --btn-active-shadow: ...;
}
{% endhighlight %}
</div>

---

### Branded Buttons

There are three types of branded button variants available, `primary`, `secondary`, and `tertiary`. These can be further customized to match your brand.

<section class="radius-sm bg-silver-100 p-6 flex flex-wrap justify-content-center">
  <button class="btn btn-primary mr-4">Button</button>
  <button class="btn btn-secondary mr-4">Button</button>
  <button class="btn btn-tertiary">Button</button>
</section>

```html
<button class="btn btn-primary">Button</button>
<button class="btn btn-secondary">Button</button>
<button class="btn btn-tertiary">Button</button>
```

<div class="mb-10"></div>

#### Branded button root variables

To customize the look of your branded buttons, override the following root variables.

<div class="bg-black radius-sm h-24 overflow-auto">
{% highlight css %}
/* styles.css */
:root {
  --btn-primary-bg: ...;
  --btn-primary-color: ...;
  --btn-primary-border: ...;
  --btn-primary-shadow: ...;
  --btn-primary-hover-bg: ...;
  --btn-primary-hover-color: ...;
  --btn-primary-hover-border: ...;
  --btn-primary-hover-shadow: ...;
  --btn-primary-focus-shadow: ...;
  --btn-primary-active-bg: ...;
  --btn-primary-active-color: ...;
  --btn-primary-active-border: ...;
  --btn-primary-active-shadow: ...;

  --btn-secondary-bg: ...;
  --btn-secondary-color: ...;
  --btn-secondary-border: ...;
  --btn-secondary-shadow: ...;
  --btn-secondary-hover-bg: ...;
  --btn-secondary-hover-color: ...;
  --btn-secondary-hover-border: ...;
  --btn-secondary-hover-shadow: ...;
  --btn-secondary-focus-shadow: ...;
  --btn-secondary-active-bg: ...;
  --btn-secondary-active-color: ...;
  --btn-secondary-active-border: ...;
  --btn-secondary-active-shadow: ...;

  --btn-tertiary-bg: ...;
  --btn-tertiary-color: ...;
  --btn-tertiary-border: ...;
  --btn-tertiary-shadow: ...;
  --btn-tertiary-hover-bg: ...;
  --btn-tertiary-hover-color: ...;
  --btn-tertiary-hover-border: ...;
  --btn-tertiary-hover-shadow: ...;
  --btn-tertiary-focus-shadow: ...;
  --btn-tertiary-active-bg: ...;
  --btn-tertiary-active-color: ...;
  --btn-tertiary-active-border: ...;
  --btn-tertiary-active-shadow: ...;
}
{% endhighlight %}
</div>

---

### Light and Dark Buttons

There are two types of `light` and `dark` button variants available.

<section class="radius-sm bg-silver-100 p-6 flex flex-wrap justify-content-center">
  <button class="btn btn-light mr-4">Button</button>
  <button class="btn btn-dark">Button</button>
</section>

```html
<button class="btn btn-light">Button</button>
<button class="btn btn-dark">Button</button>
```

<div class="mb-10"></div>

#### Light and Dark button root variables

To customize the look of your light and dark buttons, override the following root variables.

<div class="bg-black radius-sm h-24 overflow-auto">
{% highlight css %}
/* styles.css */
:root {
  --btn-light-bg: ...;
  --btn-light-color: ...;
  --btn-light-border: ...;
  --btn-light-shadow: ...;
  --btn-light-hover-bg: ...;
  --btn-light-hover-color: ...;
  --btn-light-hover-border: ...;
  --btn-light-hover-shadow: ...;
  --btn-light-focus-shadow: ...;
  --btn-light-active-bg: ...;
  --btn-light-active-color: ...;
  --btn-light-active-border: ...;
  --btn-light-active-shadow: ...;

  --btn-dark-bg: ...;
  --btn-dark-color: ...;
  --btn-dark-border: ...;
  --btn-dark-shadow: ...;
  --btn-dark-hover-bg: ...;
  --btn-dark-hover-color: ...;
  --btn-dark-hover-border: ...;
  --btn-dark-hover-shadow: ...;
  --btn-dark-focus-shadow: ...;
  --btn-dark-active-bg: ...;
  --btn-dark-active-color: ...;
  --btn-dark-active-border: ...;
  --btn-dark-active-shadow: ...;
}
{% endhighlight %}
</div>

---

### State Buttons

There are three types of state buttons to handle `success`, `warning`, and `danger`.

<section class="radius-sm bg-silver-100 p-6 flex flex-wrap justify-content-center">
  <button class="btn btn-success mr-4">Button</button>
  <button class="btn btn-warning mr-4">Button</button>
  <button class="btn btn-danger">Button</button>
</section>

```html
<button class="btn btn-success">Button</button>
<button class="btn btn-warning">Button</button>
<button class="btn btn-danger">Button</button>
```

<div class="mb-10"></div>

#### State button root variables

To customize the look of your state buttons, override the following root variables.

<div class="bg-black radius-sm h-24 overflow-auto">
{% highlight css %}
/* styles.css */
:root {
  --btn-success-bg: ...;
  --btn-success-color: ...;
  --btn-success-border: ...;
  --btn-success-shadow: ...;
  --btn-success-hover-bg: ...;
  --btn-success-hover-color: ...;
  --btn-success-hover-border: ...;
  --btn-success-hover-shadow: ...;
  --btn-success-focus-shadow: ...;
  --btn-success-active-bg: ...;
  --btn-success-active-color: ...;
  --btn-success-active-border: ...;
  --btn-success-active-shadow: ...;

  --btn-warning-bg: ...;
  --btn-warning-color: ...;
  --btn-warning-border: ...;
  --btn-warning-shadow: ...;
  --btn-warning-hover-bg: ...;
  --btn-warning-hover-color: ...;
  --btn-warning-hover-border: ...;
  --btn-warning-hover-shadow: ...;
  --btn-warning-focus-shadow: ...;
  --btn-warning-active-bg: ...;
  --btn-warning-active-color: ...;
  --btn-warning-active-border: ...;
  --btn-warning-active-shadow: ...;

  --btn-danger-bg: ...;
  --btn-danger-color: ...;
  --btn-danger-border: ...;
  --btn-danger-shadow: ...;
  --btn-danger-hover-bg: ...;
  --btn-danger-hover-color: ...;
  --btn-danger-hover-border: ...;
  --btn-danger-hover-shadow: ...;
  --btn-danger-focus-shadow: ...;
  --btn-danger-active-bg: ...;
  --btn-danger-active-color: ...;
  --btn-danger-active-border: ...;
  --btn-danger-active-shadow: ...;
}
{% endhighlight %}
</div>


---

### Outline Buttons

You can create outline buttons by appending `btn-outline`.

<section class="radius-sm bg-silver-100 p-6 flex flex-wrap justify-content-center">
  <button class="btn btn-outline">Button</button>
</section>

```html
<button class="btn btn-outline">Button</button>
```

<div class="mb-10"></div>

#### Outline button root variables

To customize the look of your outline buttons, override the following root variables.

<div class="bg-black radius-sm h-24 overflow-auto">
{% highlight css %}
/* styles.css */
:root {
  --btn-outline-bg: ...;
  --btn-outline-color: ...;
  --btn-outline-border: ...;
  --btn-outline-shadow: ...;
  --btn-outline-hover-bg: ...;
  --btn-outline-hover-color: ...;
  --btn-outline-hover-border: ...;
  --btn-outline-hover-shadow: ...;
  --btn-outline-focus-shadow: ...;
  --btn-outline-active-bg: ...;
  --btn-outline-active-color: ...;
  --btn-outline-active-border: ...;
  --btn-outline-active-shadow: ...;
}
{% endhighlight %}
</div>

---

### Button Sizes

Three are **5** button sizes to choose from.

<section class="radius-sm bg-silver-100 p-6 flex flex-wrap align-items-center justify-content-center">
  <button class="btn btn-xs mr-4">Button</button>
  <button class="btn btn-sm mr-4">Button</button>
  <button class="btn btn-md mr-4">Button</button>
  <button class="btn btn-lg mr-4">Button</button>
  <button class="btn btn-xl">Button</button>
</section>

```html
<button class="btn btn-xs">Button</button>
<button class="btn btn-sm">Button</button>
<button class="btn btn-md">Button</button>
<button class="btn btn-lg">Button</button>
<button class="btn btn-xl">Button</button>
```

<div class="mb-10"></div>

#### Button size root variables

To customize the sizes of your buttons, override the following root variables.

<div class="bg-black radius-sm h-24 overflow-auto">
{% highlight css %}
/* styles.css */
:root {
  --btn-xs-height: ...;
  --btn-xs-padding: ...;
  --btn-xs-font-size: ...;

  --btn-sm-height: ...;
  --btn-sm-padding: ...;
  --btn-sm-font-size: ...;

  --btn-md-height: ...;
  --btn-md-padding: ...;
  --btn-md-font-size: ...;

  --btn-lg-height: ...;
  --btn-lg-padding: ...;
  --btn-lg-font-size: ...;

  --btn-xl-height: ...;
  --btn-xl-padding: ...;
  --btn-xl-font-size: ...;
}
{% endhighlight %}
</div>

---

### Responsive Button Sizes

Button sizes can change based on breakpoint

<section class="radius-sm bg-silver-100 p-6 flex flex-wrap align-items-center justify-content-center">
  <button class="btn btn-sm md.btn-lg lg.btn-xl">Button</button>
</section>

```html
<button class="btn btn-sm md.btn-lg lg.btn-xl">Button</button>
```

---

### Button Groups

Buttons can be combined by wrapping them with a `btns` class assigned container. Buttons can also have an `is-active` state.

<section class="radius-sm bg-silver-100 p-6 flex flex-wrap align-items-center justify-content-center">
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

### Loading Buttons

Buttons can have loading animation by appending `is-loading`.

<section class="radius-sm bg-silver-100 p-6 flex flex-wrap align-items-center justify-content-center">
  <button class="btn is-loading">Loading</button>
</section>

```html
<div class="btns">
  <button class="btn is-loading">Loading</button>
</div>
```

---

### How to disable this Module

By default, all modules are enabled. To disable this button module, set the `$include-button-module` variable to `false` in your module configuration.

```scss
@use "uniform" as * with (
  $include-button-module: false
);
```
