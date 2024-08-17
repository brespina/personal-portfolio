+++
title = "configuring apollo"
date = "2024-07-09"

[taxonomies]
tags=["documentation"]

[extra]
repo_view = true
+++

## theme mode (`theme`)

sets the color theme for your blog.

- type: string
- options: "light", "dark", "auto", "toggle"
- default: "toggle"
- usage: `theme = "toggle"`

the "toggle" option allows users to switch between light and dark modes, while "auto" typically follows the user's system preferences.

## menu 

defines the navigation menu items for your blog.

- type: array of objects
- default: []
- usage:
  ```toml
  menu = [
      { name = "/posts", url = "/posts", weight = 1 },
      { name = "/projects", url = "/projects", weight = 2 },
      { name = "/about", url = "/about", weight = 3 },
      { name = "/tags", url = "/tags", weight = 4 },
  ]
  ```

## socials

defines the social media links. 

- type: array of objects
- default: []
- usage:
  ```toml
  socials = [
    { name = "twitter", url = "https://twitter.com/not_matthias", icon = "twitter" },
    { name = "github", url = "https://github.com/not-matthias/", icon = "github" },
  ]
  ```

## table of contents (`toc`)

enables or disables the table of contents for posts.

- type: boolean
- default: true
- usage: `toc = true`

when enabled, a table of contents will be generated for posts, making it easier for readers to navigate through longer articles.

## cdn usage (`use_cdn`)

determines whether to use a content delivery network (cdn) for assets.

- type: boolean
- default: false
- usage: `use_cdn = false`

when set to true, the theme will attempt to load assets from a cdn, which can improve loading times for visitors from different geographic locations.

## favicon (`favicon`)

specifies the path to the favicon image for your blog.

- type: string
- default: "/icon/favicon.png"
- usage: `favicon = "/icon/favicon.png"`

this sets the small icon that appears in the browser tab for your website.

## comments (`comment`)

enables or disables the comment system for posts.

- type: boolean
- default: false
- usage: `comment = false`

after making `comment = true` save your script from [giscus](https://giscus.app) to `templates/_giscus_script.html`.
when enabled, this allows readers to leave comments on your blog posts.


## fancy code styling (`fancy_code`)

enables enhanced styling for code blocks.

- type: boolean
- default: true
- usage: `fancy_code = true`

this option adds the language label and a copy button.

## dynamic notes (`dynamic_note`)

allows for the creation of togglable note sections in your content.

- type: boolean
- default: true
- usage: `dynamic_note = true`

when enabled, you can create expandable/collapsible note sections in your blog posts.

## source code (`repo_view`)

do you want to link to the source code of your blog post? you can turn on the `repo_view` inside the `[extra]` section of your blog post.

```toml
[extra]
repo_view = true
repo_url = "https://github.com/not-matthias/apollo/tree/main/content"   # alternatively add the repo here
```

the `repo_url` can be set in the `[extra]` section or in your `config.toml`.

## anchor links

you can add anchor links by adding the following to your `_index.md`:
```toml
insert_anchor_links = "heading"
```
