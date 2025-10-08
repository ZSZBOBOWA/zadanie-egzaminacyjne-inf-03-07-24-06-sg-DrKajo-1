# Podział strony HTML i CSS Float - Powtórka do egzaminu INF.03

## 📚 CZĘŚĆ TEORETYCZNA

### 1. Znaczniki HTML5 do budowy strony

HTML5 wprowadził specjalne znaczniki semantyczne, które pomagają podzielić stronę na logiczne części:

#### Podstawowe znaczniki:

- **`<header>`** - nagłówek strony (góra)
- **`<nav>`** - menu nawigacyjne
- **`<main>`** - główna treść strony
- **`<section>`** - sekcja/część strony
- **`<article>`** - artykuł, wpis, samodzielna treść
- **`<aside>`** - boczny panel, dodatkowe informacje
- **`<footer>`** - stopka strony (dół)

#### Prosty schemat strony:

```
┌─────────────────────┐
│     <header>        │  ← Nagłówek
├─────────────────────┤
│     <nav>           │  ← Menu
├──────────┬──────────┤
│  <main>  │ <aside>  │  ← Treść + Panel boczny
│          │          │
├──────────┴──────────┤
│     <footer>        │  ← Stopka
└─────────────────────┘
```

### 2. Właściwość CSS: float

**Float** pozwala "wypływać" elementom na prawą lub lewą stronę.

#### Wartości float:

- **`float: left;`** - element wypływa w lewo
- **`float: right;`** - element wypływa w prawo
- **`float: none;`** - element nie wypływa (domyślnie)

#### Ważna zasada!

Po elementach z float trzeba **wyczyścić opływanie** używając:
```css
clear: both;
```

### 3. Właściwości CSS do formatowania bloków

Oprócz float, do formatowania bloków używamy wielu innych właściwości CSS:

#### Wymiary:
- **`width`** - szerokość elementu (np. `width: 50%;` lub `width: 300px;`)
- **`height`** - wysokość elementu (np. `height: 200px;`)
- **`min-height`** - minimalna wysokość (np. `min-height: 400px;`)
- **`max-width`** - maksymalna szerokość (np. `max-width: 1200px;`)

#### Odstępy:
- **`margin`** - odstęp NA ZEWNĄTRZ elementu
  - `margin: 10px;` - ze wszystkich stron
  - `margin: 10px 20px;` - góra/dół lewo/prawo
  - `margin-top`, `margin-right`, `margin-bottom`, `margin-left` - pojedyncze strony
- **`padding`** - odstęp WEWNĄTRZ elementu (działa tak samo jak margin)

#### Obramowanie:
- **`border`** - ramka wokół elementu
  - `border: 1px solid black;` - grubość, styl, kolor
  - `border-radius: 5px;` - zaokrąglone rogi

#### Tło:
- **`background-color`** - kolor tła (np. `background-color: lightblue;`)
- **`background-image`** - obrazek w tle (np. `background-image: url('obraz.jpg');`)

#### Tekst:
- **`color`** - kolor tekstu
- **`text-align`** - wyrównanie tekstu (left, center, right, justify)
- **`font-size`** - rozmiar czcionki (np. `font-size: 18px;`)
- **`font-family`** - rodzaj czcionki (np. `font-family: Arial, sans-serif;`)

#### Wyświetlanie:
- **`display`** - sposób wyświetlania (block, inline, none)
- **`overflow`** - co zrobić z zawartością wykraczającą poza blok (hidden, auto, scroll)

#### Ważna właściwość:
- **`box-sizing: border-box;`** - sprawia, że padding i border są WLICZANE w szerokość elementu
  - Bez tego: width 100% + padding 20px = element szerszy niż 100%!
  - Z tym: width 100% zawiera już padding i border

#### Przykład różnicy box-sizing:

```css
/* BEZ box-sizing */
.blok1 {
    width: 100%;
    padding: 20px;
    border: 2px solid black;
    /* Rzeczywista szerokość: 100% + 40px padding + 4px border = ZA SZEROKIE! */
}

/* Z box-sizing */
.blok2 {
    width: 100%;
    padding: 20px;
    border: 2px solid black;
    box-sizing: border-box;
    /* Rzeczywista szerokość: dokładnie 100% (padding i border wliczone) */
}
```

### 4. Zewnętrzny plik CSS

W egzaminie INF.03 style CSS są zawsze w **oddzielnym pliku**.

#### Struktura projektu:
```
projekt/
├── index.html
└── style.css
```

#### Podłączenie pliku CSS w HTML:
```html
<head>
    <meta charset="UTF-8">
    <title>Tytuł strony</title>
    <link rel="stylesheet" href="style.css">
</head>
```

---

## 💡 PRZYKŁADY

### Przykład 1: Prosty układ dwukolumnowy

