---
title: Form
date: 1000-01-01
---

### Form Module

Form is an optional module that extends the default functionality and styling of forms and input fields. You can group your fields with the `form__group` child element.

<section class="radius-lg bg-gray-100 p-6">
  <div class="bg-white shadow-3 max-w-18 mx-auto p-5 radius-lg">
    <h5 class="font-600 align-center mt-2 mb-4">Sign Up</h5>
    <form class="form">
      <div class="form__group">
        <label class="label is-required">Email</label>
        <input placeholder=" " required>
      </div>
      <div class="form__group">
        <label class="label is-required">Password</label>
        <input type="password" placeholder=" " required>
      </div>
      <div class="form__group">
        <label class="input-checkbox">
          <input type="checkbox" required/>
          <div class="input-checkbox/box"></div>
          I agree to the Terms and Conditions
        </label>
      </div>
      <div class="form__group flex justify-content-end">
        <button class="btn px-6">Sign Up</button>
      </div>
    </form>
  </div>
</section>

```html
<form class="form">
	<div class="form__group">
		<label class="label is-required">Email</label>
		<input placeholder=" " required />
	</div>
	<div class="form__group">
		<label class="label is-required">Password</label>
		<input type="password" placeholder=" " required />
	</div>
	<div class="form__group">
		<label class="input-checkbox">
			<input type="checkbox" required />
			<div class="input-checkbox/box"></div>
			I agree to the Terms and Conditions
		</label>
	</div>
	<div class="form__group flex justify-content-end">
		<button class="btn px-6">Sign Up</button>
	</div>
</form>
```

---

### Input Fields

The Form module also provides styling for common input types such as checkboxes, radio buttons, and toggles. Focus box shadow and selected fill colors are all styled using the core theme values.

<section class="radius-lg bg-gray-100 p-6">
  <div class="bg-white shadow-3 p-4 radius-lg">
    <form class="form">
      <div class="form__group">
        <label class="label">Email</label>
        <input placeholder="Email" value="john.titor@apple.com">
      </div>
      <div class="form__group">
        <label class="label">Username</label>
        <input type="text" placeholder="UniformCSS" value="@UniformCSS">
      </div>
      <div class="form__group">
        <label class="input-checkbox">
          <input type="checkbox" checked required />
          <div class="input-checkbox/box"></div>
          Checkbox
        </label>
      </div>
      <div class="form__group">
        <label class="input-radio mr-4">
          <input type="radio" name="radio" checked />
          <div class="input-radio/selection"></div>
          Radio
        </label>
        <label class="input-radio">
          <input type="radio" name="radio" checked />
          <div class="input-radio/selection"></div>
          Radio
        </label>
      </div>
      <div class="form__group">
        <label class="input-toggle">
          <input type="checkbox" checked />
          <div class="input-toggle/slide"></div>
        </label>
      </div>
      <div class="form__group">
        <div class="input-select">
          <select>
            <option selected>Selected</option>
            <option>Option</option>
            <option>Option</option>
          </select>
          <div class="input-select/angle"></div>
        </div>
      </div>
    </form>
  </div>
</section>

```html
<form class="form">
	<div class="form__group">
		<label class="label">Email</label>
		<input placeholder="Email" value="john.titor@apple.com" />
	</div>
	<div class="form__group">
		<label class="label">Username</label>
		<input type="text" placeholder="UniformCSS" value="@UniformCSS" />
	</div>
	<div class="form__group">
		<label class="input-checkbox">
			<input type="checkbox" checked required />
			<div class="input-checkbox/box"></div>
			Checkbox
		</label>
	</div>
	<div class="form__group">
		<label class="input-radio mr-4">
			<input type="radio" name="radio" checked />
			<div class="input-radio/selection"></div>
			Radio
		</label>
		<label class="input-radio">
			<input type="radio" name="radio" checked />
			<div class="input-radio/selection"></div>
			Radio
		</label>
	</div>
	<div class="form__group">
		<label class="input-toggle">
			<input type="checkbox" checked />
			<div class="input-toggle/slide"></div>
		</label>
	</div>
	<div class="form__group">
		<div class="input-select">
			<select>
				<option selected>Selected</option>
				<option>Option</option>
				<option>Option</option>
			</select>
			<div class="input-select/angle"></div>
		</div>
	</div>
</form>
```

---

### Disabled Input Fields

Input types can also be disabled with the `disabled` attribute. You can also disable the hover pointer state by applying `is-disabled` to the parent input element.

