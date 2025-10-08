# 📚 INSTRUKCJA DO ZADAŃ - FORMATOWANIE HTML/CSS

## 📋 INFORMACJE OGÓLNE

### Pliki do pracy:

1. **`formatowanie_teoria.md`** - Zawiera:
   - ✅ Podstawy teoretyczne (powtórkowe)
   - ✅ Przypomnienie składni HTML i CSS
   - ✅ Przykłady kodu
   - ✅ 15 zadań do wykonania (od łatwych do bardzo trudnych)

2. **`formatowanie_wizualizacja.html`** - Zawiera:
   - ✅ Podgląd wykonanych ćwiczeń
   - ✅ Wzory wizualne jak powinny wyglądać gotowe zadania
   - ✅ Możliwość porównania swojej pracy z wzorem

3. **`formatowanie_pdf_schema.md`** - Zawiera:
   - ✅ Schematy wizualne bez kodu
   - ✅ Opisy wymagań
   - ✅ Do wydruku lub zapisania jako PDF

---

## 🎯 TWOJE ZADANIE

### Krok 1: Utwórz repozytorium Git

Stwórz nowe repozytorium o nazwie:

```
Formatowanie_HTML_CSS
```

**Ważne:** Nazwa repozytorium musi być dokładnie taka!

---

### Krok 2: Struktura folderów

Każde zadanie umieść w **osobnym folderze** według poniższej struktury:

```
Formatowanie_HTML_CSS/
│
├── zadanie_01/
│   ├── index.html
│   ├── style.css
│   └── screenshot.png
│
├── zadanie_02/
│   ├── index.html
│   ├── style.css
│   └── screenshot.png
│
├── zadanie_03/
│   ├── index.html
│   ├── style.css
│   └── screenshot.png
│
├── zadanie_04/
│   ├── index.html
│   ├── style.css
│   └── screenshot.png
│
... (i tak dalej dla wszystkich zadań)
│
├── zadanie_15/
│   ├── index.html
│   ├── style.css
│   └── screenshot.png
│
└── README.md
```

---

### Krok 3: Wymagania dla każdego zadania

Każdy folder z zadaniem **MUSI** zawierać:

#### 1. Plik `index.html`
- Kod HTML zadania
- Poprawna struktura HTML5
- Wszystkie wymagane elementy z polecenia

#### 2. Plik `style.css`
- Wszystkie style w **zewnętrznym** pliku CSS
- **NIE używaj** styli inline!
- Kod sformatowany i czytelny

#### 3. Plik `screenshot.png` (lub .jpg)
- Zrzut ekranu wykonanej strony
- **WAŻNE:** Na zrzucie ekranu musi być widoczna **data i godzina** w prawym dolnym rogu ekranu!

---

## 📸 JAK ZROBIĆ ZRZUT EKRANU Z DATĄ I GODZINĄ?

### Opcja 1: Windows (zalecana)

1. Otwórz swoją stronę w przeglądarce
2. Upewnij się, że w prawym dolnym rogu Windows widoczny jest zegar
3. Naciśnij **Win + Shift + S** (Narzędzie wycinania)
4. Zaznacz obszar z całą stroną **włącznie z zegarem Windows**
5. Zapisz jako `screenshot.png` w folderze zadania

### Opcja 2: Dodaj datę/czas w kodzie HTML

Jeśli zegar Windows nie jest widoczny, możesz dodać na swojej stronie:

```html
<div style="position: fixed; bottom: 10px; right: 10px; 
            background: rgba(0,0,0,0.7); color: white; 
            padding: 10px; font-family: monospace;">
    Data: 08.10.2025 | Godzina: 14:30
</div>
```

**Uwaga:** Wpisz aktualną datę i godzinę wykonania zadania!

### Opcja 3: Narzędzie Snipping Tool

1. Otwórz "Narzędzie wycinania" / "Snipping Tool"
2. Przed zrobieniem screenshota upewnij się że widoczny jest zegar
3. Zrób zrzut ekranu ze stroną i zegarem
4. Zapisz jako `screenshot.png`

---

## ✅ LISTA KONTROLNA PRZED ODDANIEM

Przed oddaniem projektu sprawdź każde zadanie:

### Struktura:
- [ ] Repozytorium nazywa się **Formatowanie_HTML_CSS**
- [ ] Każde zadanie w osobnym folderze (zadanie_01, zadanie_02, ...)
- [ ] Każdy folder zawiera: index.html, style.css, screenshot.png

### Pliki HTML:
- [ ] Poprawna struktura HTML5 (<!DOCTYPE html>, <html>, <head>, <body>)
- [ ] Wszystkie wymagane elementy z polecenia
- [ ] Link do pliku CSS: `<link rel="stylesheet" href="style.css">`
- [ ] Brak styli inline (nie używaj atrybutu style="" w HTML!)

