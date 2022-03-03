### Rodzaje błędów
- Błędy modelowania
	- model ma wadę lub jest uproszczony
	- wnioski moga przez to być mylące
- [[Błędy Danych]]
- [[Błędy metody (błędy obcięcia)]]
- [[Błędy zaokrągleń]]

### Postać mantysa
$$x = \pm mP^c$$
m - mantysa, c - cecha (liczba całkowita)
$$\tilde{x} = \pm \tilde{m}P^c$$

### Błąd względny (eps)
![[Pasted image 20220224111858.png]]
![[Pasted image 20220224112038.png]]

L - liczba liczb po kropce
eps - błąd maszynowy


### Zadania źle uwarunkowane
Jest to zadanie w którym przy małych względnych zmianach danych mamy duże zmiany rozwiązania.

c = cond(zadanie) - wskaźnik uwarunkowania zadania
a = błąd względny(wyniki zadania)
b = błąd względny(dane zadania)

$$a \le c * b$$

np: ![[Pasted image 20220224105011.png]]
