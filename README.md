# Source for whoisNicoleHarris.com

<img src="https://travis-ci.org/nlhkabu/nlhkabu.github.io.svg?branch=master" alt="CI status"/>

This website is built with [Jekyll](http://jekyllrb.com) and hosted on Github Pages.

## Adding New Projects

New projects should be added to the `_projects` folder, named as `<slug>.md`.  Available front matter:

```yaml
---
layout: project
colors:
  default: <hex code for banner - do not include a hash symbol>
  dark: <hex code for nav - do not include a hash symbol>
  light: <hex code for borders - do not include a hash symbol>
title: <page title>
skills: [<skill 1>, <skill 2>] # e.g. HTML, UI, Django, etc.
summary: <descriptive text used for project introduction and meta description>
feature_image:
    small: /assets/<image name>.png # For screens smaller than 400px
    medium: /assets/<image name>.png # For screens smaller than 700px
    large: /assets/<image name>.png # For screens larger than 700px
site_url: <absolute path to live site url>
github_url: <absolute path to source code url>
priority: <Integer between 1 and 5> # 1 == important.  Determines ordering of projects on Homepage
sections: # Each section is separated by horizontal padding and borders - use these instead of content
- |
  ## <title of a section>
  <markdown of a section>
- |
  ## <title of the next section>
  <markdown of the next section>
---
```

## Adding Blog Posts

New posts should be added in the `_posts` folder, named as `<publish year>-<publish month>-<publish date>-<slug>.md` Available front matter:

```yaml
---
layout: post
colors:
  default: <hex code for banner - do not include a hash symbol>
  dark: <hex code for nav - do not include a hash symbol>
  light: <hex code for borders - do not include a hash symbol>
title: <post title>
summary: <descriptive text used for post introduction and meta description>
comments: <status> # Set to 'on' to enable disqus comments.  Otherwise omit.
---

<markdown content here>
```

## Editing the homepage
`index.html` can be edited directly.  Available front matter:

```yaml
---
layout: default
title: <post title>
summary: <descriptive text used meta description>
learning: <description of what I'm currently learning> # e.g. Behavior Driven Development with <a href="http://pythonhosted.org/behave/">behave</a>
---
```

## Adding new decorative images

New (randomly selected) images can be added to the banner by:

* Adding the image to `/assets/banner-images` in svg format
* Adding the image name to the `images` array in `js/main.js`
* Adding image specific styling in `_sass/_banner_images.scss`

## Serving Locally

```bash
$ jekyll serve
$ jekyll serve --drafts # Serve articles in drafts folder
```



