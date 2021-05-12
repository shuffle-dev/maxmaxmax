
# maxmaxmax

Add the two best Tailwind CSS features to Bootstrap and Bulma!

## Motivation

We are the team that created [Shuffle](https://shuffle.dev), a visual editor for Tailwind CSS, Bootstrap, Bulma, and Material-UI.  We create 2-4 new UI libraries per month for these frameworks, and then we add them to our editor.

Tailwind CSS has the greatest number of them in Shuffle because the easiest way for us is to create a new library in this technology in the first place. Only later do we port a library to subsequent technologies. 

Why development in Tailwind CSS is the fastest (for us)? 

We have been thinking about it and according to our subjective assessment it is about ***two features that are responsible for 80% of the convenience in building a layout with Tailwind CSS***. 

___
<sup>* If you are interested in how we port the UI library from Tailwind CSS to Bootstrap, please check [Zeus for Tailwind CSS](https://shuffle.dev/project/new-project?library=tailwind-zeus/1.0.0) and [Zeus for Bootstrap](https://shuffle.dev/project/new-project?library=bootstrap-zeus/1.0.0) in our editor.</sup>


## 🥇 Two best Tailwind CSS features

### 1. Much larger range of spacing-values in the basic version. 

Have you ever used such a structure in HTML in order to give the container the largest possible spacing without writing your own CSS? 

```html
<div class="mt-5 pt-5">
    // Content
</div>
```

Bootstrap and Bulma in the basic version provide spacing values in the range 0 - 3rem, divided into six classes, e.g. mt-0, mt-1, mt-2, mt-3, mt-4, mt-5.

Tailwind CSS has 30 of these classes in the range of 0 - 24rem. The classes are named using the format {property}{sides}-{size} where size is one of 0-12,14,16,20,24,28,32,36,40,44,48,52,56,60,64,72,80,96.

This extension adds identical values to the resulting CSS as in Tailwind CSS. 

![](https://static.shuffle.dev/files/drake-1.png)

### 2. The .max-w-* classes that allow the width of the container to be managed "rigidly". 

Have you ever used such a structure in Bootstrap in order to give the section header the maximum width? Or the equivalent for Bulma?

```html
<div class="row”>
   <div class="col-12 col-lg-6 mx-auto">
       <h2>Section header</h2>
       <p>Description</h2>
   </div>
</div>
```

The main problem with this solution is that in any resolution the text can be broken somewhere else, because the .col-lg-6 class uses percentages. 

![](https://static.shuffle.dev/files/drake-2.gif)

The ***maxmaxmax*** extension adds similar classes to Bootstrap and Bulma as in Tailwind CSS, so that you can create such structures as:

```html
<div class="container">
    <div class="max-w-3xl mx-auto">
       <h2>Section header</h2>
       <p>Description</h2>
    </div>
</div>
```

Thanks to it, the section header will always have the same width, regardless of the resolution used by the user. 

___
<sup>* Please check class names for each framework in the Bootstrap and Bulma section below. We keep the naming standard from the base framework.</sup>

## Bootstrap

### Added feature #1

The ***maxmaxmax*** extension adds new classes to Bootstrap to manage spacing (for example, .mt-\*, .pb-\* and their negative values, e.g. .mt-n5). 

The names of these classes are analogous to those in the basic version of Bootstrap. 


```css
.mt-8
.mt-sm-8
.mt-md-8
.mt-lg-8
.mt-xl-8
.mt-xxl-8

// Negative
.mt-n8
.mt-sm-n8
.mt-md-n8
.mt-lg-n8
.mt-xl-n8
.mt-xxl-n8
```


View the files:
- [scss/bootstrap/maxmaxmax/_variables.scss](scss/bootstrap/maxmaxmax/_variables.scss)

### Added feature #2

The second novelty are the classes for managing the width of the container ("rigidly") and their responsive values, the full list of classes:

```css
.mw-0 { max-width: 0rem; }
.mw-none { max-width: none; }
.mw-xs { max-width: 20rem; }
.mw-sm { max-width: 24rem; }
.mw-md { max-width: 28rem; }
.mw-lg { max-width: 32rem; }
.mw-xl { max-width: 36rem; }
.mw-2xl { max-width: 42rem; }
.mw-3xl { max-width: 48rem; }
.mw-4xl { max-width: 56rem; }
.mw-5xl { max-width: 64rem; }
.mw-6xl { max-width: 72rem; }
.mw-7xl { max-width: 80rem; }
```

Each class has its own responsive version, for example: 

```css
.mw-lg-0 { max-width: 0rem; }
.mw-lg-none { max-width: none; }
.mw-lg-xs { max-width: 20rem; }
.mw-lg-sm { max-width: 24rem; }
.mw-lg-md { max-width: 28rem; }
.mw-lg-lg { max-width: 32rem; }
.mw-lg-xl { max-width: 36rem; }
.mw-lg-2xl { max-width: 42rem; }
.mw-lg-3xl { max-width: 48rem; }
.mw-lg-4xl { max-width: 56rem; }
.mw-lg-5xl { max-width: 64rem; }
.mw-lg-6xl { max-width: 72rem; }
.mw-lg-7xl { max-width: 80rem; }
```

View the files:
- [scss/bootstrap/maxmaxmax/_extension-max-width.scss](scss/bootstrap/maxmaxmax/_extension-max-width.scss)

## Bulma

### Added feature #1

The ***maxmaxmax*** extension adds new classes to Bulma to manage spacing (for example, .mt-\*, .pb-\* and their negative values, e.g., .mt-n5). 

The names of these classes are analogous to those in the basic version of Bulma. The novelty are the responsive versions:


```css
.mt-8-mobile
.mt-8-tablet
.mt-8-tablet-only
.mt-8-touch
.mt-8-desktop
.mt-8-desktop-only
.mt-8-widescreen
.mt-8-widescreen-only
.mt-8-fullhd
```

View the files:
- [scss/bulma/maxmaxmax/_variables.scss](scss/bulma/maxmaxmax/_variables.scss)
- [scss/bulma/maxmaxmax/_extension-max-spacing.scss](scss/bulma/maxmaxmax/_extension-max-spacing.scss)

### Added feature #2

The second novelty are the classes for managing the width of the container ("rigidly") and their responsive values, the full list of classes:


```css
.has-mw-0 { max-width: 0rem; }
.has-mw-none { max-width: none; }
.has-mw-xs { max-width: 20rem; }
.has-mw-sm { max-width: 24rem; }
.has-mw-md { max-width: 28rem; }
.has-mw-lg { max-width: 32rem; }
.has-mw-xl { max-width: 36rem; }
.has-mw-2xl { max-width: 42rem; }
.has-mw-3xl { max-width: 48rem; }
.has-mw-4xl { max-width: 56rem; }
.has-mw-5xl { max-width: 64rem; }
.has-mw-6xl { max-width: 72rem; }
.has-mw-7xl { max-width: 80rem; }
```

Each size has its own responsive version, for example: 

```css
.has-mw-3xl
.has-mw-3xl-mobile
.has-mw-3xl-tablet
.has-mw-3xl-tablet-only
.has-mw-3xl-touch
.has-mw-3xl-desktop
.has-mw-3xl-desktop-only
.has-mw-3xl-widescreen
.has-mw-3xl-widescreen-only
.has-mw-3xl-fullhd
```

View the files:
- [scss/bulma/maxmaxmax/_variables.scss](scss/bulma/maxmaxmax/_variables.scss)
- [scss/bulma/maxmaxmax/_extension-max-width.scss](scss/bulma/maxmaxmax/_extension-max-width.scss)

## How to use it

1. You can download the resulting CSS file from the ./dist/ directory. 
2. You can compile your version locally, using npm.

```bash
npm install
npm run css
```

3. You can also copy the ***maxmaxmax*** directory from the suitable framework and add these options to your existing project. 

## Why "maxmaxmax"?

- This repository is related to three frameworks.
- Helpers for max-width are new features added to Bootstrap and Bulma.
- We add a lot of spacing options for Bootstrap and Bulma.
- The extended CSS is maaaaxed! That's why you need to read the next section about PurgeCSS. 

## Limitations

Adding these two features enlarges the resulting CSS file at least twice. Therefore, in a production environment, you should use such tools as ***PurgeCSS*** that will remove unused CSS code from the resulting file. 

In the attached repository, there is an example of using PurgeCSS (`npm run purge-bootstrap` or `npm run purge-bulma`), which retrieves a list of used classes from the ./public/ directory and then creates the resulting file for Bootstrap/Bulma in the ./purged directory. 
