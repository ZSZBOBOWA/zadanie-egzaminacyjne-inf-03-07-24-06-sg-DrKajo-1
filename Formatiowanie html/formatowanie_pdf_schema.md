# FORMATOWANIE HTML/CSS - SCHEMATY WIZUALNE

**Materiał pomocniczy dla uczniów**  
**Temat:** Listy, tabele, obrazki, formatowanie tekstu  
**Egzamin:** INF.03

---

## 📌 INSTRUKCJA

Ten dokument pokazuje **schematy i opisy jak powinny wyglądać gotowe zadania**.  
Porównuj swoje rozwiązania z poniższymi opisami.

**UWAGA:** To tylko schematy wizualne - musisz sam napisać kod HTML i CSS!

---

## 📚 ZADANIE 1 - NAGŁÓWKI I FORMATOWANIE

### Wymagania:
- Nagłówek `<h1>`: tekst "Moja pierwsza strona"
- Nagłówek `<h2>`: tekst "O mnie"
- Akapit z imieniem (imię **pogrubione** przez `<strong>`)
- Akapit z hobby (nazwa hobby *pochylona* przez `<em>`)
- Nagłówek `<h2>`: tekst "Ulubione przedmioty"

### Style CSS:
- h1: kolor **niebieski**, **wyśrodkowany**
- h2: kolor **zielony**
- Tło strony: **#f5f5f5** (jasny szary)

### Schemat:

```
┌─────────────────────────────────────────┐
│                                         │
│     Moja pierwsza strona                │ (h1, niebieski, środek)
│                                         │
├─────────────────────────────────────────┤
│  O mnie                                 │ (h2, zielony)
│                                         │
│  Nazywam się Jan Kowalski i jestem...   │ (Jan Kowalski pogrubiony)
│                                         │
│  Moim hobby jest programowanie i...     │ (programowanie pochylone)
│                                         │
├─────────────────────────────────────────┤
│  Ulubione przedmioty                    │ (h2, zielony)
│                                         │
└─────────────────────────────────────────┘

Tło całej strony: jasny szary (#f5f5f5)
```

**Sprawdź:**
- ✅ Czy h1 jest niebieski i wyśrodkowany?
- ✅ Czy h2 są zielone?
- ✅ Czy użyto `<strong>` i `<em>`?
- ✅ Czy tło jest szare?

---

## 📚 ZADANIE 2 - LISTA PUNKTOWANA

### Wymagania:
- Nagłówek "Moje hobby"
- Lista punktowana (`<ul>`) z 5 elementami

### Style CSS:
- Lista: `list-style-type: none` (bez domyślnych punktorów)
- Każdy element listy: `margin-left: 20px`
- Każdy element: `padding: 10px`
- Każdy element: tło **#e0e0e0**
- Odstęp między elementami: `margin-bottom: 10px`

### Schemat:

```
Moje hobby                               (h2)

┌────────────────────────────────────┐
│ Programowanie stron internetowych  │ (tło szare #e0e0e0)
└────────────────────────────────────┘

┌────────────────────────────────────┐
│ Gra na gitarze                     │
└────────────────────────────────────┘

┌────────────────────────────────────┐
│ Czytanie książek fantasy           │
└────────────────────────────────────┘

┌────────────────────────────────────┐
│ Fotografia                         │
└────────────────────────────────────┘

┌────────────────────────────────────┐
│ Granie w gry komputerowe           │
└────────────────────────────────────┘
```

**Każdy element to prostokąt z szarym tłem i paddingiem!**

**Sprawdź:**
- ✅ Czy lista nie ma punktorów?
- ✅ Czy każdy element ma szare tło?
- ✅ Czy są odstępy między elementami?

---

## 📚 ZADANIE 3 - PRZEPIS (LISTY)

### Wymagania:
- Nagłówek h1: nazwa dania
- Nagłówek h2: "Składniki"
- Lista punktowana (`<ul>`) - minimum 5 składników
- Nagłówek h2: "Sposób przygotowania"
- Lista numerowana (`<ol>`) - minimum 5 kroków

### Style CSS:
- Lista numerowana: kolor tekstu **#333**
- Każdy krok: `margin-bottom: 15px`

### Schemat:

