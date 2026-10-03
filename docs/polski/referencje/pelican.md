# Pelican w 5 minut

- [Pelican docs](https://docs.getpelican.com/en/latest/)

## Instalacja

```
python -m pip install "pelican[markdown]"
```

## Inicjacja projektu

```
pelican-quickstart
```

## Budowanie strony

```
pelican content
```

## Strona lokalnie

```
pelican --listen
```

## Metadane

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

## Umieszczanie mediów na stronie

```html
<iframe width="560" height="315" src="https://www.youtube.com/embed/fC9PZrvA6ho?si=gQNO57FM2IYzUzA4" frameborder="0" allowfullscreen></iframe>
```

<iframe width="560" height="315" src="https://www.youtube.com/embed/fC9PZrvA6ho?si=gQNO57FM2IYzUzA4" frameborder="0" allowfullscreen></iframe>

## Pelican themes

Wygląd strony Pelican różni się diametralnie zależnie od użytego motywu (theme).

- [GitHub | pelican-themes](https://github.com/getpelican/pelican-themes)
- [pelicanthemes.com](https://pelicanthemes.com/)

## Pelican plugins

Funkcje Pelican są rozwijane poprzez wtyczki.

- [GitHub | pelican-plugins](https://github.com/pelican-plugins)

### Wtyczki, które mogą Ci się przydać

- [search](https://github.com/pelican-plugins/search) - dodaje opcję wyszukiwania na stronie
- [image-process](https://github.com/pelican-plugins/image-process) - optymalizuje załączone na stronie obrazy