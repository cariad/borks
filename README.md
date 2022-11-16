# Borks: A Hugo theme

The Hugo theme for [cardboardborks.com](https://cardboardborks.com).

## Features

- Responsive; tested on iPhones and iPads
- Local fonts; no calls to Google Fonts
- No JavaScript
- OpenGraph
- Emoji favicon
- Fathom Analytics
- Resizes and converts images to WebP
- Featured images

## Installation

```console
cd <your Hugo site>
git submodule add https://github.com/cariad/borks.git themes/borks
```

In your `config.toml`, set the theme to `borks`:

```toml
theme = "borks"
```

## Configuration

### Site

In your `config.[toml|json|yaml]`:

```toml
# Your site's title.
title = "Danny's Sausages"

[Params]
# Full name of your site's author.
author = "Danny Sausages"

# URL to your site's logotype.
banner = "/logotype.svg"

# Copyright notice.
copyright = "Sausages' Sausages &copy; 1996 Danny Sausages"

# Fathom Analytics (referral link: https://usefathom.com/ref/TVWIFS) site ID.
# Optional and defaults to no Fathom integration.
fathom = "MACARONI"

# List of menu items.
[[Params.menu]]
# Menu item title.
title = "Home"

# Menu item URI.
uri = "/"

[Params.socials]
# Your site's email address.
email = "danny@sausages.local"

# Your site's Instagram username.
instagram = "xxxxxxxdannysausagesxxxxxxx"
```

### Pages

```yaml
---
# Describes the featured image for the header and OpenGraph.
# Optional and defaults to no image.
image:
  # Name of the image in your images page bundle.
  name: hello
---
```

## Images

To embed images, they must be stored in a [page bundle](https://gohugo.io/content-management/page-bundles/).

Your bundle's `index.md` should contain data like this:

```yaml
---
headless: true
resources:
  # "name" is the reference to this image from shortcodes and the "image" front
  # matter property.
  - name: parade
    params:
      # Accessible text.
      alt: An ice cream parade on Pluto.

      # Anchor point when the image is resized. Choose from "TopLeft", "Top",
      # "TopRight", "Left", "Center", "Right", "BottomLeft", "Bottom",
      # "BottomRight" or "Smart".
      # Optional and defaults to "Smart".
      anchor: Top

    src:  spine.jpg
    title: Ice Cream Parade
---
```

To embed this image in a page, use the `image` shortcode:

```markdown
Do you remember last year's ice cream parade?

{{< image parade >}}

It was so good!
```

## Contributing

Full contribution guidelines are in [CONTRIBUTING.md](CONTRIBUTING.md).

## Licences

### Fonts

Figtree is &copy; 2022 Erik Kennedy and redistributed under the [SIL Open Font License](static/fonts/figtree/OFL.txt). <!-- cspell:disable-line -->

Sriracha is &copy; 2015 Cadson Demak, Copyright &copy; 2014 Pablo Impallari and redistributed under the [SIL Open Font License](static/fonts/sriracha/OFL.txt). <!-- cspell:disable-line -->

### Theme

This theme is released under the [MIT Licence](/LICENSE) and remains the copyright of Cariad Eccleston. This grants you permission to use the theme without restriction as long as [the licence text](/LICENSE) is included with any copies that you redistribute.

**Credit is not required, but a link to [cariad/borks](https://github.com/cariad/borks), [cardboardborks.com](https://cardboardborks.com) or [cariad.earth](https://cariad.earth) would be appreciated!&nbsp;🚀**
