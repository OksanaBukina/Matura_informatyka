# 🐍 Podstawy języka Python
Kompleksowy konspekt wiedzy z podstaw języka Python. Zawiera omówienie typów danych, operatorów, kontenerów, funkcji wbudowanych, metod obiektów oraz formatowania tekstu, wraz z czytelnymi przykładami kodu oraz **samodzielnymi zadaniami** po każdym dziale.

---

## 📋 Spis treści
1. [Obiekty, podstawowe typy i zmienne](#1-obiekty-podstawowe-typy-i-zmienne)
2. [Podstawowe operatory](#2-podstawowe-operatory)
3. [Podstawowe kontenery](#3-podstawowe-kontenery)
4. [Dostęp do danych w kontenerach (Indeksowanie i Slicing)](#4-dostęp-do-danych-w-kontenerach-indeksowanie-i-slicing)
5. [Wbudowane funkcje i obiekty wywoływalne](#5-wbudowane-funkcje-i-obiekty-wywoływalne)
6. [Atrybuty obiektów (Metody i Właściwości)](#6-atrybuty-obiektów-metody-i-właściwości)
7. [Argumenty pozycyjne i nazwane w funkcjach](#7-argumenty-pozycyjne-i-nazwane-w-funkcjach)
8. [Formatowanie łańcuchów znaków (Strings)](#8-formatowanie-łańcuchów-znaków-strings)

---

## 1. Obiekty, podstawowe typy i zmienne

Wszystko w Pythonie jest **obiektem** posiadającym określony **typ**. Zmienne to nazwy przypisane do obiektów w pamięci.

### Podstawowe typy danych:
* **`int`** — liczby całkowite, np. `20`, `-3`, `0`
* **`float`** — liczby zmiennoprzecinkowe (z częścią dziesiętną), np. `9.57`, `-0.03`
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
   - `user-age = 18`
   - `class = "2A"`

---

## 2. Podstawowe operatory

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
# Przypisanie kilku liczb do różnych zmiennych
liczba1 = 1
liczba2 = 2
liczba3 = 3
liczba4 = 45
liczba5 = 2130
liczba6 = -25
liczba7 = 8.132

# Operacje arytmetyczne
print(liczba1 + liczba2)   # 3
print(liczba2 - liczba3)   # -1
print(liczba3 * liczba4)   # 135
print(liczba4 / liczba5)   # 0.02112676056
print(liczba5 ** liczba2)  # 4536900

# Operatory przypisania z modyfikacją
liczba4 += 4   # liczba4 wynosi teraz 49
liczba6 -= 2   # liczba6 wynosi teraz -27
liczba4 *= 5   # liczba4 wynosi teraz 225

# Łączenie operatorów
liczba8 = liczba1 + liczba2 * liczba3   # 1 + (2 * 3) = 7

# Porównania
print(liczba1 + liczba2 == liczba3)   # True
print(liczba3 != liczba4)             # True
print(liczba5 < liczba6)              # False

# Porównania łańcuchowe
print(5 > 3 > 1)             # True
print(5 > 3 < 4 == 3 + 1)    # True

# Operacje na ciągach znaków (str)
prosty_lancuch1 = 'jakiś przykład'
prosty_lancuch2 = "pomarańcze"

print(prosty_lancuch1 + ' użycia operatora +')   # 'jakiś przykład użycia operatora +'
print(prosty_lancuch2 * 4)                       # 'pomarańczepomarańczepomarańczepomarańcze'
print((prosty_lancuch2 + " ") * 4)               # 'pomarańcze pomarańcze pomarańcze pomarańcze '

prosty_lancuch1 += ' który ponownie przypisał oryginalny łańcuch'
prosty_lancuch2 *= 3
```

> [!CAUTION]
> Operatory odejmowania (`-`), dzielenia (`/`) oraz dekrementacji (`-=`) nie mają zastosowania do łańcuchów znaków (`str`).

---

### ✏️ Samodzielne zadania: Operatory
1. **Kalkulator geometrii:** Oblicz pole i obwód koła o promieniu $r = 7.5$ używając wzorów $P = \pi \cdot r^2$ oraz $O = 2 \cdot \pi \cdot r$ (przyjmij $\pi = 3.14159$).
2. **Wyrażenie logiczne:** Sprawdź za pomocą jednego wyrażenia logicznego w Pythonie, czy podwojona wartość zmiennej $x = 15$ jest większa od 20 i jednocześnie różna od 30.

---

## 3. Podstawowe kontenery

Kontenery to obiekty używane do grupowania innych obiektów.

> [!NOTE]
> - **Obiekty mutowalne (zmienne):** można modyfikować po utworzeniu (np. `list`, `set`, `dict`).
> - **Obiekty niemutowalne (niezmienne):** nie można ich modyfikować po utworzeniu (np. `str`, `tuple`, `int`, `float`).

### Przegląd typów kontenerowych

| Typ | Nazwa | Mutowalność | Indeksowanie | Opis | Przykład |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `str` | Łańcuch | Niemutowalny | Liczbami (`int`) | Sekwencja znaków | `'Python'` |
| `list` | Lista | Mutowalna | Liczbami (`int`) | Uporządkowana sekwencja | `[3, 5, 'pies', False]` |
| `tuple` | Krotka | Niemutowalna | Liczbami (`int`) | Uporządkowana, niezmienna sekwencja | `(3, 5, 'pies', False)` |
| `set` | Zbiór | Mutowalny | Brak | Nieuporządkowane Unikalne elementy | `{3, 5, 'pies', False}` |
| `dict` | Słownik | Mutowalny | Kluczami | Pary `klucz: wartość` | `{'imię': 'Jadwiga', 'wiek': 23}` |

### Przykłady kodu

```python
# Definiowanie kontenerów
lista1 = [3, 5, 6, 3, 'pies', 'kot', False]
krotka1 = (3, 5, 6, 3, 'pies', 'kot', False)
zbior1 = {3, 5, 6, 3, 'pies', 'kot', False}
slownik1 = {'imię': 'Jadwiga', 'wiek': 23, 'ulub_jedzenie': ['pizza', 'owoce', 'ryba']}

# Elementy w zbiorze usuwają dublety i nie mają określonej kolejności!
print(zbior1)   # Output np.: {False, 3, 5, 6, 'kot', 'pies'}

# Operacje łączenia i powielania sekwencji (+, *, +=, *=)
lista1 += [5, 'winogrona']
krotka1 += (5, 'winogrona')

print([1, 2, 3, 4] * 2)   # [1, 2, 3, 4, 1, 2, 3, 4]
print((1, 2, 3, 4) * 3)   # (1, 2, 3, 4, 1, 2, 3, 4, 1, 2, 3, 4)
```

---

### ✏️ Samodzielne zadania: Kontenery
1. **Wybór kontenera:** Utwórz listę `zakupy` zawierającą 5 produktów oraz krotkę `punkt_gps` zawierającą dwie wartości (szerokość i długość geograficzna). Wyjaśnij w komentarzu kodu, dlaczego dla pozycji GPS lepsza jest krotka niż lista.
2. **Unikalność w zbiorze:** Utwórz zbiór `imiona = {"Anna", "Piotr", "Anna", "Paweł", "Piotr"}`. Wyświetl go i sprawdź, ile elementów ostatecznie w nim pozostało.

---

## 4. Dostęp do danych w kontenerach (Indeksowanie i Slicing)

W przypadku `str`, `list` i `tuple` używamy nawiasów kwadratowych `[]` do indeksowania liczbowego (od `0`). Słowniki `dict` indeksujemy za pomocą ich **kluczy**.

> [!WARNING]
> Zbiory (`set`) nie są indeksowane — użycie `zbior[0]` zgłosi błąd `TypeError`.

### Składnia wycinania (Slicing): `sekwencja[start:stop:step]`
- `start`: indeks początkowy (włącznie)
- `stop`: indeks końcowy (wyłącznie)
- `step`: krok (opcjonalnie, domyślnie 1)
- Ujemny indeks (np. `-1`) oznacza dostęp od końca sekwencji.

### Przykłady kodu

```python
lista1 = [3, 5, 6, 3, 'pies', 'kot', False, 5, 'winogrona']
krotka1 = (3, 5, 6, 3, 'pies', 'kot', False, 5, 'winogrona')
prosty_lancuch1 = 'jakiś przykład'
slownik1 = {'imię': 'Jadwiga', 'wiek': 23, 'ulub_jedzenie': ['pizza', 'owoce', 'ryba']}

# Dostęp do pojedynczych elementów
print(lista1[0])        # Pierwszy element: 3
print(krotka1[-1])      # Ostatni element: 'winogrona'

# Wycinanie (slicing)
print(prosty_lancuch1[3:8])   # Od indeksu 3 do 7: 'iś pr'
print(krotka1[:-3])           # Od początku do 3. elementu od końca: (3, 5, 6, 3, 'pies', 'kot')
print(lista1[4:])             # Od indeksu 4 do końca: ['pies', 'kot', False, 5, 'winogrona']

# Dostęp do danych w słowniku
print(slownik1['imię'])                  # 'Jadwiga'
print(slownik1['ulub_jedzenie'][2])      # 'ryba' (trzeci element z listy wewnątrz słownika)
```

---

### ✏️ Samodzielne zadania: Dostęp i Slicing
1. **Zabawy ze stringiem:** Dla napisu `napis = "Programowanie w Pythonie"`:
   - Wyciągnij słowo `"Pythonie"` używając ujemnych indeksów slicing `napis[-8:]`.
   - Odwróć cały napis za pomocą wycinania z krokiem `-1`.
2. **Nawigacja w strukturach:** Ze słownika `student = {"dane": {"imie": "Marek", "nazwisko": "Kowalski"}, "oceny": [4, 5, 3, 5]}` pobierz i wyświetl nazwisko oraz drugą ocenę z listy.

---

## 5. Wbudowane funkcje i obiekty wywoływalne

Funkcja to obiekt Pythona, który wywołujemy nawiasami `()`, aby wykonać działanie lub obliczyć i zwrócić wynik.

### Najważniejsze funkcje wbudowane

| Funkcja | Opis | Przykład | Wynik |
| :--- | :--- | :--- | :--- |
| `type(obj)` | Zwraca typ obiektu | `type("ABC")` | `<class 'str'>` |
| `len(kontener)` | Zwraca liczbę elementów | `len([1, 2, 3])` | `3` |
| `callable(obj)` | Sprawdza, czy obiekt jest wywoływalny | `callable(len)` | `True` |
| `sorted(kontener)` | Zwraca nową, posortowaną listę | `sorted([3, 1, 2])` | `[1, 2, 3]` |
| `sum(kontener)` | Oblicza sumę liczb w kontenerze | `sum([1, 2, 3])` | `6` |
| `min(kontener)` | Najmniejszy element | `min([1, 2, 3])` | `1` |
| `max(kontener)` | Największy element | `max([1, 2, 3])` | `3` |
| `abs(liczba)` | Wartość bezwzględna | `abs(-12)` | `12` |
| `repr(obj)` | Reprezentacja napisowa obiektu | `repr({1, 2})` | `'{1, 2}'` |

> 🔗 Pełną listę wbudowanych funkcji znajdziesz w [Oficjalnej dokumentacji Pythona](https://docs.python.org/3/library/functions.html).

### Przykłady kodu

```python
prosty_lancuch1 = 'jakiś przykład'
slownik1 = {'imię': 'Jadwiga', 'wiek': 23, 'ulub_jedzenie': ['pizza', 'owoce', 'ryba']}
zbior1 = {3, 5, 6, False, 'kot', 'pies'}

print(type(prosty_lancuch1))   # <class 'str'>
print(len(slownik1))           # 3
print(callable(len))           # True
print(callable(slownik1))      # False

# Sortowanie liczb i tekstów (Wielkie litery trafiają na początek!)
print(sorted([10, 1, 3.6, 7, 5, 2, -3]))
# Output: [-3, 1, 2, 3.6, 5, 7, 10]

print(sorted(['psy', 'koty', 'zebry', 'Chicago', 'Kalifornia', 'mrówki', 'myszy']))
# Output: ['Chicago', 'Kalifornia', 'koty', 'mrówki', 'myszy', 'psy', 'zebry']

# Operacje statystyczne i matematyczne
liczby = [10, 1, 3.6, 7, 5, 2, -3]
print(sum(liczby))   # 25.6
print(min(liczby))   # -3
print(max(liczby))   # 10
print(abs(-12))      # 12
print(repr(zbior1))  # "{False, 3, 5, 6, 'pies', 'kot'}"
```

---

### ✏️ Samodzielne zadania: Wbudowane funkcje
1. **Średnia ocen:** Mając listę ocen `oceny = [4.5, 3.0, 5.0, 4.0, 2.0]`, oblicz ich średnią arytmetyczną korzystając wyłącznie z funkcji `sum()` oraz `len()`.
2. **Najdłuższe słowo:** Znajdź najkrótsze i najdłuższe słowo z listy `slowa = ["jabłko", "banan", "gruszka", "arbuz", "kiwi"]` używając funkcji `min()` i `max()` z przekazanym argumentem nazwanym `key=len`.

---

## 6. Atrybuty obiektów (Metody i Właściwości)

Dostęp do atrybutów obiektu uzyskuje się za pomocą kropki: `obiekt.atrybut`.
- **Metoda:** wywoływalny atrybut (funkcja związana z obiektem, np. `napis.upper()`).
- **Właściwość (Property):** dana / informacja opisująca obiekt.
- `dir(obiekt)` — zwraca listę wszystkich dostępnych atrybutów obiektu.

---

### A. Metody dla łańcuchów znaków (`str`)

* `.capitalize()` — Pierwszy znak wielką literą.
* `.upper()` — Wszystkie znaki wielkimi literami.
* `.lower()` — Wszystkie znaki małymi literami.
* `.count(podłańcuch)` — Zlicza wystąpienia podłańcucha.
* `.startswith(podłańcuch)` — Sprawdza, czy napis zaczyna się od podłańcucha.
* `.endswith(podłańcuch)` — Sprawdza, czy napis kończy się podłańcuchem.
* `.replace(stary, nowy[, limit])` — Zastępuje wystąpienia tekstal

```python
jakis_lancuch = 'tHis is a sTriNg'

print(jakis_lancuch.capitalize())   # 'This is a string'
print(jakis_lancuch.upper())        # 'THIS IS A STRING'
print(jakis_lancuch.lower())        # 'this is a string'

# Wywołania metod nie modyfikują oryginalnego stringa!
print(jakis_lancuch.count('i'))     # 3
print(jakis_lancuch.count('is'))    # 2

print(jakis_lancuch.lower().startswith('this'))   # True
print(jakis_lancuch.endswith('Ng'))               # True

print(jakis_lancuch.replace('is', 'XYZ'))         # 'tXYZ XYZ a sTriNg'
print(jakis_lancuch.replace('i', '!', 2))         # 'tH!s !s a sTriNg'
```

---

### B. Metody dla list (`list`)

* `.append(element)` — Dodaje pojedynczy element na koniec listy.
* `.extend([el1, el2])` — Dodaje wiele elementów z innej sekwencji.
* `.remove(element)` — Usuwa pierwsze wystąpienie wskazanego elementu.
* `.pop([indeks])` — Usuwa i zwraca element z podanego indeksu (domyślnie ostatni).

```python
jakas_lista = [1, 2, 3, 'witaj']

jakas_lista.append(True)          # [1, 2, 3, 'witaj', True]
jakas_lista.extend([4, 5, 6])     # [1, 2, 3, 'witaj', True, 4, 5, 6]
jakas_lista.remove('witaj')       # [1, 2, 3, True, 4, 5, 6]

ostatni = jakas_lista.pop()       # Zwraca 6, lista: [1, 2, 3, True, 4, 5]
pierwszy = jakas_lista.pop(0)     # Zwraca 1, lista: [2, 3, True, 4, 5]
```

---

### C. Metody dla zbiorów (`set`)

* `.add(element)` — Dodaje element do zbioru.
* `.update(inne_zbiory)` — Dodaje elementy ze zbiorów / sekwencji.
* `.remove(element)` — Usuwa element ze zbioru.
* `.pop()` — Usuwa i zwraca losowy element.
* `.difference(zbior2)` — Różnica zbiorów ($A \setminus B$).
* `.intersection(zbior2)` — Iloczyn / część wspólna ($A \cap B$).
* `.union(zbior2)` — Suma zbiorów ($A \cup B$).
* `.symmetric_difference(zbior2)` — Różnica symetryczna.
* `.issuperset(zbior2)` / `.issubset(zbior2)` — Test nadzbioru / podzbioru.

```python
zbior_a = {1, 2, 3, 4, 5}
zbior_b = {4, 5, 6, 7, 8}

zbior_a.add(0)
zbior_a.update([1, 9, 10])

print(zbior_a.difference(zbior_b))             # Elementy w A nieobecne w B
print(zbior_a.intersection(zbior_b))           # Część wspólna: {4, 5}
print(zbior_a.union(zbior_b))                  # Suma obu zbiorów
print(zbior_a.symmetric_difference(zbior_b))   # Unikalne dla poszczególnych zbiorów

print(zbior_a.issuperset({1, 9}))   # True
print({4, 5}.issubset(zbior_b))     # True
```

---

### D. Metody dla słowników (`dict`)

* `.update(slownik2)` — Dodaje lub aktualizuje pary klucz-wartość.
* `.pop(klucz[, domyslna])` — Usuwa klucz i zwraca jego wartość.
* `.get(klucz[, domyslna])` — Bezpiecznie pobiera wartość bez ryzyka błędu `KeyError`.
* `.keys()` — Zwraca listę / widok kluczy.
* `.values()` — Zwraca listę / widok wartości.
* `.items()` — Zwraca pary `(klucz, wartość)` w postaci krotek.

```python
slownik_a = {'a': 1, 'b': 2, 'c': 3}

slownik_a.update([('d', 4), ('e', 5)])
slownik_a.update({'a': 100, 'f': 6})   # Wartość klucza 'a' zostaje nadpisana!

wartosc_b = slownik_a.pop('b')
wartosc_z = slownik_a.pop('z', 'Nie dotyczy')

print(slownik_a.get('c'))                   # 3
print(slownik_a.get('z', 'Nie znaleziono'))   # 'Nie znaleziono'

print(slownik_a.keys())     # dict_keys(['a', 'c', 'd', 'e', 'f'])
print(slownik_a.values())   # dict_values([100, 3, 4, 5, 6])
print(slownik_a.items())    # dict_items([('a', 100), ('c', 3), ...])
```

---

### ✏️ Samodzielne zadania: Metody obiektów
1. **Czyszczenie tekstu:** Mając zmienną `email = "  Jan.Kowalski@Domain.COM  "`:
   - Usuń spory spacji na początku i końcu za pomocą metody `.strip()`.
   - Przekształć cały ciąg na małe litery za pomocą `.lower()`.
   - Sprawdź metodą `.endswith()`, czy adres kończy się domeną `".com"`.
2. **Analiza umiejętności:** Mając dwa zbiory technologii: `osoba1 = {"Python", "SQL", "Git", "C++"}` oraz `osoba2 = {"Python", "Java", "Git", "Docker"}`:
   - Wyznacz wspólne umiejętności obydwu osób (`intersection`).
   - Wyznacz umiejętności, które ma pierwsza osoba, ale nie ma ich druga osoba (`difference`).

---

## 7. Argumenty pozycyjne i nazwane w funkcjach

Funkcje wywołujemy przekazując argumenty **pozycyjne** (positional) lub **nazwane** (keyword arguments).

```python
def wypisz_argumenty(arg1, arg2, arg3='wartość_domyślna'):
    print('arg1 to:', arg1)
    print('arg2 to:', arg2)
    print('arg3 to:', arg3)
```

### Zasady przekazywania argumentów
1. **Argumenty pozycyjne:** musimy zachować dokładną kolejność zdefiniowaną w funkcji.
2. **Argumenty nazwane:** możemy podawać je w dowolnej kolejności, określając nazwę argumentu (`nazwa=wartość`).
3. **Wywołanie mieszane:** argumenty pozycyjne **zawsze muszą być umieszczone przed** argumentami nazwanymi!

### Przykłady kodu

```python
# Wywołanie z argumentami pozycyjnymi
wypisz_argumenty('a', 'b', 'c')

# Wywołanie z argumentami nazwanymi (kolejność dowolna)
wypisz_argumenty(arg3='C', arg1='A', arg2='B')

# Wywołanie mieszane (pozycyjne pierwsze!)
wypisz_argumenty('pierwszy', arg3='trzeci', arg2='drugi')

# Wywołanie z wykorzystaniem wartości domyślnej
wypisz_argumenty('jabłko', 'banan')   # arg3 przybiera wartość domyślną

# ❌ BŁĄD SYNTAKSY (SyntaxError): argument pozycyjny po nazwanym!
# wypisz_argumenty(arg1='x', 'y', 'z')
```

---

### ✏️ Samodzielne zadania: Argumenty w funkcjach
1. **Kalkulator ceny brutto:** Napisz funkcję `oblicz_cene_brutto(cena_netto, vat=0.23)`, która zwraca wartość brutto. Wywołaj ją na dwa sposoby:
   - Podając jedynie `cena_netto` pozycyjnie.
   - Podając `cena_netto = 100` oraz `vat = 0.08` przy użyciu argumentów nazwanych.
2. **Analiza błędów:** Przetestuj w interpreterze wywołanie `wypisz_argumenty(arg2='B', 'A')` i zapoznaj się z komunikatem błędu podawanym przez Pythona.

---

## 8. Formatowanie łańcuchów znaków (Strings)

W Pythonie używamy trzech głównych sposobów wstawiania wartości do ciągów znaków:

### 1. "Stary" styl (operator `%`)
```python
imie = 'Alicja'
wiek = 30
print('Witaj, %s. Masz %d lat.' % (imie, wiek))
```

### 2. "Nowy" styl (metoda `.format()`)
```python
# Kolejność domyślna
print('Witaj, {}. Masz {} lat.'.format(imie, wiek))

# Indeksy pozycyjne
print('Witaj, {1}. Masz {0} lat. Tak, {1}!'.format(wiek, imie))

# Nazwane placeholdery
print('Witaj, {n}. Masz {a} lat.'.format(n=imie, a=wiek))
```

### 3. "Najnowszy" i rekomendowany styl: **f-strings** (Python 3.6+)
Prefiks `f` przed cudzysłowem pozwala na bezpośrednie umieszczanie zmiennych i wyrażeń w nawiasach klamrowych `{}`.

```python
print(f'Witaj, {imie}. Masz {wiek} lat.')

# Wyrażenia bezpośrednio w f-stringu
print(f'Za 5 lat {imie} będzie mieć {wiek + 5} lat.')
print(f'Twoje imię wielkimi literami to {imie.upper()}.')
```

---

### ✏️ Samodzielne zadania: Formatowanie stringów
1. **Podsumowanie koszyka:** Utwórz zmienne `towar = "Kawa"`, `cena = 24.99`, `sztuki = 3`. Używając **f-stringa**, wygeneruj tekst podsumowania:
   `"Zamówiono 3 szt. towaru Kawa. Łączny koszt: 74.97 zł."` (oblicz koszt wewnątrz f-stringa).
2. **Precyzja zmiennoprzecinkowa:** Wyświetl wartość `pi = 3.14159265` z dokładnością do dwóch miejsc po przecinku (wskazówka: użyj specyfikatora formatu `{pi:.2f}`).
