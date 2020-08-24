---
title: Form
date: 1000-01-02
---

{% include shortcodes/chapter, text: 'Modules', color: 'purple' %}

### Form Module

The Form module is an optional pre-built component that provides customizable styling of input text fieds, checkboxes, select dropdown etc.

<section class="radius-sm bg-silver-100 p-6">
  <form>
    <div class="mb-6 last.mb-0">
      <label class="label mb-2">Email</label>
      <input class="input" placeholder="Email" value="Placeholder Text">
    </div>
    <div class="mb-6 last.mb-0">
      <label class="checkbox">
        <input type="checkbox" checked required />
        <div class="checkbox__checkmark"></div>
        Checkbox
      </label>
    </div>
    <div class="mb-6 last.mb-0">
      <label class="radio mr-4">
        <input type="radio" name="radio" checked />
        <div class="radio__checkmark"></div>
        Radio
      </label>
      <label class="radio">
        <input type="radio" name="radio" checked />
        <div class="radio__checkmark"></div>
        Radio
      </label>
    </div>
    <div class="mb-6 last.mb-0">
      <label class="toggle">
        <input type="checkbox" checked />
        <div class="toggle__switch"></div>
      </label>
    </div>
    <div class="mb-6 last.mb-0">
      <div class="select">
        <select>
          <option selected>Selected</option>
          <option>Option</option>
          <option>Option</option>
        </select>
        <div class="select__angle"></div>
      </div>
    </div>
  </form>
</section>

<div class="mb-6"></div>

<div class="bg-black radius-sm h-24 overflow-auto">
{% highlight html %}
<form>
  <div class="mb-6 last.mb-0">
    <label class="label mb-2">Email</label>
    <input class="input" placeholder="Email" value="Placeholder Text">
  </div>

  <div class="mb-6 last.mb-0">
    <label class="checkbox">
      <input type="checkbox" checked required />
      <div class="checkbox__checkmark"></div>
      Checkbox
    </label>
  </div>

  <div class="mb-6 last.mb-0">
    <label class="radio mr-4">
      <input type="radio" name="radio" checked />
      <div class="radio__checkmark"></div>
      Radio
    </label>
    <label class="radio">
      <input type="radio" name="radio" checked />
      <div class="radio__checkmark"></div>
      Radio
    </label>
  </div>

  <div class="mb-6 last.mb-0">
    <label class="toggle">
      <input type="checkbox" checked />
      <div class="toggle__switch"></div>
    </label>
  </div>

  <div class="mb-6 last.mb-0">
    <div class="select">
      <select>
        <option selected>Selected</option>
        <option>Option</option>
        <option>Option</option>
      </select>
      <div class="select__angle"></div>
    </div>
  </div>
</form>
{% endhighlight %}
</div>

---

### Labels and Textfields

To add a required asterisk append the class `is-required` to your label.

<section class="radius-sm bg-silver-100 p-6">
  <label class="label is-required mb-2">Email</label>
  <input class="input" placeholder="Email" value="Placeholder Text" required>
</section>

```html
<label class="label is-required mb-2">Email</label>
<input class="input" placeholder="Email" value="Placeholder Text" required>
```


<div class="mb-10"></div>

#### Label and Textfield root variables

To customize the look of your label and textfields, override the following root variables.

<div class="bg-black radius-sm h-24 overflow-auto">
{% highlight css %}
/* styles.css */
:root {
  --label-font-size: ...;
  --label-font-weight: ...;
  --label-color: ...;
  --label-tracking: ...;
  --label-text-transform: ...;
  --label-required-color: ...;

  --input-height: ...;
  --input-padding: ...;
  --input-bg: ...;
  --input-border: ...;
  --input-radius: ...;
  --input-shadow: ...;
  --input-transition: ...;

  --input-hover-border: ...;
  --input-hover-shadow: ...;

  --input-focus-border: ...;
  --input-focus-shadow: ...;
}
{% endhighlight %}
</div>


---

### Input field sizes

Text fields come in **5 sizes**.