**Plik: index.html**
```html
<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <title>Dwukolumnowy układ</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Moja Strona</h1>
    </header>

    <nav>
        <a href="#">Strona główna</a>
        <a href="#">O nas</a>
        <a href="#">Kontakt</a>
    </nav>

    <main>
        <h2>Treść główna</h2>
        <p>To jest główna część strony z artykułami.</p>
    </main>

    <aside>
        <h3>Panel boczny</h3>
        <p>Dodatkowe informacje i linki.</p>
    </aside>

    <footer>
        <p>Stopka © 2024</p>
    </footer>
</body>
</html>
```

**Plik: style.css**
```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

header {
    background-color: lightblue;
    padding: 20px;
    text-align: center;
}

nav {
    background-color: lightgray;
    padding: 10px;
}

nav a {
    margin: 0 10px;
    text-decoration: none;
    color: black;
}

main {
    float: left;
    width: 70%;
    background-color: lightyellow;
    padding: 20px;
    min-height: 400px;
}

aside {
    float: right;
    width: 28%;
    background-color: lightgreen;
    padding: 20px;
    min-height: 400px;
}

footer {
    clear: both;
    background-color: lightcoral;
    padding: 20px;
    text-align: center;
}
```

### Przykład 2: Trzy kolumny produktów

**Plik: produkty.html**
```html
<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <title>Produkty</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Sklep Internetowy</h1>
    </header>

    <section class="produkty">
        <article class="produkt">
            <h3>Produkt 1</h3>
            <p>Opis produktu pierwszego</p>
        </article>

        <article class="produkt">
            <h3>Produkt 2</h3>
            <p>Opis produktu drugiego</p>
        </article>

        <article class="produkt">
            <h3>Produkt 3</h3>
            <p>Opis produktu trzeciego</p>
        </article>
    </section>

    <div class="clearfix"></div>

    <footer>
        <p>Sklep © 2024</p>
    </footer>
</body>
</html>
```

**Plik: style.css**
```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

header {
    background-color: navy;
    color: white;
    padding: 30px;
    text-align: center;
}

.produkty {
    width: 100%;
    padding: 20px;
}

.produkt {
    float: left;
    width: 30%;
    margin: 1.5%;
    padding: 20px;
    background-color: #f0f0f0;
    border: 1px solid #ccc;
}

.clearfix {
    clear: both;
}

footer {
    background-color: #333;
    color: white;
    padding: 20px;
    text-align: center;
}
```

---

## ✏️ ZADANIA DO POWTÓRKI

### Zadanie 1 (łatwe)
Stwórz pliki `index.html` i `style.css`. W HTML dodaj `<header>` i `<footer>`. W CSS ustaw nagłówek na tło niebieskie, stopkę na czerwone.

### Zadanie 2 (łatwe)
Dodaj znacznik `<nav>` między nagłówkiem a stopką. W CSS ustaw tło menu na szare i padding 15px.

### Zadanie 3 (łatwe)
Dodaj znacznik `<main>` z tekstem "Strona główna". W CSS ustaw tło żółte, padding 20px i czcionkę 18px.

### Zadanie 4 (średnie)
Stwórz dwa elementy `<div>` z klasami "lewy" i "prawy". W CSS ustaw dla klasy .lewy: `float: left` i szerokość 48%. Dla klasy .prawy: `float: right` i szerokość 48%.

### Zadanie 5 (średnie)
Stwórz układ: `<main>` (float: left, szerokość 65%) i `<aside>` (float: right, szerokość 32%). Oba mają mieć min-height: 300px.

### Zadanie 6 (średnie)
Do zadania 5 dodaj `<footer>` z właściwością `clear: both` w CSS. Sprawdź, że stopka jest pod obiema kolumnami.

### Zadanie 7 (średnie)
Utwórz trzy sekcje `<section>` z klasą "kolumna". W CSS ustaw dla .kolumna: float: left, width: 30%, margin: 1.5%.

### Zadanie 8 (średnie)
Dodaj po sekcjach z zadania 7 pusty `<div class="clearfix"></div>`. W CSS dodaj `.clearfix { clear: both; }`.

### Zadanie 9 (trudne)
Zbuduj kompletną stronę w dwóch plikach (HTML + CSS):
- `<header>` - tło #333, kolor tekstu biały
- `<nav>` - tło #666, linki w poziomie
- `<main>` - float: left, width: 70%, tło białe
- `<aside>` - float: right, width: 28%, tło #f5f5f5
- `<footer>` - clear: both, tło #333, tekst biały

### Zadanie 10 (trudne)
Wewnątrz `<main>` dodaj dwa znaczniki `<article>` z klasą "wpis". W CSS ustaw .wpis: float: left, width: 48%, margin: 1%, padding: 15px, background: #eee.

