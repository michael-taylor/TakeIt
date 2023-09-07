---
author: "Hugo Authors"
title: "Hugo Standard Shortcodes"
date: "2023-09-02"
description: "Article describing Hugo standard shortcodes."
tags: ["markdown", "css", "html", "themes"]
categories: ["themes", "syntax"]
---

<!--more-->

Here are the shortcodes built in to Hugo and demonstrations of their use.

## `figure`

`figure` is an extension of the image syntax in Markdown, which does not provide a shorthand for the more semantic HTML5 `<figure>` element.

{{< figure src="elephant.png" title="An AI generated image of an elephant" >}}

## `gist`

A shortcode to display a [GitHub](https://github.com) gist.

{{< gist jmooring 50a7482715eac222e230d1e64dd9a89b >}}

## `highlight`

The `highlight` shortcode provides code highlighting with more options than the standard Markdown style.

{{< highlight go-html-template "lineNos=inline, lineNoStart=42" >}}
{{ range .Pages }}
  <h2><a href="{{ .RelPermalink }}">{{ .LinkTitle }}</a></h2>
{{ end }}
{{< /highlight >}}

## Instagram

{{< admonition warning >}}
TODO: Need to get authentication token for this.
{{< /admonition >}}

## `param`

The `param` shortcode gets a value from the current Page's parameters set in front matter, with a fallback to the site parameter value. It will log an ERROR if the parameter with the given key could not be found in either.

Page tags: {{< param tags >}}

## `ref` and `relref`

These shortcodes will look up the pages by their relative path (e.g., `blog/post.md`) or their logical name (`post.md`) and return the permalink (`ref`) or relative permalink (`relref`) for the found page.

The markup:
```
Link to basic syntax post: {{</* ref "posts/basic-syntax/index.md" */>}}.
```
will output:

Link to basic syntax post: {{< ref "posts/basic-syntax/index.md" >}}.

## `tweet`

A shortcode that can display a Tweet.

{{< tweet user="SanDiegoZoo" id="1453110110599868418" >}}

## `vimeo`

To display a Vimeo video with this URL:

| https://vimeo.com/channels/staffpicks/55073825

include this in your markdown:

```
{{</* vimeo 55073825 */>}}
```

and this will be rendered:

{{< vimeo 55073825 >}}

## `youtube`

The `youtube` shortcode embeds a responsive video player for YouTube videos using only the video ID.

{{< youtube w7Ft2ymGmfc >}}