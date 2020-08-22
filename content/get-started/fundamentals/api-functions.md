---
title: API Functions
date: 1000-01-08
---

{% include shortcodes/chapter, text: 'Fundamentals', color: 'orange' %}

### API Functions

If you are using the native Sass implementation of Uniform, you get access to useful internal API functions that allow you to **directly access theme variables and return values**. This is particularly useful for situations where you need to extrapolate a component.

To better understand how this works, it's important to note that behind the scenes, all user-defined variables such as colors and font-sizes in Uniform are enclosed inside a map. API Functions query this map and return the value of the key you are passing through (**API functions can either return a single value or the entire map**).

```scss
// Example custom element
.element {
  margin-bottom: size(12);
  padding: size(4);
  background: fill(gray-100);
  font-size: font-size(xl);
  line-height: leading(8);
}

// Example custom loop using map
@each $breakpoint, $breakpoint-value in breakpoints() {
  // for each breakpoint, do the following
}

@each $fill, $fill-value in fills() {
  // for each fill, do the following
}
```

For more information, please also visit the page on <a class="hover.underline" href="/get-started/custom-components">custom components</a>


---

### Breakpoints API

The `screen()` function returns values from the breakpoint map provided a variant is passed in as a parameter. `screens()` function returns the entire map.

For more information on which variants are available, visit <a class="hover.underline" href="/get-started/breakpoints">breakpoints</a>.

```bash
screen()
screens()
```

```scss
.element {
  @media (min-width: screen(sm)) {
    ...
  }
}

@each $breakpoint, $breakpoint-value in screens() {
  // for each breakpoint, do the following
}
```

---

### Color API

The `fill()` function returns values from the color map provided a variant is passed in as a parameter. The `fills()` function returns the entire map.

This function has access to both **colors** and **gradient** map values, however these sets can also be queried seperately as well.

For more information on which variants are available, visit <a class="hover.underline" href="/get-started/colors">colors</a>.

```bash
fill()
fills()
color()
colors()
gradient()
gradients()
```

```scss
.element {
  background-color: fill(gray-200);
}

@each $fill, $fill-value in fills() {
  // for each fill, do the following
}

@each $color, $color-value in colors() {
  // for each color, do the following
  // this map does not include the gradient map
}
```

---

### Sizes API

The `size()` function returns values from the size map provided a variant is passed in as a parameter. `sizes()` function returns the entire map.

This function has access to both **positive-sizes** and **negative-sizes** map values, however these sets can also be queried seperately as well.

For more information on which variants are available, visit <a class="hover.underline" href="/get-started/sizes">sizes</a>.

```bash
size()
sizes()
positive-size()
positive-sizes()
negative-size()
negative-sizes()
```

```scss
.element {
  margin-top: size(n6); // -1.5rem  
  padding: size(6); // 1.5rem
}

@each $size, $size-value in sizes() {
  // for each size, do the following
}
```

Unlike other API Functions the `sizes()` function can query multiple sizes. This is particulary useful for shorthand properties such as `margin` or `padding`.

```scss
// INPUT
.element {
  padding: size(5, 6, 7, 8);
}

// OUTPUT
.element {
  padding: 1.25rem 1.5rem 1.75rem 2rem;
}
```

---

### Shadows API

The `shadow()` function returns values from the shadow map provided a variant is passed in as a parameter. `shadows()` function returns the entire map.

For more information on which variants are available, visit <a class="hover.underline" href="/get-started/shadows">shadows</a>.

```bash
shadow()
shadows()
```

```scss
.element {
  box-shadow: shadow(3);
}

@each $shadow, $shadow-value in shadows() {
  // for each effect, do the following
}
```

---

### Typography API

Uniform provides various font related API function such as `font-size` and `font-family`. For more information on which variants are available, visit <a class="hover.underline" href="/get-started/typography">typography</a>.

```bash
font-family()
font-families()

font-size()
font-sizes()

leading()
leadings()

tracking()
trackings()
```

```scss
.element {
  font-family: font-family(sans);
  font-size: font-size(xl);
  font-weight: 700;
  line-height: leading(8);
}

@each $font-size, $font-size-value in font-sizes() {
  // for each font-size, do the following
}
```

---

### Radius API

The `radius()` function returns values from the radius map provided a variant is passed in as a parameter. `radiuses()` function returns the entire map.

For more information on which variants are available, visit <a class="hover.underline" href="/get-started/radius">radius</a>.

```scss
radius()
radiuses()
```

```scss
.element {
  border-radius: radius(md);
}

@each $radius, $radius-value in radiuses() {
  // for each radius, do the following
}
```

---

### Private Functions

Additional to theme API functions, Uniform also provides two helper functions to help you perform certain tasks more easily.

---

#### Rem Function

The `rem()` function allows you easily convert a pixel value into a rem value.

```scss
.element {
  font-size: rem(18); // this will convert 18px to rem
}
```

---

#### Merge Function

The `merge()` function allows you merge any number of maps as you like. This differs from the native Sass module feature `map.merge()` where you are limited to merging only two maps.

```scss
$map: merge($map1, $map2, $map3, $map4);
```
