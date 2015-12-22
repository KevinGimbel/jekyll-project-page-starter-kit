---
title: "Customization"
in_page_link: customization
---

You can customize whatever you want. All the rendering is done inside the `_layouts/front-page.html` file. The Header and Footer come from the `_includes` directory.  The colors used by the theme are mostly configurable with the `_config.scss` file inside `src/sass/` - all other styles come from the `style.scss` file. The generated code is compressed with the use of the `compress.html` file in `_layouts`. I recommend to keep this.

### Jekyll and Ruby

To run the site, either run `$ bundle install` followed by `$ guard` or the good old `$ jekyll serve`. You'll need to have [Ruby](https://www.ruby-lang.org/en/) and [Jekyll](http://jekyllrb.com/) setup to build the site locally.

### NPM, Node, Sass and Gulp

By default the Sass compiling is done with Node, Libsass and Gulp. You'll need to run `$ npm install` from the directory to install all dependencies. From then on run `$ gulp` to compile the CSS files.
