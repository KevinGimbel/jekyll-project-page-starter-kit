---
title: "Usage"
in_page_link: usage
---

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
