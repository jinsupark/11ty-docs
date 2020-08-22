---
title: Basic Configuration
date: 1000-01-01
---

{% include shortcodes/chapter, text: 'Customization', color: 'violet' %}

### Easiest way to Get Started

The quickest way to customize Uniform is to include the pre-packaged CSS version of Uniform and apply CSS variable overrides directly to the `:root`. There are a wide range of CSS variables you can override, use this guide to see what is available.

```css
:root {
  --font-sans: 'Inter';
  --red-500: #FF4242;
  --btn-radius: 4px;
}
```

---


### Font Family Root Variables

Values for the following CSS variables apply to the `font-family` property. 

```css
:root {
  --font-sans: sans-serif;
  --font-serif: serif;
  --font-mono: monospace;
}
```

---


### Font Size Root Variables

Values for the following CSS variables apply to the `font-size` property. 

```css
:root {
  --font-10xl: 4.5rem;
  --font-9xl: 4rem;
  --font-8xl: 3.5rem;
  --font-7xl: 3rem;
  --font-6xl: 2.5rem;
  --font-5xl: 2.25rem;
  --font-4xl: 2rem;
  --font-3xl: 1.75rem;
  --font-2xl: 1.5rem;
  --font-xl: 1.25rem;
  --font-lg: 1.125rem;
  --font-md: 1rem;
  --font-sm: 0.875rem;
  --font-xs: 0.75rem;
  --font-2xs: 0.625rem;
}
```


---


### Line Height Root Variables

Values for the following CSS variables apply to the `line-height` property. 

```css
:root {
  --leading-1: 1;
  --leading-2: 1.125;
  --leading-3: 1.25;
  --leading-4: 1.375;
  --leading-5: 1.5;
  --leading-6: 1.625;
  --leading-7: 1.75;
  --leading-8: 1.875;
  --leading-9: 2;
  --leading-10: 2.125;
  --leading-11: 2.25;
  --leading-12: 2.375;
  --leading-13: 2.5;
}
```

---


### Letter-spacing Root Variables

Values for the following CSS variables apply to the `letter-spacing` property. 

```css
:root {
  --tracking-n3: -0.075em;
  --tracking-n2: -0.05em;
  --tracking-n1: -0.025em;
  --tracking-0: 0;
  --tracking-1: 0.025em;
  --tracking-2: 0.05em;
  --tracking-3: 0.075em;
}
```

---


### Border Radius Root Variables

Values for the following CSS variables apply to the `border-radius` property. 

```css
:root {
  --radius-xs: 0.25rem;
  --radius-sm: 0.5rem;
  --radius-md: 0.75rem;
  --radius-lg: 1rem;
  --radius-xl: 1.25rem;
  --radius-round: 9999px;
}
```

---


### Box Shadow Root Variables

Values for the following CSS variables apply to the `box-shadow` property. 

```css
:root {
  --shadow-1: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
  --shadow-2: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);
  --shadow-3: 0 10px 20px rgba(0, 0, 0, 0.19), 0 6px 6px rgba(0, 0, 0, 0.23);
  --shadow-4: 0 14px 28px rgba(0, 0, 0, 0.25), 0 10px 10px rgba(0, 0, 0, 0.22);
  --shadow-5: 0 19px 38px rgba(0, 0, 0, 0.3), 0 15px 12px rgba(0, 0, 0, 0.22);
}
```

---

### Spacing Root Variables

Values for the following CSS variables apply to any spacing related properties such as `margin` or `padding`. 