### Pliki CSS:
- [ ] Wszystkie style w pliku style.css
- [ ] Kod sformatowany i czytelny
- [ ] Style zgodne z poleceniem zadania

### Zrzuty ekranu:
- [ ] Każde zadanie ma screenshot.png
- [ ] Na screenshocie widoczna data i godzina
- [ ] Zrzut pokazuje całą stronę

### Git:
- [ ] Wszystkie pliki są scommitowane
- [ ] Repozytorium jest wypushowane na GitHub/GitLab
- [ ] Commit messages są opisowe (np. "Dodano zadanie 1 - nagłówki")

---

## 📝 PRZYKŁADOWY README.md

Stwórz plik `README.md` w głównym folderze repozytorium:

```markdown
# Formatowanie HTML/CSS - Zadania

**Autor:** [Twoje Imię i Nazwisko]  
**Klasa:** [Twoja klasa]  
**Data:** [Data rozpoczęcia]

## Opis projektu

Repozytorium zawiera 15 zadań z formatowania tekstu i elementów w HTML/CSS.
Zadania obejmują:
- Listy punktowane i numerowane
- Tabele
- Obrazki i galerie
- Formularze
- Nawigację
- Kompletne strony internetowe

## Struktura projektu

- `zadanie_01/` - Nagłówki i formatowanie tekstu
- `zadanie_02/` - Lista punktowana
- `zadanie_03/` - Przepis kulinarny (listy)
- ... (i tak dalej)
- `zadanie_15/` - Blog (zadanie kompleksowe)

## Technologie

- HTML5
- CSS3

## Status wykonania

- [x] Zadanie 1
- [x] Zadanie 2
- [ ] Zadanie 3
- [ ] Zadanie 4
... (aktualizuj w miarę postępów)

## Uwagi

[Tu możesz dodać własne uwagi, napotkane problemy, ciekawe rozwiązania]
```

---

## 🎓 WSKAZÓWKI

### 1. Zacznij od teorii
Przed rozpoczęciem zadań **przeczytaj dokładnie** plik `formatowanie_teoria.md`:
- Sekcja "CZĘŚĆ 1: PRZYPOMNIENIE TEORII" zawiera wszystko czego potrzebujesz
- Są tam przykłady kodu które możesz adaptować

### 2. Sprawdzaj z podglądem
Otwórz plik `formatowanie_wizualizacja.html` w przeglądarce:
- Zobacz jak powinno wyglądać gotowe zadanie
- Porównuj swoje rozwiązanie z wzorem
- Zwracaj uwagę na szczegóły (kolory, odstępy, wyrównania)

### 3. Pracuj systematycznie
- Wykonuj zadania po kolei (od 1 do 15)
- Nie przeskakuj zadań
- Każde zadanie commituj zaraz po wykonaniu

### 4. Testuj w przeglądarce
Po każdej zmianie:
- Odśwież stronę w przeglądarce (F5)
- Sprawdź czy wszystko wygląda dobrze
- Testuj linki, hover, formularze

### 5. Waliduj kod
Przed oddaniem sprawdź poprawność HTML:
- Wejdź na https://validator.w3.org/
- Wklej swój kod lub podaj URL
- Popraw wszystkie błędy

---

## ⚠️ NAJCZĘSTSZE BŁĘDY DO UNIKNIĘCIA

### ❌ BŁĄD 1: Style inline w HTML
```html
<!-- ŹLE -->
<p style="color: red;">Tekst</p>

<!-- DOBRZE -->
<p class="red-text">Tekst</p>
```
I w CSS:
```css
.red-text {
    color: red;
}
```

### ❌ BŁĄD 2: Brak pliku CSS
```html
<!-- ŹLE - style w <head> -->
<style>
    p { color: red; }
</style>

<!-- DOBRZE - link do zewnętrznego pliku -->
<link rel="stylesheet" href="style.css">
```

### ❌ BŁĄD 3: Zła struktura folderów
```
❌ ŹLE:
Formatowanie_HTML_CSS/
├── zadanie1.html
├── zadanie1.css
├── zadanie2.html
├── zadanie2.css

✅ DOBRZE:
Formatowanie_HTML_CSS/
├── zadanie_01/
│   ├── index.html
│   ├── style.css
│   └── screenshot.png
├── zadanie_02/
│   ├── index.html
│   ├── style.css
│   └── screenshot.png
```

### ❌ BŁĄD 4: Brak screenshota z datą
- Screenshot MUSI pokazywać datę i godzinę
- Data i godzina potwierdzają kiedy zadanie zostało wykonane
- Bez tego zadanie może zostać odrzucone!

