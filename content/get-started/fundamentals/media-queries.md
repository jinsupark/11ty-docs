---
title: Media Queries
date: 1000-01-03
---

{% include shortcodes/chapter, text: 'Fundamentals', color: 'blueberry' %}

### Responsive Design

You can apply responsive utility classes by appending the breakpoint variant to the beginning of your class name e.g. `<variant>.keyword-variant`.

<section class="radius-sm bg-silver-100 p-6">
  <div class="bg-black sm.bg-teal-500 md.bg-red-500 lg.bg-blue-500 color-white align-center py-8">
    Adjust your browser to see change
  </div>
</section>

```html
<div class="bg-black sm.bg-teal-500 md.bg-red-500 lg.bg-blue-500">
	Adjust your browser to see change
</div>
```


---

### Mobile-First Design

Uniform uses a mobile-first CSS approach to allow for styles to be displayed correctly on mobile screens first before larger more complex screens styles.

This means is that by **default classes will cascade upwards in screen size** unless specified otherwise. To see this in action, adjust your browser width to see changes.

<section class="flex align-items-center justify-content-center radius-sm bg-silver-100 p-6">
  <div class="color-red-500 sm.color-blue-500 md.color-pink-500 lg.color-green-500 align-center">
    <p>Red on mobile, blue on sm, pink on md, green on lg, green on xl (inherited)</p>
  </div>
</section>

```html
<div class="color-red-500 sm.color-blue-500 md.color-pink-500 lg.color-green-500">
  <p>Red on mobile, blue on sm, pink on md, green on lg, green on xl (inherited)</p>
</div>
```

---

### Breakpoint Variants

By default, there are **four** breakpoint variants available `sm`, `md`, `lg` and `xl` each assigned with the value of common screen sizes. For more information on modifying these variants, please visit the page on <a class="hover.underline" href="/get-started/breakpoints">breakpoints</a>.

```scss
// sm
@media (min-width: 768px) {
  ...
}
// md
@media (min-width: 1024px) {
  ...
}
// lg
@media (min-width: 1280px) {
  ...
}
// xl
@media (min-width: 1536px) {
  ...
}
```


---

### Breakpoint Delimiter

By default, Uniform uses the `.` character to separate the breakpoints and pseudos from the property. You can override the default breakpoint delimiter by defining `$breakpoint-delimiter` in your configuration.

```scss
@use "uniform" as * with (
  $breakpoint-delimiter: '\\.'
);
```

---

### Enabling Responsiveness

By design, Uniform takes common design patterns into consideration and only enables responsiveness to a subset of CSS properties in order to maintain a reasonable file-size.

You can override the default responsive setting by passing the value `true` to `$<property>-responsive` in the configuration.

```scss
@use "uniform" as * with (
  $letter-spacing-responsive: true,
  $list-style-type-responsive: true,
  $text-transform-responsive: true
);
```

> To see which properties are responsive, please visit the <a href="/glossary" class="hover.underline">glossary</a>.


---

### Extending Breakpoints

You can change the number of breakpoints and even change their `min-width` values by passing in your own custom map to the `$screens` variable.

```scss
@use "uniform" as * with (
  $screens: (
    sm: 768px,
    md: 1024px,
    lg: 1280px,
    xl: 1536px,
    custom-breakpoint: 1920px
  )
);
```

---

### Replacing Core Breakpoints

You can replace the breakpoint map entirely by adding key value pairs to the `$core-screens` variable.

```scss
@use "uniform" as * with (
  $core-screens: (
    ... // this will replace all default screen values
  )
);
```

