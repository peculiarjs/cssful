# @peculiarjs/cssful

Minimalistic `css` library of simple **utilitarian** classes,
focused on **positioning**, **sizing**, fast set-up and prototyping.


## What `cssful` is:
* **`just css`** — simple bits of good, old `css`
* **`lib, not a framework`** — it's here to be useful and not try to replace your current `styling` approach
* **`minimalistic`** — up to 10 sm/md size `css` files
* **`easy to setup`** — because it's plain `css`, it is easy to add to any project without hustle
* **`focused`** — this project is focused around `positioning` and `sizing` helpers,
rather than a _swiss knife_ for all the cases in the modern frontend.


## Classes naming approach

### Shortenings

It is **expected** that some utilities will be used **much more often**: `width`, `height`, `margins`
so for a better and easier readability in `HTML/JSX`, these utils names are shortened and used as mnemonics:
```css
/* "w" stands for width */
.w-100 {
  width: 100%;
}

/* "h" stands for height */
.h-100 {
  height: 100%;
}

/* "mt" stands for margin-top */
.mt-20px {
  margin-top: 20px;
}
```

### Measurement units
Majority of classes in this lib approach 2 main `measurement units`:
* `%`
* `px`

For simplicity `%` is made the default, so class `w-100` should be read like `width: 100%`.
On the opposite, absolute values like `px`, need additional `px` ending:
`mr-20px` means `margin-right: 20px`.


## Utilities

Brief overview of the classes.

### flex.css

Everything around **flexbox** properties with simple naming.

```css
.flex {
  display: flex
}
.column {
  flex-direction: column;
}
.row {
  flex-direction: row;
}
...
```

### width.css

Set of classes for approaching elements **width** in `%`.

```css
/* from 100 to 0 with a step of 5 */
.w-100 {
  width: 100%;
}
.w-95 {
  width: 95%;
}
...

.w-auto {
  width: auto;
}
```

### height.css

Same but for **height**.

```css
/* from 100 to 0 with a step of 5 */
.h-100 {
  height: 100%;
}
.h-95 {
  height: 95%;
}
...

.h-auto {
  height: auto;
}
```

### margin.css

Pretty Similiar approach to `width` and `height` classes is used for `margins`.
There are mnemonic for every margin side:
* `mt` — `margin-top`
* `mr` — `margin-right`
* `mb` — `margin-bottom`
* `ml` — `margin-left`

So for every side classes go with a step of `1px` from `0` to `20px` and then 
with a step of `5px` from `20px` to `50px`.

```css
/* top */ 
.mt-0 {
  margin-top: 0;
}
.mt-1px {
  margin-top: 1px;
}
.mt-2px {
  margin-top: 2px;
}
...

.mt-20px {
  margin-top: 20px;
}
.mt-25px {
  margin-top: 25px;
}
...

.mt-50px {
  margin-top: 50px;
}
```

### position.css

Main `positioning` helpers are created around: `relative`, `absolute`, `fixed`, `static` and `sticky` options. 
Also there are helpers for every side `top`, `right`, `bottom`, `left` with 3 values `[0, 50%, 100%]` each.

```css 
.relative {
  position: relative;
}
.absolute {
  position: absolute;
}
...

.top-0 {
  top: 0;
}
.top-50 {
  top: 50%;
}
.top-100 {
  top: 100%;
}
```