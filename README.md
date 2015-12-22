# jekyll-project-page-starter-kit
#### Quickly create single-page project pages

### Demos 
- [vhost](http://kevingimbel.com/vhost) 
- [Page for this project](http://kevingimbel.com/jekyll-project-page-starter-kit/)

### About
This Jekyll Project Page Starter Kit is a starting point for creating project pages hosted on GitHub Pages. It is very opinionated and made for [myslef](https://twitter.com/_kevinatari), currently used for the [vhost project](http://kevingimbel.com/vhost). You can, however, fork it or get inspired by this skeleton to create your own version.

### Usage
To use the [Jekyll Project Page Starter Kit](https://github.com/kevingimbel/jekyll-project-page-starter-kit), clone the repository somewhere, create a `gh-pages` branch for your project and copy the files over.

```sh
$ cd /path/to/workspace
$ git clone https://github.com/kevingimbel/jekyll-project-page-starter-kit
$ cd /path/to/project
$ git checkout -b gh-pages
$ cp -R jekyll-project-page-starter-kit /path/to/your/project
```
Now you need to edit the content inside the `_content` directory. The ordering in which the files are rendered to the page are defined by the numbers inside the name. So - for this page - `1_about.md` is rendered before `2_usage.md` and so on. Every file has the following [Front Matter](http://jekyllrb.com/docs/frontmatter/):

```yaml
---
title: "Usage"
in_page_link: usage
---
```

The `title` is used as the card title, `the in_page_link` is used to link to the page section. The rest of the file is then put inside the card content.

### Project YAML file

The main configuration file is the `project.yml` file inside the `_data` folder. It is here were you configure what is written in the header, the footer, what keywords and twitter/search descriptions to output and so on.

```yaml
- accentcolor: '#FFEB3B'
  twitter_description: 'Jekyll Project Page Starter is a Starter Kit for quickly creating project overview pages'
  search_description: 'Jekyll Project Page Starter is a Starter Kit for quickly creating project overview pages'
  keywords: 'project page, starter kit, jekyll, static site, github pages'
  title: 'Jekyll Project Page Starter Kit'
  name: 'Jekyll Project Page Starter Kit'
  sub_title: 'Quickly create single-page project pages'
  url: 'jekyll-project-page-starter-kit'
  repo_url: 'https://github.com/kevingimbel/jekyll-project-page-starter-kit'
  gitter: 'https://gitter.im/kevingimbel/jekyll-project-page-starter-kit'
  author:
    name: 'Kevin Gimbel'
    url: 'http://kevingimbel.com'

```

Everything should be self explaining, expect the accentcolor. This is used to [Create Android 5.0+ theme colors](http://kevingimbel.com/snippet-theme-color-android-5-0/). If you've questions ask them over at [Gitter](https://gitter.im/kevingimbel/jekyll-project-page-starter-kit).

### Customization

You can customize whatever you want. All the rendering is done inside the `_layouts/front-page.html` file. The Header and Footer come from the `_includes` directory.  The colors used by the theme are mostly configurable with the `_config.scss` file inside `src/sass/` - all other styles come from the `style.scss` file. The generated code is compressed with the use of the `compress.html` file in `_layouts`. I recommend to keep this.

#### Jekyll and Ruby

To run the site, either run `$ bundle install` followed by `$ guard` or the good old `$ jekyll serve`. You'll need to have [Ruby](https://www.ruby-lang.org/en/) and [Jekyll](http://jekyllrb.com/) setup to build the site locally.

#### NPM, Node, Sass and Gulp

By default the Sass compiling is done with Node, Libsass and Gulp. You'll need to run `$ npm install` from the directory to install all dependencies. From then on run `$ gulp` to compile the CSS files.
