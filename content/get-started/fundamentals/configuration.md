---
title: Configuration
date: 1000-01-01
---

{% include shortcodes/chapter, text: 'Fundamentals', color: 'pink' %}

### Customizing Uniform

There are **two ways** you can customize Uniform to fit your project needs, **Basic** and **Native**. The Basic way to configure Uniform is to simply apply CSS variable overrides inside the `:root` pseudo element. The native method requires a native Sass implementation and overrides are performed in the form of a <a class="hover.underline" href="https://sass-lang.com/documentation/at-rules/use#configuration">module configuration</a>.

---

{% include shortcodes/video, id: 'tLqqi5gyxQg' %}

---

### Basic Configuration 🍼

The basic configuration method is the easiest way to customize and get started with Uniform. This method only allows you to customize basic attributes such as **fonts**, **colors**, and **sizes** etc. It does not however, allow you to perform more deeper customizations such as apply a prefix or enable/disable the important tag etc. 

Lets assume you have included a pre-packaged CDN version of Uniform into your project. To apply basic configuration, simply apply CSS variable overrides inside a `:root` pseudo element.

```css
:root {
  --font-sans: 'Open Sans', Helvetica, Arial, Sans-Serif;
  --red-500: #FF4242;
  --btn-radius: 4px;
}
```

---

### Native Configuration 😎

The native configuration method is the best way to take full advantage of Uniform's customization features. You can customize almost every aspect of this framework using the new and awesome <a class="hover.underline" href="https://sass-lang.com/documentation/at-rules/use#configuration">module configuration</a> method.

To apply native configuration, pass-through Sass variable overrides to the Uniform module in your Sass stylesheet.

```scss
// styles.scss
@use "uniform" as * with (
  $prefix: myPrefix-,
  $important: true,
  $colors: (
    juicy-color: #F3F5FA,
  ),
  ...
);
```

```css
/* styles.css */
.myPrefix-bg-juicy-color: {
  background-color: #F3F5FA !important;
}
...
```
