# Bits.sass arrange

Component for arranging/aligning horizontal cells, a bit like flexbox.

Read more about [Bits.sass toolkit](https://github.com/bits-sass/bits.sass).

## Installation

* __Bower:__ `bower install --save bits-sass-arrange`
* __Download:__ [zip](https://github.com/bits-sass/arrange/zipball/master), [tar.gz](https://github.com/bits-sass/arrange/tarball/master)
* __Git:__ `git clone https://github.com/bits-sass/arrange.git`

## Available SASS variables

* `bits-components-ns` - components namespace, defaults to 'bits-'
* `bits-arrange-gutter` - size of inter-cell gutter (used by `Arrange--withGutter`)

## Available classes

* `Arrange` - core component class
* `Arrange--middle` - modifier class for middle-aligned cells
* `Arrange--bottom` - modifier class for bottom-aligned cells
* `Arrange--equal` - modifier class for equal-width cells
* `Arrange--withGutter` - modifier class for a 10px inter-cell gutter
* `Arrange-sizeFit` - child class for cells to snap to fit their content
* `Arrange-sizeFill` - child class for cells to expand to fill the remaining space

## Usage

Like many Bits.sass components, `bits-sass-arrange` relies on a base component
class that is extended by any number of additional modifier classes.
This component works best for small-scale UI layout, for example, image-content
pairs:

```html
<div class="Arrange">
  <div class="Arrange-sizeFit">
    <img src="img.png" alt="">
  </div>
  <div class="Arrange-sizeFill">
    Lorem ipsum dolor sit amet.
    …
  </div>
</div>
```

Or for an equally spaced row of buttons or icons, etc.

```html
<ul class="Arrange Arrange--equal">
  <li class="Arrange-sizeFill">
    <button class="Button Button--full">Reply</button>
  </li>
  <li class="Arrange-sizeFill">
    <button class="Button Button--full">Like</button>
  </li>
  <li class="Arrange-sizeFill">
    <button class="Button Button--full">Save</button>
  </li>
  <li class="Arrange-sizeFill">
    <button class="Button Button--full">Remove</button>
  </li>
</ul>
```

If you want to change the default gutter associated with the
`Arrange--withGutter` modifier, you can do so by modifying the
`bits-arrange-gutter` variable.

N.B. This component affects the width of images in cells.

## Requirements

* Sass 3.2+

## Browser support

* Google Chrome (latest)
* Opera (latest)
* Firefox 4+
* Safari 5+
* Internet Explorer 8+