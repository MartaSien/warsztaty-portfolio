---
icon: lucide/rocket
---

# Lekcja 2: Pelican

- [Pelican docs](https://docs.getpelican.com/en/latest/)

## Instalacja

### Pobieramy bibliotekę

```bash
python -m pip install "pelican[markdown]"
```

### Tworzymy folder projektu

```
mkdir -p ~/projects/pelican-portfolio
cd ~/projects/pelican-portfolio
```

### Inicjujemy projekt

```
pelican-quickstart
```

### Dodajemy pierwszy post

Tworzymy plik `my-post.md` w folderze `content`.

Wklejamy przykładową treść posta (lub tworzymy własną):

```markdown
Title: My super title
Date: 2010-12-03 10:20
Modified: 2010-12-05 19:30
Category: Python
Tags: pelican, publishing
Slug: my-super-post
Authors: Alexis Metaireau, Conan Doyle
Summary: Short version for index and feeds

This is the content of my super blog post.
```

Dla ułatwienia, zainstalowaliśmy wcześniej Pelican z rozszerzeniem `markdown`. Pozwala nam ono na tworzenie postów w formacie Markdown. Innym dostępnym formatem jest reStructuredText.

### Uruchamiamy stronę lokalnie

```
pelican --listen
```

### Przykład

- [pelican-sandbox](https://github.com/MartaSien/pelican-sandbox) - stworzyłam tą przykładową stronę by zademonstrować Wam jak możecie rozpocząć tworzenie portfolio


### Pelican themes

Wygląd naszej strony możemy dostosować przy pomocy [themes](https://docs.getpelican.com/en/latest/pelican-themes.html). 