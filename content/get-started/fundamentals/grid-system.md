---
title: Grid System
date: 1000-01-06
---

{% include shortcodes/chapter, text: 'Fundamentals', color: 'cyan' %}

### Getting started with Grid

Unlike more traditional grid systems, Uniform grid systems are built using the `grid` display type and designed to support between `1` to `12` columns.

<section class="radius-sm bg-silver-100 p-6">
  <div class="grid grid-cols-2 mb-4">
    <div class="h-8 bg-gray-300">
    </div>
    <div class="h-8 bg-gray-100">
    </div>
  </div>

  <div class="grid grid-cols-3 mb-4">
    <div class="h-8 bg-gray-300">
    </div>
    <div class="h-8 bg-gray-100">
    </div>
    <div class="h-8 bg-gray-300">
    </div>
  </div>

  <div class="grid grid-cols-4">
    <div class="h-8 bg-gray-100">
    </div>
    <div class="h-8 bg-gray-300">
    </div>
    <div class="h-8 bg-gray-100">
    </div>
    <div class="h-8 bg-gray-300">
    </div>
  </div>
</section>

```html
<div class="grid grid-cols-2">
  <div>...</div>
  <div>...</div>
</div>

<div class="grid grid-cols-3">
  <div>...</div>
  <div>...</div>
  <div>...</div>
</div>

<div class="grid grid-cols-4">
  <div>...</div>
  <div>...</div>
  <div>...</div>
  <div>...</div>
</div>
```

---

### Gutters

You can create gutters by combining your grid layout with the `gap-<size>` property.

<section class="radius-sm bg-silver-100 p-6">
  <div class="grid grid-cols-3 gap-4 mb-4">
    <div class="h-8 bg-gray-300">
    </div>
    <div class="h-8 bg-gray-100">
    </div>
    <div class="h-8 bg-gray-300">
    </div>
  </div>

  <div class="grid grid-cols-3 gap-8 mb-4">
    <div class="h-8 bg-gray-300">
    </div>
    <div class="h-8 bg-gray-100">
    </div>
    <div class="h-8 bg-gray-300">
    </div>
  </div>

  <div class="grid grid-cols-3 gap-12 mb-4">
    <div class="h-8 bg-gray-300">
    </div>
    <div class="h-8 bg-gray-100">
    </div>
    <div class="h-8 bg-gray-300">
    </div>
  </div>

  <div class="grid grid-cols-3 gap-16 mb-4">
    <div class="h-8 bg-gray-300">
    </div>
    <div class="h-8 bg-gray-100">
    </div>
    <div class="h-8 bg-gray-300">
    </div>
  </div>

  <div class="grid grid-cols-3 gap-18">
    <div class="h-8 bg-gray-300">
    </div>
    <div class="h-8 bg-gray-100">
    </div>
    <div class="h-8 bg-gray-300">
    </div>
  </div>
</section>

```html
<div class="grid grid-cols-3 gap-4">
	...
</div>

<div class="grid grid-cols-3 gap-8">
	...
</div>

<div class="grid grid-cols-3 gap-12">
	...
</div>

<div class="grid grid-cols-3 gap-16">
	...
</div>

<div class="grid grid-cols-3 gap-18">
	...
</div>
```

---

### Responsive Gutters

Gutters can be responsive by prefixing the `gap-<size>` property with the breakpoint variant. For more information on media queries, <a class="hover.underline" href="/get-started/media-queries">click here</a>. 

<section class="radius-sm bg-silver-100 p-6">
  <div class="grid grid-cols-3 gap-4 sm.gap-6 md.gap-8 lg.gap-12">
    <div class="h-8 bg-gray-300">
    </div>
    <div class="h-8 bg-gray-100">
    </div>
    <div class="h-8 bg-gray-300">
    </div>
  </div>
</section>

```html
<div class="grid grid-cols-3 gap-4 sm.gap-6 md.gap-8 lg.gap-12">
	...
</div>
```

---

### Columns

You can control the size of each column by specifying its column span count.

<section class="radius-sm bg-silver-100 p-6">
  <div class="grid grid-cols-5">
    <div class="h-8 bg-gray-100 col-1">
    </div>
    <div class="h-8 bg-gray-300 col-3">
    </div>
    <div class="h-8 bg-gray-100 col-1">
    </div>
  </div>
</section>

```html
<div class="grid grid-cols-5">
	<div class="col-1">...</div>
	<div class="col-3">...</div>
	<div class="col-1">...</div>
</div>
```

---

### Responsive Columns

Both the grid column count and column span count can be responsive by prefixing each with the breakpoint variant. Adjust your browser width to see this in action.

<section class="radius-sm bg-silver-100 p-6">
  <div class="grid grid-cols-1 md.grid-cols-5">
    <div class="h-8 bg-gray-100 col-1 md.col-1">
    </div>
    <div class="h-8 bg-gray-300 col-1 md.col-3">
    </div>
    <div class="h-8 bg-gray-100 col-1 md.col-1">
    </div>
  </div>
</section>

```html
<div class="grid grid-cols-1 md.grid-cols-5">
	<div class="col-1 md.col-1">...</div>
	<div class="col-1 md.col-3">...</div>
	<div class="col-1 md.col-1">...</div>
</div>
```
