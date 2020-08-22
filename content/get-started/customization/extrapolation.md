---
title: Extrapolation
date: 1000-01-05
---





### Extracting Components

Uniform is a utility-first framework to allow designs to be implemented without over-abstraction of components. However, as patterns emerge, Uniform provides useful API-like Sass functions that you can use to build your own custom components using the same values that are shared across your theme.

For more information on API functions please visit <a class="hover.underline" href="/get-started/api-functions">API Functions</a>

---

### Utilize API Functions

As your project grows and component patterns emerge, you can create custom classes in a native Sass way whilst still being able to pull theme values which helps minimize the chance of introducing one-off variants. All the <a class="hover.underline" href="/get-started/modules">modules</a> in Uniform are built using this API approach. For more information on which API functions are available, please see the theme section.

```scss
@use "uniform" as *;

.custom-component {
  display: block;
  margin-bottom: size(5);
  padding: size(4);
  background: fill(gray-200);
  font-size: font-size(tiny);
  box-shadow: effects(md);
}
```

> It is important to note, only properties where the values can vary greatly such as colors, and spacing units are available in the form of API functions. You are still encouraged to write your own native CSS for basic properties such as `display`.

---

### Replacing Components

If you take a look inside the `uniform` directory you might have noticed that everything is a name folder that contains `_index.scss`. This design is to get around a Sass limitation of being able to optionally replace if a file exists.

For example, if you import an file named `button.scss`, this will take precedence over `button/_index.scss`. Uniform takes advantange of this by providing you the ability to replace modules, default styles, or even utility classes entirely by simply dropping in a `.scss` extension file with the same name.

<section class="radius-lg bg-gray-100 p-6 mb-6">
  <img src="/img/module-directory.png" class="shadow-3 radius-lg">
</section>
