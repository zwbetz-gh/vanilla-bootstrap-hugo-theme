# Vanilla Bootstrap

A vanilla [Bootstrap](https://getbootstrap.com/) theme for [Hugo](https://gohugo.io/). 

## Table of Contents

* [Demos](#demos)
* [Minimum Hugo Version](#minimum-hugo-version)
* [Installation](#installation)
* [Updating](#updating)
* [Run Against the Example Site Locally](#run-against-the-example-site-locally)
* [Configuration](#configuration)
* [Shortcodes](#shortcodes)
    * [bootstrap-blockquote](#bootstrap-blockquote)
    * [bootstrap-table](#bootstrap-table)
    * [bootstrap-card](#bootstrap-card)
* [Getting Help](#getting-help)
* [Credits](#credits)

## Demos

| Env | URL |
| --- | --- |
| Dev demo, immediate updates | https://vanilla-bootstrap-hugo-theme.netlify.com/ |
| Hugo Themes demo, weekly-ish updates | TODO | 

## Minimum Hugo Version

This theme **requires** Hugo version `0.48` or higher. Take a look at the [Hugo releases](https://github.com/gohugoio/hugo/releases) and download the binary for your OS.

## Installation

```
git submodule add https://github.com/zwbetz-gh/vanilla-bootstrap-hugo-theme.git themes/vanilla-bootstrap-hugo-theme
```

## Updating

```
git submodule update --remote --merge
```

## Run Against the Example Site Locally

From the root of the theme directory: 

```
hugo server \
--gc \
--renderToDisk \
--source exampleSite \
--config exampleSite/config.yaml \
--themesDir ../.. \
--theme vanilla-bootstrap-hugo-theme
```

## Configuration

Copy the `config.toml` or `config.yaml` from the [`exampleSite`](https://github.com/zwbetz-gh/vanilla-bootstrap-hugo-theme/tree/master/exampleSite), then edit as desired. Make sure to **uncomment** the `theme` line. 

## Shortcodes

### bootstrap-blockquote

This will format your quotes nicely, with [Bootstrap blockquotes](https://getbootstrap.com/docs/4.1/content/typography/#blockquotes). To use it, pass the quote inside the shortcode. The `author` argument is optional. Example usage:

```
{{% bootstrap-blockquote author="Laura Ingalls" %}}
I am beginning to learn that it is the sweet, **simple** things of life which are the real ones after all.  
{{% /bootstrap-blockquote %}}
```

### bootstrap-table

This will format your tables nicely, with [Bootstrap table classes](https://getbootstrap.com/docs/4.1/content/tables/). Pass the markdown table inside the shortcode, then pass the classes as an argument. Example usage:

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

This will display your [page bundle](https://gohugo.io/content-management/page-bundles/) images nicely, with [Bootstrap cards](https://getbootstrap.com/docs/4.2/components/card/) and [Hugo image processing](https://gohugo.io/content-management/image-processing/#readout). To `img`, `command`, and `options` arguments are required. All other arguments are optional. Example usage: 

```
{{< bootstrap-card 
img="sun.jpg" 
command="Resize" 
options="700x" 
title="The Sun"
text="The Sun is the star at the center of the Solar System."
alt="sun" 
class="mb-3" >}}
```

## Getting Help

If you run into an issue that isn't answered by this documentation, then head over to the [Hugo discussion forum](https://discourse.gohugo.io/). The folks there are helpful and friendly. **Before** asking your question, be sure to read the [requesting help guidelines](https://discourse.gohugo.io/t/requesting-help/9132). Feel free to tag me in your question, my username there is [`@zwbetz`](https://discourse.gohugo.io/u/zwbetz/summary).

## Credits

In addition to Bootstrap and Hugo, thank you to:

* [Feather](https://feathericons.com/) for icons
* [Netlify](https://www.netlify.com/) for deploys
* [gh-md-toc](https://github.com/ekalinin/github-markdown-toc) for toc generation
* [vscode](https://code.visualstudio.com/) for text editing
* [Fedora](https://getfedora.org/) and [VirtualBox](https://www.virtualbox.org/) for development environment
