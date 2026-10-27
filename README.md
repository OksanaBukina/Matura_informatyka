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
  - [1.6 Atrybuty obiektów Pythona (Metody i Właściwości)](#16-atrybuty-obiektów-pythona-metody-i-właściwości)
  - [1.7 Funkcja filtrowanie listy](#17-funkcja-filtrowanie-listy)
  - [1.8 Argumenty pozycyjne i nazwane (keyword) w obiektach wywoływalnych](#18-argumenty-pozycyjne-i-nazwane-keyword-w-obiektach-wywoływalnych)
  - [1.9 Formatowanie łańcuchów i używanie placeholderów](#19-formatowanie-łańcuchów-i-używanie-placeholderów)
  - [1.10 Algorytmy NWD i NWW (Algorytm Euklidesa)](#110-algorytmy-nwd-i-nww-algorytm-euklidesa)
  - [1.11 Instrukcje warunkowe (if, elif, else)](#111-instrukcje-warunkowe-if-elif-else)
  - [1.12 Pętle w Pythonie (while oraz for)](#112-pętle-w-pythonie-while-oraz-for)
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
  - [Zadanie 11: Generator opisów w menu kawiarni](#zadanie-11-generator-opisów-w-menu-kawiarni)
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

print(lista1[0])                    # 3
print(prosty_lancuch1[3:8])         # 'iś pr'
```

---

### ✏️ Samodzielne zadania: Dostęp i Slicing
1. **Zabawy ze slicingiem tekstu:** Mając zmienną `slowo = "MATEMATYKA"`:
   - Wyciągnij pierwsze 5 znaków słowa .
   - Wyciągnij ostatnie 4 znaki słowa .
   - Wyciągnij tekst bez pierwszego i ostatniego znaku .
   - Odwróć słowo za pomocą wycinania .
   - Wyciągnij tylko znaki na indeksach parzystych (.
2. **Wycinanie nieparzystych indeksów oraz nawigacja:**
   - Dla napisu `napis = "Egzamin Maturalny"` wyciągnij znaki na indeksach nieparzystych .
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

## 1.6 Atrybuty obiektów Pythona (Metody i Właściwości)

Różne typy obiektów w Pythonie mają różne **atrybuty**, do których można odwoływać się po nazwie (podobnie jak do zmiennej). Aby uzyskać dostęp do atrybutu obiektu, użyj kropki (`.`) po obiekcie, a następnie podaj atrybut (tj. `obiekt.atrybut`).

* **Metoda:** Kiedy atrybut obiektu jest **wywoływalny**, ten atrybut nazywa się **metodą**. Jest to to samo co funkcja, tylko ta funkcja jest związana z konkretnym obiektem (np. `napis.upper()`).
* **Właściwość (Property):** Kiedy atrybut obiektu **nie jest wywoływalny**, ten atrybut nazywa się **właściwością**. Jest to po prostu fragment danych o obiekcie, który sam w sobie jest innym obiektem (np. `liczba_zespolona.real`).
* `dir(obiekt)` — zwraca listę wszystkich dostępnych atrybutów obiektu.

---

### Metody dla łańcuchów znaków (`str`)

* `.capitalize()` — Pierwszy znak wielką literą.
* `.upper()` — Wszystkie znaki wielkimi literami.
* `.lower()` — Wszystkie znaki małymi literami.
* `.count(sub)` — Zlicza wystąpienia podłańcucha.
* `.startswith(sub)` — Sprawdza, czy napis zaczyna się od podłańcucha `sub`.
* `.endswith(sub)` — Sprawdza, czy napis kończy się podłańcuchem `sub`.
* `.replace(old, new[, count])` — Zastępuje wystąpienia tekstu.
* `strip("#!")` - usuwania białych (domyślnie bez parametru) lub wskazanych znaków (z parametru) na początku i na końcu ciągów
* `.split` - zamiana tekstu na listę i listy na tekst
* ` .join()` - zamiana listy na tekst
* `.clear()` - usuwa wszystkie elementy z listy
* `.sort([key])`- sortuje elementy listy. Domyślnie sortuje w porządku rosnącym (niemalejącym), ale za pomocą parametru key można przekazać funkcję określającą kryterium sortowania.
* `copy()` -tworzy kopię listy
  

#### Przykłady i objaśnienie metod łańcuchowych:

```python
jakis_lancuch = 'tHis is a sTriNg'

# Zwróć wersję łańcucha z wielką pierwszą literą
print(jakis_lancuch.capitalize())   # Output: 'This is a string'

# Zwróć wersję łańcucha pisaną wielkimi literami
print(jakis_lancuch.upper())        # Output: 'THIS IS A STRING'

# Zwróć wersję łańcucha pisaną małymi literami
print(jakis_lancuch.lower())        # Output: 'this is a string'

# Zlicz liczbę wystąpień podłańcucha w łańcuchu
print(jakis_lancuch.count('i'))     # Output: 3
print(jakis_lancuch.count('i', 7))  # Output: 1 (zliczanie od indeksu 7)
print(jakis_lancuch.count('is'))    # Output: 2

# Czy łańcuch zaczyna się od 'this'?
print(jakis_lancuch.startswith('this'))  # Output: False (wielkość liter ma znaczenie!)

# Czy łańcuch pisany małymi literami zaczyna się od 'this'? (Łączenie metod .lower() i .startswith())
print(jakis_lancuch.lower().startswith('this'))  # Output: True

# Czy łańcuch kończy się na 'Ng'?
print(jakis_lancuch.endswith('Ng'))  # Output: True

# Zwróć wersję łańcucha z podłańcuchem zastąpionym czymś innym
print(jakis_lancuch.replace('is', 'XYZ'))   # Output: 'tXYZ XYZ a sTriNg'
print(jakis_lancuch.replace('i', '!'))      # Output: 'tH!s !s a sTriNg'
print(jakis_lancuch.replace('i', '!', 2))   # Output: 'tH!s !s a sTriNg' (zastąp tylko pierwsze 2 wystąpienia)

text2 = "###hello!!!"
print(text2.strip("#!"))  # "hello"

napis="           MINISTERSTWO DO SPRAW NIEZBYT ISTOTNYCH SPRAW  "
print(napis.strip())

napis="MINISTERSTWO DO SPRAW NIEZBYT ISTOTNYCH SPRAW"
print(napis.split()) #['MINISTERSTWO', 'DO', 'SPRAW', 'NIEZBYT', 'ISTOTNYCH', 'SPRAW']
```

---

### Metody dla list (`list`)

```python
jakas_lista = [1, 2, 3, 'witaj']

# Dodaj pojedynczy element na koniec listy
jakas_lista.append(True)
print(jakas_lista)   # [1, 2, 3, 'witaj', True]

# Dodaj wiele elementów do listy
jakas_lista.extend([4, 5, 6])
print(jakas_lista)   # [1, 2, 3, 'witaj', True, 4, 5, 6]

# Usuń pojedynczy element z listy
jakas_lista.remove('witaj')
print(jakas_lista)   # [1, 2, 3, True, 4, 5, 6]

# Usuń i zwróć element z końca listy
ostatni = jakas_lista.pop()
print(ostatni)       # 6
print(jakas_lista)   # [1, 2, 3, True, 4, 5]

# Usuń i zwróć element o podanym indeksie
pierwszy = jakas_lista.pop(0)
print(pierwszy)      # 1
print(jakas_lista)   # [2, 3, True, 4, 5]

tagi_produkt1 = ['buty', 'sportowe', 'nike', 'rozmiar-42']
print(' | '.join(tagi_produkt1)) # 'buty | sportowe | nike | rozmiar-42'

# intersection - zwraca nowy zbiór zawierający elementy wspólne dla dwóch lub więcej zbiorów
# difference - służy do znajdowania różnicy między zbiorami (typ set), zwracając elementy, które znajdują się w pierwszym zbiorze, ale # nie ma ich w pozostałych podanych zbiorach
a = {1, 2, 3, 4}
b = {2, 3, 4, 5, 6}
wynik = a.intersection(b)  
wynik3 = a.difference(b) 
wynik4 = b.difference(a)
print(wynik) # {2, 3, 4}
print(wynik3) #{1}
print(wynik4) #{5, 6}

```

---

### Metody dla słowników (`dict`)

Słownik (`dict`) to mutowalna kolekcja par `klucz: wartość`, gdzie klucze muszą być unikalne i niezmienne (haszowalne, np. `str`, `int`, `tuple`).

* `.get(key[, default])` — bezpieczne pobieranie wartości dla podanego klucza. Jeśli klucz nie istnieje, zwraca wartość domyślną (`None` lub podaną jako drugi argument) zamiast zgłaszać błąd `KeyError`.
* `.keys()` — zwraca dynamiczny widok wszystkich kluczy słownika (`dict_keys`).
* `.values()` — zwraca dynamiczny widok wszystkich wartości słownika (`dict_values`).
* `.items()` — zwraca dynamiczny widok wszystkich par `(klucz, wartość)` w postaci krotek (`dict_items`).
* `.update([other])` — aktualizuje słownik o pary klucz-wartość pochodzące z innego słownika lub sekwencji par.
* `.pop(key[, default])` — usuwa podany klucz i zwraca przypisaną mu wartość. Jeśli klucz nie istnieje i nie podano wartości domyślnej, rzuca wyjątek `KeyError`.
* `.popitem()` — usuwa i zwraca ostatnią dodaną parę `(klucz, wartość)` (zgodnie z porządkiem LIFO).
* `.setdefault(key[, default])` — jeśli klucz istnieje w słowniku, zwraca jego wartość; jeśli nie istnieje, wstawia klucz z wartością `default` i zwraca tę wartość.
* `.clear()` — usuwa wszystkie elementy ze słownika.
* `.copy()` — tworzy płytką kopię (shallow copy) słownika.
* `klucz in slownik` / `klucz not in slownik` — bardzo szybkie (średnio $O(1)$) sprawdzenie, czy klucz występuje w słowniku.

---

### .items() wyciąga ze słownika wszystkie pary klucz-wartość jednocześnie.

Metoda `.items()` pozwala na jednoczesny dostęp do klucza i powiązanej z nim wartości. Zwracany obiekt `dict_items` można bezpośrednio iterować w pętli `for` lub przekształcić w listę za pomocą `list()`, co umożliwia m.in. operacje wycinania (slicing) na parach:

```python
koszyk = {"jabłka": 5, "banany": 3, "pomarańcze": 2}
print(koszyk.items()) # dict_items([('jabłka', 5), ('banany', 3), ('pomarańcze', 2)])
print(list(koszyk.items())[1]) # Output: ('banany', 3)

slownik1 = {'imię': 'Jadwiga', 'wiek': 23, 'ulub_jedzenie': ['pizza', 'owoce', 'ryba']}
print(slownik1['imię'])             # 'Jadwiga'
print(slownik1['ulub_jedzenie'][1]) #'owoce'
print(list(slownik1.items())[1:2])  # [('wiek', 23)]
print(list(slownik1.items())[::2])  #[('imię', 'Jadwiga'), ('ulub_jedzenie', ['pizza', 'owoce', 'ryba'])]

# Iteracja po kluczach i wartościach jednocześnie (bardzo częste na maturze!):
for owoc, ilosc in koszyk.items():
    print(f"Produkt: {owoc}, Ilość: {ilosc}")
```

---

### Przykłady kodu i operacji na Słownik

#### 1. Bezpieczny dostęp i metoda `.get()`

W standardowym dostępie indeksowym `slownik[klucz]`, odwołanie się do nieistniejącego klucza kończy się błędem `KeyError` i przerwaniem działania programu. Metoda `.get()` pozwala tego bezpiecznie uniknąć.

```python
student = {"imie": "Marek", "kierunek": "Informatyka", "rok": 2}

# Zwykły dostęp indeksowy [klucz]:
print(student["imie"])              # 'Marek'
# print(student["stypendium"])      # BŁĄD! KeyError: 'stypendium'

# Bezpieczne pobieranie za pomocą .get() — brak klucza zwraca None:
print(student.get("stypendium"))    # None

# Bezpieczne pobieranie z podaniem własnej wartości domyślnej:
print(student.get("stypendium", 0.0))       # 0.0
print(student.get("rok", 1))                # 2 (klucz istnieje, zwraca wartość z bazy)

# Zastosowanie maturalne: Zliczanie częstości występowania elementów
tekst = "matura informatyka python matura informatyka informatyka"
licznik = {}

for slowo in tekst.split():
    # Jeśli słowa nie ma w słowniku, get zwraca 0, dodajemy 1 i zapisujemy:
    licznik[slowo] = licznik.get(slowo, 0) + 1

print(licznik)
# Output: {'matura': 2, 'informatyka': 3, 'python': 1}
```

#### 2. Metody `.keys()`, `.values()` oraz operacje agregujące

```python
ceny = {"chleb": 4.50, "mleko": 3.20, "masło": 7.80, "ser": 9.00}

# Pobieranie samych kluczy oraz samych wartości:
print(list(ceny.keys()))    # ['chleb', 'mleko', 'masło', 'ser']
print(list(ceny.values()))  # [4.5, 3.2, 7.8, 9.0]

# Operacje matematyczne na wartościach:
laczny_koszt = sum(ceny.values())
print(f"Łączny koszt: {laczny_koszt:.2f} zł")  # 24.50 zł

# Wyszukiwanie klucza o największej wartości:
najdrozszy = max(ceny, key=ceny.get)
print(f"Najdroższy produkt: {najdrozszy} ({ceny[najdrozszy]} zł)")  # ser (9.0 zł)
```

#### 3. Dodawanie, modyfikacja i metoda `.update()`

```python
konfiguracja = {"motyw": "ciemny", "jezyk": "pl", "autozapis": True}

# Dodanie nowego klucza lub modyfikacja istniejącego:
konfiguracja["rozmiar_czcionki"] = 14
konfiguracja["motyw"] = "jasny"

# .update() — łączenie słowników lub masowa aktualizacja:
nowe_opcje = {"rozdzielczosc": "1920x1080", "autozapis": False, "jezyk": "en"}
konfiguracja.update(nowe_opcje)
print(konfiguracja)
# {'motyw': 'jasny', 'jezyk': 'en', 'autozapis': False, 'rozmiar_czcionki': 14, 'rozdzielczosc': '1920x1080'}
```

#### 4. Usuwanie elementów: `.pop()`, `.popitem()`, `del` i `.clear()`

```python
dane = {"id": 101, "login": "admin", "token": "xyz123", "aktywny": True}

# .pop(klucz) — usuwa klucz i zwraca powiązaną wartość:
token = dane.pop("token")
print(token)        # 'xyz123'

# .pop(klucz, default) — bezpieczne usunięcie (zwraca default zamiast KeyError):
rola = dane.pop("rola", "brak_roli")
print(rola)         # 'brak_roli'

# .popitem() — usuwa i zwraca ostatnią dodaną parę (klucz, wartość):
ostatni = dane.popitem()
print(ostatni)      # ('aktywny', True)

# Instrukcja del:
del dane["id"]

# .clear() — czyści słownik do stanu pustego:
dane.clear()
print(dane)         # {}
```

#### 5. Metoda `.setdefault()` oraz sprawdzanie `in` / `not in`

```python
# setdefault: pobiera wartość; jeśli klucza nie ma, tworzy go z wartością domyślną
grupy = {}
grupy.setdefault("owoce", []).append("jabłko")
grupy.setdefault("owoce", []).append("gruszka")
grupy.setdefault("warzywa", []).append("marchewka")
print(grupy)
# {'owoce': ['jabłko', 'gruszka'], 'warzywa': ['marchewka']}

# Sprawdzanie obecności klucza w słowniku:
if "owoce" in grupy:
    print("Mamy zarejestrowaną kategorię owoce!")

if "nabial" not in grupy:
    print("Brak kategorii nabiał.")
```

---

### ✏️ Samodzielne zadania: Metody obiektów
1. Mając zmienną `email = "  Jan.Kowalski@Domain.COM  "`: usuń spacje (`.strip()`), zamień na małe litery (`.lower()`) i sprawdź końcówkę (`.endswith(".com")`).
2. Mając dwa zbiory technologii: `osoba1 = {"Python", "SQL", "Git", "C++"}` oraz `osoba2 = {"Python", "Java", "Git", "Docker"}`: znajdź część wspólną (`intersection`) oraz różnicę (`difference`).
3. Mając słownik magazynu `magazyn = {"zeszyt": 15, "dlugopis": 30, "olowek": 10}`:
   - Pobierz liczbę artykułów `"gumka"` za pomocą metody `.get()`, podając wartość domyślną `0`.
   - Zaktualizuj słownik o dostawę `{"gumka": 20, "linijka": 5}` za pomocą metody `.update()`.
   - Oblicz łączną liczbę wszystkich artykułów w magazynie korzystając z metody `.values()` oraz funkcji `sum()`.

> 💡 **Więcej zadań praktycznych:** Zobacz osobny zestaw zadań treningowych (bez gotowych odpowiedzi) obejmujący m.in. grę Scrabble, problem plecakowy z wagami oraz operacje na zagnieżdżonych słownikach i zbiorach: [Zadania — Słowniki i Zbiory](Zadania_slowniki_i_zbiory.md).

---
## 1.7 Funkcja filtrowanie listy
`filter(fun, iter)`
Funkcja przyjmuje dwa parametry:
* `fun:` funkcja warunkowa (predykat), do której przekazywany jest po kolei każdy element kolekcji. Zwraca ona `True`, jeśli dany element spełnia określony warunek, w przeciwnym razie zwraca False.
* `iter:` filtrowana kolekcja (obiekt iterowalny, np. lista, krotka).

W wyniku funkcja zwraca przefiltrowane elementy (tylko te, dla których funkcja fun zwróciła wartość `True`).

```python
numbers = [-5, -4, -3 ,-2, -1, 0, 1, 2, 3, 4, 5]
result = filter(lambda x: x > - 1, numbers)
for x in result: print(x, end=" ")  # 0 1 2 3 4 5
```
---
### ✏️ Samodzielne zadania: filtrowanie listy
Dana jest lista liczb całkowitych `liczby = [1, 2, 3, 4, 5, 6]`
Napisz program, który wybierze z podanej listy liczby wyłącznie liczby parzyste i wyświetli je na ekranie.
Oczekiwany wynik:
`[2, 4, 6]`

---
## 1.8 Argumenty pozycyjne i nazwane (keyword) w obiektach wywoływalnych

Funkcję/metodę można wywołać na wiele różnych sposobów:

* `func()`: Wywołaj `func` bez argumentów
* `func(arg)`: Wywołaj `func` z jednym argumentem pozycyjnym
* `func(arg1, arg2)`: Wywołaj `func` z dwoma argumentami pozycyjnymi
* `func(arg1, arg2, ..., argn)`: Wywołaj `func` z wieloma argumentami pozycyjnymi
* `func(nazwa_arg=wartosc)`: Wywołaj `func` z jednym argumentem nazwanym
* `func(nazwa_arg1=wartosc1, nazwa_arg2=wartosc2)`: Wywołaj `func` z dwoma argumentami nazwanymi
* `func(nazwa_arg1=wartosc1, nazwa_arg2=wartosc2, ..., nazwa_argn=wartosc_n)`: Wywołaj `func` z wieloma argumentami nazwanymi
* `func(arg1, arg2, nazwa_arg1=wartosc1, nazwa_arg2=wartosc2)`: Wywołaj `func` z argumentami pozycyjnymi i nazwanymi
* `obiekt.metoda()`: To samo co dla `func`.. i każdego innego przykładu `func`

> [!IMPORTANT]
> **Zasady przekazywania argumentów:**
> 1. Używając **argumentów pozycyjnych**, musisz je podać w kolejności, w jakiej funkcja je zdefiniowała (w sygnaturze funkcji).
> 2. Używając **argumentów nazwanych**, możesz podać argumenty, które chcesz, w dowolnej kolejności, o ile określisz nazwę każdego argumentu.
> 3. Używając **argumentów pozycyjnych i nazwanych**, argumenty pozycyjne muszą być pierwsze.

### Przykłady kodu

```python
# Zdefiniuj funkcję, która przyjmuje 3 argumenty
def wypisz_argumenty(arg1, arg2, arg3='wartość_domyślna'):
    print('arg1 to:', arg1)
    print('arg2 to:', arg2)
    print('arg3 to:', arg3)

# Wywołanie z argumentami pozycyjnymi
print('Wywołanie z argumentami pozycyjnymi:')
wypisz_argumenty('a', 'b', 'c')

# Wywołanie z argumentami nazwanymi (kolejność nie ma znaczenia)
print('\nWywołanie z argumentami nazwanymi:')
wypisz_argumenty(arg3='C', arg1='A', arg2='B')

# Wywołanie z argumentami pozycyjnymi i nazwanymi
print('\nWywołanie z mieszanymi argumentami:')
wypisz_argumenty('pierwszy', arg3='trzeci', arg2='drugi')

# Wywołanie używające wartości domyślnej dla arg3
print('\nWywołanie używające wartości domyślnej:')
wypisz_argumenty('jabłko', 'banan')

# To spowoduje błąd: argument pozycyjny po argumencie nazwanym
# wypisz_argumenty(arg1='x', 'y', 'z')
```

**Wynik działania programu (Output):**
```text
Wywołanie z argumentami pozycyjnymi:
arg1 to: a
arg2 to: b
arg3 to: c

Wywołanie z argumentami nazwanymi:
arg1 to: A
arg2 to: B
arg3 to: C

Wywołanie z mieszanymi argumentami:
arg1 to: pierwszy
arg2 to: drugi
arg3 to: trzeci

Wywołanie używające wartości domyślnej:
arg1 to: jabłko
arg2 to: banan
arg3 to: wartość_domyślna
```

---

### ✏️ Samodzielne zadania: Argumenty w funkcjach
1. Napisz funkcję `oblicz_cene_brutto(cena_netto, vat=0.23)`, która zwraca wartość brutto. Wywołaj ją z domyślnym VAT oraz ze stawką 8% (`vat=0.08`).
2. Przetestuj wywołanie z błędną kolejnością argumentów nazwanych i pozycyjnych (np. `func(arg2='B', 'A')`) i zaobserwuj błąd interpretera.

---

## 1.9 Formatowanie łańcuchów i używanie placeholderów

W Pythonie istnieje kilka sposobów formatowania łańcuchów znaków i wstawiania do nich wartości (placeholderów): od starszego operatora `%`, przez metodę `.format()`, aż po nowoczesne **f-stringi** (Python 3.6+).

```python
# "Stary" styl używający operatora %
imie = 'Tomek'
wiek = 30
print('Witaj, %s. Masz %d lat.' % (imie, wiek))

# "Nowy" styl używający metody .format()
print('Witaj, {}. Masz {} lat.'.format(imie, wiek))

# Metoda .format() z indeksami pozycyjnymi
print('Witaj, {1}. Masz {0} lat. Tak, {1}!'.format(wiek, imie))

# Metoda .format() z nazwami
print('Witaj, {n}. Masz {a} lat.'.format(n=imie, a=wiek))

# "Najnowszy" styl: f-stringi (Python 3.6+)
print(f'Witaj, {imie}. Masz {wiek} lat.')

# f-stringi mogą zawierać wyrażenia
print(f'Za 5 lat {imie} będzie mieć {wiek + 5} lat.')
print(f'Twoje imię wielkimi literami to {imie.upper()}.')
```

**Wynik działania programu (Output):**
```text
Witaj, Tomek. Masz 30 lat.
Witaj, Tomek. Masz 30 lat.
Witaj, Tomek. Masz 30 lat. Tak, Tomek!
Witaj, Tomek. Masz 30 lat.
Witaj, Tomek. Masz 30 lat.
Za 5 lat Tomek będzie mieć 35 lat.
Twoje imię wielkimi literami to TOMEK.
```

---

### ✏️ Samodzielne zadania: Formatowanie stringów
1. Utwórz zmienne `towar = "Kawa"`, `cena = 24.99`, `sztuki = 3`. Używając f-stringa, wygeneruj tekst podsumowania koszyka.
2. Wyświetl liczbę `pi = 3.14159265` z dokładnością do 2 miejsc po przecinku (`{pi:.2f}`).

---

## 1.10 Algorytmy NWD i NWW (Algorytm Euklidesa)

W zadaniach maturalnych bardzo często pojawiają się pojęcia **NWD** oraz **NWW**:

* **NWD (Największy Wspólny Dzielnik)**, ang. *GCD (Greatest Common Divisor)* — największa liczba naturalna, która dzieli bez reszty obie podane liczby $a$ i $b$. Najszybszym sposobem jego wyznaczania jest **algorytm Euklidesa** (z użyciem reszty z dzielenia `%`).
* **NWW (Najmniejsza Wspólna Wielokrotność)**, ang. *LCM (Least Common Multiple)* — najmniejsza dodatnia liczba naturalna, która jest podzielna zarówno przez $a$, jak i przez $b$. Oblicza się ją ze wzoru wykorzystującego NWD:

$$\text{NWW}(a, b) = \frac{|a \cdot b|}{\text{NWD}(a, b)}$$

### Implementacja w Pythonie

```python
# NWD (Największy Wspólny Dzielnik) — Algorytm Euklidesa
def gcd(a, b):
    while b:
        a, b = b, a % b
    return a


# NWW (Najmniejsza Wspólna Wielokrotność)
def lcm(a, b):
    if a == 0 or b == 0:
        return 0
    return abs(a * b) // gcd(a, b)
```

### Przykłady użycia

```python
# 1. Wywołanie własnych funkcji gcd() i lcm():
print("NWD(24, 36) =", gcd(24, 36))   # Output: 12
print("NWW(24, 36) =", lcm(24, 36))   # Output: 72

print("NWD(17, 13) =", gcd(17, 13))   # Output: 1 (liczby względnie pierwsze)
print("NWW(17, 13) =", lcm(17, 13))   # Output: 221

# 2. Praktyczne zastosowanie: skracanie ułamka zwykłego (np. 48/64)
licznik = 48
mianownik = 64
dzielnik = gcd(licznik, mianownik)
print(f"Ułamek {licznik}/{mianownik} po skróceniu to: {licznik // dzielnik}/{mianownik // dzielnik}")
# Output: Ułamek 48/64 po skróceniu to: 3/4

# 3. Gotowe funkcje z modułu standardowego math (Python 3.9+):
import math
print(math.gcd(24, 36))  # 12
print(math.lcm(24, 36))  # 72
```

---

### ✏️ Samodzielne zadania: NWD i NWW
1. Napisz funkcję `czy_wzglednie_pierwsze(a, b)`, która zwraca `True`, jeśli dwie liczby są względnie pierwsze (czyli ich $\text{NWD}(a, b) = 1$), oraz `False` w przeciwnym wypadku.
2. Oblicz NWD oraz NWW dla trzech liczb: `a = 12`, `b = 18`, `c = 30` (wskazówka: $\text{NWD}(a, b, c) = \text{NWD}(\text{NWD}(a, b), c)$).

---

## 1.11 Instrukcje warunkowe (`if`, `elif`, `else`)

### Instrukcje `if` i pętle `while` w Pythonie — wprowadzenie

Wyrażenia warunkowe mogą być używane z tymi dwiema instrukcjami:

* **Instrukcja `if`** pozwala przetestować warunek i wykonać pewne działania, jeśli warunek jest prawdziwy (`True`). Możesz również dodać klauzule `elif` i/lub `else` do instrukcji `if`, aby podjąć alternatywne działania, jeśli warunek jest fałszywy (`False`).
* **Pętla `while`** będzie się wykonywać dopóki jej wyrażenie warunkowe nie będzie fałszywe (`False`).

> [!WARNING]
> **Uwaga:** Możliwe jest „zapętlenie w nieskończoność” podczas używania pętli `while` z wyrażeniem warunkowym, które nigdy nie staje się fałszywe.

> [!NOTE]
> **Uwaga:** Ponieważ pętla `for` iteruje po kontenerze elementów, dopóki nie ma ich więcej, nie ma potrzeby określania warunku „zatrzymaj pętlę”.

---

### Konstrukcja warunkowa `if`

Konstrukcje warunkowe używają wyrażeń logicznych i kierują wykonaniem programu po jednej z określonych ścieżek w zależności od wartości wyrażenia warunkowego (`True` lub `False`). Jedną z takich konstrukcji jest instrukcja **`if`**.

Jej formalna definicja wygląda następująco:

```python
if wyrazenie_logiczne:
    instrukcje
[elif wyrazenie_logiczne:
    instrukcje]
[else:
    instrukcje]
```

W najprostszej postaci po słowie kluczowym `if` występuje wyrażenie logiczne. Jeśli to wyrażenie logiczne zwraca `True`, wykonywany jest następujący po nim blok instrukcji. Każda z tych instrukcji musi zaczynać się z **wcięciem** (rekomendowane są **4 spacje**). Po wyrażeniu logicznym stawia się dwukropek (`:`):

```python
language = "english"
if language == "english":
    print("Hello")
print("End")
```

Ponieważ w tym przypadku wartość zmiennej `language` jest równa `"english"`, wykonany zostanie blok `if`, który zawiera tylko jedną instrukcję — `print("Hello")`. W rezultacie konsola wyświetli następujące linie:

```text
Hello
End
```

Zwróć uwagę na ostatnią linijkę kodu w programie: `print("End")`. Nie posiada ona wcięcia, dlatego nie należy do bloku `if` i zostanie wykonana w każdym przypadku, nawet jeśli wyrażenie w instrukcji `if` zwróci `False`.

Gdybyśmy jednak dodali wcięcie do ostatniej linii, również należałaby ona do konstrukcji `if`:

```python
language = "english"
if language == "english":
    print("Hello")
    print("End")
```

---

### Blok `else`

Czasami pojawia się potrzeba zdefiniowania alternatywnego rozwiązania na wypadek, gdyby wyrażenie w `if` zwróciło `False`. W tym celu możemy dodać blok **`else`**:

```python
language = "polish"
if language == "english":
    print("Hello")
else:
    print("Cześć")
print("End")
```

Jeśli wyrażenie `language == "english"` zwraca `True`, wykonywany jest blok `if`, w przeciwnym razie wykonywany jest blok `else`. Ponieważ w powyższym przykładzie warunek `language == "english"` zwraca `False`, wykonane zostaną instrukcje z bloku `else`.

Instrukcje bloku `else` również muszą posiadać wcięcia na początku wiersza:

```python
language = "polish"
if language == "english":
    print("Hello")
    print("World")
else:
    print("Cześć")
    print("Świecie")
```

---

### Konstrukcja `elif`

Jeżeli w programie należy sprawdzić kilka warunków, możemy dodać dodatkowe bloki **`elif`** (skrót od *else if*), po których następuje warunek logiczny, a po nim blok instrukcji z wcięciami:

```python
language = "german"
if language == "english":
    print("Hello")
    print("World")
elif language == "german":
    print("Hallo")
    print("Welt")
else:
    print("Cześć")
    print("Świecie")
```

Na początku Python sprawdza warunek `if`. Jeśli jest on równy `False`, program przechodzi do sprawdzenia warunku w `elif`. Jeśli ten warunek również zwróci `False`, wykonywany jest blok `else`. W razie potrzeby można zdefiniować wiele bloków `elif` dla różnych warunków:

```python
language = "german"
if language == "english":
    print("Hello")
elif language == "german":
    print("Hallo")
elif language == "french":
    print("Salut")
else:
    print("Cześć")
```

---

### Zagnieżdżone konstrukcje `if`

Konstrukcja `if` może z kolei sama zawierać wewnątrz siebie zagnieżdżone instrukcje `if`:

```python
language = "english"
daytime = "morning"
if language == "english":
    print("English")
    if daytime == "morning":
        print("Good morning")
    else:
        print("Good evening")
```

Tutaj wewnątrz głównego bloku `if` znajduje się wewnętrzna konstrukcja `if / else`. Jeśli wartość zmiennej `language` jest równa `"english"`, wówczas wewnętrzna konstrukcja sprawdza dodatkowo, czy zmienna `daytime` jest równa `"morning"`. Warto pamiętać, że zagnieżdżone instrukcje również muszą zaczynać się z odpowiednimi, głębszymi wcięciami (np. 8 spacji).

Można też umieścić zagnieżdżone konstrukcje `if` w blokach `elif` oraz `else`:

```python
language = "english"
daytime = "morning"
if language == "english":
    if daytime == "morning":
        print("Good morning")
    else:
        print("Good evening")
else:
    if daytime == "morning":
        print("Dzień dobry")
    else:
        print("Dobry wieczór")
```

---

### ✏️ Samodzielne zadania: Instrukcje warunkowe `if` (z wykorzystaniem list, słowników, zbiorów i metod)

1. **System kwalifikacji maturalnej (słowniki, listy, zbiory, metody stringów i `if/elif/else`):**
   Dany jest słownik opisujący ucznia:
   ```python
   uczen = {
       "imie_nazwisko": "  tomek kowalski  ",
       "punkty_probne": [78, 85, 92],
       "przedmioty_dodatkowe": {"fizyka", "matematyka"},
       "olimpiada": False
   }
   ```
   Napisz program, który:
   - Oczyści pole `"imie_nazwisko"` z białych znaków na końcach (`.strip()`), rozdzieli je na listę słów (`.split()`), zamieni pierwsze litery imienia i nazwiska na wielkie (`.capitalize()`) i połączy z powrotem spacją (`" ".join(...)`).
   - Obliczy średni wynik z listy `"punkty_probne"` za pomocą funkcji wbudowanych `sum()` i `len()`, a następnie zapisze go w słowniku pod nowym kluczem `"srednia"`.
   - Za pomocą instrukcji `if / elif / else` oraz bezpiecznego odczytu `.get("olimpiada", False)` przypisze ocenę końcową pod kluczem `"ocena_opisowa"`:
     - Jeśli uczeń jest laureatem olimpiady (`True`): ustaw `"Celujący — zwolniony z egzaminu (100%)"` i dodaj `100` na koniec listy `"punkty_probne"` (`.append(100)`).
     - W przeciwnym razie sprawdź wyliczoną średnią:
       - `90–100`: `"Bardzo dobry (5)"` — wewnątrz tego bloku dodaj **zagnieżdżony `if`**, który sprawdzi, czy `"informatyka"` **nie znajduje się** (`not in`) w zbiorze `"przedmioty_dodatkowe"`; jeśli jej nie ma, wypisz komunikat zachęcający do jej wyboru.
       - `75–89.99`: `"Dobry (4)"`
       - `50–74.99`: `"Dostateczny (3)"`
       - poniżej `50`: `"Niedostateczny (2)"`
   - Na koniec wyświetli podsumowanie za pomocą **f-stringa** z zaokrągleniem średniej do 2 miejsc po przecinku (`{uczen['srednia']:.2f}`).

2. **Weryfikacja koszyka zakupowego i rabatów (słowniki, listy i warunki złożone):**
   Masz słownik cen produktów `cennik = {"laptop": 3500.0, "myszka": 120.0, "klawiatura": 250.0, "monitor": 1100.0}`, listę zakupów klienta `koszyk = ["laptop", "myszka", "podkladka"]` oraz kod rabatowy `kod = "  PROMO20  "`.
   Napisz program, który:
   - Sprawdzi instrukcją `if`, czy ostatni element koszyka (`koszyk[-1]`) znajduje się w słowniku `cennik`. Jeśli go nie ma (`not in`), usunie go z listy `koszyk` metodą `.pop()`, a do `cennik` doda ten produkt z ceną domyślną `45.0` za pomocą `.setdefault()`.
   - Obliczy sumę cen towarów pozostałych w liście `koszyk`.
   - Oczyści zmienną `kod` ze spacji i wielkości liter (`.strip().upper()`) i za pomocą `if / elif / else` obliczy kwotę po rabacie:
     - jeśli `kod == "PROMO20"` **oraz** suma przekracza `3000`, naliczy **20% rabatu**,
     - `elif` suma przekracza `2000`, naliczy **10% rabatu**,
     - `else` nie naliczy żadnego rabatu.
   - Wyświetli końcową kwotę do zapłaty za pomocą **f-stringa**.

---

## 1.12 Pętle w Pythonie (`while` oraz `for`)

Do powtarzania określonych działań w zależności od warunku w Pythonie stosuje się pętle. W języku Python istnieją dwa rodzaje pętli: **`while`** oraz **`for`**.

---

### 1. Pętla `while`

Formalna definicja pętli `while` składa się z warunku oraz bloku wykonywanych instrukcji:

```python
while wyrazenie_logiczne:
    instrukcje
```

Po słowie kluczowym `while` określa się wyrażenie warunkowe, a po tym wyrażeniu stawia się dwukropek (`:`). Następnie w kolejnych wierszach z wcięciami (4 spacje) umieszczany jest blok instrukcji pętli.

Dopóki wyrażenie warunkowe zwraca wartość `True` (prawda), wykonywane są wszystkie instrukcje bloku pętli `while`. Każde pojedyncze przejście przez ten blok nazywa się **iteracją**. Gdy tylko wyrażenie warunkowe zwróci `False` (fałsz), wykonywanie pętli zostaje przerwane.

Przykład pętli `while`:

```python
number = 1

while number < 5:
    print(f"number = {number}")
    number += 1
print("Praca programu została zakończona")
```

Pętla `while` będzie się wykonywać, dopóki zmienna `number` jest mniejsza niż `5`. W samym ciele pętli wartość zmiennej `number` jest wypisywana na ekran, a następnie zwiększana o `1`. Kiedy `number` osiągnie `5`, pętla zakończy pracę. Na końcu wykona się instrukcja `print("Praca programu została zakończona")` (ponieważ nie ma ona wcięcia, znajduje się poza pętlą):

```text
number = 1
number = 2
number = 3
number = 4
Praca programu została zakończona
```

---

### 2. Pętla `for`

Drugim typem pętli w Pythonie jest pętla **`for`**. Ta pętla przebiega po określonym zbiorze (kolekcji) elementów i wykonuje dla każdego z nich blok instrukcji.

Formalna definicja pętli `for`:

```python
for zmienna in kolekcja_elementow:
    instrukcje
```

Po słowie kluczowym `for` podaje się nazwę zmiennej, w której zapisywane będą kolejne elementy, następnie słowo kluczowe `in`, a po nim kolekcję elementów i dwukropek (`:`).

W trakcie pracy pętla pobiera po kolei każdy element z `kolekcja_elementow`, przypisuje go do zmiennej i wykonuje blok instrukcji z wcięciami. Pętla kończy działanie, gdy przejdzie przez wszystkie elementy kolekcji.

Jako kolekcję elementów można przekazać np. łańcuch znaków (`str`), który w istocie reprezentuje sekwencję pojedynczych znaków:

```python
message = "Hello"

for c in message:
    print(c)
```

W pętli zdefiniowano zmienną `c`, do której podczas każdej iteracji trafia kolejny znak napisu `message`. Efekt działania:

```text
H
e
l
l
o
```

#### Funkcja `range()` w pętli `for`
W połączeniu z pętlą `for` bardzo często stosuje się wbudowaną funkcję **`range()`**, która generuje sekwencję liczb:
* `range(stop)` — generuje liczby od `0` do `stop - 1`
* `range(start, stop)` — generuje liczby od `start` do `stop - 1`
* `range(start, stop, step)` — generuje liczby od `start` do `stop - 1` z krokiem `step`

```python
# Wypisanie liczb od 0 do 4:
for n in range(5):
    print(n, end=" ")       # 0 1 2 3 4
print()

# Wypisanie liczb od 4 do 9:
for n in range(4, 10):
    print(n, end=" ")       # 4 5 6 7 8 9
print()

# Wypisanie liczb parzystych od 0 do 8 (krok 2):
for n in range(0, 10, 2):
    print(n, end=" ")       # 0 2 4 6 8
print()
```

---

### 3. Blok `else` w pętlach

Dla pętli w Pythonie można również zdefiniować blok **`else`**. Instrukcje z bloku `else` wykonują się po zakończeniu pętli (gdy warunek w `while` stanie się fałszywy lub gdy w `for` skończą się elementy kolekcji):

```python
number = 1
while number < 5:
    print(f"number = {number}")
    number += 1
else:
    print(f"number = {number}. Praca pętli zakończona")
print("Praca programu zakończona")
```

To samo dotyczy pętli `for`:

```python
message = "Hello"
for c in message:
    print(c)
else:
    print(f"Ostatni symbol: {c}. Pętla zakończona;")
print("Praca programu zakończona")
```

Warto zauważyć, że blok `else` ma dostęp do zmiennych używanych w nagłówku pętli (np. zmiennej `c`), ale wykona się **tylko wtedy**, gdy pętla zakończyła się w sposób naturalny (nie została przerwana instrukcją `break`).

---

### 4. Zagnieżdżone pętle

Jedne pętle mogą zawierać wewnątrz siebie inne pętle. Rozważmy przykład wypisania tabliczki mnożenia za pomocą zagnieżdżonych pętli `while`:

```python
i = 1
j = 1
while i < 10:
    while j < 10:
        print(i * j, end="\t")
        j += 1
    print("\n")
    j = 1
    i += 1
```

Wewnętrzna pętla `while j < 10` wykonuje 9 iteracji dla każdej jednej iteracji pętli zewnętrznej `while i < 10`. Po zakończeniu pętli wewnętrznej zmienna `j` jest resetowana z powrotem do `1`, zmienna `i` zwiększa się o `1` i proces powtarza się aż `i` osiągnie `10`.

Podobnie można definiować zagnieżdżone pętle `for`:

```python
for c1 in "ab":
    for c2 in "ba":
        print(f"{c1}{c2}")
```
**Wynik:**
```text
ab
aa
bb
ba
```

---

### 5. Wyjście z pętli: `break` i `continue`

Do zarządzania przebiegiem pętli służą specjalne instrukcje **`break`** oraz **`continue`**:

* **`break`** — dokonuje natychmiastowego wyjścia z pętli (przerywa całe dalsze wykonywanie pętli).
* **`continue`** — wykonuje przejście do następnej iteracji pętli (pomija pozostałe instrukcje wyłącznie w bieżącym kroku).

#### Przykład użycia `break`:
```python
number = 0
while number < 5:
    number += 1
    if number == 3:    # jeśli number jest równe 3, wychodzimy z pętli
        break
    print(f"number = {number}")
```
Gdy wartość zmiennej `number` stanie się równa `3`, wykona się instrukcja `break` i pętla zostanie natychmiast zakończona:
```text
number = 1
number = 2
```

#### Przykład użycia `continue`:
```python
number = 0
while number < 5:
    number += 1
    if number == 3:    # jeśli number == 3, przechodzimy do nowej iteracji pętli
        continue
    print(f"number = {number}")
```
W tej sytuacji, gdy wartość zmiennej `number` wyniesie `3`, po wykonaniu `continue` kolejne instrukcje (czyli `print`) nie zostaną wywołane dla tej iteracji, a program przejdzie od razu do następnego kroku pętli:
```text
number = 1
number = 2
number = 4
number = 5
```

---

### ✏️ Samodzielne zadania: Pętle `while` i `for`
1. Napisz pętlę `while`, która oblicza sumę cyfr podanej liczby naturalnej `n = 5482` (wykorzystaj operatory `% 10` oraz `// 10`).
2. Używając pętli `for`, funkcji `range()` oraz instrukcji `continue`, wypisz wszystkie liczby z przedziału od `1` do `20`, które **nie są podzielne przez 3**.

> 💡 **Więcej zadań praktycznych z pętli:** Zobacz osobny zestaw 15 zadań treningowych (obejmujący m.in. przetwarzanie list, ciąg Fibonacciego, zadanie „Zepsuta klawiatura”, liczby niepotęgowe oraz liczby pierwsze): [Zadania — Pętla for i while](Zadania_petla_for.md).

---

# 2. Praktyka — Zadania programistyczne

Ten rozdział zawiera **10 zadań praktycznych** w języku polskim.

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
## Zadanie 11: Generator opisów w menu kawiarni
### Opis
Wyobraź sobie, że piszesz program przygotowujący skrócone opisy pozycji do cyfrowego menu kawiarni. Każdy napój opisany jest zestawem składników i cech w postaci listy tagów.

### Dane wejściowe:
Utwórz trzy oddzielne listy zawierające po 4 tagi tekstowe dla trzech różnych napojów (np. kawa1, kawa2, kawa3):
Pierwszy napój: 'espresso', 'mocna', 'arabska', 'goraca'
Drugi napój: 'cappuccino', 'mleko-owsiane', 'pianka', 'cynamon'
Trzeci napój: 'matcha', 'zielona', 'na-zimno', 'lod'

Połącz elementy każdej z list w pojedynczy ciąg znaków (napis) za pomocą metody .join(), używając separatora " - " (spacja, myślnik, spacja).

Zapisz otrzymane trzy połączone napisy do nowej, wspólnej listy (np. karty_menu).
### Dane wyjściowe
Wyświetl na ekranie końcową listę za pomocą funkcji print()
['espresso - mocna - arabska - goraca', 'cappuccino - mleko-owsiane - pianka - cynamon', 'matcha - zielona - na-zimno - lod']

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
3. **Operacje na słowniku:**
   ```python
   magazyn = {"zeszyt": 15, "dlugopis": 30, "olowek": 10}
   gumka_sztuk = magazyn.get("gumka", 0) # 0
   magazyn.update({"gumka": 20, "linijka": 5})
   suma_przedmiotow = sum(magazyn.values()) # 80
   ```

### Zadania 1.7: Filtrowanie listy
1. **Wybór liczb parzystych za pomocą `filter()`:**
   ```python
   liczby = [1, 2, 3, 4, 5, 6]
   parzyste = list(filter(lambda x: x % 2 == 0, liczby))
   print(parzyste)  # [2, 4, 6]
   ```

### Zadania 1.8: Argumenty w funkcjach
1. **Kalkulator ceny brutto:**
   ```python
   def oblicz_cene_brutto(cena_netto, vat=0.23):
       return cena_netto * (1 + vat)

   print(oblicz_cene_brutto(100))                      # 123.0 (pozycyjnie)
   print(oblicz_cene_brutto(cena_netto=100, vat=0.08)) # 108.0 (nazwane)
   ```

### Zadania 1.9: Formatowanie stringów
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

### Zadania 1.10: Algorytmy NWD i NWW
1. **Sprawdzanie liczb względnie pierwszych:**
   ```python
   def gcd(a, b):
       while b:
           a, b = b, a % b
       return a

   def czy_wzglednie_pierwsze(a, b):
       return gcd(a, b) == 1

   print(czy_wzglednie_pierwsze(14, 25))  # True (NWD = 1)
   print(czy_wzglednie_pierwsze(14, 21))  # False (NWD = 7)
   ```
2. **NWD i NWW dla trzech liczb (`12, 18, 30`):**
   ```python
   def lcm(a, b):
       if a == 0 or b == 0:
           return 0
       return abs(a * b) // gcd(a, b)

   a, b, c = 12, 18, 30
   nwd_3 = gcd(gcd(a, b), c)   # 6
   nww_3 = lcm(lcm(a, b), c)   # 180
   print(f"NWD = {nwd_3}, NWW = {nww_3}")
   ```

### Zadania 1.11: Instrukcje warunkowe `if` (ze słownikami, listami i zbiorami)
1. **System kwalifikacji maturalnej:**
   ```python
   uczen = {
       "imie_nazwisko": "  tomek kowalski  ",
       "punkty_probne": [78, 85, 92],
       "przedmioty_dodatkowe": {"fizyka", "matematyka"},
       "olimpiada": False
   }

   # 1. Czyszczenie i formatowanie imienia oraz nazwiska
   czesci = uczen["imie_nazwisko"].strip().split()
   uczen["imie_nazwisko"] = " ".join([czesci[0].capitalize(), czesci[1].capitalize()])

   # 2. Obliczanie średniej punktów
   uczen["srednia"] = sum(uczen["punkty_probne"]) / len(uczen["punkty_probne"])

   # 3. Instrukcje warunkowe if / elif / else
   if uczen.get("olimpiada", False):
       uczen["ocena_opisowa"] = "Celujący — zwolniony z egzaminu (100%)"
       uczen["punkty_probne"].append(100)
   elif uczen["srednia"] >= 90:
       uczen["ocena_opisowa"] = "Bardzo dobry (5)"
       if "informatyka" not in uczen["przedmioty_dodatkowe"]:
           print("Wskazówka: Warto rozważyć informatykę jako przedmiot dodatkowy!")
   elif uczen["srednia"] >= 75:
       uczen["ocena_opisowa"] = "Dobry (4)"
   elif uczen["srednia"] >= 50:
       uczen["ocena_opisowa"] = "Dostateczny (3)"
   else:
       uczen["ocena_opisowa"] = "Niedostateczny (2)"

   # 4. Wyświetlenie sformatowanego podsumowania
   print(f"Uczeń: {uczen['imie_nazwisko']} | Średnia: {uczen['srednia']:.2f}% | Ocena: {uczen['ocena_opisowa']}")
   # Output: Uczeń: Tomek Kowalski | Średnia: 85.00% | Ocena: Dobry (4)
   ```
2. **Weryfikacja koszyka zakupowego i rabatów:**
   ```python
   cennik = {"laptop": 3500.0, "myszka": 120.0, "klawiatura": 250.0, "monitor": 1100.0}
   koszyk = ["laptop", "myszka", "podkladka"]
   kod = "  PROMO20  "

   if koszyk[-1] not in cennik:
       brakujacy = koszyk.pop()
       cennik.setdefault(brakujacy, 45.0)

   suma = cennik[koszyk[0]] + cennik[koszyk[1]]
   kod_clean = kod.strip().upper()

   if kod_clean == "PROMO20" and suma > 3000:
       do_zaplaty = suma * 0.80
   elif suma > 2000:
       do_zaplaty = suma * 0.90
   else:
       do_zaplaty = suma

   print(f"Suma przed rabatem: {suma:.2f} zł | Do zapłaty: {do_zaplaty:.2f} zł")
   # Output: Suma przed rabatem: 3620.00 zł | Do zapłaty: 2896.00 zł
   ```

### Zadania 1.12: Pętle `while` i `for`
1. **Suma cyfr liczby naturalnej (`while`):**
   ```python
   n = 5482
   suma_cyfr = 0
   while n > 0:
       suma_cyfr += n % 10
       n //= 10
   print(f"Suma cyfr: {suma_cyfr}")  # 19
   ```
2. **Liczby niepodzielne przez 3 (`for` + `continue`):**
   ```python
   for i in range(1, 21):
       if i % 3 == 0:
           continue
       print(i, end=" ")
   # Output: 1 2 4 5 7 8 10 11 13 14 16 17 19 20
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
