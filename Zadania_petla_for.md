# 🔁 Zadania: Pętla `for` oraz `while` w języku Python

Zbiór 15 zadań praktycznych dotyczących pętli (`for` i `while`), iteracji po listach, przedziałach liczbowych (`range`) oraz napisach, przygotowany do samodzielnego rozwiązywania.

---

## 📋 Spis zadań
1. [Zadanie 1: Kwadraty liczb parzystych (Квадраты чётных чисел)](#zadanie-1-kwadraty-liczb-parzystych)
2. [Zadanie 2: Suma liczb do słowa „The End” (Сумма чисел до "The End")](#zadanie-2-suma-liczb-do-słowa-the-end)
3. [Zadanie 3: Suma dwucyfrowych](#zadanie-3-suma-dwucyfrowych)
4. [Zadanie 4: Największa liczba parzysta](#zadanie-4-największa-liczba-parzysta)
5. [Zadanie 5: Trzy worki i piłki](#zadanie-5-trzy-worki-i-piłki)
6. [Zadanie 6: Zamiana sąsiednich elementów listy](#zadanie-6-zamiana-sąsiednich-elementów-listy)
7. [Zadanie 7: Wypisywanie naprzemienne (z lewej i z prawej)](#zadanie-7-wypisywanie-naprzemienne-z-lewej-i-z-prawej)
8. [Zadanie 8: Liczba różnych wartości w liście](#zadanie-8-liczba-różnych-wartości-w-liście)
9. [Zadanie 9: Czy lista jest permutacją?](#zadanie-9-czy-lista-jest-permutacją)
10. [Zadanie 10: Zepsuta klawiatura (OIJ)](#zadanie-10-zepsuta-klawiatura-oij)
11. [Zadanie 11: Generowanie listy (ciąg Fibonacciego)](#zadanie-11-generowanie-listy-ciąg-fibonacciego)
12. [Zadanie 12: Liczby niepotęgowe](#zadanie-12-liczby-niepotęgowe)
13. [Zadanie 13: Liczby bez cyfry 5 w przedziale (Числа без цифры 5)](#zadanie-13-liczby-bez-cyfry-5-w-przedziale)
14. [Zadanie 14: Suma liczb pierwszych (Сумма простых чисел)](#zadanie-14-suma-liczb-pierwszych)
15. [Zadanie 15: Maksymalna suma cyfr potęgi $c^d$ (Максимальная сумма цифр степени)](#zadanie-15-maksymalna-suma-cyfr-potęgi-cd)

---

## Zadanie 1: Kwadraty liczb parzystych

### Opis
Wczytaj liczbę naturalną $n$. Wypisz na ekranie wszystkie kwadraty liczb parzystych z przedziału od $0$ do $n - 1$ (włącznie), każdy w nowym wierszu.

### Wejście
W pierwszym wierszu jedna liczba naturalna $n$ ($n \ge 1$).

### Wyjście
Kwadraty kolejnych liczb parzystych mniejszych od $n$, każda liczba w osobnym wierszu.

### Przykład
| Wejście | Wyjście |
| :--- | :--- |
| `7` | `0`<br>`4`<br>`16`<br>`36` |

---

## Zadanie 2: Suma liczb do słowa „The End”

### Opis
Wczytuj liczby całkowite ze strumienia wejścia po jednej w każdym wierszu tak długo, aż napotkasz napis `"The End"`. Wypisz na ekranie sumę wszystkich wczytanych liczb.

### Wejście
Dowolna liczba wierszy zawierających po jednej liczbie całkowitej, zakończona wierszem z napisem `"The End"`.

### Wyjście
Jedna liczba całkowita — suma wczytanych liczb.

### Przykład
| Wejście | Wyjście |
| :--- | :--- |
| `10`<br>`-3`<br>`25`<br>`The End` | `32` |

---

## Zadanie 3: Suma dwucyfrowych

### Opis
Dana jest lista zawierająca $N$ liczb. Oblicz sumę liczb dwucyfrowych w tej liście (uwzględniając zarówno dodatnie, jak i ujemne liczby dwucyfrowe, tj. z przedziału $[10, 99]$ oraz $[-99, -10]$).

### Wejście
W pierwszym wierszu liczba naturalna $N$, a w drugim $N$ liczb całkowitych.

### Wyjście
Suma liczb dwucyfrowych podanej listy.

### Przykłady
| Przykład 1 | Przykład 2 | Przykład 3 |
| :--- | :--- | :--- |
| **Wejście:**<br>`4`<br>`15 100 1 13` | **Wejście:**<br>`6`<br>`5 10 15 -15 -10 -1` | **Wejście:**<br>`1`<br>`-20` |
| **Wyjście:**<br>`28` | **Wyjście:**<br>`0` | **Wyjście:**<br>`-20` |

---

## Zadanie 4: Największa liczba parzysta

### Opis
Dana jest lista zawierająca $N$ liczb. Znajdź największą parzystą liczbę w liście. Możesz założyć, że w liście wystąpi co najmniej jedna liczba parzysta.

### Wejście
W pierwszym wierszu liczba naturalna $N$, a w drugim $N$ liczb całkowitych.

### Wyjście
Największa liczba parzysta z podanej listy.

### Przykłady
| Przykład 1 | Przykład 2 | Przykład 3 |
| :--- | :--- | :--- |
| **Wejście:**<br>`5`<br>`3 12 7 25 8` | **Wejście:**<br>`4`<br>`-10 -3 -4 -9` | **Wejście:**<br>`3`<br>`101 2 99` |
| **Wyjście:**<br>`12` | **Wyjście:**<br>`-4` | **Wyjście:**<br>`2` |

---

## Zadanie 5: Trzy worki i piłki

### Opis
Mamy trzy worki, do których zostanie wrzuconych $N$ piłek, jedna po drugiej. Numer na piłce oznacza, do którego worka zostanie ona wrzucona. Po każdym wrzuceniu piłki do worka sprawdzamy, czy liczba piłek w każdym worku jest taka sama. Ile razy w każdym z trzech worków było tyle samo piłek?

### Wejście
W pierwszym wierszu liczba naturalna $N$, a w drugim $N$ liczb naturalnych od $1$ do $3$ oznaczających numery na kolejno wrzucanych piłkach.

### Wyjście
Liczba określająca, ile razy w każdym worku było tyle samo piłek.

### Przykłady
| Przykład 1 | Przykład 2 | Przykład 3 |
| :--- | :--- | :--- |
| **Wejście:**<br>`4`<br>`1 3 2 3` | **Wejście:**<br>`13`<br>`2 1 2 1 3 3 3 1 2 1 2 3 1` | **Wejście:**<br>`2`<br>`1 2` |
| **Wyjście:**<br>`1` | **Wyjście:**<br>`3` | **Wyjście:**<br>`0` |

---

## Zadanie 6: Zamiana sąsiednich elementów listy

### Opis
Dana jest lista zawierająca $N$ liczb. Zamień miejscami sąsiednie liczby, tj. liczby na pozycjach `(0 i 1)`, `(2 i 3)`, `(4 i 5)` itd. W przypadku listy o długości nieparzystej ostatni element nie zmienia pozycji. Pamiętaj, że elementy listy numerowane są od `0`. Wypisz otrzymaną listę.

### Wejście
W pierwszym wierszu liczba naturalna $N$, a w drugim $N$ liczb całkowitych.

### Wyjście
W jednym wierszu lista po opisanych zamianach. Zwróć uwagę na format wyjścia — do wypisania listy w odpowiednim formacie możesz użyć polecenia `print(nazwa_listy)`.

### Przykłady
| Przykład 1 | Przykład 2 | Przykład 3 |
| :--- | :--- | :--- |
| **Wejście:**<br>`4`<br>`1 -2 8 -5` | **Wejście:**<br>`6`<br>`0 1 2 3 4 5` | **Wejście:**<br>`5`<br>`-2 1 0 3 -3` |
| **Wyjście:**<br>`[-2, 1, -5, 8]` | **Wyjście:**<br>`[1, 0, 3, 2, 5, 4]` | **Wyjście:**<br>`[1, -2, 3, 0, -3]` |

---

## Zadanie 7: Wypisywanie naprzemienne (z lewej i z prawej)

### Opis
Dana jest lista zawierająca $N$ liczb. Wypisz na zmianę jeden element z lewej strony, jeden z prawej, aż zostaną wypisane wszystkie liczby.

### Wejście
W pierwszym wierszu liczba naturalna $N$, w drugim $N$ liczb całkowitych.

### Wyjście
Lista z elementami w zmienionej kolejności. Liczby należy oddzielić spacjami.

### Przykłady
| Przykład 1 | Przykład 2 | Przykład 3 |
| :--- | :--- | :--- |
| **Wejście:**<br>`4`<br>`5 2 -8 0` | **Wejście:**<br>`6`<br>`1 2 3 4 5 6` | **Wejście:**<br>`3`<br>`-3 4 -5` |
| **Wyjście:**<br>`5 0 2 -8` | **Wyjście:**<br>`1 6 2 5 3 4` | **Wyjście:**<br>`-3 -5 4` |

---

## Zadanie 8: Liczba różnych wartości w liście

### Opis
Dana jest lista zawierająca $N$ liczb. Policz, ile jest różnych liczb w tej liście.

### Wejście
W pierwszym wierszu liczba naturalna $N$, w drugim $N$ liczb naturalnych, ułożonych w kolejności od najmniejszej do największej wartości.

### Wyjście
Liczba różnych wartości w liście.

### Przykłady
| Przykład 1 | Przykład 2 | Przykład 3 |
| :--- | :--- | :--- |
| **Wejście:**<br>`6`<br>`1 1 2 4 4 4` | **Wejście:**<br>`5`<br>`1 2 3 4 5` | **Wejście:**<br>`1`<br>`9` |
| **Wyjście:**<br>`3` | **Wyjście:**<br>`5` | **Wyjście:**<br>`1` |

---

## Zadanie 9: Czy lista jest permutacją?

### Opis
Dana jest lista zawierająca $N$ liczb. Sprawdź, czy ta lista jest permutacją liczb od $1$ do $N$ (zawiera każdą liczbę z przedziału od $1$ do $N$ dokładnie raz).

### Wejście
W pierwszym wierszu liczba naturalna $N$, w drugim $N$ liczb naturalnych.

### Wyjście
Słowo `TAK`, jeśli lista jest permutacją, lub `NIE` w przeciwnym przypadku.

### Przykłady
| Przykład 1 | Przykład 2 | Przykład 3 |
| :--- | :--- | :--- |
| **Wejście:**<br>`4`<br>`4 2 1 3` | **Wejście:**<br>`5`<br>`1 2 2 7 4` | **Wejście:**<br>`3`<br>`1 1 3` |
| **Wyjście:**<br>`TAK` | **Wyjście:**<br>`NIE` | **Wyjście:**<br>`NIE` |

---

## Zadanie 10: Zepsuta klawiatura (OIJ)

### Opis
Bajtek pisze tekst na zepsutej klawiaturze, wciskając kolejno klawisze z małymi literami alfabetu angielskiego:
* Wciśnięcie dowolnej litery **oprócz `'d'`** powoduje dopisanie tej litery na koniec dotychczasowego tekstu.
* Wciśnięcie klawisza **`'d'`** nie dopisuje litery `'d'`, lecz działa jak specyficzny klawisz usuwania: wyszukuje w aktualnym tekście **największą alfabetycznie literę** (czyli położoną najdalej w alfabecie: najpierw `'z'`, potem `'y'` itd.) i usuwa jej **ostatnie (najbardziej prawe) wystąpienie**.
* Jeśli w momencie wciśnięcia `'d'` tekst na ekranie jest pusty, nic się nie dzieje.

Napisz program, który na podstawie ciągu wciśniętych klawiszy wyznaczy ostateczny napis widoczny na ekranie.

### Wejście
W pierwszym i jedynym wierszu wejścia znajduje się niepusty ciąg małych liter alfabetu angielskiego (o długości od $1$ do $1\,000\,000$), oznaczający kolejne klawisze wciskane przez Bajtka.

### Wyjście
W pierwszym i jedynym wierszu wyjścia należy wypisać ostateczny tekst, który pozostanie na ekranie po przetworzeniu wszystkich wciśnięć klawiszy (lub pusty wiersz, jeśli wszystkie znaki zostały usunięte).

### Przykłady
| Test | Wejście | Wyjście | Wyjaśnienie |
| :--- | :--- | :--- | :--- |
| `zkl0a` | `zadanie` | `aanie` | Po wpisaniu `za`, klawisz `d` usuwa największą literę `z` (zostaje `a`), a następnie dopisywane są `anie`. |
| `zkl0b` | `informatyka` | `informatyka` | Brak litery `d` — wszystkie znaki zostają dopisane bez zmian. |
| `zkl0c` | `abcdabc` | `ababc` | Po `abc`, klawisz `d` usuwa największą literę `c` (zostaje `ab`), po czym dopisywane jest `abc`. |
| `zkl0d` | `abcdd` | `a` | Dwa klawisze `d` usuwają kolejno `c`, a następnie `b`. |
| `zkl0e` | `dddabcd` | `ab` | Pierwsze trzy `d` na pustym napisie nic nie robią; z `abc` ostatnie `d` usuwa `c`. |

---

## Zadanie 11: Generowanie listy (ciąg Fibonacciego)

### Opis
Wygeneruj listę o długości $N$ według poniższych zasad:
* pierwsze dwa elementy listy są równe `1`;
* każdy kolejny element jest sumą dwóch poprzednich.

Przykładowo, dla $N = 5$, otrzymamy listę `[1, 1, 2, 3, 5]` (ostatni element wynosi `5`, ponieważ suma dwóch poprzednich elementów to `2 + 3`).

### Wejście
Liczba naturalna $N$ (większa lub równa $2$).

### Wyjście
Wygenerowana lista. Zwróć uwagę na format wyjścia — do wypisania listy w odpowiednim formacie możesz użyć komendy `print(nazwa_listy)`.

### Przykłady
| Przykład 1 | Przykład 2 | Przykład 3 |
| :--- | :--- | :--- |
| **Wejście:**<br>`5` | **Wejście:**<br>`2` | **Wejście:**<br>`8` |
| **Wyjście:**<br>`[1, 1, 2, 3, 5]` | **Wyjście:**<br>`[1, 1]` | **Wyjście:**<br>`[1, 1, 2, 3, 5, 8, 13, 21]` |

---

## Zadanie 12: Liczby niepotęgowe

### Opis
Liczbę nazywamy **potęgową**, gdy może być przedstawiona jako potęga $a^b$, w której podstawa $a$ i wykładnik $b$ są liczbami naturalnymi większymi lub równymi $2$. Pozostałe dodatnie liczby całkowite to **liczby niepotęgowe**.

Przykładowo: liczby $4 = 2^2$, $64 = 2^6 = 4^3 = 8^2$, $27 = 3^3$ lub $8 = 2^3$ są potęgowe, zaś liczby $10, 1, 3$ oraz $13$ są niepotęgowe.

Uporządkujmy rosnąco wszystkie liczby niepotęgowe:
$$1, 2, 3, 5, 6, 7, 10, 11, 12, 13, 14, 15, 17, 18, 19, \dots$$

Napisz program, który dla różnych wartości $N$ wyznaczy $N$-te liczby niepotęgowe.

### Wejście
W pierwszym wierszu wejścia znajduje się jedna liczba całkowita $T$ ($1 \le T \le 1\,000$) oznaczająca liczbę przypadków testowych. Każdy z $T$ kolejnych wierszy zawiera po jednej liczbie całkowitej $N_i$ ($1 \le N_i \le 10^{18}$).

### Wyjście
Na wyjście należy wypisać $T$ wierszy, w $i$-tym z nich powinna znaleźć się $N_i$-ta w kolejności liczba niepotęgowa.

### Przykład (`lic0a`)
| Wejście | Wyjście |
| :--- | :--- |
| `7`<br>`1`<br>`2`<br>`3`<br>`4`<br>`5`<br>`6`<br>`7` | `1`<br>`2`<br>`3`<br>`5`<br>`6`<br>`7`<br>`10` |

---

## Zadanie 13: Liczby bez cyfry 5 w przedziale

### Opis
Na wejście programu podawane są dwie liczby całkowite $a$ oraz $b$, oddzielone spacją. Twoim zadaniem jest wypisanie na ekranie liczby wszystkich liczb całkowitych z przedziału od $a$ do $b$ włącznie, które w swoim zapisie dziesiętnym **nie zawierają cyfry `5`**.
Początek przedziału jest zawsze mniejszy od końca przedziału ($a < b$). Liczby $a$ i $b$ mogą być ujemne.

⏳ **Limit czasu wykonania kodu:** Kod powinien wykonać się w czasie nieprzekraczającym 12 sekund.

* **Przykład 1:** Jeśli $a = 1$, a $b = 9$, to na ekran należy wypisać `8` (wszystkie cyfry oprócz `5`).

### Format danych wejściowych
Na wejście programu podawane są dwie liczby całkowite $a$ i $b$, oddzielone spacją.

### Format danych wyjściowych
Program powinien wypisać na ekranie liczbę liczb całkowitych spełniających warunek zadania.

### Dane testowe
| Nr testu | Dane wejściowe | Dane wyjściowe |
| :---: | :--- | :--- |
| **1** | `1 9` | `8` |
| **2** | `-17 9` | `24` |
| **3** | `4 17` | `12` |
| **4** | `-17 -4` | `12` |
| **5** | `984 4304` | `2449` |
| **6** | `2313 2317` | `4` |
| **7** | `-4045 2575` | `4819` |

---

## Zadanie 14: Suma liczb pierwszych

### Opis
Suma liczb pierwszych mniejszych od $10$ wynosi $17$:
$$2 + 3 + 5 + 7 = 17$$

Na wejście programu podawana jest liczba naturalna $n$. Twoim zadaniem jest wypisanie na ekranie sumy wszystkich liczb pierwszych, których wartość jest **mniejsza od $n$**.

### Format danych wejściowych
Na wejście programu podawana jest jedna liczba naturalna $n$.

### Format danych wyjściowych
Program powinien wypisać na ekranie sumę wszystkich liczb pierwszych mniejszych od $n$.

### Dane testowe
| Nr testu | Dane wejściowe | Dane wyjściowe |
| :---: | :--- | :--- |
| **1** | `10` | `17` |
| **2** | `100` | `1060` |
| **3** | `2000` | `277050` |
| **4** | `1000000` | `37550402023` |
| **5** | `5000` | `1548136` |
| **6** | `2000000` | `142913828922` |

---

## Zadanie 15: Maksymalna suma cyfr potęgi $c^d$

### Opis
Na wejście programu podawane są dwie liczby naturalne $a$ oraz $b$, oddzielone spacją. Należy znaleźć **maksymalną sumę cyfr** liczby naturalnej postaci $c^d$, gdzie $c < a$ oraz $d < b$ ($c, d \ge 1$).

### Format danych wejściowych
Na wejście programu podawane są dwie liczby naturalne $a$ i $b$, oddzielone spacją.

### Format danych wyjściowych
Program powinien wypisać na ekranie maksymalną sumę cyfr liczby naturalnej postaci $c^d$, gdzie $c < a$ oraz $d < b$.

### Dane testowe
| Nr testu | Dane wejściowe | Dane wyjściowe |
| :---: | :--- | :--- |
| **1** | `100 100` | `972` |
| **2** | `50 50` | `406` |
| **3** | `25 30` | `202` |
| **4** | `15 100` | `548` |
| **5** | `100 25` | `236` |
| **6** | `50 100` | `801` |
