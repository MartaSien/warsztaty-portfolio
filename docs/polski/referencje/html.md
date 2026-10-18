---
icon: lucide/code-xml
---

# HTML w 5 min

## Popularne znaczniki

| Znacznik | Opis |
| --- | --- |
| `<html></html>` | Główny element dokumentu HTML |
| `<head></head>` | Metadane dokumentu, np. tytuł i kodowanie |
| `<title></title>` | Tytuł strony wyświetlany na karcie przeglądarki |
| `<body></body>` | Treść strony widoczna w przeglądarce |
| `<header></header>` | Nagłówek strony lub sekcji |
| `<nav></nav>` | Sekcja z nawigacją |
| `<main></main>` | Główna, unikalna treść strony |
| `<section></section>` | Tematyczna sekcja dokumentu |
| `<article></article>` | Samodzielna treść, np. wpis lub artykuł |
| `<footer></footer>` | Stopka strony lub sekcji |
| `<h1></h1>`–`<h6></h6>` | Nagłówki - mają strukturę hierarchiczną od `<h1>` do `<h6>` |
| `<p></p>` | Akapit tekstu |
| `<a href=""></a>` | Odnośnik do innej strony lub miejsca w dokumencie (w `href=` podajemy adres docelowy) |
| `<img src="" alt="">` | Obraz; `alt` zawiera jego tekstowy opis |
| `<strong></strong>` | Ważny fragment tekstu |
| `<em></em>` | Fragment tekstu z naciskiem |
| `<div></div>` | Blokowy kontener bez określonego znaczenia semantycznego |
| `<span></span>` | Liniowy kontener bez określonego znaczenia semantycznego |
| `<ul></ul>` | Lista nieuporządkowana |
| `<ol></ol>` | Lista uporządkowana |
| `<li></li>` | Element listy |
| `<br>` | Podział wiersza |
| `<form></form>` | Formularz do przesyłania danych |
| `<label></label>` | Etykieta pola formularza |
| `<input>` | Pole formularza, np. tekstowe lub wyboru |
| `<button></button>` | Przycisk |

## Tabela

``` html
<table> <!-- (1)! -->
    <tr> <!-- (2)! -->
        <th>Imię psa</th> <!-- (3)! -->
        <th>Rasa</th>
        <th>Wiek (lata)</th>
    </tr> <!-- (4)! -->
    <tr>
        <td>Klusek</td>
        <td>Mieszaniec</td>
        <td>4</td>
    </tr>
    <tr>
        <td>Alba</td>
        <td>Mops</td>
        <td>3</td>
    </tr>
</table> <!-- (5)! -->
```

1. Rozpoczęcie tabel
2. Nowy wiersz
3. Komórka tabeli
4. Zamknięcie wiersza 
5. Zamknięcie tabeli

<table>
    <tr>
        <th>Imię psa</th>
        <th>Rasa</th>
        <th>Wiek (lata)</th>
    </tr>
    <tr>
        <td>Klusek</td>
        <td>Mieszaniec</td>
        <td>4</td>
    </tr>
    <tr>
        <td>Alba</td>
        <td>Mops</td>
        <td>3</td>
    </tr>
</table>