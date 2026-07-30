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
git status
```

```
git stage README.md
```

```
git commit -m "Add README.md"
```

```
git status
```

### Dlaczego programiści używają git?

> [A brief introduction to Git for beginners | GitHub](https://www.youtube.com/watch?v=r8jQ9hVA2qs)

Co gdybyś zamiast komendy `cofnij` miał dostęp do całej historii pliku? Mógłbyś sprawdzić:
- kto zrobił daną zmianę
- jak wyglądał plik `n` operacji temu
- dlaczego plik został zmieniony

- by śledzić historię zmian w plikach
- by mieć dostęp do starszych wersji plików
- by współpracować równolegle z innymi na jednym pliku
- by zapisywać kilka wariantów tego samego projektu
- to najbardziej znany system kontroli wersji (ale nie jedyny)

## Visual Studio Code

### Instalacja

- [download Visual Studio Code](https://code.visualstudio.com/download?_exp_download=d53503e735)

### Wstęp

1. Otwórz stworzone wcześniej repozytorium.
1. 

- tworzymy i tłumaczymy plik .gitignore
- tworzymy nowy branch i robimy na nim zmiany
- merge'ujemy zmiany do brancha głównego
- revertujemy zmianę, której nie chcemy mieć w repo