# FORMATOWANIE TEKSTU I ELEMENTÓW W HTML/CSS

**Temat:** Listy, tabele, obrazki, formatowanie tekstu  
**Egzamin:** INF.03 - umiejętności podstawowe  
**Czas:** 3-4 godziny lekcyjne

---

## 📚 CZĘŚĆ 1: PRZYPOMNIENIE TEORII

### 🔤 1. FORMATOWANIE TEKSTU

#### Nagłówki (headings)
```html
<h1>Nagłówek poziomu 1 - największy</h1>
<h2>Nagłówek poziomu 2</h2>
<h3>Nagłówek poziomu 3</h3>
<h4>Nagłówek poziomu 4</h4>
<h5>Nagłówek poziomu 5</h5>
<h6>Nagłówek poziomu 6 - najmniejszy</h6>
```

**Ważne:** Na stronie powinien być tylko JEDEN `<h1>` (tytuł główny)

#### Formatowanie wewnątrz tekstu
```html
<p>To jest <strong>pogrubiony tekst</strong></p>
<p>To jest <em>pochylony tekst</em> (italic)</p>
<p>To jest <u>podkreślony tekst</u></p>
<p>To jest <mark>zaznaczony tekst</mark> (highlight)</p>
<p>To jest <small>mały tekst</small></p>
<p>To jest <del>przekreślony tekst</del></p>
```

#### Akapity i łamanie linii
```html
<p>To jest akapit. Tekst w akapicie.</p>
<p>To jest kolejny akapit.</p>

<p>Pierwsza linia<br>Druga linia w tym samym akapicie</p>
```

---

### 📋 2. LISTY

#### Lista punktowana (unordered list)
```html
<ul>
    <li>Element 1</li>
    <li>Element 2</li>
    <li>Element 3</li>
</ul>
```

**Wygląd:** • Element 1, • Element 2, • Element 3

#### Lista numerowana (ordered list)
```html
<ol>
    <li>Pierwszy element</li>
    <li>Drugi element</li>
    <li>Trzeci element</li>
</ol>
```

**Wygląd:** 1. Pierwszy element, 2. Drugi element, 3. Trzeci element

#### Listy zagnieżdżone
```html
<ul>
    <li>Element główny 1
        <ul>
            <li>Podelement 1.1</li>
            <li>Podelement 1.2</li>
        </ul>
    </li>
    <li>Element główny 2</li>
</ul>
```

#### Stylizacja list w CSS
```css
/* Zmiana stylu punktorów */
ul { list-style-type: square; }  /* kwadratowe punktory */
ul { list-style-type: circle; }  /* puste kółka */
ul { list-style-type: none; }    /* bez punktorów */

/* Zmiana stylu numeracji */
ol { list-style-type: upper-alpha; }  /* A, B, C */
ol { list-style-type: lower-roman; }  /* i, ii, iii */
ol { list-style-type: decimal; }      /* 1, 2, 3 (domyślne) */
```

---

### 🖼️ 3. OBRAZKI

#### Podstawowe wstawianie obrazka
```html
<img src="obrazek.jpg" alt="Opis obrazka">
```

**Atrybuty OBOWIĄZKOWE:**
- `src` - ścieżka do pliku graficznego
- `alt` - tekst alternatywny (dla osób niewidomych i gdy obrazek się nie wczyta)

#### Dodatkowe atrybuty
```html
<img src="logo.png" alt="Logo firmy" width="300" height="200">
<img src="zdjecie.jpg" alt="Zdjęcie" title="Podpowiedź po najechaniu">
```

#### Obrazek jako link
```html
<a href="strona.html">
    <img src="miniatura.jpg" alt="Kliknij aby zobaczyć więcej">
</a>
```

#### Stylizacja obrazków w CSS
```css
img {
    width: 100%;           /* szerokość 100% kontenera */
    max-width: 500px;      /* maksymalna szerokość */
    height: auto;          /* automatyczna wysokość (proporcje) */
    border: 2px solid black;
    border-radius: 10px;   /* zaokrąglone rogi */
}
```

