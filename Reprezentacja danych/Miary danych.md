## Miary danych
---
### Dane jako opis rzeczy
- cechy atrybutów:
	- ilościowe - numertczne np. prędkość
	- jakościowe - kategoryczne np. płeć
- uporządkowana postać [[Macierz danych|macierz danych]]

### Funkcje [[Atrybuty|atrybutów]]

### Porządkowanie danych
#### [[Dane wektorowe|wektorowe]]
- $[1, 4] ? [3, 2]$
- rozwiązanie 1: leksykograficznie $[1, 4] < [3, 2]$ bo $1 < 3$
- rozwiązanie 2: normy wektorów $|[a, b]| = a + b$, wtedy $[1, 4] = [3, 2]$

#### tekstowe
- porównywanie **ASCII**
- porównywanie kodów jeśli są alfabetycznie w nich litery ustawione
- leksykograficznie **"aac" < "aaa"** bo **a > c**
- odpowiedni porządek zakodowany np. "**generał" = 100, "szeregowy" = 1** więc **"generał" > "szeregowy"**

### Miary tendencji centralnej
- pozwalają na wyznaczenie "środka" wartości atrybutu
- interpretacja "środka" zależy od miary
- wartości średnie, mediany, moda (dominanta)

#### Moda (dominanta)
- wartość dominująca
- można wyznaczyć dla kazdego atrybutu
- dany atrybut może mieć wiele dominant (np. jak występuje tyle samo razy jakaś popularna wartość)

### Miary pozycyjne
- mediana
- kwartyle:
	- dzielą zbiór na 4 równe części
	- pierwszy kwartyl to wartości rozdzielające pierwsze 25% od następnych 75%
	- drugi kwartyl to mediana
- decyle (podział na 10)
- centyle (podział na 100)
	- siatki centylowe
- kwantyle (rząd kwantyla - % miejsce podziału)

### Miary rozrzutu
- pozwalają na ocenę rozproszenia wartości wokół wartości średniej
- odchylenie standardowe, przeciętne, współczynnik zmienności, zakres, rozstęp międzykwartylowy

#### Rozstęp
- różnica między max a min

#### Rozstęp międzykwartylowy
- różnica między trzecim a pierwszym kwartylem
- odchylenie ćwiartkowe = połowa rozstępu międzykwartylowego

### Skalowanie
- przeliczenie atrybutu tak aby:
	- zmieniał się w ściśle określonym zakresie
	- rozkład był w miarę równomierny
- standaryzacja
- skalowanie logarytmiczne

### Miary odległości i podobieństwa
- porównujemy atrybuty
- metryka minkowskiego
- normy:
	- L1 / metryka miejska
	- L2 / norma euklidesowa
	- norma maksimum / metryka Czebyszewa
- tabela krzyżowa (tablica kontyngencji):
	- kombinacje atrybutów (ile wystąpień kombinacji)
	- kowariancja (jest nieunormowana więc utrudnia interpretację trochę)
	- macierze kowariancji każdych 2 atrybutów
	- korelacja
	- macierz korelacji

#### Korelacja
- nie jest wrażliwa na rozrzut danych
- od -1 do 1
- Wykresy punktowe ![[wspolczynniki_korelacji.png]]