<div class="bg-black radius-sm h-24 overflow-auto">
{% highlight css %}
:root {
  --size-0: 0;
  --size-1: 0.25rem;
  --size-2: 0.5rem;
  --size-3: 0.75rem;
  --size-4: 1rem;
  --size-5: 1.25rem;
  --size-6: 1.5rem;
  --size-7: 1.75rem;
  --size-8: 2rem;
  --size-9: 2.25rem;
  --size-10: 2.5rem;
  --size-11: 2.75rem;
  --size-12: 3rem;
  --size-13: 3.5rem;
  --size-14: 4rem;
  --size-15: 4.5rem;
  --size-16: 5rem;
  --size-17: 5.5rem;
  --size-18: 6rem;
  --size-19: 8rem;
  --size-20: 10rem;
  --size-21: 12rem;
  --size-22: 16rem;
  --size-23: 20rem;
  --size-24: 24rem;
  --size-25: 32rem;
  --size-26: 40rem;
  --size-27: 48rem;
  --size-28: 64rem;
  --size-29: 80rem;
  --size-30: 96rem;
  --size-n1: -0.25rem;
  --size-n2: -0.5rem;
  --size-n3: -0.75rem;
  --size-n4: -1rem;
  --size-n5: -1.25rem;
  --size-n6: -1.5rem;
  --size-n7: -1.75rem;
  --size-n8: -2rem;
  --size-n9: -2.25rem;
  --size-n10: -2.5rem;
  --size-n11: -2.75rem;
  --size-n12: -3rem;
  --size-n13: -3.5rem;
  --size-n14: -4rem;
  --size-n15: -4.5rem;
  --size-n16: -5rem;
  --size-n17: -5.5rem;
  --size-n18: -6rem;
  --size-n19: -8rem;
  --size-n20: -10rem;
  --size-n21: -12rem;
  --size-n22: -16rem;
  --size-n23: -20rem;
  --size-n24: -24rem;
  --size-n25: -32rem;
  --size-n26: -40rem;
  --size-n27: -48rem;
  --size-n28: -64rem;
  --size-n29: -80rem;
  --size-n30: -96rem;
}
{% endhighlight %}
</div>

---

### Color Root Variables

Values for the following CSS variables apply to any color related properties such as `background-color` or `border-color`. 

