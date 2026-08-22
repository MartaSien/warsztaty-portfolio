---
icon: simple/git
---

# Git w 5 minut

## Komendy

Komendy wykonujemy w terminalu, będąc w folderze naszego repozytorium.

| Komenda | Działanie |
| --- | --- |
| `git status` | Pokazuje stan repozytorium: zmienione, nowe i przygotowane do commita pliki |
| `git log` | Pokazuje historię commitów <br>`--oneline` - tylko ostatni commit |
| `git add nazwa-pliku` | Przygotowuje konkretny plik do commita |
| `git add .` | Przygotowuje wszystkie zmienione pliki do commita |
| `git commit -m "Opis zmian"` | Zapisuje przygotowane zmiany w historii repozytorium |
| `git diff` | Pokazuje zmiany, które nie zostały jeszcze dodane przez `git add` |
| `git branch` | Wyświetla listę branchy |
| `git switch nazwa-brancha` | Przechodzi na wskazany branch |
| `git switch -c nazwa-brancha` | Tworzy nowy branch i od razu na niego przechodzi |
| `git help nazwa-komendy` | Otwiera pomoc dla wybranej komendy, np. `git help commit` |

## Przykłady

### Stwórz commit

Tworzy commit ze wszystkimi zmianami w repozytorium.

```bash
git status
git add .
git commit -m "Opis zmian"
```