<section class="radius-sm bg-silver-100 p-6">
  <input class="input input-xs mb-4 last.mb-0" placeholder="Email" value="Placeholder Text">
  <input class="input input-sm mb-4 last.mb-0" placeholder="Email" value="Placeholder Text">
  <input class="input input-md mb-4 last.mb-0" placeholder="Email" value="Placeholder Text">
  <input class="input input-lg mb-4 last.mb-0" placeholder="Email" value="Placeholder Text">
  <input class="input input-xl mb-4 last.mb-0" placeholder="Email" value="Placeholder Text">
</section>

```html
<input class="input input-xs" placeholder="Email" value="Placeholder Text">
<input class="input input-sm" placeholder="Email" value="Placeholder Text">
<input class="input input-md" placeholder="Email" value="Placeholder Text">
<input class="input input-lg" placeholder="Email" value="Placeholder Text">
<input class="input input-xl" placeholder="Email" value="Placeholder Text">
```


<div class="mb-10"></div>

#### Input size root variables

To customize your text and select input field sizes, override the following root variables.

<div class="bg-black radius-sm h-24 overflow-auto">
{% highlight css %}
/* styles.css */
:root {
  --input-xs-height: ...;
  --input-xs-padding: ...;
  --input-xs-font-size: ...;

  --input-sm-height: ...;
  --input-sm-padding: ...;
  --input-sm-font-size: ...;

  --input-md-height: ...;
  --input-md-padding: ...;
  --input-md-font-size: ...;

  --input-lg-height: ...;
  --input-lg-padding: ...;
  --input-lg-font-size: ...;

  --input-xl-height: ...;
  --input-xl-padding: ...;
  --input-xl-font-size: ...;
}
{% endhighlight %}
</div>

---

### Select Fields


<section class="radius-sm bg-silver-100 p-6">
  <div class="select">
    <select>
      <option selected>Selected</option>
      <option>Option</option>
      <option>Option</option>
    </select>
    <div class="select__angle"></div>
  </div>
</section>

```html
<div class="select">
  <select>
    <option selected>Selected</option>
    <option>Option</option>
    <option>Option</option>
  </select>
  <div class="select__angle"></div>
</div>
```


<div class="mb-10"></div>

#### Select root variables

To customize your select input field sizes, override the following root variables.

<div class="bg-black radius-sm h-24 overflow-auto">
{% highlight css %}
/* styles.css */
:root {
  --select-height: ...;
  --select-padding: ...;
  --select-bg: ...;
  --select-border: ...;
  --select-radius: ...;
  --select-shadow: ...;
  --select-font-size: ...;
  --select-transition: ...;
  --select-hover-border: ...;
  --select-hover-shadow: ...;
  --select-focus-border: ...;
  --select-focus-shadow: ...;
  --select-disabled-bg: ...;
  --select-disabled-color: ...;
  --select-hover-angle-color: ...;
  --select-hover-focus-color: ...;
  --select-success-border: ...;
  --select-focus-success-shadow: ...;
  --select-warning-border: ...;
  --select-focus-warning-shadow: ...;
  --select-danger-border: ...;
  --select-focus-danger-shadow: ...;
}
{% endhighlight %}
</div>

---

### Select field sizes

Select fields come in **5 sizes**.

<section class="radius-sm bg-silver-100 p-6">
  <div class="select select-xs mb-4 last.mb-0">
    <select>
      <option selected>Selected</option>
      <option>Option</option>
      <option>Option</option>
    </select>
    <div class="select__angle"></div>
  </div>

  <div class="select select-sm mb-4 last.mb-0">
    <select>
      <option selected>Selected</option>
      <option>Option</option>
      <option>Option</option>
    </select>
    <div class="select__angle"></div>
  </div>

  <div class="select select-md mb-4 last.mb-0">
    <select>
      <option selected>Selected</option>
      <option>Option</option>
      <option>Option</option>
    </select>
    <div class="select__angle"></div>
  </div>

  <div class="select select-lg mb-4 last.mb-0">
    <select>
      <option selected>Selected</option>
      <option>Option</option>
      <option>Option</option>
    </select>
    <div class="select__angle"></div>
  </div>

  <div class="select select-xl mb-4 last.mb-0">
    <select>
      <option selected>Selected</option>
      <option>Option</option>
      <option>Option</option>
    </select>
    <div class="select__angle"></div>
  </div>
</section>

