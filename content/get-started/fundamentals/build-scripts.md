---
title: Build Scripts
date: 1000-01-02
---

{% include shortcodes/chapter, text: 'Fundamentals', color: 'teal' %}

### Build Scripts

Uniform relies on Sass, PostCSS and CleanCSS to compile, auto-prefix and optimize before outputting CSS. The following **npm build commands** help perform and automate these tasks.

> By default, the build scripts will automatically input `styles.scss` and output files into the root directory. You can modify the output location inside `package.json` to change this default behavior.

---

#### uniform

The following command will compile Sass and run deep optimizations to your CSS. This is the command you should run when outputting for **production**.

```bash
npm run uniform
```

---

#### uniform:compile

The following command will only compile Sass and output CSS.

```bash
npm run uniform:compile
```

---

#### uniform:dev

The following command is will compile, autoprefix, and run basic optimizations to your CSS before outputting. This command is designed to be used for development purposes.

```bash
npm run uniform:dev
```

---

#### uniform:watch

The following command will run `npm run uniform:dev` and repeatedly run this command as changes are detected.

```bash
npm run uniform:watch
```

---

#### uniform:autoprefix

The following command will automatically apply **vendor prefixes** to your CSS. 

```bash
npm run uniform:autoprefix
```

> Default browserlist queries are applied (`> 0.5%, last 2 versions, Firefox ESR, not dead`). To learn more about browserlist queries <a class="hover.underline" href="https://github.com/browserslist/browserslist">click here</a>. 

---

#### uniform:groupmedia

The following command will group similar media queries and put them at the end of your stylesheet in the order of breakpoint pixel size.

```bash
npm run uniform:groupmedia
```

> It is important to note, due to the way Uniform is built, you must run this command after compiling or include this build process in your own project in order to ensure your styles are ordered and displayed correctly.

---

#### uniform:cleancss

The following command will run deep `level 2` minification to your CSS.

```bash
npm run uniform:cleancss
```
