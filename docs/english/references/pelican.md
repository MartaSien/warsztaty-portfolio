# Pelican in 5 min

- [Pelican docs](https://docs.getpelican.com/en/latest/)

## Installation

```
python -m pip install "pelican[markdown]"
```

## Project initialization

```
pelican-quickstart
```

## Building the site

```
pelican content
```

## Local site preview

```
pelican --listen
```

## Metadata

In Pelican, added at the top of the page:

W Pelican, dodawane na górze strony:

```markdown
Title: Example Post
Date: 2024-11-14
Category: Markdown Tutorial
Tags: pelican, markdown, tutorial
Slug: example-post
Author: Your Name
Summary: A quick overview of markdown formatting in Pelican.
```

## Embedding media on the site

```html
<iframe width="560" height="315" src="https://www.youtube.com/embed/fC9PZrvA6ho?si=gQNO57FM2IYzUzA4" frameborder="0" allowfullscreen></iframe>
```

<iframe width="560" height="315" src="https://www.youtube.com/embed/fC9PZrvA6ho?si=gQNO57FM2IYzUzA4" frameborder="0" allowfullscreen></iframe>

## Pelican themes

The appearance of a Pelican site varies greatly depending on the theme used.

- [GitHub | pelican-themes](https://github.com/getpelican/pelican-themes)
- [pelicanthemes.com](https://pelicanthemes.com/)

## Pelican plugins

Pelican’s functionality is extended through plugins.

- [GitHub | pelican-plugins](https://github.com/pelican-plugins)

### Plugins that may be useful

- [search](https://github.com/pelican-plugins/search) - adds a search option to the site
- [image-process](https://github.com/pelican-plugins/image-process) - optimizes images included on the site
