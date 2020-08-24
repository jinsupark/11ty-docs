---
title: Table
date: 1000-01-03
---

{% include shortcodes/chapter, text: 'Modules', color: 'violet' %}

### Table Module

The Table module is an optional pre-built component that provides customizable styling for tables. This module also provides tables with the ability to become responsive.

<section class="radius-sm bg-silver-100 p-6">
  <table class="table">
    <thead>
      <tr>
        <th>Column A</th>
        <th>Column B</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>1</td>
        <td>2</td>
      </tr>
      <tr>
        <td>1</td>
        <td>2</td>
      </tr>
    </tbody>
  </table>
</section>

```html
<table class="table">
  <thead>
    <tr>
      <th>Column A</th>
      <th>Column B</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <td>1</td>
      <td>2</td>
    </tr>
  </tbody>
</table>
```

<div class="mb-10"></div>

#### Table root variables

To customize the look of your table, override the following root variables.

<div class="bg-black radius-sm overflow-auto">
{% highlight css %}
/* styles.css */
:root {
  --table-border: ...;
  --table-radius: ...;
  --table-shadow: ...;
  --table-bg: ...;

  --table-th-height: ...;
  --table-th-padding: ...;

  --table-td-height: ...;
  --table-td-padding: ...;
}
{% endhighlight %}
</div>

---

### Responsive Tables

Tables can become responsive at various breakpoints by adding the `table-stack` and `table-unstack` classes. You can also add the `data-table-label` attribute to allow for labels when table columns are stacked.

<section class="radius-sm bg-silver-100 p-6">
  <table class="table table-stack md.table-unstack">
    <thead>
      <tr>
        <th>Column A</th>
        <th>Column B</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Resize your browser</td>
        <td data-table-label="Column B">Resize your browser</td>
      </tr>
      <tr>
        <td data-table-label="Column A">Resize your browser</td>
        <td data-table-label="Column B">Resize your browser</td>
      </tr>
    </tbody>
  </table>
</section>

```html
<table class="table table-stack md.table-unstack">
  <thead>
    <tr>
      <th>Column A</th>
      <th>Column B</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Resize your browser</td>
      <td data-table-label="Column B">Resize your browser</td>
    </tr>
    <tr>
      <td data-table-label="Column A">Resize your browser</td>
      <td data-table-label="Column B">Resize your browser</td>
    </tr>
  </tbody>
</table>
```


<div class="mb-10"></div>

#### Responsive table root variables

To customize the look of your table, override the following root variables.

<div class="bg-black radius-sm overflow-auto">
{% highlight css %}
/* styles.css */
:root {
  --table-stack-margin: ...;

  --table-label-margin: ...;
  --table-label-font-size: ...;
  --table-label-font-weight: ...;
  --table-label-text-transform: ...;
  --table-label-tracking: ...;
  --table-label-color: ...;
}
{% endhighlight %}
</div>

---

### Alternating Tables

Table rows can also feature alternating rows with the `table-alt` class.

<section class="radius-sm bg-silver-100 p-6">
  <table class="table table-alt">
    <thead>
      <tr>
        <th>Column A</th>
        <th>Column B</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>1</td>
        <td>2</td>
      </tr>
      <tr>
        <td>1</td>
        <td>2</td>
      </tr>
      <tr>
        <td>1</td>
        <td>2</td>
      </tr>
      <tr>
        <td>1</td>
        <td>2</td>
      </tr>
      <tr>
        <td>1</td>
        <td>2</td>
      </tr>
    </tbody>
  </table>
</section>

```html
<table class="table">
  <thead>
    <tr>
      <th>Column A</th>
      <th>Column B</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <td>1</td>
      <td>2</td>
    </tr>
  </tbody>
</table>
```

<div class="mb-10"></div>

#### Alternating table variables

To customize the look of your alternating table, override the following root variables.

<div class="bg-black radius-sm overflow-auto">
{% highlight css %}
/* styles.css */
:root {
  --table-alt-bg: ...;
}
{% endhighlight %}
</div>

---

### How to Disable this Module

By default, all modules are enabled. To disable this module, set the `$include-table-module` variable to `false` in your module configuration.

```scss
@use "uniform" as * with (
  $include-table-module: false
);
```