```
Naleśniki                                (h1)

Składniki                                (h2)

• 2 szklanki mąki
• 2 jajka
• 500 ml mleka
• Szczypta soli
• Olej do smażenia

Sposób przygotowania                     (h2)

1. Wymieszaj mąkę z jajkami

2. Dodaj mleko i wymieszaj na gładkie ciasto

3. Dodaj sól

4. Rozgrzej patelnię z odrobiną oleju

5. Smaż naleśniki z obu stron na złoty kolor
```

**Uwaga:** Między krokami powinny być odstępy (margin-bottom)!

**Sprawdź:**
- ✅ Czy użyto `<ul>` dla składników?
- ✅ Czy użyto `<ol>` dla kroków?
- ✅ Czy kroki mają odstępy?

---

## 📚 ZADANIE 4 - LISTY ZAGNIEŻDŻONE

### Wymagania:
- Lista punktowana główna z kategoriami
- Każda kategoria zawiera zagnieżdżoną listę z daniami (minimum 3)
- 3 kategorie: Przystawki, Dania główne, Desery

### Style CSS:
- Lista główna: `list-style-type: none`
- Listy zagnieżdżone: `list-style-type: circle`
- Kategorie: `font-weight: bold`, `font-size: 20px`
- Dania: `font-size: 16px`, kolor **#555**

### Schemat:

```
Menu Restauracji                         (h2)

Przystawki                               (pogrubione, 20px)
  ○ Sałatka grecka                       (16px, #555)
  ○ Carpaccio z łososia
  ○ Bruschetta

Dania główne                             (pogrubione, 20px)
  ○ Stek z polędwicy                     (16px, #555)
  ○ Ryba z grilla
  ○ Lasagne bolognese

Desery                                   (pogrubione, 20px)
  ○ Tiramisu                             (16px, #555)
  ○ Lody włoskie
  ○ Tarta czekoladowa
```

**Uwaga:** Kategorie bez punktorów, dania z okrągłymi punktorami!

**Sprawdź:**
- ✅ Czy kategorie są pogrubione?
- ✅ Czy dania mają okrągłe punktory?
- ✅ Czy listy są prawidłowo zagnieżdżone?

---

## 📚 ZADANIE 5 - GALERIA OBRAZKÓW

### Wymagania:
- Nagłówek h1: "Moja galeria"
- 4 obrazki obok siebie
- Każdy obrazek z atrybutem `alt`
- Pod każdym obrazkiem krótki opis w `<p>`

### Style CSS:
- Obrazki: szerokość **23%**, margin **1%**
- Obrazki: ramka **2px solid black**
- Obrazki: `border-radius: 10px`
- Opisy: `text-align: center`, `font-size: 14px`

### Schemat:

```
Moja galeria                             (h1)

┌────────┐  ┌────────┐  ┌────────┐  ┌────────┐
│        │  │        │  │        │  │        │
│ ZDJĘCIE│  │ ZDJĘCIE│  │ ZDJĘCIE│  │ ZDJĘCIE│
│   1    │  │   2    │  │   3    │  │   4    │
│        │  │        │  │        │  │        │
└────────┘  └────────┘  └────────┘  └────────┘
   23%         23%         23%         23%

Opis zdjęcia Opis zdjęcia Opis zdjęcia Opis zdjęcia
    1            2            3            4
```

**Każdy obrazek ma:**
- Czarną ramkę 2px
- Zaokrąglone rogi
- Wyśrodkowany opis pod spodem

**Sprawdź:**
- ✅ Czy obrazki są obok siebie?
- ✅ Czy każdy ma 23% szerokości?
- ✅ Czy mają ramki i zaokrąglone rogi?
- ✅ Czy opisy są wyśrodkowane?

---

## 📚 ZADANIE 6 - TABELA (PLAN LEKCJI)

### Wymagania:
- Tabela z planem lekcji
- Kolumny: Godzina | Przedmiot | Sala
- Minimum 5 lekcji
- Nagłówki w `<th>`, dane w `<td>`

### Style CSS:
- Tabela: `width: 100%`, `border-collapse: collapse`
- Komórki: `border: 1px solid black`, `padding: 10px`
- Nagłówki: tło **#333**, kolor **biały**
- Wiersze parzyste: tło **#f2f2f2**

### Schemat:

