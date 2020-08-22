---
title: Browser Support
date: 1000-01-04
---

{% include shortcodes/chapter, text: 'Introduction', color: 'purple' %}

### Browser Support

Out of the box, Uniform looks and performs great on all the latest version of modern browsers such as **Chrome**, **Firefox**, **Safari**, and **Edge**. Due to the utility nature of this framework it is easy to only pick and use the CSS properties that are applicable to your audience.

---

### Vendor Prefixes

Uniform provides build scripts that uses the Autoprefixer package to automatically handle vendor prefixes. It uses the the following default browserlist setting (can be overwritten by modifying the npm build scripts).

To learn more about browserlist queries <a class="hover.underline" href="https://github.com/browserslist/browserslist">click here</a>.

```bash
> 0.5%, last 2 versions, Firefox ESR, not dead
```

---

### IE Support

It is important to note that Uniform relies quite heavily on CSS custom properties (CSS variables). This means Uniform styles will not display correctly on all versions of **Internet Explorer**. To get around this by passing the value `false` to `$variablize` in your configuration. Doing this will compile all variables as static values.

```scss
@use "uniform" as * with (
	$variablize: false
);
```