---
title: Extracting Components
date: 1000-01-06
---

{% include shortcodes/chapter, text: 'Customization', color: 'orange' %}


### Extracting Components

Even though Uniform is a Utility-first CSS framework, it encourages extraction of components as design patterns emerge. Depending on your setup and workflow, Uniform provides multiple ways of extracting components. The following guide will cover the various ways you can extract components.

---

#### Option 1. Use Custom Properties <div class="inline-block ml-2 px-2 py-1 bg-black radius-xs font-2xs font-600 align-middle color-white uppercase tracking-1">Basic</div>

The simplest and easiest way you can extract components is to build your own CSS component using the custom properties that are available to you. This workflow is suitable for users who are using the pre-packaged CSS or CDN version of Uniform (basic coniguration).

```css
// stylesheet.css

.card {
  display: block;
  padding: var(--size-6);
  background: var(--white);
  box-shadow: var(--shadow-1);
  border-radius: var(--radius-md);
}
.card:hover {
  box-shadow: var(shadow-3);
}
```
---

#### Option 2. Use API Functions <div class="inline-block ml-2 px-2 py-1 bg-pink-400 radius-xs font-2xs font-600 align-middle color-white uppercase tracking-1">Native</div>

Similarly to **option 1**, if you are using the native configuration setup of Uniform you can build your own components using <a class="hover.underline" href="/get-started/api-functions">API functions</a>.

```scss
// stylesheet.scss

.card {
  display: block;
  padding: size(6);
  background: fill(white);
  box-shadow: shadow(1);
  border-radius: radius(md);

  &:hover {
    box-shadow: var(shadow-3);
  }
}
```

---

#### Option 3. Use Sass @extend <div class="inline-block ml-2 px-2 py-1 bg-pink-400 radius-xs font-2xs font-600 align-middle color-white uppercase tracking-1">Native</div>

You can also extract components by utilizing the Sass `@extend` rule. This method is particularly useful when you want to simply copy and paste the html class list without having to write CSS properties from scratch.

```scss
// stylesheet.scss

.card {
  @extend .block, .p-6, .bg-white, .shadow-1, .hover\.shadow-3;
}
```