---

### 📊 4. TABELE

#### Podstawowa struktura tabeli
```html
<table>
    <tr>
        <th>Nagłówek 1</th>
        <th>Nagłówek 2</th>
    </tr>
    <tr>
        <td>Komórka 1</td>
        <td>Komórka 2</td>
    </tr>
    <tr>
        <td>Komórka 3</td>
        <td>Komórka 4</td>
    </tr>
</table>
```

**Znaczniki:**
- `<table>` - cała tabela
- `<tr>` - wiersz (table row)
- `<th>` - nagłówek kolumny (table header) - pogrubiony
- `<td>` - zwykła komórka (table data)

#### Zaawansowana tabela z sekcjami
```html
<table>
    <thead>
        <tr>
            <th>Imię</th>
            <th>Nazwisko</th>
            <th>Wiek</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Jan</td>
            <td>Kowalski</td>
            <td>25</td>
        </tr>
        <tr>
            <td>Anna</td>
            <td>Nowak</td>
            <td>30</td>
        </tr>
    </tbody>
</table>
```

#### Łączenie komórek
```html
<!-- Łączenie w poziomie (colspan) -->
<tr>
    <td colspan="2">Ta komórka zajmuje 2 kolumny</td>
    <td>Normalna komórka</td>
</tr>

<!-- Łączenie w pionie (rowspan) -->
<tr>
    <td rowspan="2">Ta komórka zajmuje 2 wiersze</td>
    <td>Komórka 1</td>
</tr>
<tr>
    <td>Komórka 2</td>
</tr>
```

#### Stylizacja tabel w CSS
```css
table {
    width: 100%;
    border-collapse: collapse;  /* łączy ramki komórek */
}

th, td {
    border: 1px solid black;
    padding: 10px;
    text-align: left;
}

th {
    background-color: #333;
    color: white;
}

tr:nth-child(even) {
    background-color: #f2f2f2;  /* co drugi wiersz szary */
}

tr:hover {
    background-color: #ddd;  /* podświetlenie po najechaniu */
}
```

---

### 🔗 5. LINKI

#### Podstawowy link
```html
<a href="strona.html">Kliknij tutaj</a>
<a href="https://www.google.com">Link do Google</a>
```

#### Link w nowej karcie
```html
<a href="https://example.com" target="_blank">Otwórz w nowej karcie</a>
```

#### Link do sekcji na stronie
```html
<a href="#sekcja1">Przejdź do sekcji 1</a>

<!-- Gdzieś niżej na stronie -->
<h2 id="sekcja1">Sekcja 1</h2>
```

#### Link do emaila
```html
<a href="mailto:info@example.com">Napisz do nas</a>
```

#### Stylizacja linków w CSS
```css
a {
    color: blue;
    text-decoration: none;  /* usuwa podkreślenie */
}

a:hover {
    color: red;
    text-decoration: underline;
}

a:visited {
    color: purple;  /* kolor odwiedzonych linków */
}
```

---

### 📝 6. FORMULARZE (podstawy)

#### Prosty formularz
```html
<form action="wyslij.php" method="post">
    <label for="imie">Imię:</label>
    <input type="text" id="imie" name="imie">
    
    <label for="email">Email:</label>
    <input type="email" id="email" name="email">
    
    <input type="submit" value="Wyślij">
</form>
```

#### Podstawowe typy input
```html
<input type="text">        <!-- pole tekstowe -->
<input type="password">    <!-- hasło (ukryte znaki) -->
<input type="email">       <!-- email -->
<input type="number">      <!-- liczba -->
<input type="date">        <!-- data -->
<input type="checkbox">    <!-- checkbox -->
<input type="radio">       <!-- radio button -->
<input type="submit">      <!-- przycisk wyślij -->
```

#### Textarea (pole wieloliniowe)
```html
<textarea rows="5" cols="30" name="wiadomosc">
Domyślny tekst
</textarea>
```

