---
title: Build Settings
date: 1000-01-03
---

{% include shortcodes/chapter, text: 'Customization', color: 'yellow' %}

### Further Build Settings

Uniform provides build settings to provide extra control over your properties.

```scss
// styles.scss
@use "uniform" as * with (
  $important: true,
  $prefix: 'myPrefix-'
  // chain as many variable overrides as you like here
);
```

```css
/* styles.css */
.myPrefix-block {display: block !important;}
.myPrefix-inline {display: inline !important;}
...
```


---


### Core Build Settings

Uniform provides build settings to provide extra control over your properties.

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

<div class="mb-10"></div>

<table class="table leading-7">
  <thead class="uppercase font-xs font-600 tracking-1 color-black">
    <tr>
      <th>
        Setting
      </th>
      <th>
        Description
      </th>
    </tr>
  </thead>
  <tbody class="font-sm">
    <tr>
      <td class="font-xs md.font-sm color-teal-700 align-top whitespace-no-wrap"><code>$important</code></td>
      <td>Adds the <code class="color-blue-500">!important</code> tag at the end of all classes.</td>
    </tr>
    <tr>
      <td class="font-xs md.font-sm color-teal-700 align-top whitespace-no-wrap"><code>$prefix</code></td>
      <td>Adds a prefix at the beginning of all classes.</td>
    </tr>
    <tr>
      <td class="font-xs md.font-sm color-teal-700 align-top whitespace-no-wrap"><code>$delimiter</code></td>
      <td>Defines the characters that separates variants.</td>
    </tr>
    <tr>
      <td class="font-xs md.font-sm color-teal-700 align-top whitespace-no-wrap"><code>$child-delimiter</code></td>
      <td>Defines the characters that separates block and elements featured in modules.</td>
    </tr>
    <tr>
      <td class="font-xs md.font-sm color-teal-700 align-top whitespace-no-wrap"><code>$pseudo-delimiter</code></td>
      <td>Defines the characters that separates pseudo variants with property.</td>
    </tr>
    <tr>
      <td class="font-xs md.font-sm color-teal-700 align-top whitespace-no-wrap"><code>$screen-delimiter</code></td>
      <td>Defines the characters that separates breakpoint variants with property.</td>
    </tr>
    <tr>
      <td class="font-xs md.font-sm color-teal-700 align-top whitespace-no-wrap"><code>$responsive-pseudos</code></td>
      <td>When enabled, if property is responsive then pseudo variants also become responsive.</td>
    </tr>
    <tr>
      <td class="font-xs md.font-sm color-teal-700 align-top whitespace-no-wrap"><code>$variablize</code></td>
      <td>If disabled, all custom properties will be converted to static values.</td>
    </tr>
    <tr>
      <td class="font-xs md.font-sm color-teal-700 align-top whitespace-no-wrap"><code>$headless</code></td>
      <td>When enabled, Uniform will load in Headless mode.</td>
    </tr>
    <tr>
      <td class="font-xs md.font-sm color-teal-700 align-top whitespace-no-wrap"><code>$headless-with-root</code></td>
      <td>When enabled, Uniform will load in Headless mode with custom properties.</td>
    </tr>
    <tr>
      <td class="font-xs md.font-sm color-teal-700 align-top whitespace-no-wrap"><code>$debugger</code></td>
      <td>When enabled, Uniform will enable all properties with all pseudos and responsiveness enabled (for debugging purposes only).</td>
    </tr>
  </tbody>
</table>

