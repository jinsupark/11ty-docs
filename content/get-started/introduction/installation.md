---
title: Installation
date: 1000-01-02
---

{% include shortcodes/chapter, text: 'Introduction', color: 'orange' %}

### Getting up and running

Uniform is super easy to get started and setup, you can either:

1. Use **npm** to install the Uniform package.
3. Use the **jsDelivr CDN** to link directly to the Uniform stylesheet.
4. Clone or download the project **directly** from the GitHub repository.

---

{% include shortcodes/video, id: 'GUQqC8abh6Y' %}

---

### Native installation

<div class="mb-10"></div>

<h4><span class="w-6 h-6 mr-2 inline-flex align-items-center justify-content-center font-sm font-600 leading-none bg-blue-500 leading-1 color-white radius-round">1</span> Clone and install dependencies</h4>

Make sure you have <a class="hover.underline" href="https://nodejs.org/en/"  target="_black">Node.js</a> installed. Clone the latest version of Uniform and install its dependencies.

```bash
# Clone project
git clone https://github.com/UniformCSS/uniformcss

# Install dependencies
npm install
```

<div class="mb-10"></div>

<h4><span class="w-6 h-6 mr-2 inline-flex align-items-center justify-content-center font-sm font-600 leading-none bg-blue-500 leading-1 color-white radius-round">3</span> Compile and watch for changes</h4>

Run the following command to build your first `uniform.css`. Optionally you can find pre-packaged versions in the dist directory. 

```bash
npm run uniform:watch
```

> By default Uniform **npm build scripts** will output to the root directory. To change the output destination, specify the location in `package.json`. For more info on other build commands refer to the page on <a class="hover.underline" href="/get-started/build-scripts/">build scripts</a>.

<div class="mb-10"></div>

<h4><span class="w-6 h-6 mr-2 inline-flex align-items-center justify-content-center font-sm font-600 leading-none bg-blue-500 leading-1 color-white radius-round">4</span> Add compiled stylesheet</h4>

Import the compiled stylesheet and you will now have access to all the Uniform goodness, it's that simple!

```html
<link rel="stylesheet" href="styles.css" />
```

<div class="mb-10"></div>

<h4><span class="w-6 h-6 mr-2 inline-flex align-items-center justify-content-center font-sm font-600 leading-none bg-blue-500 leading-1 color-white radius-round">3</span> Configure Uniform (optional)</h4>

You can customize Uniform directly in your stylesheet. For more information on what can be customized, visit the page on <a class="hover.underline" href="/get-started/configuration/">configuration</a>.

```scss
@use "uniform" as * with (
  $important: true,
  $prefix: myProject,
  $colors: (
    custom-color-1: red,
    custom-color-2: blue
  )
);
```

> If you're unfamiliar with the `@use` rule or configuring modules in this way, you can learn more about the new Sass module system <a class="hover.underline" href="https://sass-lang.com/blog/the-module-system-is-launched" target="_black">here.</a>

---

### Using the jsDelivr CDN

For a even quicker way to get started, simply add Uniform through **jsDelivr CDN**.

```html
<link rel="stylesheet" href="https://www.jsdelivr.com/package/npm/uniformcss" />
```

> Unlike the native installation, using the pre-packaged version of Uniform will only allow for customizations for attributes such as fonts, sizes and colors, you will get access to advanced customization options such as prefixing, custom variants, and custom breakpoints etc.

---

### Install with NPM

Run the following command to install Uniform as a package.

```bash
npm i uniformcss
```

---

### Download Project Directly

To download the project directly, please visit the Github repository.

<a class="font-600" href="https://github.com/ThinkUniform/UniformCSS" target="_blank">Visit Github Repository <i class="fas fa-external-link-alt ml-2"></i></a>