<div class="bg-black radius-sm h-24 overflow-auto">
{% highlight css %}
:root {
  --red-100: #feefef;
  --red-200: #fee0e0;
  --red-300: #fdb0b0;
  --red-400: #fb7f7f;
  --red-500: #fa6060;
  --red-600: #e04646;
  --red-700: #cf3535;
  --red-800: #a72929;
  --red-900: #6f1b1b;
  --orange-100: #fff2ea;
  --orange-200: #fee5d5;
  --orange-300: #febd96;
  --orange-400: #fd9557;
  --orange-500: #fc7b2d;
  --orange-600: #e1661b;
  --orange-700: #c75919;
  --orange-800: #9f4814;
  --orange-900: #69300d;
  --brown-100: #f8efe7;
  --brown-200: #f1ddcf;
  --brown-300: #dbac88;
  --brown-400: #c67940;
  --brown-500: #a75a21;
  --brown-600: #8e4c1c;
  --brown-700: #7e4319;
  --brown-800: #643614;
  --brown-900: #43240d;
  --yellow-100: #fff7e8;
  --yellow-200: #ffefd0;
  --yellow-300: #ffd78b;
  --yellow-400: #ffbf45;
  --yellow-500: #ffaf16;
  --yellow-600: #df970d;
  --yellow-700: #c4850c;
  --yellow-800: #9d6a09;
  --yellow-900: #694706;
  --lime-100: #f4fae4;
  --lime-200: #eaf5c8;
  --lime-300: #cae776;
  --lime-400: #a8d624;
  --lime-500: #8ab900;
  --lime-600: #759d00;
  --lime-700: #688b00;
  --lime-800: #536f00;
  --lime-900: #374a00;
  --green-100: #e5fae4;
  --green-200: #cbf5c8;
  --green-300: #7ee675;
  --green-400: #32d424;
  --green-500: #0fb600;
  --green-600: #0d9b00;
  --green-700: #0b8900;
  --green-800: #096d00;
  --green-900: #064900;
  --teal-100: #e4fbf6;
  --teal-200: #c9f7ec;
  --teal-300: #78ebcf;
  --teal-400: #26e0b3;
  --teal-500: #00c797;
  --teal-600: #00a980;
  --teal-700: #009571;
  --teal-800: #00775b;
  --teal-900: #00503c;
  --cyan-100: #e5fbfd;
  --cyan-200: #caf8fa;
  --cyan-300: #7becf4;
  --cyan-400: #2be1ed;
  --cyan-500: #00d1de;
  --cyan-600: #00b2bd;
  --cyan-700: #009da7;
  --cyan-800: #007d85;
  --cyan-900: #005459;
  --blue-100: #e6f4ff;
  --blue-200: #cce9ff;
  --blue-300: #80c9ff;
  --blue-400: #33a8ff;
  --blue-500: #0092ff;
  --blue-600: #007cd9;
  --blue-700: #006ebf;
  --blue-800: #005899;
  --blue-900: #003a66;
  --indigo-100: #e6eeff;
  --indigo-200: #ccddff;
  --indigo-300: #80abff;
  --indigo-400: #3379ff;
  --indigo-500: #0057ff;
  --indigo-600: #004ad9;
  --indigo-700: #0041bf;
  --indigo-800: #003499;
  --indigo-900: #002366;
  --blueberry-100: #e8eaf6;
  --blueberry-200: #d1d6ed;
  --blueberry-300: #8c99d2;
  --blueberry-400: #475db5;
  --blueberry-500: #2c3f90;
  --blueberry-600: #26367a;
  --blueberry-700: #212f6c;
  --blueberry-800: #1b2656;
  --blueberry-900: #121a3a;
  --violet-100: #efe6ff;
  --violet-200: #dfccff;
  --violet-300: #b080ff;
  --violet-400: #8133ff;
  --violet-500: #6100ff;
  --violet-600: #5200d9;
  --violet-700: #4900bf;
  --violet-800: #3a0099;
  --violet-900: #270066;
  --purple-100: #f1e4fb;
  --purple-200: #e3c9f7;
  --purple-300: #bb78eb;
  --purple-400: #9226e0;
  --purple-500: #7400c7;
  --purple-600: #6300a9;
  --purple-700: #570095;
  --purple-800: #460077;
  --purple-900: #2e0050;
  --magenta-100: #ffe6ff;
  --magenta-200: #feccff;
  --magenta-300: #fd80ff;
  --magenta-400: #fb33ff;
  --magenta-500: #fa00ff;
  --magenta-600: #d500d9;
  --magenta-700: #bc00bf;
  --magenta-800: #960099;
  --magenta-900: #640066;
  --pink-100: #ffebf2;
  --pink-200: #ffd6e5;
  --pink-300: #ff99be;
  --pink-400: #ff5c96;
  --pink-500: #ff337c;
  --pink-600: #e42066;
  --pink-700: #ca1b5a;
  --pink-800: #a21647;
  --pink-900: #6c0e30;
  --silver-100: #f3f3f5;
  --silver-200: #e6e8eb;
  --silver-300: #dadce1;
  --silver-400: #ced0d7;
  --silver-500: #c2c5ce;
  --silver-600: #b5b9c4;
  --silver-700: #a9adba;
  --silver-800: #9da1b0;
  --silver-900: #9096a6;
  --gray-100: #848a9c;
  --gray-200: #747b8f;
  --gray-300: #676d80;
  --gray-400: #5a5f70;
  --gray-500: #4d5260;
  --gray-600: #404450;
  --gray-700: #333640;
  --gray-800: #272930;
  --gray-900: #1a1b20;
  --tint-100: rgba(255, 255, 255, 0.1);
  --tint-200: rgba(255, 255, 255, 0.2);
  --tint-300: rgba(255, 255, 255, 0.3);
  --tint-400: rgba(255, 255, 255, 0.4);
  --tint-500: rgba(255, 255, 255, 0.5);
  --tint-600: rgba(255, 255, 255, 0.6);
  --tint-700: rgba(255, 255, 255, 0.7);
  --tint-800: rgba(255, 255, 255, 0.8);
  --tint-900: rgba(255, 255, 255, 0.9);
  --shade-100: rgba(0, 0, 0, 0.1);
  --shade-200: rgba(0, 0, 0, 0.2);
  --shade-300: rgba(0, 0, 0, 0.3);
  --shade-400: rgba(0, 0, 0, 0.4);
  --shade-500: rgba(0, 0, 0, 0.5);
  --shade-600: rgba(0, 0, 0, 0.6);
  --shade-700: rgba(0, 0, 0, 0.7);
  --shade-800: rgba(0, 0, 0, 0.8);
  --shade-900: rgba(0, 0, 0, 0.9);
  --black: black;
  --white: white;
  --transparent: transparent;
}
{% endhighlight %}
</div>