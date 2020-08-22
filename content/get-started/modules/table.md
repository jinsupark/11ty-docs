---
title: Table
date: 1000-01-01
---

### Table Module

Table is an optional module that extends the default table styling to provide interactivity and responsivness.

<section class="radius-lg bg-gray-100 p-6">
  <table class="table-interactive-row">
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
<table class="table-interactive-row">
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

---

### Interactive Rows and Columns

Tables rows and columns can have hover interactivity by adding `table-interactive-row` or `table-interactive-col` class to the table element.

<section class="radius-lg bg-gray-100 p-6">
  <table class="table-interactive-row">
    <thead>
      <tr>
        <th>Column A</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>These rows are hoverable</td>
      </tr>
      <tr>
        <td>These rows are hoverable</td>
      </tr>
    </tbody>
  </table>

  <table class="table-interactive-col">
    <thead>
      <tr>
        <th>Column A</th>
        <th>Column B</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Hover on me</td>
        <td>Hover on me</td>
      </tr>
      <tr>
        <td>Hover on me</td>
        <td>Hover on me</td>
      </tr>
    </tbody>
  </table>
</section>

```html
<table class="table-interactive-row">
	...
</table>

<table class="table-interactive-col">
	...
</table>
```

---

### Responsive Tables

Tables can become responsive at various breakpoints by adding the `table-stack` and `table-unstack` class.

<section class="radius-lg bg-gray-100 p-6">
  <table class="table-stack md.table-unstack">
    <thead>
      <tr>
        <th>Column A</th>
        <th>Column B</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td data-table-label="Column A">Resize your browser</td>
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
<table class="table-stack md.table-unstack">
	...
</table>
```

---

### How to Enable this Module

By default, all modules are disabled. To enable this table module, set the `$include-table-module` variable to `true`.

```scss
@use "uniform" as * with (
  $include-table-module: true
);
```
