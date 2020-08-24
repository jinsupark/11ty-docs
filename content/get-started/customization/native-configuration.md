---
title: Native Configuration
date: 1000-01-02
---

{% include shortcodes/chapter, text: 'Customization', color: 'red' %}

### Setup for Maximum Flexibility

Native Uniform configuration workflow provides full customization features that go beyond what a basic setup may provide. The native configuration setup requires the Sass version of Uniform and its PostCSS dependencies. For more information on setting up Uniform natively, check out <a class="hover.underline" href="/get-started/installation">installation</a>.

```scss
// styles.scss
@use "uniform" as * with (
  // settings here
);
```

---

### Variable Types

There are two types of variables in Uniform, **Global** and **Local**. Global variables are used across all the properties, whereas Local variables can be set on a per property basis.

---

#### Build Setting Variables <div class="inline-block ml-2 px-2 py-1 bg-black radius-xs font-2xs font-600 align-middle color-white uppercase tracking-1">Global</div>

Build setting variables deal with controlling how the Uniform build should be handled.

```scss
// default values
@use "uniform" as * with (
  $important: false,
  $prefix: '',
  $delimiter: '-',
  $child-delimiter: '__',
  $pseudo-delimiter: '\\.',
  $screen-delimiter: '\\.',
  $responsive-pseudos: false,
  $variablize: true,
  $headless: false,
  $headless-with-root: false,
  $debugger: false,
);
```

---

#### Include Variables <div class="inline-block ml-2 px-2 py-1 bg-black radius-xs font-2xs font-600 align-middle color-white uppercase tracking-1">Global</div>

Include variables deal with controlling which reset, starter or modules should be included in the build process.

```scss
@use "uniform" as * with (
  $include-reset-styles: true,
  $include-starter-styles: true,
  $include-button-module: true,
  $include-form-module: true,
  $include-table-module: true,
  $include-wrapper-module: true,
);
```

---

#### Theme Variables <div class="inline-block ml-2 px-2 py-1 bg-black radius-xs font-2xs font-600 align-middle color-white uppercase tracking-1">Global</div>

Theme variables are theme specific maps such as breakpoints, colors, and spacing that is used across multiple CSS properties. For more about theme variables, visit the **theme section**.

```scss
@use "uniform" as * with (
  $colors: (
    custom-red: red,
    custom-blue: blue
  ),
  $screens: (
    sm: 768px,
    md: 1024px,
    lg: 1280px
  ),
  $font-sizes: (
    extra-large: 72px
  )
)
```

---

### Local Variables <div class="inline-block ml-2 px-2 py-1 bg-black radius-xs font-2xs font-600 align-middle color-white uppercase tracking-1">Local</div>

Unlike Global variables, each CSS property has Locally scoped variables that control how that particular property is handled. For more information on configuring CSS properties, check out <a class="hover.underline" href="/get-started/customizing-properties">customizing-properties</a>.

```scss
@use "uniform" as * with (
  $background-color-keyword: bg,
  $background-color-responsive: true,
  $background-color-responsive-pseudos: false,
  $background-color-properties: (background-color),
  $background-color-core-variants: (core.colors()),
  $background-color-variants: (),
  $background-color-pseudos: (hover, focus, active, group-hover),
);
```
