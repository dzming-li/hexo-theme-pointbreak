# Hexo-theme-pointbreak

## Installation

### Install

npm install:

```
npm install git+https://github.com/dzming-li/hexo-theme-pointbreak.git --force
```

### Enable

Modify `theme` setting in `_config.yml` to `landscape`.

``` diff
_config.yml
- theme: some-theme
+ theme: landscape
```

## Configuration

It is recommended not to modify `theme/landscape/_config.yml` but to use the `theme_config` section of `_config.yml` or to create `_config.landscape.yml` (see [Alternate Theme Config](https://hexo.io/docs/configuration#Alternate-Theme-Config)).

``` yml
# Header
menu:
  Home: /
  Archives: /archives
rss: /atom.xml
banner: images/banner.jpg
subtitle: This a subtitle

# Content
excerpt_link: Read More
fancybox: true
recent_posts_limits: 5
# Footer
copyright: |-
  <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-nd/4.0/88x31.png" /></a></br>
  All website licensed under <a href="https://creativecommons.org/licenses/by-nc-nd/4.0/" target="_blank">CC BY-NC-ND 4.0</a></br>

# Sidebar
sidebar: right
widgets:
- category
- tag
- tagcloud
- archive
- recent_posts

# Miscellaneous
google_analytics:
favicon: /favicon.png
twitter:

# Header links
# Each name must correspond to the icon name of Fork Awesome
# https://forkaweso.me/Fork-Awesome/icons/
#links:
#  github: https://github.com/your_github_account
#  twitter: https://twitter.com/your_twitter_account
#  telegram: https://t.me/your_telegram_account
```

- **menu** - Navigation menu
- **rss** - RSS link
- **banner** - Path of title banner image of page top
- **excerpt_link** - "Read More" link at the bottom of excerpted articles. `false` to hide the link.
- **fancybox** - Enable [Fancybox]
- **recent_posts_limits** - How many posts display in Home page.
- **sidebar** - Sidebar style. You can choose `left`, `right`, `bottom` or `false`.
- **widgets** - Widgets displaying in sidebar
- **google_analytics** - Google Analytics ID
- **favicon** - Favicon path
- **twitter** - Twitter ID
- **links** - Header links with icon, specified links will appear at the top right corner of the page

## Features

### Fancybox

Landscape uses [Fancybox] to showcase your photos. You can use Markdown syntax or fancybox tag plugin to add your photos.

```
![img caption](img url)

{% fancybox img_url [img_thumbnail] [img_caption] %}
```

### Sidebar

You can put your sidebar in left side, right side or bottom of your site by editing `sidebar` setting.

Landscape provides 5 built-in widgets:

- category
- tag
- tagcloud
- archives
- recent_posts

All of them are enabled by default. You can edit them in `widget` setting.

### Header links

You can add links to the header area with icons.

```
social:
  github: https://github.com/your_github_account
  twitter: https://twitter.com/your_twitter_account
  telegram: https://t.me/your_telegram_account
```

[Hexo]: https://hexo.io/
[Fancybox]: https://github.com/fancyapps/fancyBox