```html
<div class="select select-xs">...</div>
<div class="select select-sm">...</div>
<div class="select select-md">...</div>
<div class="select select-lg">...</div>
<div class="select select-xl">...</div>
```


<div class="mb-10"></div>

#### Select size root variables

To customize your select input field sizes, override the following root variables.

<div class="bg-black radius-sm h-24 overflow-auto">
{% highlight css %}
/* styles.css */
:root {
  --select-xs-height: ...;
  --select-xs-padding: ...;
  --select-xs-font-size: ...;

  --select-sm-height: ...;
  --select-sm-padding: ...;
  --select-sm-font-size: ...;

  --select-md-height: ...;
  --select-md-padding: ...;
  --select-md-font-size: ...;

  --select-lg-height: ...;
  --select-lg-padding: ...;
  --select-lg-font-size: ...;

  --select-xl-height: ...;
  --select-xl-padding: ...;
  --select-xl-font-size: ...;
}
{% endhighlight %}
</div>


---

### Responsive Text and Select Sizes

Both text and select field sizes can vary depending on breakpoint.

<section class="radius-sm bg-silver-100 p-6">
  <input class="input input-xs lg.input-xl" placeholder="Resize browser to see change">
</section>

```html
<input class="input input-xs lg.input-xl" placeholder="Resize browser to see change">
```

---

### Input States

Text, select, and textarea fields come in *4* different states.

<section class="radius-sm bg-silver-100 p-6">
  <input class="input mb-4 last.mb-0" placeholder="Disabled" disabled>
  <input class="input is-success mb-4 last.mb-0" placeholder="Success">
  <input class="input is-warning mb-4 last.mb-0" placeholder="Warning">
  <input class="input is-danger mb-4 last.mb-0" placeholder="Danger">
  <textarea class="textarea is-warning leading-8" rows="4">Warning textarea</textarea>
</section>

```html
<input class="input" placeholder="Success" disabled>
<input class="input is-success" placeholder="Success">
<input class="input is-warning" placeholder="Warning">
<input class="input is-danger" placeholder="Danger">
<textarea class="textarea is-warning leading-8" rows="4">Warning textarea</textarea>
```

<div class="mb-10"></div>

#### State field root variables

To customize your state fields, override the following root variables.

<div class="bg-black radius-sm overflow-auto">
{% highlight css %}
/* styles.css */
:root {
  --input-disabled-bg: ...;
  --input-disabled-color: ...;

  --input-success-border: ...;
  --input-focus-success-shadow: ...;

  --input-warning-border: ...;
  --input-focus-warning-shadow: ...;

  --input-danger-border: ...;
  --input-focus-danger-shadow: ...;
}
{% endhighlight %}
</div>


---

### Radio and Checkboxes

Text and select input fields come in **5 sizes**.

<section class="radius-sm bg-silver-100 p-6">
  <div class="mb-6">
    <label class="radio mr-4">
      <input type="radio" name="radio" checked />
      <div class="radio__checkmark"></div>
      Radio
    </label>
    <label class="radio">
      <input type="radio" name="radio" checked />
      <div class="radio__checkmark"></div>
      Radio
    </label>
  </div>
  <div>
    <label class="checkbox">
      <input type="checkbox" checked required />
      <div class="checkbox__checkmark"></div>
      I agree to the terms and agreement.
    </label>
  </div>
</section>

```html
<label class="radio mr-4">
  <input type="radio" name="radio" checked />
  <div class="radio__checkmark"></div>
  Radio
</label>
<label class="radio">
  <input type="radio" name="radio" checked />
  <div class="radio__checkmark"></div>
  Radio
</label>

<label class="checkbox">
  <input type="checkbox" checked required />
  <div class="checkbox__checkmark"></div>
  I agree to the terms and agreement.
</label>
```


<div class="mb-10"></div>

#### Radio and Checkbox root variables

To customize your radio or checkbox input fields, override the following root variables.