```
Plan lekcji - Poniedziałek               (h2)

╔══════════════╦════════════════╦═══════════════╗
║   Godzina    ║   Przedmiot    ║     Sala      ║ (th, #333, biały tekst)
╠══════════════╬════════════════╬═══════════════╣
║ 8:00 - 8:45  ║  Matematyka    ║      12       ║ (białe tło)
╠══════════════╬════════════════╬═══════════════╣
║ 8:55 - 9:40  ║  Język polski  ║      15       ║ (szare tło #f2f2f2)
╠══════════════╬════════════════╬═══════════════╣
║ 9:50 - 10:35 ║  Angielski     ║       8       ║ (białe tło)
╠══════════════╬════════════════╬═══════════════╣
║10:45 - 11:30 ║ Programowanie  ║      22       ║ (szare tło)
╠══════════════╬════════════════╬═══════════════╣
║11:40 - 12:25 ║     WF         ║Sala gimnast.  ║ (białe tło)
╚══════════════╩════════════════╩═══════════════╝
```

**Uwaga:** Co drugi wiersz (2, 4) ma szare tło!

**Sprawdź:**
- ✅ Czy nagłówki mają ciemne tło i biały tekst?
- ✅ Czy wiersze parzyste mają szare tło?
- ✅ Czy tabela ma border-collapse?
- ✅ Czy wszystkie komórki mają ramki?

---

## 📚 ZADANIE 7 - TABELA Z SUMĄ

### Wymagania:
- Tabela produktów
- Kolumny: Nazwa produktu | Cena | Ilość | Wartość
- Minimum 5 produktów
- Wiersz RAZEM na końcu

### Style CSS:
- Tabela: szerokość **80%**, wyśrodkowana
- Cena i Wartość: `text-align: right`
- Wiersz RAZEM: `font-weight: bold`, tło **#ffeb3b** (żółte)
- Hover na wierszach: tło **#e0e0e0**

### Schemat:

```
Lista zakupów                            (h2)

╔═════════════════════╦════════╦════════╦═════════╗
║  Nazwa produktu     ║  Cena  ║ Ilość  ║ Wartość ║
╠═════════════════════╬════════╬════════╬═════════╣
║ Laptop Dell         ║3500 zł ║   2    ║ 7000 zł ║
╠═════════════════════╬════════╬════════╬═════════╣
║ Mysz bezprzewodowa  ║ 150 zł ║   5    ║  750 zł ║
╠═════════════════════╬════════╬════════╬═════════╣
║ Klawiatura          ║ 450 zł ║   3    ║ 1350 zł ║
╠═════════════════════╬════════╬════════╬═════════╣
║ Monitor 27"         ║1200 zł ║   4    ║ 4800 zł ║
╠═════════════════════╬════════╬════════╬═════════╣
║ Słuchawki           ║ 300 zł ║   6    ║ 1800 zł ║
╠═════════════════════╩════════╩════════╬═════════╣
║         RAZEM                         ║15700 zł ║ (pogrubione, żółte tło)
╚═══════════════════════════════════════╩═════════╝
                      ^
                      |
            Użyj colspan="3"!
```

**Uwaga:** Wiersz RAZEM łączy 3 pierwsze kolumny (colspan)!

**Sprawdź:**
- ✅ Czy ceny są wyrównane do prawej?
- ✅ Czy wiersz RAZEM jest pogrubiony?
- ✅ Czy wiersz RAZEM ma żółte tło?
- ✅ Czy hover działa na wierszach?

---

## 📚 ZADANIE 8 - TABELA Z COLSPAN

### Wymagania:
- Tabela ocen
- Pierwszy wiersz: nagłówek semestru łączący WSZYSTKIE kolumny (colspan)
- Kolumny: Przedmiot | Październik | Listopad | Grudzień | Średnia
- Minimum 3 przedmioty

### Style CSS:
- Nagłówek semestru: `text-align: center`, tło **#4CAF50**, tekst **biały**
- Średnia: `font-weight: bold`
- Oceny: `text-align: center`

### Schemat:

```
Oceny                                    (h2)

╔═════════════════════════════════════════════════════════╗
║          SEMESTR I - ROK 2024/2025                      ║ (colspan="5", zielone)
╠═════════════╦═══════════╦═══════════╦═════════╦═════════╣
║ Przedmiot   ║Październik║ Listopad  ║ Grudzień║ Średnia ║
╠═════════════╬═══════════╬═══════════╬═════════╬═════════╣
║ Matematyka  ║     4     ║     5     ║    4    ║  4.33   ║ (średnia pogrubiona)
╠═════════════╬═══════════╬═══════════╬═════════╬═════════╣
║Programowan. ║     5     ║     5     ║    6    ║  5.33   ║
╠═════════════╬═══════════╬═══════════╬═════════╬═════════╣
║Język polski ║     3     ║     4     ║    4    ║  3.67   ║
╚═════════════╩═══════════╩═══════════╩═════════╩═════════╝
```