---

## ✏️ CZĘŚĆ 2: ZADANIA DO WYKONANIA

---

### ZADANIE 1 (ŁATWE - 2 punkty)
**Temat:** Nagłówki i formatowanie tekstu

Stwórz stronę HTML z następującymi elementami:
- Nagłówek `<h1>` z tekstem "Moja pierwsza strona"
- Nagłówek `<h2>` z tekstem "O mnie"
- Akapit z Twoim imieniem (użyj `<strong>` do pogrubienia imienia)
- Akapit z opisem hobby (użyj `<em>` do podkreślenia nazwy hobby)
- Nagłówek `<h2>` z tekstem "Ulubione przedmioty"

Wszystko ostyluj w CSS:
- h1: kolor niebieski, wyśrodkowany
- h2: kolor zielony
- Tło strony: jasny szary (#f5f5f5)

---

### ZADANIE 2 (ŁATWE - 3 punkty)
**Temat:** Lista punktowana

Stwórz stronę z nagłówkiem "Moje hobby" i listą punktowaną zawierającą 5 hobby.

W CSS ustaw:
- Lista bez domyślnych punktorów (list-style-type: none)
- Każdy element listy z lewym marginesem 20px
- Każdy element listy z paddingiem 10px
- Każdy element listy z tłem #e0e0e0
- Odstęp między elementami (margin-bottom: 10px)

---

### ZADANIE 3 (ŁATWE - 3 punkty)
**Temat:** Lista numerowana

Stwórz przepis kulinarny:
- Nagłówek h1: nazwa dania
- Nagłówek h2: "Składniki"
- Lista punktowana ze składnikami (min. 5)
- Nagłówek h2: "Sposób przygotowania"
- Lista numerowana z krokami (min. 5)

Ostyluj w CSS:
- Lista numerowana: kolor tekstu #333
- Lista numerowana: każdy krok z marginesem dolnym 15px

---

### ZADANIE 4 (ŚREDNIE - 4 punkty)
**Temat:** Listy zagnieżdżone

Stwórz strukturę menu restauracji:
- Lista punktowana z kategoriami:
  - Przystawki (z zagnieżdżoną listą min. 3 dań)
  - Dania główne (z zagnieżdżoną listą min. 3 dań)
  - Desery (z zagnieżdżoną listą min. 3 dań)

W CSS:
- Lista główna: list-style-type: none
- Listy zagnieżdżone: list-style-type: circle
- Kategorie (lista główna): font-weight: bold, font-size: 20px
- Dania: font-size: 16px, kolor #555

---

### ZADANIE 5 (ŚREDNIE - 5 punktów)
**Temat:** Wstawianie obrazków

Stwórz galerię 4 obrazków:
- Nagłówek h1: "Moja galeria"
- 4 obrazki obok siebie
- Każdy obrazek z atrybutem alt
- Pod każdym obrazkiem krótki opis w `<p>`

W CSS:
- Obrazki: szerokość 23%, margin 1%
- Obrazki: ramka 2px solid black
- Obrazki: border-radius 10px
- Opisy: text-align: center, font-size: 14px

**Wskazówka:** Jeśli nie masz obrazków, użyj https://via.placeholder.com/300

---

### ZADANIE 6 (ŚREDNIE - 5 punktów)
**Temat:** Tabela podstawowa

Stwórz tabelę z planem lekcji dla jednego dnia:
- Kolumny: Godzina, Przedmiot, Sala
- Minimum 5 lekcji
- Nagłówki w `<th>`
- Dane w `<td>`

W CSS:
- Tabela: width 100%, border-collapse: collapse
- Komórki: border 1px solid black, padding 10px
- Nagłówki: tło #333, kolor biały
- Wiersze parzyste: tło #f2f2f2

---

### ZADANIE 7 (ŚREDNIE - 5 punktów)
**Temat:** Tabela z danymi

Stwórz tabelę produktów w sklepie:
- Kolumny: Nazwa produktu, Cena, Ilość, Wartość
- Minimum 5 produktów
- Wiersz nagłówkowy
- Wiersz podsumowania (RAZEM) na końcu

W CSS:
- Tabela: wyśrodkowana, szerokość 80%
- Kolumna "Cena" i "Wartość": text-align: right
- Wiersz podsumowania: font-weight: bold, background: #ffeb3b
- Tabela: hover na wierszach (background: #e0e0e0)

---

### ZADANIE 8 (TRUDNE - 6 punktów)
**Temat:** Tabela z łączeniem komórek (colspan)

Stwórz tabelę ocen:
- Pierwsza kolumna: Przedmiot
- Następne kolumny: Oceny z kolejnych miesięcy (minimum 3 miesiące)
- Ostatnia kolumna: Średnia
- Pierwszy wiersz: nagłówek z nazwą semestru łączący wszystkie kolumny (colspan)

W CSS:
- Nagłówek semestru: text-align: center, background: #4CAF50, color: white
- Średnia: font-weight: bold
- Oceny: text-align: center

---

### ZADANIE 9 (TRUDNE - 6 punktów)
**Temat:** Linki i nawigacja

Stwórz stronę z nawigacją:
- Nagłówek strony
- Menu nawigacyjne z 5 linkami (lista pozioma)
- Sekcja "O nas" z tekstem
- Sekcja "Kontakt" z linkiem do emaila
- Stopka z linkiem do strony głównej

W CSS:
- Menu: lista bez punktorów, elementy obok siebie (display: inline-block)
- Linki: bez podkreślenia, padding 10px 20px
- Linki hover: tło #ddd
- Menu: tło #333, linki białe

---

### ZADANIE 10 (TRUDNE - 7 punktów)
**Temat:** Formularz kontaktowy

Stwórz formularz kontaktowy:
- Pole: Imię i nazwisko (type="text", wymagane)
- Pole: Email (type="email", wymagane)
- Pole: Telefon (type="tel")
- Pole: Wybór tematu (lista rozwijana select z 3 opcjami)
- Pole: Wiadomość (textarea, 5 wierszy)
- Checkbox: Zgoda na przetwarzanie danych
- Przycisk: Wyślij

W CSS:
- Formularz: max-width 500px, margin: auto
- Każde pole: width 100%, padding 10px, margin-bottom 15px
- Label: display: block, font-weight: bold
- Przycisk: background #4CAF50, color white, padding 15px, border: none

---

### ZADANIE 11 (BARDZO TRUDNE - 8 punktów)
**Temat:** Strona z artykułem

Stwórz kompletną stronę artykułu:
- Header z tytułem strony
- Menu nawigacyjne (lista pozioma)
- Artykuł zawierający:
  - Nagłówek h1
  - Obraz wyróżniający (float: left, margin-right: 20px)
  - 3 akapity tekstu
  - Nagłówek h2: "Zobacz też"
  - Lista punktowana z 3 linkami
- Sidebar (float: right, 30% szerokości) z:
  - Nagłówek "Popularne artykuły"
  - Lista numerowana z 5 linkami
- Footer z informacjami

Wszystkie style w osobnym pliku CSS.

---

### ZADANIE 12 (BARDZO TRUDNE - 8 punktów)
**Temat:** Tabela zaawansowana z grafiką

Stwórz tabelę produktów:
- Kolumny: Zdjęcie, Nazwa, Opis, Cena, Akcja
- Minimum 4 produkty
- W kolumnie "Zdjęcie": małe obrazki (50x50px)
- W kolumnie "Akcja": przycisk "Kup teraz" (jako link stylizowany)

W CSS:
- Tabela: stylizowana profesjonalnie
- Obrazki: border-radius: 5px
- Przyciski: background: #ff5722, color: white, padding: 8px 15px
- Przyciski hover: background: #e64a19
- Tabela: responsive (width: 100%)

---

### ZADANIE 13 (BARDZO TRUDNE - 10 punktów)
**Temat:** Portfolio osobiste

Stwórz stronę portfolio zawierającą:
- Header z Twoim imieniem i tytułem
- Menu nawigacyjne
- Sekcja "O mnie" z:
  - Zdjęciem profilowym (zaokrąglonym)
  - Tekstem opisowym
  - Listą umiejętności (ul)
- Sekcja "Projekty" z:
  - 3 projektami w formie kart
  - Każdy projekt: obrazek + tytuł + opis
- Sekcja "Kontakt" z:
  - Formularzem kontaktowym
  - Listą kanałów kontaktu (email, telefon, social media jako linki)
- Footer

Wszystkie style w zewnętrznym CSS, profesjonalny wygląd.

---

### ZADANIE 14 (BARDZO TRUDNE - 10 punktów)
**Temat:** Strona restauracji

Stwórz stronę restauracji:
- Header z logo (obrazek) i nazwą
- Menu nawigacyjne
- Sekcja "O nas" z tekstem i 2 zdjęciami obok tekstu
- Sekcja "Menu" z:
  - Tabelą dań (nazwa, składniki, cena)
  - Minimum 3 kategorie (przystawki, dania główne, desery)
- Sekcja "Galeria" z 6 zdjęciami w siatce 3x2
- Sekcja "Rezerwacja" z formularzem:
  - Imię i nazwisko
  - Email
  - Telefon
  - Data (type="date")
  - Liczba osób (type="number")
  - Komentarz (textarea)
- Footer z danymi kontaktowymi

Kompletny CSS, profesjonalny design.

---

### ZADANIE 15 (BARDZO TRUDNE - 10 punktów)
**Temat:** Blog ze wszystkimi elementami

Stwórz stronę bloga zawierającą:
- Header z tytułem bloga i menu
- Lista 3 artykułów, każdy z:
  - Obrazkiem wyróżniającym
  - Tytułem (h2)
  - Datą publikacji
  - Skrótem tekstu
  - Linkiem "Czytaj więcej"
- Sidebar (30%) z:
  - Formularzem wyszukiwania
  - Listą kategorii (punktowaną)
  - Tabelą "Popularne posty" (tytuł + liczba wyświetleń)
  - Sekcją "Tagi" (linki jako przyciski)
- Footer z:
  - 3 kolumnami informacji
  - Menu linków
  - Formularzem newsletter

Kompletny projekt HTML + CSS.

---

## 📊 KRYTERIA OCENY

### Każde zadanie oceniane jest według:
1. **Poprawność HTML** (30%)
   - Prawidłowa struktura
   - Odpowiednie znaczniki
   - Wszystkie wymagane elementy

2. **Poprawność CSS** (30%)
   - Działające style
   - Zewnętrzny plik CSS
   - Zgodność z poleceniem

3. **Funkcjonalność** (20%)
   - Wszystko działa
   - Linki działają
   - Obrazki się wyświetlają

4. **Estetyka** (20%)
   - Czytelny kod
   - Ładny wygląd
   - Spójność wizualna

---

## ✅ LISTA KONTROLNA

Przed oddaniem zadania sprawdź:

- [ ] Czy HTML jest poprawny? (Walidator: https://validator.w3.org/)
- [ ] Czy wszystkie wymagane elementy są na stronie?
- [ ] Czy style są w ZEWNĘTRZNYM pliku CSS?
- [ ] Czy wszystkie obrazki mają atrybut alt?
- [ ] Czy tabele mają border-collapse: collapse?
- [ ] Czy listy są poprawnie zagnieżdżone?
- [ ] Czy linki działają?
- [ ] Czy formularz ma wszystkie wymagane pola?
- [ ] Czy kod jest sformatowany i czytelny?
- [ ] Czy strona wygląda dobrze?

---

**Termin oddania:** ___________________  
**Ocena:** ___________________

**POWODZENIA!** 🚀