<div class="bg-black radius-sm h-24 overflow-auto">
{% highlight css %}
/* styles.css */
:root {
  --checkbox-size: ...;
  --checkbox-margin: ...;
  --checkbox-radius: ...;
  --checkbox-border: ...;
  --checkbox-bg: ...;
  --checkbox-transition: ...;
  --checkbox-hover-border: ...;
  --checkbox-checked-bg: ...;
  --checkbox-checked-border: ...;
  --checkbox-disabled-bg: ...;
  --checkbox-disabled-color: ...;

  --radio-size: ...;
  --radio-margin: ...;
  --radio-radius: ...;
  --radio-border: ...;
  --radio-bg: ...;
  --radio-transition: ...;
  --radio-hover-border: ...;
  --radio-checked-bg: ...;
  --radio-checked-border: ...;
  --radio-disabled-bg: ...;
  --radio-disabled-color: ...;
}
{% endhighlight %}
</div>



---

### Toggle switch

Checkboxes can also be transformed into a toggle switch.

<section class="radius-sm bg-silver-100 p-6 flex justify-content-center">
  <label class="toggle">
    <input type="checkbox" checked />
    <div class="toggle__switch"></div>
  </label>
</section>

```html
<label class="toggle">
  <input type="checkbox" checked />
  <div class="toggle__switch"></div>
</label>
```


<div class="mb-10"></div>

#### Toggle switch root variables

To customize your toggle switch, override the following root variables.

{% highlight css %}
/* styles.css */
:root {
  --toggle-width: ...;
  --toggle-height: ...;
  --toggle-bg: ...;
  --toggle-transition: ...;
  --toggle-radius: ...;
  --toggle-hover-bg: ...;
  --toggle-checked-bg: ...;
  --toggle-checked-translate: ...;
  --toggle-disabled-bg: ...;
}
{% endhighlight %}


---

### Textarea

Checkboxes can also be transformed into a toggle switch. Note, to set a default line-height apply the leading property.

<section class="radius-sm bg-silver-100 p-6 flex justify-content-center">
  <textarea class="textarea leading-8" rows="4">Ask your question here</textarea>
</section>

```html
<textarea class="textarea leading-8" rows="4">Ask your question here</textarea>
```


<div class="mb-10"></div>

#### Textarea root variables

To customize your textarea, override the following root variables.

{% highlight css %}
/* styles.css */
:root {
  --textarea-hover-border: ...;
  --textarea-hover-shadow: ...;
  --textarea-focus-border: ...;
  --textarea-focus-shadow: ...;
  --textarea-disabled-bg: ...;
  --textarea-disabled-color: ...;
  --textarea-success-border: ...;
  --textarea-focus-success-shadow: ...;
  --textarea-warning-border: ...;
  --textarea-focus-warning-shadow: ...;
  --textarea-danger-border: ...;
  --textarea-focus-danger-shadow: ...;
}
{% endhighlight %}

---

### Disabled form fields

All form field elements can be disabled with assigning the `disabled` attribute.

<section class="radius-sm bg-silver-100 p-6">
  <form>
    <div class="mb-6 last.mb-0">
      <label class="label mb-2">Email</label>
      <input class="input" placeholder="Email" value="Placeholder Text" disabled>
    </div>
    <div class="mb-6 last.mb-0">
      <label class="checkbox pointer-events-none">
        <input type="checkbox" checked required disabled />
        <div class="checkbox__checkmark"></div>
        Checkbox
      </label>
    </div>
    <div class="mb-6 last.mb-0">
      <label class="radio pointer-events-none mr-4">
        <input type="radio" name="radio" checked disabled />
        <div class="radio__checkmark"></div>
        Radio
      </label>
      <label class="radio pointer-events-none">
        <input type="radio" name="radio" checked disabled />
        <div class="radio__checkmark"></div>
        Radio
      </label>
    </div>
    <div class="mb-6 last.mb-0">
      <label class="toggle pointer-events-none">
        <input type="checkbox" checked disabled />
        <div class="toggle__switch"></div>
      </label>
    </div>
    <div class="mb-6 last.mb-0">
      <div class="select">
        <select disabled>
          <option selected>Selected</option>
          <option>Option</option>
          <option>Option</option>
        </select>
        <div class="select__angle"></div>
      </div>
    </div>
  </form>
</section>


---

### How to Disable this Module

By default, all modules are enabled. To disable this module, set the `$include-form-module` variable to `false` in your module configuration.

```scss
@use "uniform" as * with (
  $include-form-module: false
);
```
