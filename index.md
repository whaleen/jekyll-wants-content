---
layout: page
title: Home
---

All content you see on this website is generated from files in the ```_data``` directory.

- _data/article.csv creates the collection Articles (These can have chronology)
- _data/sections.csv creates the collection Sections (The Main Navigation is generated from these)
- _data/config.yml everything else comes from here.

### Settings

Settings for importing from csv are defined by collections in the root/_config.yml file

```collections:
  sections:
    output: true
    source: sections.csv
    id_key: pid
    layout: section
  articles:
    output: true
    source: articles.csv
    id_key: pid
    layout: article
```


The Pagemaster plugin is how the collection pages are imported.


``` $ bundle exec jekyll pagemaster articles```

``` $ bundle exec jekyll pagemaster sections```

_This will not overwrite previously generated pages._


### Skinning

Get skins from
https://bootswatch.com/

Replace the following

- _sass/_variables.scss
- _sass/_bootstrap_customization.scss

Jekyll will rebuild when either of those are edited.

By this point there should be a unique enough looking site which can be tuned up as desired. Setting the container width is a good first step if your going to do serious modifications.

### Components

Zillions of places with pre-made Components/Snippets

This is a good example:

https://startbootstrap.com/snippets/

These can be married with liquid to build out whatever components we need depending on the context of the site.

Article lists, Category pages, Individual article pages, Contact pages, etc...

Each of these have as many components to choose from as we develop.
