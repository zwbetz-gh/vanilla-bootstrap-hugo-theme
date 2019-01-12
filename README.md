# Vanilla Bootstrap

A vanilla [Bootstrap](https://getbootstrap.com/) theme for [Hugo](https://gohugo.io/). 

## Table of Contents

* [Demos](#demos)
* [Minimum Hugo Version](#minimum-hugo-version)
* [Installation](#installation)
* [Updating](#updating)
* [Run Example Site](#run-example-site)
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
| Hugo Themes demo, weekly-ish updates | https://themes.gohugo.io//theme/vanilla-bootstrap-hugo-theme/ | 

## Minimum Hugo Version

This theme **requires** Hugo version `0.48` or higher. Take a look at the [Hugo releases](https://github.com/gohugoio/hugo/releases) and download the binary for your OS.

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

## Run Example Site

From the root of `themes/vanilla-bootstrap-hugo-theme/exampleSite`:

```
hugo server --themesDir ../..
```

## Configuration

Copy the `config.toml` or `config.yaml` from the [`exampleSite`](https://github.com/zwbetz-gh/vanilla-bootstrap-hugo-theme/tree/master/exampleSite), then edit as desired. 

## Shortcodes

### bootstrap-blockquote

Uses [Bootstrap blockquotes](https://getbootstrap.com/docs/4.2/content/typography/#blockquotes) to format your blockquotes nicely. Pass the quote inside the shortcode. The `author` argument is optional. 

[Here's an actual usage](https://raw.githubusercontent.com/zwbetz-gh/vanilla-bootstrap-hugo-theme/master/exampleSite/content/post/quotes-by-carl-jung.md), and here's an example usage:

```
{{% bootstrap-blockquote author="Carl Jung" %}}
Knowing your own darkness is the best method for dealing with the darknesses of other people.
{{% /bootstrap-blockquote %}}
```

### bootstrap-table

Uses [Bootstrap tables](https://getbootstrap.com/docs/4.2/content/tables/) to format your tables nicely. Pass the markdown table inside the shortcode, then pass the classes as an argument. 

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

Uses [Bootstrap cards](https://getbootstrap.com/docs/4.2/components/card/) and [Hugo image processing](https://gohugo.io/content-management/image-processing/#readout) to display your [page bundle](https://gohugo.io/content-management/page-bundles/) images nicely. Only the `img`, `command`, and `options` arguments are required. 

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

## Getting Help

If you run into an issue that isn't answered by this documentation or the [`exampleSite`](https://github.com/zwbetz-gh/vanilla-bootstrap-hugo-theme/tree/master/exampleSite), then head over to the [Hugo discussion forum](https://discourse.gohugo.io/). The folks there are helpful and friendly. **Before** asking your question, be sure to read the [requesting help guidelines](https://discourse.gohugo.io/t/requesting-help/9132). Feel free to tag me in your question, my username there is [`@zwbetz`](https://discourse.gohugo.io/u/zwbetz/summary).

## Credits

In addition to Bootstrap and Hugo, thank you to:

* [Feather](https://feathericons.com/) for icons
* [Netlify](https://www.netlify.com/) for deploys
* [gh-md-toc](https://github.com/ekalinin/github-markdown-toc) for toc generation
* [vscode](https://code.visualstudio.com/) for text editing
* [Fedora](https://getfedora.org/), [Xfce](https://www.xfce.org/), and [VirtualBox](https://www.virtualbox.org/) for development environment
* [befunky](https://www.befunky.com/) for screenshot editing
* [Freepik](https://www.freepik.com/) and [Flaticon](https://www.flaticon.com/) for favicon
