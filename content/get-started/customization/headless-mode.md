---
title: Headless Mode
date: 1000-01-07
---

{% include shortcodes/chapter, text: 'Customization', color: 'teal' %}

### What is Headless Mode?

When you include and compile the Uniform Sass module, you will automatically include all the CSS properties, theme root variables, and also grant you access to all the theme <a class="hover.underline" href="/get-started/api-functions/" target="_black">API Functions</a>. 

However, there may be a case where you need API Functions **only** or load Uniform as a standalone package without including any CSS properties. This can be achieved by enabling headless mode in your configuration.

As an example, headless mode can be particularly useful in a component-based application framework such as Angular where you may want to load a pre-configured Uniform to a component without having to include all the CSS properties as well.

```scss
// styles.scss
@use "uniform" as * with (
  $headless: true,
);
```

---


### Headless Mode

Enabling headless mode will include Uniform as a standalone module without any root variables or CSS properties. This mode will grant you access to API functions and private functions only.

```scss
// styles.scss
@use "uniform" as * with (
  $headless: true,
);
```

---


### Headless Mode with Root

By default, headless mode will not include any root variables to your stylesheet, to include root variables enable the `$headless-with-root` setting.

```scss
// styles.scss
@use "uniform" as * with (
  $headless: true,
  $headless-with-root: true,
);
```
