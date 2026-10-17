# Lekcja 2: Git i zaawansowane fukcje Pelican

## Wymagania wstępne

Ta lekcja polega na poprzednich. To dobry moment by je teraz nadrobić. 
Mamy zapas czasu. :>

1. [Przygotowanie środowiska do pracy](1-srodowisko.md)
1. [Wstęp do Pelican](1-wstep-pelican.md)

## Dlaczego programiści używają git?

Git to najbardziej znany system kontroli wersji (ale nie jedyny).

- [A brief introduction to Git for beginners | GitHub](https://www.youtube.com/watch?v=r8jQ9hVA2qs)

> Wyobraź sobie, że zamiast komendy `cofnij` masz dostęp do całej historii pliku. Mógłbyś sprawdzić:

> - kto zrobił daną zmianę
> - jak wyglądał plik `n` operacji temu
> - dlaczego plik został zmieniony

Programiści wykorzystują git by:

- śledzić historię zmian w plikach
- mieć dostęp do starszych wersji plików
- współpracować równolegle z innymi na jednym pliku
- zapisywać kilka wariantów tego samego projektu

## Wstęp

### Wstępne ustawienia git

Żeby pracować z git, najpierw musimy ustawić swoją nazwę użytkownika i e-mail. 
Możesz pominąć ten krok, jeśli już to masz. Sprawdź przy pomocy komendy:

```bash
git config user.name
git config user.email
```

Ustawienie z opcją `--global` działa dla wszystkich repozytoriów na Twoim komputerze.

Jeśli nie możesz ustawić użytkownika globalnego, możesz to zrobić lokalnie dla repozytorium. 
Pomiń `--global`; zapiszesz ustawienia użytkownika tylko w lokalnym repozytorium. Te ustawienia mają pierwszeństwo nad globalnymi.

=== "Globalnie"
    ```bash
    git config --global user.name "Twoje Imię i Nazwisko"
    git config --global user.email "twoj@email.com"
    ```

=== "Lokalnie"
    ```bash
    git config user.name "Twoje Imię i Nazwisko"
    git config user.email "twoj@email.com"
    ```

### Otwieramy nasze repozytorium `moje-portfolio`

Stworzyliśmy je na lekcji [Wstęp do Pelican](1-wstep-pelican.md).

### Tworzymy plik .gitignore

Plik `.gitignore` służy do wybierania plików i folderów, których nie chcemy udostępnić innym - pliki cache, sekrety, lokalne ustawienia. Zmiany w tych plikach nie będą śledzone przez `git`.

??? info ".gitignore"
    ```bash
    __pycache__
    ```

### Sprawdzamy czy mamy zmiany, które wymagają commitu

```
git status
``` 

Powinniśmy zobaczyć przynajmniej dopiero co stworzony plik `.gitignore`. Mogą być tu także widoczne zmiany z poprzednich zajęć, jeszcze nie scommitowane. 
Poświęć chwilę by sprawdzić czy wszystko co masz chcesz na zapisać na stałe. Usuń wszystko co niepotrzebne i stwórz commit:

```
git stage .
git commit -m "Initial pelican website"
```

### Tworzymy nowy branch

Dzięki pracy na osobnym branchu, możemy zapisywać na nim zmiany i nadal zachować naszą ostatnią działającą wersję repozytorium na branchu głównym.

```
git branch "custom-html-article"
```

Stworzymy branch, na którym wypróbujemy sobie zaawansowane funkcje html, które oferuje Pelican.

### Tworzymy nowy post

```html-post.md
Title: My Custom Page
Date: 2026-10-11
Slug: demo
Status: published

# Normal Markdown heading

This is Markdown text.

<div class="custom-box">
  <h2>Custom HTML section</h2>
  <p>You can use arbitrary HTML here.</p>
  <a class="button" href="https://getpelican.com/">Get Pelican</a>
</div>

<style>
.custom-box {
  border: 1px solid #ccc;
  padding: 1rem;
  border-radius: 8px;
}
.button {
  display: inline-block;
  padding: 0.5rem 1rem;
  background: #2563eb;
  color: white;
  text-decoration: none;
}
</style>

```

### Merge'ujemy zmiany do brancha głównego

Przechodzimy na główny branch:

```bash
git switch master
```

Łączymy zmiany z brancha `custom-html-article`:

```bash
git merge custom-html-article
```

Sprawdzamy historię commitów. Po zmerge'owaniu brancha, na naszym branchu głównym pojawiają się zmiany z brancha `custom-html-article`.


```bash
git log
```

Po udanym merge'u branch roboczy nie jest już potrzebny, więc możemy go usunąć:

```bash
git branch -d custom-html-article
```

### Revertujemy zmianę, której nie chcemy mieć w repo

`git revert` nie usuwa historii. Tworzy nowy commit, który odwraca zmiany z wybranego commita.

- Stwórz commit z dowolną treścią - za chwilę go zrevertujemy.

Najpierw sprawdzamy ID commita:

```bash
git log
```

Następnie cofamy wybrany commit:

```bash
git revert <id-commita>
```

Przykład:

```bash
git revert a1b2c3d
```

### Przydatne wtyczki

- [LiveShare](https://visualstudio.microsoft.com/services/live-share/) - pozwala na udostępnienie swojej sesji w Visual Studio Code innym i wspólną pracę nad jednym plikiem
- [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens) - pokazuje historię zmian, autorów linii kodu i informacje o commitach bezpośrednio w edytorze.
