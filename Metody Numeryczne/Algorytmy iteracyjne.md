### Opis
- musi być zbieżny
- mogą się kumulować błędy zaokrągleń

### Zapis prostego algorytmu
![[Pasted image 20220310105627.png]]

$\rho = 1$ -> algorytmy ze zbieżnością liniową
$\rho = 2,3,...$ -> zbieżność kwadratowa, sześcienna itd. 

Im większy współczynnik zbieżności tym lepiej ponieważ obniża to błąd w kolejnej iteracji

### Osiągalna dokładnośc algorytmu
![[Pasted image 20220310113828.png]]
![[Pasted image 20220317102016.png]]

### Metoda na bardziej skomplikowany algorytm
![[Pasted image 20220317105610.png]]

### Przykłady
#### przykład 1
$y=\sqrt{x}$ , $y_{it} = \frac{1}{2} (y_i + \frac{x}{y_i})$ <-- (algorytm Herona)

![[Pasted image 20220310105544.png]]

![[Pasted image 20220310111150.png]]

Czyli jest zbieżny kwadratowo

![[Pasted image 20220310111323.png]]


#### przykład 2
![[Pasted image 20220310112128.png]]
![[Pasted image 20220310112235.png]]

#### przykład 3
![[Pasted image 20220310112745.png]]
![[Pasted image 20220310112824.png]]

#### przykład 4
Szacowanie błędu w i-tej iteracji ze znanym już $\rho$ (na rysunku $\varrho$)

![[Pasted image 20220317102849.png]]

![[Pasted image 20220317103139.png]]

![[Pasted image 20220317103813.png]]

![[Pasted image 20220317104030.png]]

#### przykład 5
![[Pasted image 20220317105144.png]]

#### przykład 6
[[Algorytmy iteracyjne#Metoda na bardziej skomplikowany algorytm|Inne podejście]], znowu algorytm Herona.

![[Pasted image 20220317105850.png]]

![[Pasted image 20220317110218.png]]

![[Pasted image 20220317110613.png]]

(to $\varrho \rightarrow 2$ jest błędem)