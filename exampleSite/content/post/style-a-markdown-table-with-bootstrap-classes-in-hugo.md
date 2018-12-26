---
date: 2018-12-12T12:47:56-06:00
tags: ["css", "bootstrap", "hugo"]
title: "Style a markdown table with Bootstrap classes in Hugo"
---

Inspired by [this discussion](https://discourse.gohugo.io/t/how-to-customise-tables/15661/), I wanted the ability to style a markdown table with [Bootstrap table classes](https://getbootstrap.com/docs/4.1/content/tables/). In the past, I've accomplished this by [defining the table in a data file](https://zwbetz.com/create-an-html-table-from-a-toml-data-file-in-hugo/), then building it with a shortcode. 

While this works fine, it's better for a different use case. I wanted something that meets the following criteria:

- The table is defined in markdown
- It lives in the content file, e.g. `content/post/some-post.md`
- It's styled with Bootstrap table classes

After a bit of tinkering, here's the shortcode I came up with. To use it, pass the markdown table between the shortcode, then pass the Bootstrap table classes as an argument. 

## Usage

```
{{</* bootstrap-table "table table-dark table-striped table-bordered" */>}}
| Animal  | Sounds |
|---------|--------|
| Cat     | Meow   |
| Dog     | Woof   |
| Cricket | Chirp  |
{{</* /bootstrap-table */>}}
```

## Definition

```
{{ $htmlTable := .Inner | markdownify }}
{{ $class := .Get 0 }}
{{ $old := "<table>" }}
{{ $new := printf "<table class=\"%s\">" $class }}
{{ $htmlTable := replace $htmlTable $old $new }}
{{ $htmlTable | safeHTML }}
```

## Output

{{< bootstrap-table "table table-dark table-striped table-bordered" >}}
| Animal  | Sounds |
|---------|--------|
| Cat     | Meow   |
| Dog     | Woof   |
| Cricket | Chirp  |
{{< /bootstrap-table >}}