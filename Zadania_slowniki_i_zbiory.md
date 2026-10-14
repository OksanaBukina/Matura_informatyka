# 📚 Zadania: Słowniki i Zbiory w języku Python

Zbiór zadań praktycznych ze struktur danych `dict` (słowniki) oraz `set` (zbiory), przygotowany do samodzielnego rozwiązywania. Zadania nie zawierają gotowych rozwiązań (kodów odpowiedzi) — Twoim celem jest samodzielna implementacja programów realizujących poniższe wytyczne.

---

## 📋 Spis zadań
- [Zadanie 1: Wycena słów w grze Scrabble (Игра Скрабл)](#zadanie-1-wycena-słów-w-grze-scrabble)
- [Zadanie 2: Problem plecakowy — Wybór ekwipunku (Задача о рюкзаке)](#zadanie-2-problem-plecakowy--wybór-ekwipunku)
- [Zadanie 3: Lista słowników — Programiści i języki (Список словарей — Программисты)](#zadanie-3-lista-słowników--programiści-i-języki)
- [Zadanie 4: Zbiory — Różnica dwóch list (Множества — Разность списков)](#zadanie-4-zbiory--różnica-dwóch-list)
- [Zadanie 5: Zbiory — Studenci i pracownicy (Множества — Студенты и сотрудники)](#zadanie-5-zbiory--studenci-i-pracownicy)

---

## Zadanie 1: Wycena słów w grze Scrabble

### Opis problemu
W grze planszowej Scrabble każda litera ma przypisaną określoną wartość punktową.

**Tabela punktacji dla liter alfabetu angielskiego:**
* **1 punkt:** `A`, `E`, `I`, `O`, `U`, `L`, `N`, `S`, `T`, `R`
* **2 punkty:** `D`, `G`
* **3 punkty:** `B`, `C`, `M`, `P`
* **4 punkty:** `F`, `H`, `V`, `W`, `Y`
* **5 punktów:** `K`
* **8 punktów:** `J`, `X`
* **10 punktów:** `Q`, `Z`

**Tabela punktacji dla liter alfabetu rosyjskiego:**
* **1 punkt:** `А`, `В`, `Е`, `И`, `Н`, `О`, `Р`, `С`, `Т`
* **2 punkty:** `Д`, `К`, `Л`, `М`, `П`, `У`
* **3 punkty:** `Б`, `Г`, `Ё`, `Ь`, `Я`
* **4 punkty:** `Й`, `Ы`
* **5 punktów:** `Ж`, `З`, `Х`, `Ц`, `Ч`
* **8 punktów:** `Ш`, `Э`, `Ю`
* **10 punktów:** `Ф`, `Щ`, `Ъ`

### Polecenie
Napisz program, który oblicza łączną wartość punktową podanego przez użytkownika słowa.

**Wymagania:**
1. Na wejściu program przyjmuje jedno słowo (złożone z liter angielskich lub rosyjskich).
2. Wielkość liter nie ma wpływu na punktację (zarówno małe, jak i wielkie litery są punktowane tak samo).
3. Do przechowywania punktacji liter wykorzystaj słownik (`dict`).
4. Użyj bezpiecznych metod dostępu, np. `.get()`.

### Przykłady testowe
* **Przykład 1:**
  * **Wejście:** `ноутбук`
  * **Wyjście:** `12`
  *(Wyjaśnienie: н(1) + о(1) + у(2) + т(1) + б(3) + у(2) + к(2) = 12)*
* **Przykład 2:**
  * **Wejście:** `Python`
  * **Wyjście:** `14`
  *(Wyjaśnienie: P(3) + y(4) + t(1) + h(4) + o(1) + n(1) = 14)*

---

## Zadanie 2: Problem plecakowy — Wybór ekwipunku

### Opis problemu
Turysta wyrusza na wyprawę. Może unieść w plecaku maksymalnie $N$ kg ekwipunku. Rzeczy, które zaplanował zabrać, jest jednak znacznie więcej niż dopuszczalna ładowność plecaka. Należy określić, które przedmioty zmieszczą się do plecaka, wybierając je algorytmem zachłannym: **od najcięższych do najlżejszych**.

### Katalog przedmiotów (dane słownikowe)
Waga przedmiotów podana jest w **gramach**:
```python
things = {
    'зажигалка': 20, 
    'компас': 100, 
    'фрукты': 500, 
    'рубашка': 300, 
    'термос': 1000, 
    'аптечка': 200, 
    'куртка': 600, 
    'бинокль': 400, 
    'удочка': 1200, 
    'салфетки': 40, 
    'бутерброды': 820, 
    'палатка': 5500, 
    'спальный мешок': 2250, 
    'жвачка': 10
}
```

### Polecenie
1. Wczytaj od użytkownika liczbę $N$ (maksymalny udźwig plecaka w kilogramach; $1 \text{ kg} = 1000 \text{ g}$).
2. Posortuj przedmioty malejąco według wagi (wykorzystaj funkcję `sorted()` z parametrem `key` i `reverse=True`).
3. Przeglądaj przedmioty od najcięższego: jeśli waga przedmiotu mieści się w pozostałej dostępnej ładowności plecaka, dodaj go do ekwipunku i pomniejsz limit o jego wagę.
4. Wyświetl nazwy wszystkich spakowanych przedmiotów w kolejności ich dodawania.

### Przykład testowy
* **Wejście:**
  ```text
  10
  ```
* **Wyjście:**
  ```text
  палатка
  спальный мешок
  удочка
  термос
  салфетки
  жвачка
  ```
*(Wyjaśnienie: 5500 + 2250 + 1200 + 1000 + 40 + 10 = 10000 g = 10 kg)*

---

## Zadanie 3: Lista słowników — Programiści i języki

### Opis problemu
Dany jest rejestr pracowników zapisany jako lista słowników:
```python
people = [
    {"name": "Tom", "age": 39, "company": "SuperCorp", "languages": ["Python", "JavaScript"]},
    {"name": "Bob", "age": 43, "company": "BigCorp", "languages": ["Python", "C++", "C#"]},
    {"name": "Sam", "age": 28, "company": "LittleCorp", "languages": ["Python", "Java"]}
]
```

Każdy słownik opisuje jedną osobę:
* pole `"name"` przechowuje imię pracownika,
* pole `"age"` przechowuje wiek,
* pole `"company"` przechowuje nazwę firmy,
* pole `"languages"` zawiera listę języków programowania, którymi posługuje się pracownik.

### Polecenie
Napisz program, który iteruje po liście `people` i dla każdego pracownika wyświetli w konsoli jego imię oraz **ostatni** język programowania z listy `languages` (zastosuj indeksowanie listy).

### Oczekiwany wynik w konsoli
```text
Name:  Tom
Last language:  JavaScript
Name:  Bob
Last language:  C#
Name:  Sam
Last language:  Java
```

---

## Zadanie 4: Zbiory — Różnica dwóch list

### Opis problemu
Dane są dwie listy liczb całkowitych:
```python
list1 = [10, 20, 30, 40, 50]
list2 = [20, 25, 30, 35, 40]
```

### Polecenie
Napisz program, który porównuje obie listy i tworzy listę zawierającą wyłącznie elementy, które znajdują się w `list1`, lecz **nie występują** w `list2`.
W rozwiązaniu wykorzystaj typ zbioru (`set`) oraz operację różnicy zbiorów (`.difference()` lub operator `-`).

### Oczekiwany wynik w konsoli
```text
list1: [10, 20, 30, 40, 50]
list2: [20, 25, 30, 35, 40]
Разность списков:  [10, 50]
```

---

## Zadanie 5: Zbiory — Studenci i pracownicy

### Opis problemu
Dane są dwa zbiory reprezentujące grupy osób:
```python
students = {"Tom", "Bob", "Sam"}
employees = {"Tom", "Bob", "Alex", "Mike"}
```
Niektóre osoby mogą jednocześnie uczyć się (studiować) i pracować.

### Polecenie
Napisz program, który za pomocą standardowych operacji na zbiorach wyznacza i wyświetla:
1. Wszystkie unikalne osoby z obu grup (suma zbiorów: `|` lub `.union()`).
2. Osoby, które jednocześnie studiują i pracują (część wspólna / iloczyn: `&` lub `.intersection()`).
3. Osoby, które tylko studiują, ale nie pracują (różnica: `-` lub `.difference()`).
4. Osoby, które albo tylko studiują, albo tylko pracują, ale nie robią obu tych czynności naraz (różnica symetryczna: `^` lub `.symmetric_difference()`).

---
