---
title: Default Styles
date: 1000-01-05
---

{% include shortcodes/chapter, text: 'Fundamentals', color: 'red' %}

### Reset Styles

By default, Uniform applies minimal resetting styles to flatten browser inconsistencies and to provide a clean foundation to build utility classes on. 

**Here are the main points worth noting:**

- All elements have no default `margin` or `padding`.
- All elements have a default border style applied to make it easier to apply borders.
- Body has a default `line-height` of 1.
- All media elements are set to `display: block`.

```css
/* Reset everything */
*,*::before,*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  border: 0 solid var(--default-border-color, fill(silver-200));
  font: inherit;
  color: inherit;
}

/* Prevent iOS font size change */
html {
  -webkit-text-size-adjust: 100%;
}

/* Reset body line-height */
body {
  line-height: 1;
}

/* All media elements set to block */
img,svg,video,canvas,audio,iframe,embed,object {
  display: block;
  width: 100%;
  vertical-align: middle;
}

/* Collapse table */
table {
  border-collapse: collapse;
  border-spacing: 0;
}

/* Remove list style */
ol,ul {
  list-style: none;
}
```

---

### Disabling Reset Styles

If you prefer to rock your own reset or normalization, you can disable the inclusion of Uniform reset styles by setting `$include-reset-styles` to `false` in your configuration. 

```scss
@use "uniform" as * with (
	$include-reset-styles: false
);
```

---

### Starter Styles

By default, Uniform applies very basic styling to common typographical elements such as `line-height` and `margin-bottom` properties for paragraph and heading elements.

```scss
h1,h2,h3,h4,h5,h6 {
  line-height: var(--heading-leading, leading(3));
  margin-bottom: var(--heading-margin, 0.5em);
  color: var(--heading-color, black);
  &:last-child {
    margin-bottom: 0;
  }
}

p {
  line-height: var(--paragraph-leading, leading(8));
  margin-bottom: var(--paragraph-margin, 1.5em);
  color: var(--paragraph-color, fill(gray-500));
  &:last-child {
    margin-bottom: 0;
  }
}

a {
  cursor: pointer;
  transition: var(--anchor-transition, 200ms);
  text-decoration: none;
}

b,strong {
  font-weight: var(--bold-font-weight, 700);
}

sub,sup {
  position: relative;
  font-size: .75em;
}

sub {
  bottom: -0.25em;
  left: 0.25em;
}

sup {
  top: -0.5em;
  left: 0.25em;
}

pre,code {
  font-family: font-family(mono);
}
```

---

### Disabling Starter Styles

If you prefer to exclude starter styles from your build, simply set `$include-starter-styles` to `false` in your configuration. 

```scss
@use "uniform" as * with (
	$include-starter-styles: false
);
```
