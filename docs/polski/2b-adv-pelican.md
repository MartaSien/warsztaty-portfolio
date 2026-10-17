# Lekcja 2: Zaawansowane funkcje Pelican

## Własny HTML

Przed chwilą mieliśmy przedwstęp do tworzenia własnych fragmentów strony HTML przy pomocy Pelican. Wejdźmy głębiej w szczegóły tej funkcji.

- Przykład na stronie [pelican-sandbox](https://martasien.github.io/pelican-sandbox/home-assistant-hs3-plan.html#home-assistant-hs3-plan)

- Ten fragment kodu to HTML + CSS - podstawowe języki opisujące wygląd i style strony internetowej. 
- Strona wygenerowana w pelican konwertuje Markdown na taki kod.
- Jeśli Markdown nie wystarczy, możemy sami zapisać część strony w HTML + CSS.

## Co warto wiedzieć o HTML?

- służy do opisania treści strony
- HTML oznacza HyperText Markup Language
- znaczniki `<tag></tag>` opisują do czego służy konkretny element, wiele z nich występuje w parach - otwierający i zamykający
- tu znajdziesz najpopularniejsze znaczniki HTML: [HTML w 5 minut](referencje/html.md)

``` html
<div class="custom-box">
    <p>
    <a href="https://hs3.pl/">Hackerspace Trójmiasto</a> (abbrv. HS3) is a community focused on technology, as well as a physical space located in Gdańsk, Poland. It is open to anyone. The space has its Home Assistant solution, alongside many iot devices. This project aims to plot the current data from these devices and show them on the Hackerspace's plan.
    <br><br>You can see the live website here:
    </p>
    <a class="button" href="https://martasien.github.io/home-assistant-hs3-plan/">martasien.github.io/home-assistant-hs3-plan</a>
</div>
```
## Co warto wiedzieć o CSS?

- Służy do opisania wyglądu strony.
- Nasza domyślna strona Pelican ma już własny plik ze stylami CSS globalnymi dla całej strony. Definiując je na konkretnej podstronie, możemy stworzyć nowe lub nadpisać istniejące.

``` css
<style>
.custom-box {
  border: 1px solid #ccc;
  padding: 1rem;
  border-radius: 8px;
}
.button {
  display: inline-block;
  padding: 0.5rem 1rem;
  background: #c00e0e;
  color: white;
  text-decoration: none;
}
</style>
```

## 📚 Zasoby

!!! info
    Poniżej znajdziecie ciekawe zasoby, które pomogą Wam w tworzeniu własnej strony. Zachęcam Was do podzielenia się swoimi i dodania ich na poniższą listę otwierając [Pull Request](https://github.com/MartaSien/warsztaty-portfolio/pulls).

- [Utopia - fluid responsive design](https://utopia.fyi/)
- [mdn Mozilla](https://developer.mozilla.org/en-US/)
- [validator.w3.org](https://validator.w3.org/) - statyczna analiza HTML