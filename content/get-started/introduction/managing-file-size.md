---
title: Managing File Size
date: 1000-01-03
---

{% include shortcodes/chapter, text: 'Introduction', color: 'teal' %}

### Managing File Size

Utility-first frameworks are generally known for their large file-size but Uniform comes in at only **29kb gzipped** and **256kb minified**. Below is a comparison of how Uniform ranks compared to other popular frameworks.

<table class="table">
  <thead class="uppercase font-xs font-600 tracking-1 color-black">
    <tr>
      <th>
        Framework
      </th>
      <th>
        Original Size
      </th>
      <th>
        Minified
      </th>
      <th>
        Gzipped
      </th>
    </tr>
  </thead>
  <tbody class="font-sm">
    <tr>
      <td>Semantic UI</td>
      <td>809.4kb</td>
      <td>613.8kb</td>
      <td>100.6kb</td>
    </tr>
    <tr>
      <td>Tailwind</td>
      <td>783.5kb</td>
      <td>603.3kb</td>
      <td>78.0kb</td>
    </tr>
    <tr>
      <td class="color-blue-500 font-600">Uniform</td>
      <td class="color-blue-500">446kb</td>
      <td class="color-blue-500">302kb</td>
      <td class="color-blue-500">49.3kb</td>
    </tr>
    <tr>
      <td>Bulma</td>
      <td>224.2kb</td>
      <td>189.9kb</td>
      <td>24.9kb</td>
    </tr>
    <tr>
      <td>Bootstrap</td>
      <td>187.8kb</td>
      <td>152.1kb</td>
      <td>22.7kb</td>
    </tr>
    <tr>
      <td>Foundation</td>
      <td>154.1kb</td>
      <td>119.2kb</td>
      <td>15.9kb</td>
    </tr>
  </tbody>
</table>

---

### Tailored Configuration

**Uniform takes a more considered approach** in determining the responsiveness and activation of pseudo variants for each CSS property. 

For example, it makes sense for color properties such as `background-color` to change on hover, however properties such as `flex-wrap` would rarely need to. Also, properties such as `letter-spacing` will not need to be responsive as it would not normally change based on breakpoint.

You can of course, override the default settings and enable responsiveness, and customize variants for any CSS property.

```scss
@use "uniform" as * with (
  $overflow-responsive: false,
  $overflow-pseudos: (
    hover, focus
  ),
  $padding-responsive: true,
  $padding-pseudos: (
    hover, focus, active
  )
)
```

---

### Reducing Size Further

To reduce the file-size of your build even further, you can easily limit the number of variants or even disable unused CSS properties entirely. For more information on customizing your setup, visit the page on <a class="hover.underline" href="/get-started/configuration">configuration</a>.

```scss
// replace core colors

@use "uniform" as * with (
  $core-colors: (
    /* overriding this map will remove and replace core colors
       used across all color related CSS properties */
  )
);
```

```sass
// disable unused css properties in `uniform/_index.scss`

@forward "core/align-content" as align-content-*;
@forward "core/align-items" as align-items-*;
@forward "core/align-self" as align-self-*;
// @forward "core/background-attachment" as background-attachment-*;
@forward "core/background-color" as background-color-*;
// @forward "core/background-position" as background-position-*;
// @forward "core/background-repeat" as background-repeat-*;
// @forward "core/background-size" as background-size-*;
```