### Zadanie 11 (trudne)
Stwórz siatkę 4 bloków (2x2): Użyj `<section class="blok">` cztery razy. W CSS: .blok ma float: left, width: 48%, margin: 1%, height: 200px. Po drugim bloku dodaj `<div class="clearfix"></div>`.

### Zadanie 12 (trudne)
Zmodyfikuj zadanie 11: dodaj właściwość `box-sizing: border-box` i ramkę `border: 2px solid black` dla wszystkich bloków. Sprawdź, że układ się nie rozjeżdża.

### Zadanie 13 (bardzo trudne - typ egzaminacyjny)
Odtwórz layout typowy dla INF.03:
- Nagłówek na całą szerokość, wysokość 100px
- Menu poziome (linki obok siebie)
- Lewa kolumna 25% (kategorie)
- Prawa kolumna 73% (treść główna)
- Stopka na całą szerokość
Wszystkie style w zewnętrznym pliku CSS.

### Zadanie 14 (bardzo trudne - typ egzaminacyjny)
Stwórz układ sklepu:
- `<aside class="kategorie">` - float: left, 20%, lista kategorii
- `<main class="produkty">` - float: right, 78%
- Wewnątrz main: 4 elementy `<article class="produkt">` - każdy float: left, width: 23%, margin: 1%
- Wszystko w osobnym pliku CSS

### Zadanie 15 (bardzo trudne - typ egzaminacyjny)
Odtwórz poniższy układ używając HTML5 i float w zewnętrznym CSS:
```
┌────────────────────────────┐
│         HEADER             │ (height: 80px)
├────────────────────────────┤
│         NAV                │ (height: 50px)
├─────────┬──────────────────┤
│  ASIDE  │   ARTICLE 1      │
│  (25%)  ├──────────────────┤
│         │   ARTICLE 2      │
│         │                  │
├─────────┴──────────────────┤
│         FOOTER             │ (height: 60px)
└────────────────────────────┘
```

Wymagania:
- Wszystkie style w pliku style.css
- Użyj znaczników HTML5
- Artykuły obok siebie w głównej sekcji (po 2 w rzędzie)
- Poprawne użycie float i clear

---

## 📝 WSKAZÓWKI DO EGZAMINU INF.03

### Struktura plików
✅ Zawsze twórz oddzielny plik `style.css`  
✅ Podłącz CSS w sekcji `<head>` używając `<link rel="stylesheet" href="style.css">`  
✅ Pamiętaj o `<!DOCTYPE html>` i `<html lang="pl">`

### Dobre praktyki CSS
✅ Używaj `box-sizing: border-box` dla wszystkich elementów  
✅ Resetuj marginesy i paddingi używając selektora `*`  
✅ Zawsze dodawaj `clear: both` po sekcjach z float

### Typowe wymagania na egzaminie
✅ Układ dwu- lub trzykolumnowy  
✅ Znaczniki semantyczne HTML5  
✅ Float do pozycjonowania  
✅ Zewnętrzny plik CSS  
✅ Menu poziome  
✅ Responsywne szerokości (w %)

## ⚠️ CZĘSTE BŁĘDY NA EGZAMINIE

❌ Style w HTML zamiast w osobnym pliku CSS  
❌ Zapomnienie o `<link>` w sekcji `<head>`  
❌ Brak `clear: both` w stopce  
❌ Suma szerokości + marginesy > 100%  
❌ Błędna ścieżka do pliku CSS  
❌ Używanie `<div>` zamiast znaczników HTML5

## 🎯 SCHEMAT PRACY NA EGZAMINIE

**Krok 1:** Stwórz strukturę plików (index.html + style.css)  
**Krok 2:** Napisz szkielet HTML ze znacznikami HTML5  
**Krok 3:** Podłącz plik CSS w `<head>`  
**Krok 4:** Dodaj reset CSS (`* { margin: 0; padding: 0; box-sizing: border-box; }`)  
**Krok 5:** Styluj kolejne sekcje od góry do dołu  
**Krok 6:** Użyj float dla układu kolumnowego  
**Krok 7:** Dodaj clear: both po sekcjach z float  
**Krok 8:** Przetestuj w przeglądarce

---

## 📋 WZÓR STRUKTURY PLIKÓW

**index.html**
```html
<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <title>Tytuł</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>...</header>
    <nav>...</nav>
    <main>...</main>
    <aside>...</aside>
    <footer>...</footer>
</body>
</html>
```

**style.css**
```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Twoje style tutaj */
```

---

**Powodzenia na egzaminie INF.03!** 💪🎓

---

## 📖 JAK KORZYSTAĆ Z TEGO MATERIAŁU?

### Dla ucznia:

Ten materiał powtórkowy został przygotowany specjalnie dla Ciebie, aby pomóc Ci przygotować się do egzaminu **INF.03** z zakresu podziału dokumentu HTML na bloki i formatowania CSS.

#### Krok 1: Otwórz ten plik w Visual Studio Code

1. Uruchom program **Visual Studio Code**
2. Kliknij **File** (Plik) → **Open File** (Otwórz plik)
3. Znajdź i otwórz plik: **`html_css_material.md`**
4. Plik otworzy się w edytorze - zobaczysz tekst z formatowaniem

#### Krok 2: Zobacz podgląd pliku Markdown

Aby zobaczyć materiał w ładniejszej formie:

1. Naciśnij skrót klawiszowy: **`Ctrl + Shift + V`** (Windows/Linux) lub **`Cmd + Shift + V`** (Mac)
2. Lub kliknij prawym przyciskiem myszy na otwartym pliku i wybierz **"Open Preview"**
3. Zobaczysz ładnie sformatowany dokument z kolorami i układem

#### Krok 3: Ucz się krok po kroku

1. **Przeczytaj teorię** - zrozum podstawowe pojęcia
2. **Obejrzyj przykłady** - zobacz, jak to działa w praktyce
3. **Rozwiązuj zadania** - zacznij od łatwych (zadanie 1-3), potem trudniejsze
4. **Testuj w przeglądarce** - sprawdzaj, czy Twój kod działa

#### Krok 4: Twórz pliki z przykładami

Kiedy będziesz przerabiać przykłady:

1. Stwórz nowy folder, np. `przyklad1`
2. Skopiuj kod HTML z materiału i zapisz jako `index.html`
3. Skopiuj kod CSS z materiału i zapisz jako `style.css`
4. Otwórz plik `index.html` w przeglądarce (Chrome, Firefox, Edge)

#### Krok 5: Rozwiązuj zadania

Dla każdego zadania:

1. Stwórz nowy folder (np. `zadanie1`, `zadanie2`)
2. Utwórz pliki `index.html` i `style.css`
3. Napisz kod zgodnie z poleceniem
4. Sprawdź wynik w przeglądarce
5. Porównaj z przykładami z materiału

---

### 💡 WSKAZÓWKI DO NAUKI

#### Jeśli coś nie działa:
- ✅ Sprawdź, czy plik CSS jest w tym samym folderze co HTML
- ✅ Sprawdź, czy nazwa pliku to dokładnie `style.css`
- ✅ Sprawdź, czy masz `<link rel="stylesheet" href="style.css">` w sekcji `<head>`
- ✅ Otwórz narzędzia programisty w przeglądarce (klawisz **F12**) i sprawdź błędy

#### Jak pracować z materiałem:
- 📝 Rób notatki na marginesie (możesz edytować plik .md)
- ✏️ Zaznaczaj kolorem zadania, które już zrobiłeś
- 🔄 Wracaj do trudnych zadań po kilku dniach
- 👥 Pracuj w parze z kolegą/koleżanką - wyjaśniajcie sobie nawzajem

#### Plan nauki:
- **Dzień 1:** Teoria + Przykład 1 + Zadania 1-3
- **Dzień 2:** Przykład 2 + Zadania 4-8
- **Dzień 3:** Zadania 9-12
- **Dzień 4:** Zadania 13-15 (egzaminacyjne)
- **Dzień 5:** Powtórka wszystkich zadań

---

### 🆘 POTRZEBUJESZ POMOCY?

Jeśli masz problem:
1. Przeczytaj sekcję **"CZĘSTE BŁĘDY NA EGZAMINIE"**
2. Sprawdź **"WSKAZÓWKI DO EGZAMINU INF.03"**
3. Zobacz jeszcze raz przykłady
4. Zapytaj nauczyciela na lekcji

---

### ✅ LISTA KONTROLNA PRZED EGZAMINEM

Sprawdź, czy umiesz:
- [ ] Utworzyć dwa pliki: index.html i style.css
- [ ] Podłączyć CSS do HTML używając znacznika `<link>`
- [ ] Używać znaczników HTML5: header, nav, main, aside, footer, section, article
- [ ] Stosować właściwość `float: left` i `float: right`
- [ ] Ustawiać szerokość elementów w procentach
- [ ] Używać `clear: both` po elementach z float
- [ ] Dodawać padding, margin i border
- [ ] Ustawiać kolory tła (background-color)
- [ ] Wyrównywać tekst (text-align)
- [ ] Tworzyć układ dwukolumnowy (main + aside)
- [ ] Tworzyć układ trzykolumnowy (3 sekcje obok siebie)
- [ ] Resetować style używając selektora `*`
- [ ] Stosować `box-sizing: border-box`

Jeśli zaznaczyłeś wszystkie pola - jesteś gotowy! 🎉

**Powodzenia na egzaminie INF.03!** 💪🎓