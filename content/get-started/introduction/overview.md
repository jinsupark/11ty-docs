---
title: Overview
date: 1000-01-01
---

{% include shortcodes/chapter, text: 'Introduction', color: 'blue' %}

### The Sassy Utility-First Framework  🎉

First of all, thank you for taking the time to check out this project. Uniform CSS is the worlds first fully customizable utility-first CSS framework built entirely with Sass. One of its biggest strength is that it is super easy to learn and can be implemented in both pre-packaged or native way making it super adaptable to a wide range of workflows.

---

{% include shortcodes/video, id: 'GUQqC8abh6Y' %}

---

### How Uniform CSS is different

Here are the **top reasons** why Uniform could be a great fit for your next project! 🚀

<div class="mb-10"></div>

<h4><span class="w-6 h-6 mr-2 inline-flex align-items-center justify-content-center font-sm font-700 leading-none bg-blue-500 color-white radius-round">1</span> It's built entirely in Sass</h4>

Built entirely in Sass (the most well known CSS preprocessor currently out there). Adding Uniform into your existing project is **literally a single line of code**.

```scss
@use "uniform" as *;
```

<div class="mb-10"></div>

<h4><span class="w-6 h-6 mr-2 inline-flex align-items-center justify-content-center font-sm font-600 leading-none bg-blue-500 leading-1 color-white radius-round">2</span> It's super-duper easy to configure</h4>

Extend colors, replace breakpoints, change property names, add prefixes, modify syntax, and more! **You can optionally configure almost every tiny detail**.

```scss
@use "uniform" as * with (
  $important: true,
  $prefix: myProject,
  $colors: (
    custom-color-1: red,
    custom-color-2: blue
  ),
  ...
);
```

<div class="mb-10"></div>

<h4><span class="w-6 h-6 mr-2 inline-flex align-items-center justify-content-center font-sm font-600 leading-none bg-blue-500 leading-1 color-white radius-round">3</span> It's easy to add new properties</h4>

As new CSS properties become more widely supported by browsers, you don't have to wait for Uniform to support it, customize, remove or simply add your own!

```scss
// uniform/_index.scss
@forward "extension/custom-property-1";
@forward "extension/custom-property-2";
@forward "extension/that-shiny-new-property";
```

<div class="mb-10"></div>

<h4><span class="w-6 h-6 mr-2 inline-flex align-items-center justify-content-center font-sm font-600 leading-none bg-blue-500 leading-1 color-white radius-round">4</span> Comes with built-in theme APIs</h4>

Need a theme value for that one-off component you need to build? Uniform provides internal API functions to help you access your theme values directly.

```scss
.element {
  padding: size(4);
  background-color: fill(gray-200);
}
```

<div class="mb-10"></div>

<h4><span class="w-6 h-6 mr-2 inline-flex align-items-center justify-content-center font-sm font-600 leading-none bg-blue-500 leading-1 color-white radius-round">5</span> Built with CSS Variables in mind</h4>

Prefer to not worry about preprocessors and just start building pages? Just add the pre-packaged CSS version of Uniform and customize fonts, colors, sizes, and more by simply overriding each native CSS variable. It's that easy.

```css
:root {
  --font-family-sans: 'custom-font', sans-serif;
  --btn-radius: 6px;
}
```

<div class="mb-10"></div>

<h4><span class="w-6 h-6 mr-2 inline-flex align-items-center justify-content-center font-sm font-600 leading-none bg-blue-500 leading-1 color-white radius-round">6</span> Comes with pre-built common components</h4>

To help you save time, Uniform CSS comes with **optional** pre-built components for common UI elements such as buttons and form elements. These can all be enabled, disabled, and even customized down to the last pixel.

```scss
@use "uniform/core" as * with (
  $include-button-module: true,
  $include-form-module: true,
  $include-table-module: false,
  $include-wrapper-module: true
);

:root {
  --btn-radius: 0;
  --input-radius: 0;
}
```

<div class="mb-10"></div>

<h4><span class="w-6 h-6 mr-2 inline-flex align-items-center justify-content-center font-sm font-600 leading-none bg-blue-500 leading-1 color-white radius-round">7</span> Each property follow a strict naming convention</h4>

Every property name and its variants follow a strict and scalable convention to ensure they are as future-proof as they can be.

```scss
$core-variants: (
  auto: auto,
  100p: 100%,
  100vw: 100vw,
  px: 1px,
  2px: 2px,
  3px: 3px,
  ...
);
```

<div class="mb-10"></div>

<h4><span class="w-6 h-6 mr-2 inline-flex align-items-center justify-content-center font-sm font-600 leading-none bg-blue-500 leading-1 color-white radius-round">8</span> Lightweight in Size</h4>

Uniform only activates responsiveness and pseudo variants to certain properties to ensure file-size is kept to a minimal. Optionally, you can choose to activate these variants directly through your main sass file.