**WAŻNE:** Pierwszy wiersz łączy 5 kolumn - użyj `colspan="5"`!

**Sprawdź:**
- ✅ Czy pierwszy wiersz ma colspan?
- ✅ Czy nagłówek semestru jest wyśrodkowany i zielony?
- ✅ Czy oceny są wyśrodkowane?
- ✅ Czy średnia jest pogrubiona?

---

## 📚 ZADANIE 9 - MENU NAWIGACYJNE

### Wymagania:
- Header z tytułem strony
- Menu nawigacyjne z 5 linkami (lista pozioma `<ul>`)
- Sekcja "O nas" z tekstem
- Sekcja "Kontakt" z linkiem email

### Style CSS:
- Menu: lista bez punktorów
- Elementy listy: `display: inline-block`
- Linki: bez podkreślenia, `padding: 10px 20px`
- Linki hover: tło **#ddd**
- Menu: tło **#333**, linki **białe**

### Schemat:

```
╔═══════════════════════════════════════════╗
║           Moja Strona                     ║ (header)
╠═══════════════════════════════════════════╣
║ Home  O nas  Usługi  Portfolio  Kontakt   ║ (nav, tło #333, białe linki)
╠═══════════════════════════════════════════╣
║                                           ║
║  O nas                                    ║
║                                           ║
║  Lorem ipsum dolor sit amet...            ║
║                                           ║
║  Kontakt                                  ║
║  Email: kontakt@example.com               ║ (jako mailto: link)
║                                           ║
╠═══════════════════════════════════════════╣
║  Footer - © 2025 Moja Strona              ║
╚═══════════════════════════════════════════╝
```

**Menu poziome - wszystkie linki obok siebie!**

**Sprawdź:**
- ✅ Czy menu jest poziome?
- ✅ Czy linki nie mają podkreślenia?
- ✅ Czy hover działa (szare tło)?
- ✅ Czy menu ma ciemne tło?

---

## 📚 ZADANIE 10 - FORMULARZ

### Wymagania:
- Formularz kontaktowy z polami:
  - Imię i nazwisko (text, wymagane)
  - Email (email, wymagane)
  - Telefon (tel)
  - Temat (select, 3 opcje)
  - Wiadomość (textarea, 5 wierszy)
  - Checkbox: zgoda
  - Przycisk: Wyślij

### Style CSS:
- Formularz: `max-width: 500px`, `margin: auto`
- Pola: `width: 100%`, `padding: 10px`, `margin-bottom: 15px`
- Label: `display: block`, `font-weight: bold`
- Przycisk: tło **#4CAF50**, tekst **biały**, `padding: 15px`, bez ramki

### Schemat:

```
     Formularz kontaktowy                (h2, wyśrodkowany)

┌──────────────────────────────────────┐
│ Imię i nazwisko:                     │
│ ┌────────────────────────────────┐   │
│ │                                │   │ (input text)
│ └────────────────────────────────┘   │
│                                      │
│ Email:                               │
│ ┌────────────────────────────────┐   │
│ │                                │   │ (input email)
│ └────────────────────────────────┘   │
│                                      │
│ Telefon:                             │
│ ┌────────────────────────────────┐   │
│ │                                │   │ (input tel)
│ └────────────────────────────────┘   │
│                                      │
│ Temat:                               │
│ ┌────────────────────────────────┐   │
│ │ Wybierz...              ▼     │   │ (select)
│ └────────────────────────────────┘   │
│                                      │
│ Wiadomość:                           │
│ ┌────────────────────────────────┐   │
│ │                                │   │
│ │                                │   │ (textarea, 5 wierszy)
│ │                                │   │
│ └────────────────────────────────┘   │
│                                      │
│ ☐ Zgoda na przetwarzanie danych      │ (checkbox)
│                                      │
│ ┌────────────────────────────────┐   │
│ │         Wyślij                 │   │ (button, zielony)
│ └────────────────────────────────┘   │
└──────────────────────────────────────┘
```

**Formularz wyśrodkowany, max 500px szerokości!**