<section class="radius-lg bg-gray-100 p-6">
  <div class="bg-white shadow-3 p-4 radius-lg">
    <form class="form">
      <div class="form__group">
        <label class="label">Email</label>
        <input placeholder="Email" value="john.titor@apple.com" disabled>
      </div>
      <div class="form__group">
        <label class="label">Username</label>
        <input type="text" placeholder="UniformCSS" value="@UniformCSS" disabled>
      </div>
      <div class="form__group">
        <label class="input-checkbox is-disabled">
          <input type="checkbox" disabled checked required />
          <div class="input-checkbox/box"></div>
          Disabled checkbox
        </label>
      </div>
      <div class="form__group">
        <label class="input-radio is-disabled mr-4">
          <input type="radio" name="radio" disabled checked />
          <div class="input-radio/selection"></div>
          Disabled radio
        </label>
        <label class="input-radio is-disabled">
          <input type="radio" name="radio" disabled checked />
          <div class="input-radio/selection"></div>
          Disabled radio
        </label>
      </div>
      <div class="form__group">
        <label class="input-toggle is-disabled">
          <input type="checkbox" disabled />
          <div class="input-toggle/slide"></div>
        </label>
      </div>
      <div class="form__group">
        <div class="input-select">
          <select disabled>
            <option selected>Disabled</option>
            <option>Option</option>
            <option>Option</option>
          </select>
          <div class="input-select/angle"></div>
        </div>
      </div>
    </form>
  </div>
</section>

```html
<form class="form">
	<div class="form__group">
		<label class="label">Email</label>
		<input placeholder="Email" value="john.titor@apple.com" disabled />
	</div>
	<div class="form__group">
		<label class="label">Username</label>
		<input type="text" placeholder="UniformCSS" value="@UniformCSS" disabled />
	</div>
	<div class="form__group">
		<label class="input-checkbox is-disabled">
			<input type="checkbox" disabled checked required />
			<div class="input-checkbox/box"></div>
			Disabled checkbox
		</label>
	</div>
	<div class="form__group">
		<label class="input-radio is-disabled mr-4">
			<input type="radio" name="radio" disabled checked />
			<div class="input-radio/selection"></div>
			Disabled radio
		</label>
		<label class="input-radio is-disabled">
			<input type="radio" name="radio" disabled checked />
			<div class="input-radio/selection"></div>
			Disabled radio
		</label>
	</div>
	<div class="form__group">
		<label class="input-toggle is-disabled">
			<input type="checkbox" disabled />
			<div class="input-toggle/slide"></div>
		</label>
	</div>
	<div class="form__group">
		<div class="input-select">
			<select disabled>
				<option selected>Disabled</option>
				<option>Option</option>
				<option>Option</option>
			</select>
			<div class="input-select/angle"></div>
		</div>
	</div>
</form>
```

---

### Input Sizes

Text or select type input fields come in three different sizes.

<section class="radius-lg bg-gray-100 p-6">
  <input type="text" placeholder="Small Input" class="input-sm">
  <input type="text" placeholder="Medium Input" class="input-md">
  <input type="text" placeholder="Large Input" class="input-lg">
  <div class="input-select">
    <select class="input-sm">
      <option>Small</option>
      <option>Option</option>
      <option>Option</option>
    </select>
    <div class="input-select/angle"></div>
  </div>
  <div class="input-select">
    <select class="input-md">
      <option>Medium</option>
      <option>Option</option>
      <option>Option</option>
    </select>
    <div class="input-select/angle"></div>
  </div>
  <div class="input-select">
    <select class="input-lg">
      <option>Large</option>
      <option>Option</option>
      <option>Option</option>
    </select>
    <div class="input-select/angle"></div>
  </div>
</section>

```html
<input type="text" placeholder="Small Input" class="input-sm" />
<input type="text" placeholder="Medium Input" class="input-md" />
<input type="text" placeholder="Large Input" class="input-lg" />

<div class="input-select">
	<select class="input-sm">
		<option>Small</option>
		<option>Option</option>
		<option>Option</option>
	</select>
	<div class="input-select/angle"></div>
</div>

<div class="input-select">
	<select class="input-md">
		<option>Medium</option>
		<option>Option</option>
		<option>Option</option>
	</select>
	<div class="input-select/angle"></div>
</div>

<div class="input-select">
	<select class="input-lg">
		<option>Large</option>
		<option>Option</option>
		<option>Option</option>
	</select>
	<div class="input-select/angle"></div>
</div>
```

---

### Responsive Input Sizes

Input sizes can change based on breakpoint

<section class="radius-lg bg-gray-100 p-6">
  <input class="input-lg sm.input-md">
</section>

```html
<input class="input-lg sm.input-md" />
```

---

### Input States

Text or select type input fields come in three different states.

<section class="radius-lg bg-gray-100 p-6">
  <input type="text" placeholder="Valid" class="is-valid">
  <input type="text" placeholder="Warning" class="is-warning">
  <input type="text" placeholder="Error" class="is-error">
</section>

```html
<input type="text" placeholder="Valid" class="is-valid" />
<input type="text" placeholder="Warning" class="is-warning" />
<input type="text" placeholder="Error" class="is-error" />
```

---

### How to Enable this Module

By default, all modules are disabled. To enable this form module, set the `$include-form-module` variable to `true`.

```scss
@use "uniform" as * with (
  $include-form-module: true
);
```