### ❌ BŁĄD 5: Brak atrybutu alt w obrazkach
```html
<!-- ŹLE -->
<img src="obrazek.jpg">

<!-- DOBRZE -->
<img src="obrazek.jpg" alt="Opis obrazka">
```

---

## 📊 OCENIANIE

### Kryteria oceny każdego zadania:

1. **Poprawność HTML (30%)**
   - Prawidłowa struktura
   - Wszystkie wymagane elementy
   - Walidacja bez błędów

2. **Poprawność CSS (30%)**
   - Style w zewnętrznym pliku
   - Działające style
   - Zgodność z poleceniem

3. **Funkcjonalność (20%)**
   - Wszystko działa
   - Linki działają
   - Formularze działają

4. **Estetyka i zgodność ze wzorem (20%)**
   - Wygląd zgodny z podglądem
   - Czytelny kod
   - Screenshot z datą

### Ocena końcowa:

| Zadań wykonanych | Ocena |
|------------------|-------|
| 13-15 (85%+)     | Celujący (6) |
| 11-12 (70%+)     | Bardzo dobry (5) |
| 9-10 (60%+)      | Dobry (4) |
| 7-8 (50%+)       | Dostateczny (3) |
| 5-6 (35%+)       | Dopuszczający (2) |
| 0-4              | Niedostateczny (1) |

---

## 📅 TERMINY

**Termin rozpoczęcia:** ___________________

**Termin oddania:** ___________________

**Sposób oddania:**
- [ ] Link do repozytorium GitHub/GitLab
- [ ] Zgłoszenie przez Google Classroom
- [ ] Zgłoszenie przez email

**Adres zgłoszenia:** ___________________

---

## 🆘 POMOC

### Jeśli masz problem:

1. **Przeczytaj teorię** w pliku formatowanie_teoria.md
2. **Sprawdź podgląd** w formatowanie_wizualizacja.html
3. **Sprawdź schemat** w formatowanie_pdf_schema.md
4. **Zapytaj nauczyciela** podczas lekcji
5. **Sprawdź w internecie** - np. MDN Web Docs, W3Schools

### Przydatne linki:

- HTML: https://developer.mozilla.org/pl/docs/Web/HTML
- CSS: https://developer.mozilla.org/pl/docs/Web/CSS
- Walidator: https://validator.w3.org/
- Placeholder images: https://via.placeholder.com/

---

## ✨ DODATKOWE PUNKTY

Możesz zdobyć dodatkowe punkty za:

- [ ] **README.md** - Szczegółowy opis projektu (+5 pkt)
- [ ] **Wszystkie 15 zadań** - Kompletny projekt (+10 pkt)
- [ ] **Własna kreatywność** - Ładniejsze style niż wymagane (+5 pkt)
- [ ] **Responsive design** - Strona działa na telefonie (+10 pkt)
- [ ] **Dodatkowe zadanie** - Własny pomysł (+15 pkt)

---

## 📢 WAŻNE PRZYPOMNIENIA

1. ⚠️ **Każde zadanie w osobnym folderze!**
2. ⚠️ **Wszystkie style w pliku CSS, nie inline!**
3. ⚠️ **Screenshot MUSI zawierać datę i godzinę!**
4. ⚠️ **Nazwy folderów: zadanie_01, zadanie_02, ... zadanie_15**
5. ⚠️ **Nazwy plików: index.html, style.css, screenshot.png**
6. ⚠️ **Repozytorium MUSI nazywać się: Formatowanie_HTML_CSS**

---

## 🎯 PODSUMOWANIE

### Co masz zrobić:

1. ✅ Przeczytać plik **formatowanie_teoria.md** (teoria + zadania)
2. ✅ Sprawdzić plik **formatowanie_wizualizacja.html** (podgląd)
3. ✅ Utworzyć repozytorium **Formatowanie_HTML_CSS**
4. ✅ Wykonać zadania (każde w osobnym folderze)
5. ✅ Zrobić screenshoty (z datą i godziną!)
6. ✅ Scommitować i wypushować repozytorium
7. ✅ Wysłać link do repozytorium

### Pamiętaj:

📁 Każde zadanie = 3 pliki (HTML + CSS + screenshot)  
📸 Screenshot = widoczna data i godzina  
💾 Wszystko w Git = regularne commity  
✨ Jakość > Ilość = lepiej 10 dobrych zadań niż 15 złych

---

**POWODZENIA!** 🚀

*Masz pytania? Zapytaj nauczyciela podczas lekcji lub przez email.*

---

**Wersja:** 1.0  
**Data:** 2025  
**Autor instrukcji:** Nauczyciel informatyki