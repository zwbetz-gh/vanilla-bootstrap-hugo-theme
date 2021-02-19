# Vanilla Bootstrap

[![Netlify Status](https://api.netlify.com/api/v1/badges/c8f8a93c-33b9-48bc-b4d8-500c79b1b0ae/deploy-status)](https://app.netlify.com/sites/vanilla-bootstrap-hugo-theme/deploys)

A vanilla [Bootstrap](https://getbootstrap.com/) theme for [Hugo](https://gohugo.io/).

## Table of Contents

* [Demo](#demo)
* [Minimum Hugo version](#minimum-hugo-version)
* [Installation](#installation)
* [Updating](#updating)
* [Run example site](#run-example-site)
* [Configuration](#configuration)
* [Homepage content](#homepage-content)
* [Shortcodes](#shortcodes)
    * [bootstrap-blockquote](#bootstrap-blockquote)
    * [bootstrap-table](#bootstrap-table)
    * [bootstrap-card](#bootstrap-card)
* [Getting help](#getting-help)
* [Credits](#credits)

## Demo

https://vanilla-bootstrap-hugo-theme.netlify.com/

## Minimum Hugo version

Hugo version `0.60.1` or higher is required. View the [Hugo releases](https://github.com/gohugoio/hugo/releases) and download the binary for your OS.

## Installation

From the root of your site:

```
git submodule add https://github.com/zwbetz-gh/vanilla-bootstrap-hugo-theme.git themes/vanilla-bootstrap-hugo-theme
```

## Updating

From the root of your site:

```
git submodule update --remote --merge
```

## Run example site

From the root of `themes/vanilla-bootstrap-hugo-theme/exampleSite`:

```
hugo server --themesDir ../..
```

## Configuration

Copy `config.yaml` from the [`exampleSite`](https://github.com/zwbetz-gh/vanilla-bootstrap-hugo-theme/tree/master/exampleSite), then edit as desired.

## Homepage content

By default, the homepage uses the config file's `homeText` param for content.

If you wish to provide content from a file, then create `content/_index.md` and it will be used instead. For example:

```
---
title: Home
---

Homepage content goes here.
```

## Shortcodes

### bootstrap-blockquote

Uses [Bootstrap blockquotes](https://getbootstrap.com/docs/4.3/content/typography/#blockquotes) to format your blockquotes nicely. Pass the quote inside the shortcode. The `author` argument is optional.

[Here's an actual usage](https://raw.githubusercontent.com/zwbetz-gh/vanilla-bootstrap-hugo-theme/master/exampleSite/content/post/quotes-by-carl-jung.md), and here's an example usage:

```
{{< bootstrap-blockquote author="Carl Jung" >}}
Knowing your own darkness is the best method for dealing with the darknesses of other people.
{{< /bootstrap-blockquote >}}
```

### bootstrap-table

Uses [Bootstrap tables](https://getbootstrap.com/docs/4.3/content/tables/) to format your tables nicely. Pass the markdown table inside the shortcode, then pass the classes as an argument.

[Here's an actual usage](https://raw.githubusercontent.com/zwbetz-gh/vanilla-bootstrap-hugo-theme/master/exampleSite/content/post/style-a-markdown-table-with-bootstrap-classes-in-hugo.md), and here's an example usage:

```
{{< bootstrap-table "table table-dark table-striped table-bordered" >}}
| Animal  | Sounds |
|---------|--------|
| Cat     | Meow   |
| Dog     | Woof   |
| Cricket | Chirp  |
{{< /bootstrap-table >}}
```

### bootstrap-card

Uses [Bootstrap cards](https://getbootstrap.com/docs/4.3/components/card/) and [Hugo image processing](https://gohugo.io/content-management/image-processing/#readout) to display your [page bundle](https://gohugo.io/content-management/page-bundles/) images nicely. Only the `img`, `command`, and `options` arguments are required.

[Here's an actual usage](https://raw.githubusercontent.com/zwbetz-gh/vanilla-bootstrap-hugo-theme/master/exampleSite/content/post/nasa-images/index.md), and here's an example usage:

```
{{< bootstrap-card
img="sun.jpg"
command="Resize"
options="700x"
title="The Sun"
text="The Sun is the star at the center of the Solar System."
alt="sun"
class="mb-3"
style="" >}}
```

## Getting help

If you run into an issue that isn't answered by this documentation or the [`exampleSite`](https://github.com/zwbetz-gh/vanilla-bootstrap-hugo-theme/tree/master/exampleSite), then visit the [Hugo forum](https://discourse.gohugo.io/). The folks there are helpful and friendly. **Before** asking your question, be sure to read the [requesting help guidelines](https://discourse.gohugo.io/t/requesting-help/9132).

## Credits

In addition to Bootstrap and Hugo, thank you to:

* [Feather](https://feathericons.com/) for icons
* [Netlify](https://www.netlify.com/) for deploys
* [gh-md-toc](https://github.com/ekalinin/github-markdown-toc) for toc generation
* [vscode](https://code.visualstudio.com/) for text editing
* [Fedora](https://getfedora.org/), [Xfce](https://www.xfce.org/), and [VirtualBox](https://www.virtualbox.org/) for development environment
* [befunky](https://www.befunky.com/) for screenshot editing
* [Freepik](https://www.freepik.com/) and [Flaticon](https://www.flaticon.com/) for favicon
