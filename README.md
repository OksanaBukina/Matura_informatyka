# 🐍 Python — Teoria i Praktyka (Matura Informatyka)

Kompleksowy konspekt wiedzy z podstaw języka Python sformatowany pod platformę GitHub. Zawiera omówienie teorii, część praktyczną z 10 zadaniami oraz **zbiorczą sekcję rozwiązań i odpowiedzi umieszczoną na samym końcu**.

---

## 📋 Spis treści
- [1. Teoria — Podstawy języka Python](#1-teoria--podstawy-języka-python)
  - [1.1 Obiekty, podstawowe typy i zmienne](#11-obiekty-podstawowe-typy-i-zmienne)
  - [1.2 Podstawowe operatory](#12-podstawowe-operatory)
  - [1.3 Podstawowe kontenery](#13-podstawowe-kontenery)
  - [1.4 Dostęp do danych w kontenerach (Indeksowanie i Slicing)](#14-dostęp-do-danych-w-kontenerach-indeksowanie-i-slicing)
  - [1.5 Wbudowane funkcje i obiekty wywoływalne](#15-wbudowane-funkcje-i-obiekty-wywoływalne)
  - [1.6 Atrybuty obiektów (Metody i Właściwości)](#16-atrybuty-obiektów-metody-i-właściwości)
  - [1.7 Argumenty pozycyjne i nazwane w funkcjach](#17-argumenty-pozycyjne-i-nazwane-w-funkcjach)
  - [1.8 Formatowanie łańcuchów znaków (Strings)](#18-formatowanie-łańcuchów-znaków-strings)
- [2. Praktyka — Zadania programistyczne](#2-praktyka--zadania-programistyczne)
  - [Zadanie 1: Odwracanie łańcucha znaków](#zadanie-1-odwracanie-łańcucha-znaków)
  - [Zadanie 2: Wyszukiwanie najdłuższego słowa](#zadanie-2-wyszukiwanie-najdłuższego-słowa)
  - [Zadanie 3: Sprawdzanie palindromu](#zadanie-3-sprawdzanie-palindromu)
  - [Zadanie 4: Suma elementów liczbowych w liście](#zadanie-4-suma-elementów-liczbowych-w-liście)
  - [Zadanie 5: Usuwanie duplikatów z zachowaniem kolejności](#zadanie-5-usuwanie-duplikatów-z-zachowaniem-kolejności)
  - [Zadanie 6: Analiza częstotliwości słów w tekście](#zadanie-6-analiza-częstotliwości-słów-w-tekście)
  - [Zadanie 7: Generator haseł](#zadanie-7-generator-haseł)
  - [Zadanie 8: Obliczanie silni](#zadanie-8-obliczanie-silni)
  - [Zadanie 9: Sprawdzanie liczby pierwszej](#zadanie-9-sprawdzanie-liczby-pierwszej)
  - [Zadanie 10: Prosty parser URL](#zadanie-10-prosty-parser-url)
- [3. Odpowiedzi i rozwiązania zadań](#3-odpowiedzi-i-rozwiązania-zadań)
  - [3.1 Odpowiedzi do zadań teoretycznych (Sekcja 1)](#31-odpowiedzi-do-zadań-teoretycznych-sekcja-1)
  - [3.2 Rozwiązania zadań praktycznych (Sekcja 2)](#32-rozwiązania-zadań-praktycznych-sekcja-2)

---

# 1. Teoria — Podstawy języka Python

## 1.1 Obiekty, podstawowe typy i zmienne

Wszystko w Pythonie jest **obiektem** posiadającym określony **typ**. Zmienne to nazwy przypisane do obiektów w pamięci.

### Podstawowe typy danych:
* **`int`** — liczby całkowite, np. `10`, `-3`, `0`
* **`float`** — liczby zmiennoprzecinkowe (z częścią dziesiętną), np. `7.41`, `-0.006`
* **`str`** — ciągi znaków (łańcuchy ujęte w cudzysłów), np. `'tekst'`, `"tekst"`, `'''multiline'''`
* **`bool`** — wartości logiczne (`True`, `False`)
* **`NoneType`** — specjalny typ reprezentujący brak wartości (`None`)

### Zasady tworzenia nazw zmiennych (`snake_case`):
* Nazwy mogą zawierać tylko litery, cyfry i znak podkreślenia (`_`).
* Muszą rozpoczynać się od litery lub znaku `_` (nigdy od cyfry!).
* Nie mogą zawierać spacji, myślników ani znaków specjalnych.

---

### ✏️ Samodzielne zadania: Obiekty i zmienne
1. **Tworzenie zmiennych:** Stwórz zmienne opisujące Twój ulubiony produkt: `nazwa` (`str`), `cena` (`float`), `ilosc_w_magazynie` (`int`) oraz `dostepny` (`bool`). Wyświetl typ każdej z nich za pomocą funkcji `type()`.
2. **Poprawa błędów:** Popraw poniższe błędne nazwy zmiennych tak, aby były zgodne z zasadami Pythona:
   - `1st_user = "Jan"`
   - `user-age = 25`
   - `class = "3A"`

---

## 1.2 Podstawowe operatory

Operatory to specjalne symbole wykonujące operacje na wartościach.

### 1. Operatory arytmetyczne
* `+` — Dodawanie
* `-` — Odejmowanie
* `*` — Mnożenie
* `/` — Dzielenie (zawsze zwraca `float`)
* `**` — Potęgowanie

### 2. Operatory przypisania
* `=` — Przypisanie wartości
* `+=` — Inkrementacja (dodaj i przypisz)
* `-=` — Dekrementacja (odejmij i przypisz)
* `*=` — Pomnóż i przypisz

### 3. Operatory porównania (zwracają `True` lub `False`)
* `==` — Równy
* `!=` — Nierówny
* `<` — Mniejszy niż
* `<=` — Mniejszy lub równy
* `>` — Większy niż
* `>=` — Większy lub równy

> [!NOTE]
> **Priorytet operatorów (kolejność wykonywania działań):**
> 1. `()` — nawiasy (grupowanie)
> 2. `**` — potęgowanie
> 3. `*`, `/` — mnożenie i dzielenie
> 4. `+`, `-` — dodawanie i odejmowanie
> 5. `==`, `!=`, `<`, `<=`, `>`, `>=` — porównania

### Przykłady kodu

```python
liczba1 = 1
liczba2 = 2
liczba3 = 3
liczba4 = 42
liczba5 = 2138
liczba6 = -68

print(liczba1 + liczba2)   # 3
print(liczba2 - liczba3)   # -1
print(liczba3 * liczba4)   # 126
print(liczba4 / liczba5)   # 0.019644527595884004
print(liczba5 ** liczba2)  # 4571044

liczba4 += 4   # 46
liczba6 -= 2   # -70
liczba4 *= 5   # 230

print(5 > 3 > 1)             # True
print(5 > 3 < 4 == 3 + 1)    # True
```

---

### ✏️ Samodzielne zadania: Operatory
1. **Kalkulator geometrii:** Oblicz pole i obwód koła o promieniu $r = 7.5$ używając wzorów $P = \pi \cdot r^2$ oraz $O = 2 \cdot \pi \cdot r$ (przyjmij $\pi = 3.14159$).
2. **Wyrażenie logiczne:** Sprawdź za pomocą jednego wyrażenia logicznego w Pythonie, czy podwojona wartość zmiennej $x = 15$ jest większa od 20 i jednocześnie różna od 30.

---

## 1.3 Podstawowe kontenery

| Typ | Nazwa | Mutowalność | Indeksowanie | Opis | Przykład |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `str` | Łańcuch | Niemutowalny | Liczbami (`int`) | Sekwencja znaków | `'Python'` |
| `list` | Lista | Mutowalna | Liczbami (`int`) | Uporządkowana sekwencja | `[3, 5, 'pies', False]` |
| `tuple` | Krotka | Niemutowalna | Liczbami (`int`) | Uporządkowana, niezmienna sekwencja | `(3, 5, 'pies', False)` |
| `set` | Zbiór | Mutowalny | Brak | Nieuporządkowane Unikalne elementy | `{3, 5, 'pies', False}` |
| `dict` | Słownik | Mutowalny | Kluczami | Pary `klucz: wartość` | `{'imię': 'Jadwiga', 'wiek': 23}` |

### Przykłady kodu i operacji na kontenerach

```python
# Przypisz kilka kontenerów do różnych zmiennych
lista1 = [3, 5, 6, 3, 'pies', 'kot', False]
krotka1 = (3, 5, 6, 3, 'pies', 'kot', False)
zbior1 = {3, 5, 6, 3, 'pies', 'kot', False}
slownik1 = {'imię': 'Jadwiga', 'wiek': 23, 'ulub_jedzenie': ['pizza', 'owoce', 'ryba']}

# Dodaj i przypisz ponownie (modyfikacja listy / utworzenie nowej krotki)
lista1 += [5, 'winogrona']
print(lista1)
# Output: [3, 5, 6, 3, 'pies', 'kot', False, 5, 'winogrona']

krotka1 += (5, 'winogrona')
print(krotka1)
# Output: (3, 5, 6, 3, 'pies', 'kot', False, 5, 'winogrona')

# Mnożenie sekwencji
print([1, 2, 3, 4] * 2)
# Output: [1, 2, 3, 4, 1, 2, 3, 4]

print((1, 2, 3, 4) * 3)
# Output: (1, 2, 3, 4, 1, 2, 3, 4, 1, 2, 3, 4)

print(zbior1)   # Output np.: {False, 3, 5, 6, 'kot', 'pies'}
```

---

### ✏️ Samodzielne zadania: Kontenery
1. Utwórz listę `zakupy` zawierającą 5 produktów oraz krotkę `punkt_gps` zawierającą dwie wartości (szerokość i długość geograficzna). Wyjaśnij w komentarzu kodu, dlaczego dla pozycji GPS lepsza jest krotka niż lista.
2. Utwórz zbiór `imiona = {"Anna", "Piotr", "Anna", "Paweł", "Piotr"}`. Wyświetl go i sprawdź, ile elementów ostatecznie w nim pozostało.

---

## 1.4 Dostęp do danych w kontenerach (Indeksowanie i Slicing)

W przypadku `str`, `list` i `tuple` używamy nawiasów kwadratowych `[]` do indeksowania liczbowego (od `0`). Słowniki `dict` indeksujemy za pomocą ich **kluczy**.

> [!WARNING]
> Zbiory (`set`) nie są indeksowane — użycie `zbior[0]` zgłosi błąd `TypeError`.

### Składnia wycinania (Slicing): `sekwencja[start:stop:step]`
- `start`: indeks początkowy (włącznie)
- `stop`: indeks końcowy (wyłącznie)
- `step`: krok (opcjonalnie, domyślnie 1)
- Ujemny indeks (np. `-1`) oznacza dostęp od końca sekwencji.

### Przykłady wycinania na słowie `s = "INFORMATYKA"`:

| Wyrażenie | Opis | Wynik dla `"INFORMATYKA"` |
| :--- | :--- | :--- |
| `s[::-1]` | Odwrócenie ciągu znaków (sprawdzanie palindromu) | `"AKYTAMROFNI"` |
| `s[-8:]` | Ostatnie 8 znaków ciągu | `"ORMATYKA"` |
| `s[:8]` | Pierwsze 8 znaków ciągu | `"INFORMAT"` |
| `s[:-1]` | Ciąg bez ostatniego znaku | `"INFORMATYK"` |
| `s[1:]` | Ciąg bez pierwszego znaku | `"NFORMATYKA"` |
| `s[1:-1]` | Ciąg bez pierwszego i ostatniego znaku | `"NFORMATYK"` |
| `s[::2]` | Znaki na indeksach parzystych (co 2-gi znak) | `"IFRAYA"` |
| `s[1::2]` | Znaki na indeksach nieparzystych | `"NOMTK"` |

### Przykłady kodu w Pythonie:

```python
s = "INFORMATYKA"

print(s[::-1])    # "AKYTAMROFNI" — odwrócenie ciągu znaków (sprawdzanie palindromu)
print(s[-8:])     # "ORMATYKA"   — ostatnie 8 znaków ciągu
print(s[:8])      # "INFORMAT"   — pierwsze 8 znaków ciągu
print(s[:-1])     # "INFORMATYK" — bez ostatniego znaku
print(s[1:])      # "NFORMATYKA" — bez pierwszego znaku
print(s[1:-1])    # "NFORMATYK"  — bez pierwszego i ostatniego znaku
print(s[::2])     # "IFRAYA"     — tylko indeksy parzyste (co 2-gi symbol)
print(s[1::2])    # "NOMTK"      — tylko indeksy nieparzyste

lista1 = [3, 5, 6, 3, 'pies', 'kot', False, 5, 'winogrona']
prosty_lancuch1 = 'jakiś przykład'
slownik1 = {'imię': 'Jadwiga', 'wiek': 23, 'ulub_jedzenie': ['pizza', 'owoce', 'ryba']}

print(lista1[0])              # 3
print(prosty_lancuch1[3:8])   # 'iś pr'
print(slownik1['imię'])        # 'Jadwiga'
```

---

### ✏️ Samodzielne zadania: Dostęp i Slicing
1. **Zabawy ze slicingiem tekstu:** Mając zmienną `slowo = "MATEMATYKA"`:
   - Wyciągnij pierwsze 5 znaków słowa (`slowo[:5]`).
   - Wyciągnij ostatnie 4 znaki słowa (`slowo[-4:]`).
   - Wyciągnij tekst bez pierwszego i ostatniego znaku (`slowo[1:-1]`).
   - Odwróć słowo za pomocą wycinania (`slowo[::-1]`).
   - Wyciągnij tylko znaki na indeksach parzystych (`slowo[::2]`).
2. **Wycinanie nieparzystych indeksów oraz nawigacja:**
   - Dla napisu `napis = "Egzamin Maturalny"` wyciągnij znaki na indeksach nieparzystych (`napis[1::2]`).
   - Ze słownika `student = {"dane": {"imie": "Marek", "nazwisko": "Kowalski"}, "oceny": [4, 5, 3, 5]}` pobierz nazwisko oraz drugą ocenę z listy.

---

## 1.5 Wbudowane funkcje i obiekty wywoływalne

```python
print(type("ABC"))         # <class 'str'>
print(len([1, 2, 3]))      # 3
print(sorted([3, 1, 2]))   # [1, 2, 3]
print(sum([10, 20, 30]))   # 60
print(abs(-12))            # 12
```

---

### ✏️ Samodzielne zadania: Wbudowane funkcje
1. Mając listę ocen `oceny = [4.5, 3.0, 5.0, 4.0, 2.0]`, oblicz ich średnią arytmetyczną korzystając wyłącznie z `sum()` i `len()`.
2. Znajdź najkrótsze i najdłuższe słowo z listy `slowa = ["jabłko", "banan", "gruszka", "arbuz", "kiwi"]` używając `min()` i `max()` z argumentem `key=len`.

---

## 1.6 Atrybuty obiektów (Metody i Właściwości)

```python
napis = 'tHis is a sTriNg'
print(napis.lower())       # 'this is a string'
print(napis.upper())       # 'THIS IS A STRING'
print(napis.replace('is', 'XYZ')) # 'tXYZ XYZ a sTriNg'

lista = [1, 2, 3]
lista.append(4)
lista.extend([5, 6])
```

---

### ✏️ Samodzielne zadania: Metody obiektów
1. Mając zmienną `email = "  Jan.Kowalski@Domain.COM  "`: usuń spacje (`.strip()`), zamień na małe litery (`.lower()`) i sprawdź końcówkę (`.endswith(".com")`).
2. Mając dwa zbiory technologii: `osoba1 = {"Python", "SQL", "Git", "C++"}` oraz `osoba2 = {"Python", "Java", "Git", "Docker"}`: znajdź część wspólną (`intersection`) oraz różnicę (`difference`).

---

## 1.7 Argumenty pozycyjne i nazwane w funkcjach

```python
def wypisz_argumenty(arg1, arg2, arg3='domyślna'):
    print(arg1, arg2, arg3)

wypisz_argumenty('a', 'b', 'c')                # Pozycyjne
wypisz_argumenty(arg3='C', arg1='A', arg2='B') # Nazwane
```

---

### ✏️ Samodzielne zadania: Argumenty w funkcjach
1. Napisz funkcję `oblicz_cene_brutto(cena_netto, vat=0.23)`, która zwraca wartość brutto. Wywołaj ją z domyślnym VAT oraz ze stawką 8% (`vat=0.08`).
2. Przetestuj wywołanie z błędną kolejnością argumentów nazwanych i pozycyjnych (np. `func(arg2='B', 'A')`) i zaobserwuj błąd interpretera.

---

## 1.8 Formatowanie łańcuchów znaków (Strings)

```python
imie = 'Alicja'
wiek = 30

# f-strings (zalecany styl Python 3.6+)
print(f'Witaj, {imie}. Masz {wiek} lat.')
print(f'Za 5 lat będziesz mieć {wiek + 5} lat.')
```

---

### ✏️ Samodzielne zadania: Formatowanie stringów
1. Utwórz zmienne `towar = "Kawa"`, `cena = 24.99`, `sztuki = 3`. Używając f-stringa, wygeneruj tekst podsumowania koszyka.
2. Wyświetl liczbę `pi = 3.14159265` z dokładnością do 2 miejsc po przecinku (`{pi:.2f}`).

---

# 2. Praktyka — Zadania programistyczne

Ten rozdział zawiera **10 zadań praktycznych** w języku polskim. **Odpowiedzi i rozwiązania do wszystkich zadań znajdują się w [Sekcji 3 na końcu dokumentu](#3-odpowiedzi-i-rozwiązania-zadań).**

---

## Zadanie 1: Odwracanie łańcucha znaków
### Opis
Należy zaimplementować funkcję, która przyjmuje jako argument ciąg znaków (string) i zwraca go w odwrotnej kolejności. Jest to jedno z klasycznych zadań sprawdzających rozumienie podstaw pracy z sekwencjami.

### Badane umiejętności
* Praca z ciągami znaków (`str`).
* Użycie wycinania (`slicing`).
* Podstawy definiowania funkcji.

### Dane wejściowe
* `s` (`str`): Ciąg znaków do odwrócenia. Długość ciągu wynosi od $0$ do $N$.

### Dane wyjściowe
* (`str`): Nowy ciąg znaków będący odwrotną wersją ciągu wejściowego.

### Przykłady (Dane testowe)
* **Przykład 1:**
  * Wejście: `"Hello, World!"`
  * Wyjście: `"!dlroW ,olleH"`
* **Przykład 2:**
  * Wejście: `"Python"`
  * Wyjście: `"nohtyP"`
* **Przykład 3 (przypadek brzegowy):**
  * Wejście: `""` (pusty napis)
  * Wyjście: `""`

---

## Zadanie 2: Wyszukiwanie najdłuższego słowa
### Opis
Wymagane jest napisanie funkcji, która przyjmuje ciąg znaków składający się ze słów rozdzielonych spacjami i znajduje w nim najdłuższe słowo. Jeśli w tekście kilka słów ma taką samą maksymalną długość, funkcja powinna zwrócić pierwsze z nich.

### Badane umiejętności
* Praca ze stringami: metoda `.split()`.
* Iteracja po liście (pętla `for`).
* Użycie instrukcji warunkowych (`if`).
* Przechowywanie wyników pośrednich w zmiennych.

### Dane wejściowe
* `sentence` (`str`): Ciąg znaków zawierający jedno lub więcej słów rozdzielonych pojedynczą spacją.

### Dane wyjściowe
* (`str`): Najdłuższe słowo w ciągu.

### Przykłady (Dane testowe)
* **Przykład 1:**
  * Wejście: `"Python jest potężnym i uniwersalnym językiem programowania"`
  * Wyjście: `"programowania"`
* **Przykład 2:**
  * Wejście: `"Tworzenie aplikacji wymaga znajomości różnych technologii"`
  * Wyjście: `"technologii"`
* **Przykład 3 (słowa o jednakowej długości):**
  * Wejście: `"trzy dwa raz"`
  * Wyjście: `"trzy"`

---

## Zadanie 3: Sprawdzanie palindromu
### Opis
Należy zaimplementować funkcję sprawdzającą, czy przekazany ciąg znaków jest palindromem. Palindrom to tekst, który czyta się tak samo od lewej do prawej, jak i od prawej do lewej. Podczas sprawdzania należy zignorować wielkość liter oraz wszystkie znaki niebędące literami ani cyframi (znaki interpunkcyjne, spacje itp.).

### Badane umiejętności
* Manipulacje na stringach: zmiana wielkości liter (`.lower()`), sprawdzanie typu znaku (`.isalnum()`).
* Budowanie nowego ciągu znaków na podstawie iteracji.
* Porównywanie stringów i slicing.

### Dane wejściowe
* `s` (`str`): Ciąg znaków do weryfikacji.

### Dane wyjściowe
* (`bool`): `True`, jeśli tekst jest palindromem, oraz `False` w przeciwnym wypadku.

### Przykłady (Dane testowe)
* **Przykład 1:**
  * Wejście: `"А роза упала на лапу Азора"`
  * Wyjście: `True`
* **Przykład 2:**
  * Wejście: `"race a car"`
  * Wyjście: `False`
* **Przykład 3 (złożony przypadek z interpunkcją):**
  * Wejście: `"A man, a plan, a canal: Panama"`
  * Wyjście: `True`

---

## Zadanie 4: Suma elementów listy
### Opis
Należy napisać funkcję, która oblicza sumę elementów liczbowych w podanej liście. Lista może zawierać dane różnych typów (liczby, teksty, wartości logiczne itp.). Funkcja powinna poprawnie obsługiwać takie przypadki, sumując wyłącznie elementy typu `int` oraz `float`.

### Badane umiejętności
* Iteracja po liście.
* Sprawdzanie typu danych za pomocą `isinstance()`.
* Akumulacja wartości w zmiennej.
* Praca z mieszanymi typami danych.

### Dane wejściowe
* `items` (`list`): Lista zawierająca elementy różnorodnych typów.

### Dane wyjściowe
* (`int` lub `float`): Suma wszystkich elementów liczbowych. Jeśli lista nie zawiera liczb, funkcja powinna zwrócić `0`.

### Przykłady (Dane testowe)
* **Przykład 1:**
  * Wejście: `[1, 2, 3, 4, 5]`
  * Wyjście: `15`
* **Przykład 2 (typy mieszane):**
  * Wejście: `[10, "hello", 20.5, True, None, 30]`
  * Wyjście: `60.5`
* **Przykład 3 (brak liczb):**
  * Wejście: `["a", "b", "c"]`
  * Wyjście: `0`
* **Przykład 4 (pusta lista):**
  * Wejście: `[]`
  * Wyjście: `0`

---

## Zadanie 5: Usuwanie duplikatów z listy
### Opis
Należy zaimplementować funkcję, która przyjmuje listę i zwraca nową listę zawierającą tylko unikalne elementy z listy wejściowej. Ważnym warunkiem jest zachowanie pierwotnej kolejności elementów.

### Badane umiejętności
* Iteracja po liście.
* Wykorzystanie instrukcji warunkowych.
* Sprawdzanie przynależności elementu do kolekcji (`in`).
* Tworzenie nowej listy.

### Dane wejściowe
* `items` (`list`): Lista wejściowa z możliwymi duplikatami.

### Dane wyjściowe
* (`list`): Nowa lista zawierająca unikalne elementy, w kolejności zgodnej z ich pierwszym wystąpieniem.

### Przykłady (Dane testowe)
* **Przykład 1:**
  * Wejście: `[1, 2, 3, 2, 4, 1, 5]`
  * Wyjście: `[1, 2, 3, 4, 5]`
* **Przykład 2 (z ciągami znaków):**
  * Wejście: `["apple", "banana", "apple", "orange", "banana", "grape"]`
  * Wyjście: `["apple", "banana", "orange", "grape"]`
* **Przykład 3 (brak duplikatów):**
  * Wejście: `[10, 20, 30]`
  * Wyjście: `[10, 20, 30]`
* **Przykład 4 (pusta lista):**
  * Wejście: `[]`
  * Wyjście: `[]`

---

## Zadanie 6: Analiza częstotliwości słów w tekście
### Opis
Należy napisać funkcję wykonującą analizę częstotliwości słów w przekazanym tekście. Funkcja powinna zwracać słownik, w którym kluczami są unikalne słowa z tekstu, a wartościami — liczba ich powtórzeń. Analiza nie powinna brać pod uwagę wielkości liter, a znaki interpunkcyjne należy zignorować.

### Badane umiejętności
* Praca ze słownikami.
* Operacje na stringach (`.lower()`, `.split()`, usuwanie znaku interpunkcji).
* Iteracja po liście słów.
* Użycie metody słownika `.get()`.

### Dane wejściowe
* `text` (`str`): Tekst do analizy.

### Dane wyjściowe
* (`dict`): Słownik częstotliwości słów.

### Przykłady (Dane testowe)
* **Przykład 1:**
  * Wejście: `"Hello world hello"`
  * Wyjście: `{'hello': 2, 'world': 1}`
* **Przykład 2 (z wielkością liter i interpunkcją):**
  * Wejście: `"The quick brown fox jumps over the lazy dog. The dog was lazy."`
  * Wyjście: `{'the': 3, 'quick': 1, 'brown': 1, 'fox': 1, 'jumps': 1, 'over': 1, 'lazy': 2, 'dog': 2, 'was': 1}`
* **Przykład 3 (pusty napis):**
  * Wejście: `""`
  * Wyjście: `{}`

---

## Zadanie 7: Generator haseł
### Opis
Należy stworzyć funkcję do generowania losowego hasła o podanej długości. Hasło powinno składać się z zestawu znaków obejmującego małe i wielkie litery alfabetu łacińskiego, cyfry oraz znaki specjalne (`!@#$%^&*()_+-=[]{}|;:,.<>/?`).

### Badane umiejętności
* Użycie modułu `random` (`random.choice`).
* Wykorzystanie stałych napisowych z modułu `string`.
* Łączenie listy znaków w string za pomocą `.join()`.

### Dane wejściowe
* `length` (`int`): Oczekiwana długość hasła.

### Dane wyjściowe
* (`str`): Losowo wygenerowane hasło. Jeśli `length` wynosi 0 lub mniej, zwróć pusty napis `""`.

### Przykłady (Dane testowe)
* **Przykład 1:**
  * Wejście: `8` -> Przykładowe wyjście: `"aB5!d(K$"`
* **Przykład 2:**
  * Wejście: `12` -> Przykładowe wyjście: `"z&9pQ_wE!sT3"`
* **Przykład 3:**
  * Wejście: `4` -> Przykładowe wyjście: `"R#t1"`

---

## Zadanie 8: Obliczanie silni
### Opis
Należy napisać funkcję obliczającą silnię nieujemnej liczby całkowitej. Silnia liczby $n$ ($n!$) to iloczyn wszystkich liczb naturalnych od 1 do $n$ włącznie. Z definicji $0! = 1$.

### Badane umiejętności
* Użycie pętli (`for` lub `while`).
* Obsługa przypadków brzegowych ($0, 1$) i niepoprawnych danych (liczby ujemne).

### Dane wejściowe
* `n` (`int`): Nieujemna liczba całkowita.

### Dane wyjściowe
* (`int`): Wartość $n!$. Dla liczb ujemnych funkcja zwraca `None`.

### Przykłady (Dane testowe)
* **Przykład 1:**
  * Wejście: `5` -> Wyjście: `120`
* **Przykład 2:**
  * Wejście: `0` -> Wyjście: `1`
* **Przykład 3:**
  * Wejście: `-3` -> Wyjście: `None`

---

## Zadanie 9: Sprawdzanie liczby pierwszej
### Opis
Należy zaimplementować funkcję, która sprawdza, czy przekazana dodatnia liczba całkowita jest liczbą pierwszą (liczba naturalna większa od 1, dzieląca się tylko przez 1 i samą siebie).

### Badane umiejętności
* Logika budowy pętli i warunków.
* Operator reszty z dzielenia (`%`).
* Optymalizacja (sprawdzanie dzielników do $\sqrt{n}$).

### Dane wejściowe
* `number` (`int`): Liczba całkowita.

### Dane wyjściowe
* (`bool`): `True`, jeśli pierwsza, oraz `False` w przeciwnym wypadku.

### Przykłady (Dane testowe)
* **Przykład 1:**
  * Wejście: `11` -> Wyjście: `True`
* **Przykład 2:**
  * Wejście: `10` -> Wyjście: `False`
* **Przykład 3:**
  * Wejście: `1` -> Wyjście: `False`
* **Przykład 4:**
  * Wejście: `2` -> Wyjście: `True`

---

## Zadanie 10: Prosty parser URL
### Opis
Należy napisać funkcję, która przyjmuje jako napis adres URL i wyciąga z niego nazwę domeny. Funkcja powinna obsługiwać adresy URL z różnymi protokołami (`http://`, `https://`, `ftp://`) oraz z obecnością lub brakiem przedrostka `www.`.

### Badane umiejętności
* Operacje na stringach (`.split()`, `.replace()`, slicing).
* Znajomość struktury adresu URL.

### Dane wejściowe
* `url` (`str`): Ciąg znaków z adresem URL.

### Dane wyjściowe
* (`str`): Nazwa domeny (np. `example.com`).

### Przykłady (Dane testowe)
* **Przykład 1:**
  * Wejście: `"https://www.poisk.com/search?q=python"` -> Wyjście: `"poisk.com"`
* **Przykład 2:**
  * Wejście: `"http://habr.com/ru/articles/"` -> Wyjście: `"habr.com"`
* **Przykład 3:**
  * Wejście: `"yandex.ru"` -> Wyjście: `"yandex.ru"`
* **Przykład 4:**
  * Wejście: `"ftp://files1server.net/folder/file.zip"` -> Wyjście: `"files1server.net"`

---

# 3. Odpowiedzi i rozwiązania zadań

W tej sekcji znajdują się rozwiązania do zadań teoretycznych z Sekcji 1 oraz pełne kody w Pythonie do zadań praktycznych z Sekcji 2.

---

## 3.1 Odpowiedzi do zadań teoretycznych (Sekcja 1)

### Zadania 1.1: Obiekty i zmienne
1. **Przykładowe zmienne i ich typy:**
   ```python
   nazwa = "Kawa"               # str
   cena = 24.99                # float
   ilosc_w_magazynie = 10      # int
   dostepny = True             # bool

   print(type(nazwa), type(cena), type(ilosc_w_magazynie), type(dostepny))
   ```
2. **Poprawione nazwy zmiennych:**
   - `user_1st = "Jan"` (nazwa nie może zaczynać się od cyfry)
   - `user_age = 25` (użycie `_` zamiast `-`)
   - `class_name = "3A"` (`class` jest słowem zastrzeżonym w Pythonie)

### Zadania 1.2: Operatory
1. **Pole i obwód koła ($r = 7.5$):**
   ```python
   r = 7.5
   pi = 3.14159
   pole = pi * (r ** 2)     # 176.7144375
   obwod = 2 * pi * r       # 47.12385
   ```
2. **Wyrażenie logiczne:**
   ```python
   x = 15
   wynik = (x * 2 > 20) and (x * 2 != 30)  # Zwraca False (bo 30 == 30)
   ```

### Zadania 1.3: Kontenery
1. **Wybór kontenera:**
   ```python
   zakupy = ["mleko", "chleb", "jajka", "ser", "masło"]
   punkt_gps = (52.2297, 21.0122)
   # Wyjaśnienie: Krotka (tuple) jest niemutowalna. Współrzędne GPS tworzą stały punkt,
   # którego wartości nie powinny zostać przypadkowo zmienione w trakcie działania programu.
   ```
2. **Unikalność w zbiorze:**
   ```python
   imiona = {"Anna", "Piotr", "Anna", "Paweł", "Piotr"}
   print(imiona)      # Output: {'Anna', 'Piotr', 'Paweł'}
   print(len(imiona)) # Output: 3 (dublety zostały automatycznie usunięte)
   ```

### Zadania 1.4: Dostęp i Slicing
1. **Slicing słowa `slowo = "MATEMATYKA"`:**
   ```python
   slowo = "MATEMATYKA"

   pierwsze_5 = slowo[:5]      # "MATEM"
   ostatnie_4 = slowo[-4:]     # "TYKA"
   bez_krajnych = slowo[1:-1]  # "ATEMATYK"
   odwrocone = slowo[::-1]     # "AKYTAMETAM"
   parzyste = slowo[::2]       # "MTMTK"
   ```
2. **Zaawansowane wycinanie i słowniki:**
   ```python
   napis = "Egzamin Maturalny"
   nieparzyste = napis[1::2] # "gmi aurn"

   student = {"dane": {"imie": "Marek", "nazwisko": "Kowalski"}, "oceny": [4, 5, 3, 5]}
   nazwisko = student["dane"]["nazwisko"] # "Kowalski"
   druga_ocena = student["oceny"][1]       # 5
   ```

### Zadania 1.5: Wbudowane funkcje
1. **Średnia ocen:**
   ```python
   oceny = [4.5, 3.0, 5.0, 4.0, 2.0]
   srednia = sum(oceny) / len(oceny) # 3.7
   ```
2. **Najkrótsze i najdłuższe słowo:**
   ```python
   slowa = ["jabłko", "banan", "gruszka", "arbuz", "kiwi"]
   najkrotsze = min(slowa, key=len) # "kiwi"
   najdluzsze = max(slowa, key=len)  # "gruszka"
   ```

### Zadania 1.6: Metody obiektów
1. **Czyszczenie tekstu:**
   ```python
   email = "  Jan.Kowalski@Domain.COM  "
   email_clean = email.strip().lower() # "jan.kowalski@domain.com"
   is_com = email_clean.endswith(".com") # True
   ```
2. **Analiza zbiorów:**
   ```python
   osoba1 = {"Python", "SQL", "Git", "C++"}
   osoba2 = {"Python", "Java", "Git", "Docker"}
   wspolne = osoba1.intersection(osoba2) # {'Python', 'Git'}
   tylko_osoba1 = osoba1.difference(osoba2) # {'SQL', 'C++'}
   ```

### Zadania 1.7: Argumenty w funkcjach
1. **Kalkulator ceny brutto:**
   ```python
   def oblicz_cene_brutto(cena_netto, vat=0.23):
       return cena_netto * (1 + vat)

   print(oblicz_cene_brutto(100))               # 123.0 (pozycyjnie)
   print(oblicz_cene_brutto(cena_netto=100, vat=0.08)) # 108.0 (nazwanie)
   ```

### Zadania 1.8: Formatowanie stringów
1. **Podsumowanie koszyka:**
   ```python
   towar = "Kawa"
   cena = 24.99
   sztuki = 3
   print(f"Zamówiono {sztuki} szt. towaru {towar}. Łączny koszt: {sztuki * cena:.2f} zł.")
   ```
2. **Zaokrąglanie Pi:**
   ```python
   pi = 3.14159265
   print(f"{pi:.2f}") # "3.14"
   ```

---

## 3.2 Rozwiązania zadań praktycznych (Sekcja 2)

### Rozwiązanie Zadania 1: Odwracanie łańcucha znaków
```python
def reverse_string(s: str) -> str:
    """Zwraca ciąg znaków s w odwrotnej kolejności."""
    return s[::-1]

# Testy
print(reverse_string("Hello, World!"))  # Output: "!dlroW ,olleH"
print(reverse_string("Python"))         # Output: "nohtyP"
print(reverse_string(""))               # Output: ""
```

---

### Rozwiązanie Zadania 2: Wyszukiwanie najdłuższego słowa
```python
def find_longest_word(sentence: str) -> str:
    """Znajduje pierwsze najdłuższe słowo w podanym zdaniu."""
    words = sentence.split()
    if not words:
        return ""
    
    longest_word = words[0]
    for word in words:
        if len(word) > len(longest_word):
            longest_word = word
    return longest_word

# Testy
print(find_longest_word("Python jest potężnym i uniwersalnym językiem programowania")) # "programowania"
print(find_longest_word("Tworzenie aplikacji wymaga znajomości różnych technologii"))     # "technologii"
print(find_longest_word("trzy dwa raz"))                                              # "trzy"
```

---

### Rozwiązanie Zadania 3: Sprawdzanie palindromu
```python
def is_palindrome(s: str) -> bool:
    """Sprawdza, czy napis s jest palindromem (z pominięciem spacji, interpunkcji i wielkości liter)."""
    cleaned = ''.join(char.lower() for char in s if char.isalnum())
    return cleaned == cleaned[::-1]

# Testy
print(is_palindrome("А роза упала на лапу Азора"))       # True
print(is_palindrome("race a car"))                      # False
print(is_palindrome("A man, a plan, a canal: Panama"))   # True
```

---

### Rozwiązanie Zadania 4: Suma elementów listy
```python
def sum_numeric_elements(items: list):
    """Zwraca sumę elementów int oraz float znajdujących się w liście items."""
    total = 0
    for item in items:
        # W Pythonie bool dziedziczy po int (isinstance(True, int) == True),
        # dlatego wyraźnie wykluczamy typ bool!
        if isinstance(item, (int, float)) and not isinstance(item, bool):
            total += item
    return total

# Testy
print(sum_numeric_elements([1, 2, 3, 4, 5]))                       # 15
print(sum_numeric_elements([10, "hello", 20.5, True, None, 30]))   # 60.5
print(sum_numeric_elements(["a", "b", "c"]))                       # 0
print(sum_numeric_elements([]))                                    # 0
```

---

### Rozwiązanie Zadania 5: Usuwanie duplikatów z listy
```python
def remove_duplicates(items: list) -> list:
    """Zwraca nową listę bez duplikatów z zachowaniem oryginalnej kolejności."""
    unique_items = []
    seen = set()
    for item in items:
        if item not in seen:
            seen.add(item)
            unique_items.append(item)
    return unique_items

# Testy
print(remove_duplicates([1, 2, 3, 2, 4, 1, 5])) 
# Output: [1, 2, 3, 4, 5]

print(remove_duplicates(["apple", "banana", "apple", "orange", "banana", "grape"])) 
# Output: ['apple', 'banana', 'orange', 'grape']

print(remove_duplicates([10, 20, 30])) # Output: [10, 20, 30]
print(remove_duplicates([]))           # Output: []
```

---

### Rozwiązanie Zadania 6: Analiza częstotliwości słów w tekście
```python
import string

def word_frequency(text: str) -> dict:
    """Zwraca słownik częstotliwości występowania słów w tekście."""
    cleaned_text = text.translate(str.maketrans('', '', string.punctuation)).lower()
    words = cleaned_text.split()
    
    frequency = {}
    for word in words:
        frequency[word] = frequency.get(word, 0) + 1
    return frequency

# Testy
print(word_frequency("Hello world hello"))
# Output: {'hello': 2, 'world': 1}

print(word_frequency("The quick brown fox jumps over the lazy dog. The dog was lazy."))
# Output: {'the': 3, 'quick': 1, 'brown': 1, 'fox': 1, 'jumps': 1, 'over': 1, 'lazy': 2, 'dog': 2, 'was': 1}

print(word_frequency(""))
# Output: {}
```

---

### Rozwiązanie Zadania 7: Generator haseł
```python
import random
import string

def generate_password(length: int) -> str:
    """Generuje losowe hasło o długości length złożone z liter, cyfr i znaków specjalnych."""
    if length <= 0:
        return ""
    
    characters = string.ascii_letters + string.digits + "!@#$%^&*()_+-=[]{}|;:,.<>/?"
    return ''.join(random.choice(characters) for _ in range(length))

# Testy
print(generate_password(8))   # np. "aB5!d(K$"
print(generate_password(12))  # np. "z&9pQ_wE!sT3"
print(generate_password(0))   # ""
```

---

### Rozwiązanie Zadania 8: Obliczanie silni
```python
def factorial(n: int):
    """Zwraca silnię n! dla nieujemnych liczb całkowitych."""
    if n < 0:
        return None
    result = 1
    for i in range(1, n + 1):
        result *= i
    return result

# Testy
print(factorial(5))   # 120
print(factorial(0))   # 1
print(factorial(1))   # 1
print(factorial(-3))  # None
```

---

### Rozwiązanie Zadania 9: Sprawdzanie liczby pierwszej
```python
def is_prime(number: int) -> bool:
    """Sprawdza, czy liczba całkowita number jest liczbą pierwszą."""
    if number <= 1:
        return False
    if number == 2:
        return True
    if number % 2 == 0:
        return False
    
    for d in range(3, int(number**0.5) + 1, 2):
        if number % d == 0:
            return False
    return True

# Testy
print(is_prime(11))  # True
print(is_prime(10))  # False
print(is_prime(1))   # False
print(is_prime(2))   # True
```

---

### Rozwiązanie Zadania 10: Prosty parser URL
```python
def parse_domain(url: str) -> str:
    """Wyciąga nazwę domeny z przekazanego adresu URL."""
    if "://" in url:
        url = url.split("://")[1]
        
    url = url.split("/")[0].split("?")[0]
    
    if url.startswith("www."):
        url = url[4:]
        
    return url

# Testy
print(parse_domain("https://www.poisk.com/search?q=python"))  # "poisk.com"
print(parse_domain("http://habr.com/ru/articles/"))          # "habr.com"
print(parse_domain("yandex.ru"))                             # "yandex.ru"
print(parse_domain("ftp://files1server.net/folder/file.zip"))# "files1server.net"
```
