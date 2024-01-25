# basscss-sass

Transpiled Basscss Sass partials

http://basscss.com

This repository is provided as a convenience for users working within a Sass build process.
Basscss is written in standard, spec-compliant CSS, using some new features like [custom media queries](http://dev.w3.org/csswg/mediaqueries/#custom-mq) and [custom properties](http://www.w3.org/TR/css-variables/), and is distributed across multiple modules.

If you have any choice in the matter, I highly recommend using [PostCSS](https://github.com/postcss/postcss) instead of Sass.


## Getting Started

```bash
npm install 7ds7/bass-sass
```

## Sass variables defaults

In order to override basscss defaults include the file [variables-basscss.scss](https://github.com/7Ds7/basscss-sass/blob/master/variables-basscss.scss) before importing basscss on your project.

```scss
// SHAPE VARIABLES
// relates to structure

// Breakpoints
$breakpoint-xs-grid: '(min-width: 31.3125rem)';
$breakpoint-xs: '(max-width: 40em)';
$breakpoint-sm: '(min-width: 40em)';
$breakpoint-sm-md: '(min-width: 40em) and (max-width: 52em)';
$breakpoint-md: '(min-width: 52em)';
$breakpoint-md-lg: '(min-width: 52em) and (max-width: 64em)';
$breakpoint-lg: '(min-width: 64em)';

// Typography
$h00: 4rem;
$h0: 3rem;
$h1: 2rem;
$h2: 1.5rem;
$h3: 1.25rem;
$h4: 1rem;
$h5: .875rem;
$h6: .75rem;

$line-height-1: 1;
$line-height-2: 1.125;
$line-height-3: 1.25;
$line-height-4: 1.5;
$caps-letter-spacing: .2em;
$bold-font-weight: bold;

// Widths
$width-1: 24rem;
$width-2: 32rem;
$width-3: 48rem;
$width-4: 64rem;

// Margins & Paddings
$space-1: .5rem;
$space-2: 1rem;
$space-3: 2rem;
$space-4: 4rem;

// Borders
$border-width: 1px;
$border-radius: 3px;

// Z indexes
$z1: 1;
$z2: 2;
$z3: 3;
$z4: 4;

// Forms
$form-field-padding-x: .5rem;
$form-field-padding-y: .5rem;
$form-field-height: 2.25rem;

// Range field
$range-thumb-width: $form-field-padding-x;
$range-thumb-height: ( $form-field-height - ($form-field-padding-y * 2) );
$range-track-height: ( calc($form-field-padding-y / 2) );
$range-thumb-offset: ( calc($range-thumb-height / -2) + (calc($range-track-height / 2)) );
$range-thumb-pseudo-size: $form-field-height;

// Media object
$media-object-space: $space-1;

// ASPECT VARIABLES
// relates to looks

// Colors
$aqua: #7FDBFF;
$blue: #0074D9;
$navy: #001F3F;
$teal: #39CCCC;
$green: #2ECC40;
$olive: #3D9970;
$lime: #01FF70;
$yellow: #FFDC00;
$orange: #FF851B;
$red: #FF4136;
$fuchsia: #F012BE;
$purple: #B10DC9;
$maroon: #85144B;
$white: #FFFFFF;
$silver: #DDDDDD;
$gray: #AAAAAA;
$black: #111111;

// Lighten
$darken-1: rgba(0, 0, 0, .0625);
$darken-2: rgba(0, 0, 0, .125);
$darken-3: rgba(0, 0, 0, .25);

// Darken
$lighten-1: rgba(255, 255, 255, .0625);
$lighten-2: rgba(255, 255, 255, .125);
$lighten-3: rgba(255, 255, 255, .25);
$lighten-4: rgba(255, 255, 255, .5);

// Highlight Light
$hljs-comment: $gray;
$hljs-keyword: $black;
$hljs-number: $olive;
$hljs-string: $blue;
$hljs-title: $blue;
$hljs-type: $navy;
$hljs-tag: $navy;
$hljs-attribute: $olive;
$hljs-regexp: $olive;
$hljs-symbol: $purple;
$hljs-built-in: $navy;
$hljs-preprocessor: $gray;
$hljs-deletion: $fuchsia;
$hljs-addition: $lime;
$hljs-change: $navy;
$hljs-chunk: $silver;

// Highlight Dark (comment out /replace Highlight Light)
// $hljs-comment: $silver;
// $hljs-keyword: white;
// $hljs-number: $lime;
// $hljs-string: $red;
// $hljs-title: $red;
// $hljs-type: $aqua;
// $hljs-tag: $aqua;
// $hljs-attribute: $lime;
// $hljs-regexp: $lime;
// $hljs-symbol: $fuchsia;
// $hljs-built-in: $aqua;
// $hljs-preprocessor: $silver;
// $hljs-deletion: $fuchsia;
// $hljs-addition: $lime;
// $hljs-change: $aqua;
// $hljs-chunk: $gray;

// Buttons
$button-color: #fff;
$button-background-color: $blue;
$button-small-padding-y: .25rem;
$button-small-padding-x: .5rem;
$button-big-padding-y: 1rem;
$button-big-padding-x: 1.25rem;
$button-narrow-padding-x: .5rem;
$button-font-family: inherit;
$button-font-size: inherit;
$button-font-weight: $bold-font-weight;
$button-line-height: 1.125rem;
```

## Sass Tips

Using Sass as a preprocessor can cause numerous issues when working on large scale CSS with multiple contributors. I recommend following these tips when using Sass.

- **Never use @extend.** `@extend` is an anti-pattern, and Basscss is not intended to work with this functionality in Sass.
- **Avoid Mixins** Mixins lead to unnecessary complexity, are generally poorly understood, often lead to code bloat, and do not align with Basscss's design principles.
- **Avoid Nesting Selectors** To maintain the composability of Basscss, avoid nesting selectors as much as possible.


## Contributing

**The scss files in this repository are not source files.**
They are transpiled from their respective CSS modules using the
[css-scss](https://github.com/jxnblk/css-scss) module.

Do **not** edit the scss files in this repository.

See <CONTRIBUTING.md> for more.

---

[MIT License](LICENSE.md)