**Sprawdź:**
- ✅ Czy formularz jest wyśrodkowany?
- ✅ Czy wszystkie pola mają label?
- ✅ Czy pola wymagane mają atrybut required?
- ✅ Czy przycisk jest zielony?

---

## 📚 ZADANIE 11 - STRONA Z ARTYKUŁEM

### Wymagania:
- Header z tytułem
- Menu nawigacyjne poziome
- Artykuł z:
  - Obrazem (float: left, margin-right: 20px)
  - 3 akapitami tekstu
  - Sekcją "Zobacz też" z listą linków
- Sidebar (float: right, 30%) z:
  - Listą numerowaną "Popularne artykuły"
- Footer

### Schemat:

```
╔═══════════════════════════════════════════════════════╗
║              Portal Newsowy                           ║
╠═══════════════════════════════════════════════════════╣
║ Home | Technologia | Sport | Kultura                  ║ (nav)
╠═══════════════════════════════════════════════════════╣
║                                    ║                  ║
║  Przełomowe odkrycie w AI          ║ Popularne...     ║
║                                    ║                  ║
║  ┌────────┐                        ║ 1. Artykuł 1     ║
║  │ OBRAZEK│ Lorem ipsum dolor sit  ║ 2. Artykuł 2     ║
║  │   AI   │ amet consectetur...    ║ 3. Artykuł 3     ║
║  └────────┘                        ║ 4. Artykuł 4     ║
║  (float    Tekst opływa obrazek... ║ 5. Artykuł 5     ║
║   left)                            ║                  ║
║            Kolejny akapit...       ║    (sidebar      ║
║                                    ║     30%)         ║
║  Zobacz też:                       ║                  ║
║  • Link 1                          ║                  ║
║  • Link 2                          ║                  ║
║  • Link 3                          ║                  ║
║            (68%)                   ║                  ║
╠════════════════════════════════════╩══════════════════╣
║  © 2025 Portal. Wszelkie prawa zastrzeżone.          ║
╚═══════════════════════════════════════════════════════╝
```

**Obrazek float: left - tekst go opływa!**

**Sprawdź:**
- ✅ Czy obrazek jest po lewej stronie artykułu?
- ✅ Czy tekst opływa obrazek?
- ✅ Czy sidebar jest po prawej (30%)?
- ✅ Czy wszystkie elementy są na miejscu?

---

## 📚 ZADANIE 12 - TABELA Z GRAFIKĄ

### Wymagania:
- Tabela produktów
- Kolumny: Zdjęcie | Nazwa | Opis | Cena | Akcja
- Minimum 4 produkty
- Zdjęcia 50x50px
- W kolumnie "Akcja": link stylizowany jako przycisk

### Style CSS:
- Obrazki: `border-radius: 5px`
- Przycisk: tło **#ff5722**, tekst **biały**, `padding: 8px 15px`
- Przycisk hover: tło **#e64a19**
- Tabela: `width: 100%`

### Schemat:

```
Nasze produkty                           (h2)

╔════════╦═══════════════╦════════════════╦═══════╦══════════╗
║ Zdjęcie║    Nazwa      ║     Opis       ║ Cena  ║  Akcja   ║
╠════════╬═══════════════╬════════════════╬═══════╬══════════╣
║ [IMG]  ║ Laptop Dell   ║ Wydajny laptop ║4999zł ║[Kup teraz]║ (przycisk)
║ 50x50  ║               ║                ║       ║ pomarańcz.║
╠════════╬═══════════════╬════════════════╬═══════╬══════════╣
║ [IMG]  ║ Mysz Logitech ║ Ergonomiczna   ║ 299zł ║[Kup teraz]║
║ 50x50  ║               ║                ║       ║           ║
╠════════╬═══════════════╬════════════════╬═══════╬══════════╣
║ [IMG]  ║ Klawiatura    ║ RGB, Cherry MX ║ 599zł ║[Kup teraz]║
║ 50x50  ║               ║                ║       ║           ║
╠════════╬═══════════════╬════════════════╬═══════╬══════════╣
║ [IMG]  ║ Słuchawki     ║ Redukcja szumów║1299zł ║[Kup teraz]║
║ 50x50  ║               ║                ║       ║           ║
╚════════╩═══════════════╩════════════════╩═══════╩══════════╝
```

**Przycisk to stylizowany link `<a>` - nie `<button>`!**

