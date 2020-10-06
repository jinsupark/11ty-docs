---
title: Wrapper
date: 1000-01-04
---

{% include shortcodes/chapter, text: 'Modules', color: 'red' %}

### Wrapper Module

The Wrapper module is an optional pre-built component that provides `max-width` set containerization to your page layout.

```html
<div class="wrapper">
  ...
</div>
```

<div class="mb-10"></div>

#### Wrapper root variables

To customize the wrapper module, override the following root variables.

<div class="bg-black radius-sm overflow-auto">
{% highlight css %}
/* styles.css */
:root {
  --wrapper-padding: ...;
  --wrapper-max-width: ...;
  --wrapper-xs-max-width: ...;
  --wrapper-sm-max-width: ...;
  --wrapper-md-max-width: ...;
  --wrapper-lg-max-width: ...;
  --wrapper-xl-max-width: ...;
}
{% endhighlight %}
</div>

---

### How to Disable this Module

By default, all modules are enabled. To disable this module, set the `$include-wrapper-module` variable to `false` in your module configuration.

```scss
@use "uniform" as * with (
  $include-wrapper-module: false
);
```
