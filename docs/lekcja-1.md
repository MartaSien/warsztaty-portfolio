---
icon: lucide/rocket
---

# Lekcja 1: Przygotowanie środowiska

## Git

Tworzymy folder naszego repozytorium

```bash
mkdir my-project
cd my-project
```

Inicjujemy repozytorium w aktualnym folderze.

```
git init
```

Tworzymy pusty plik Markdown (md).

```
touch README.md
```

Sprawdzamy czy nam się udało.

```
git status
```

??? info "Taki powinien być wynik komendy:"
    ```bash
    On branch master

    No commits yet

    Untracked files:
    (use "git add <file>..." to include in what will be committed)
            README.md

    nothing added to commit but untracked files present (use "git add" to track)
    ```


### Tworzymy pierwszy commit

```
git stage README.md
```

```
git commit -m "Add README.md"
```

### Dlaczego programiści używają git?

> [A brief introduction to Git for beginners | GitHub](https://www.youtube.com/watch?v=r8jQ9hVA2qs)
Git to najbardziej znany system kontroli wersji (ale nie jedyny).
Wyobraź sobie, że zamiast komendy `cofnij` masz dostęp do całej historii pliku. Mógłbyś sprawdzić:

> - kto zrobił daną zmianę
> - jak wyglądał plik `n` operacji temu
> - dlaczego plik został zmieniony

Programiści wykorzystują git by:

- śledzić historię zmian w plikach
- mieć dostęp do starszych wersji plików
- współpracować równolegle z innymi na jednym pliku
- zapisywać kilka wariantów tego samego projektu

## Visual Studio Code

IDE (Integrated Development Environment) - darmowy edytor kodu, który oferuje wiele narzędzi ułatwiających programowanie. Na przykład, formatowanie, wykrywanie błędów w kodzie źródłowym, integracja z `git` i pełno wtyczek dodatkowo rozszerzających jego funkcje.

### Instalacja

- [download Visual Studio Code](https://code.visualstudio.com/download?_exp_download=d53503e735)

### Wstęp

#### Otwieramy nasze repozytorium `my-project`.

#### Tworzymy nowy branch i robimy na nim zmiany

```
git branch "initial-python-script"
```

#### Tworzymy plik .gitignore

Plik `.gitignore` służy do wyszczególniania plików i folderów, których nie chcemy udostępnić innym - pliki cache, sekrety, lokalne ustawienia. Zmiany w tych plikach nie będą śledzone przez `git`.

??? info ".gitignore"
    ```bash
    __pycache__
    ```

Tutaj tworzymy commit tak jak [poprzednio](#tworzymy-pierwszy-commit).

#### Tworzymy prosty skrypt w Python

??? info "hello-world.py"
    ```python
    print("Hello, World")
    ```

Testujemy czy działa i również go commitujemy (tu ściągniesz i zainstalujesz [Python](https://www.python.org/)).

### Merge'ujemy zmiany do brancha głównego

Przechodzimy na główny branch:

```bash
git switch master
```

Łączymy zmiany z brancha `initial-python-script`:

```bash
git merge initial-python-script
```

Sprawdzamy historię commitów:

```bash
git log
```

Po udanym merge'u branch roboczy nie jest już potrzebny, więc możemy go usunąć:

```bash
git branch -d initial-python-script
```

### Revertujemy zmianę, której nie chcemy mieć w repo

`git revert` nie usuwa historii. Tworzy nowy commit, który odwraca zmiany z wybranego commita.

Najpierw sprawdzamy identyfikator commita:

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