**Sprawdź:**
- ✅ Czy obrazki mają 50x50px?
- ✅ Czy obrazki mają zaokrąglone rogi?
- ✅ Czy przyciski są pomarańczowe?
- ✅ Czy hover działa na przyciskach?

---

## ⚠️ NAJCZĘSTSZE BŁĘDY

### 1. Brak border-collapse w tabelach
**Problem:** Podwójne ramki w tabeli  
**Rozwiązanie:** `table { border-collapse: collapse; }`

### 2. Zapomnienie o atrybucie alt w obrazkach
**Problem:** Brak dostępności  
**Rozwiązanie:** Zawsze dodawaj `alt="opis"`

### 3. Inline style zamiast zewnętrznego CSS
**Problem:** Style w HTML  
**Rozwiązanie:** Wszystkie style w osobnym pliku .css

### 4. Złe zagnieżdżenie list
**Problem:** `<ul>` bezpośrednio w `<ul>`  
**Prawidłowo:** `<ul>` w `<li>` wewnątrz `<ul>`

```html
BŁĄD:
<ul>
    <ul>
        <li>Element</li>
    </ul>
</ul>

POPRAWNIE:
<ul>
    <li>Kategoria
        <ul>
            <li>Element</li>
        </ul>
    </li>
</ul>
```

### 5. Brak clearfix po float
**Problem:** Następne elementy "wskakują" obok float  
**Rozwiązanie:** `<div style="clear: both;"></div>` lub `clear: both` w CSS

---

## ✅ LISTA KONTROLNA

Przed oddaniem zadania sprawdź:

### HTML:
- [ ] Czy struktura HTML jest poprawna?
- [ ] Czy użyto odpowiednich znaczników?
- [ ] Czy wszystkie obrazki mają alt?
- [ ] Czy listy są poprawnie zagnieżdżone?
- [ ] Czy tabele mają `<th>` i `<td>`?
- [ ] Czy formularze mają label dla każdego pola?

### CSS:
- [ ] Czy style są w ZEWNĘTRZNYM pliku?
- [ ] Czy nie ma styli inline?
- [ ] Czy kolory są zgodne z poleceniem?
- [ ] Czy użyto border-collapse dla tabel?
- [ ] Czy clearfix jest tam gdzie potrzeba?

### Funkcjonalność:
- [ ] Czy wszystkie linki działają?
- [ ] Czy obrazki się wyświetlają?
- [ ] Czy hover działa?
- [ ] Czy formularz ma required gdzie trzeba?

### Estetyka:
- [ ] Czy kod jest sformatowany?
- [ ] Czy strona wygląda jak na wzorze?
- [ ] Czy odstępy są prawidłowe?
- [ ] Czy wszystko jest czytelne?

---

## 💡 WSKAZÓWKI TECHNICZNE

### Obrazki placeholder
Jeśli nie masz własnych obrazków, użyj:
```
https://via.placeholder.com/300x200
```

### Walidator HTML
Sprawdź poprawność HTML:
```
https://validator.w3.org/
```

### Kolory w CSS
Możesz używać:
- Nazw: `red`, `blue`, `green`
- HEX: `#ff0000`, `#333`, `#f5f5f5`
- RGB: `rgb(255, 0, 0)`

### Selektory CSS
```css
/* Element */
h1 { }

/* Klasa */
.moja-klasa { }

/* ID */
#moje-id { }

/* Pseudo-klasy */
a:hover { }
tr:nth-child(even) { }
```

---

## 📊 PUNKTACJA

| Zadanie | Punkty | Trudność |
|---------|--------|----------|
| 1       | 2      | Łatwe |
| 2       | 3      | Łatwe |
| 3       | 3      | Łatwe |
| 4       | 4      | Średnie |
| 5       | 5      | Średnie |
| 6       | 5      | Średnie |
| 7       | 5      | Średnie |
| 8       | 6      | Trudne |
| 9       | 6      | Trudne |
| 10      | 7      | Trudne |
| 11      | 8      | Bardzo trudne |
| 12      | 8      | Bardzo trudne |
| 13-15   | 10     | Bardzo trudne |

**Maksymalnie:** 100+ punktów

---

**POWODZENIA!** 🚀

**Opracował:** Nauczyciel informatyki  
**Data:** 2025  
**Wersja:** 1.0 (schematy wizualne bez kodu)