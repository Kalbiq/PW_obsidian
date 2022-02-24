### Błędy modelowania
- model ma wadę lub jest uproszczony
- wnioski moga przez to być mylące

### Błędy Danych
Zła dokładność pomiarów lub błędne pomiary.

powiązane: [[Macierz Hilberta]]

![[Pasted image 20220224113757.png]]

Jak błąd względny $x$ przenosi się na błąd wyniku $\phi$

### Błędy metody / błędy obcięcia
Wynikają z zastępowania nieskończonych działań skończonymi lub działań na nieskończenie małych liczbach skończenie małymi.

np. kiedy uciąć tą sumę?:
$$e^x = \sum^{\infty}_{k=0}{\frac{1}{k!}*x^k} = 1 + x + \frac{1}{2}x^2 + \frac{1}{3}x^3 + ...$$

### Błędy zaokrągleń
Obliczenia na zaokrąglonych wartościach dają inny wynik niż zaokrąglenie na końcu.

#### Postać mantysa
$$x = \pm mP^c$$
m - mantysa, c - cecha (liczba całkowita)
$$\tilde{x} = \pm \tilde{m}P^c$$

##### Błąd względny
![[Pasted image 20220224111858.png]]
![[Pasted image 20220224112038.png]]

L - liczba liczb po kropce
eps - błąd maszynowy

#### Operacje zmiennopozycyjne
![[Pasted image 20220224113014.png]]

Pamiętamy o tym że  $\tilde{x} = x(1 + \epsilon)$ co wynika ze wzoru na błąd względny

##### Przykład
![[Pasted image 20220224113607.png]]

### Zadania źle uwarunkowane
Jest to zadanie w którym przy małych względnych zmianach danych mamy duże zmiany rozwiązania.

c = cond(zadanie) - wskaźnik uwarunkowania zadania
a = błąd względny(wyniki zadania)
b = błąd względny(dane zadania)

$$a \le c * b$$

np: ![[Pasted image 20220224105011.png]]
