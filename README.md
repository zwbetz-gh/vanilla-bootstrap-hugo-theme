# Vanilla Bootstrap

A vanilla [Bootstrap](https://getbootstrap.com/) theme for [Hugo](https://gohugo.io/). 

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

## Configuration

Copy the `config.toml` or `config.yaml` from the [`exampleSite`](https://github.com/zwbetz-gh/vanilla-bootstrap-hugo-theme/tree/master/exampleSite), then edit as desired. Make sure to **uncomment** the `theme` line. 

## Shortcodes

### bootstrap-blockquote

This will format your quotes nicely, using [Bootstrap quote classes](https://getbootstrap.com/docs/4.1/content/typography/#blockquotes). To use it, pass the quote inside the shortcode. The `author` argument is optional. Example usage:

```
{{% bootstrap-blockquote author="Laura Ingalls" %}}
I am beginning to learn that it is the sweet, **simple** things of life which are the real ones after all.  
{{% /bootstrap-blockquote %}}
```

### bootstrap-table

This will add [Bootstrap table classes](https://getbootstrap.com/docs/4.1/content/tables/) to your markdown tables. To use it, pass the markdown table inside the shortcode, then pass the classes. Example usage:

```
{{< bootstrap-table "table table-dark table-striped table-bordered" >}}
| Animal  | Sounds |
|---------|--------|
| Cat     | Meow   |
| Dog     | Woof   |
| Cricket | Chirp  |
{{< /bootstrap-table >}}
```

## Getting Help

If you run into an issue that isn't answered by this documentation, then head over to the [Hugo Discussion Forum](https://discourse.gohugo.io/). The folks there are helpful and friendly. **Before** asking your question, be sure to read the [requesting help guidelines](https://discourse.gohugo.io/t/requesting-help/9132). Feel free to tag me in your question, my username there is [`@zwbetz`](https://discourse.gohugo.io/u/zwbetz/summary).