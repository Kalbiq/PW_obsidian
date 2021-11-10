### Opis
- znamy pożądnae wyjście
- modele zależności wejście - wyjście
- klasyfikacja - na wyjściu jest kategoria
- regresja - na wyjściu wartość liczbowa

### Klasyfikacja
- obiekty opisane są cechami i pojedynczym atrybutem decyzyjnym (kategorią)
- nieznane obiekt są klasyfikowane
- cechy pomagają wybrać kategorię

#### Klasyfikator
- algorytm realizujący klasyfikację
- ma model i parametry
	- model - ustalony przez projektanta
	- parametry - ustalone podczas uczenia
- klasyfikacja wymaga znania zbioru uczącego

### Zbiór uczący
- obiekty już sklasyfikowane
- można używać:
	- bezpośrednio - klasyfikatory minimalnoodległościowe
	- pośrednio - klasyfikatory używające funkcji dyskryminiacji i inne metody (uczenie, model)

### Lazy learning vs eager learning
![[Pasted image 20211110104157.png]]

#### Proces uczenia
- niezbędny w eager learning
- wyznaczamy na podstawie zbioru uczącego parametry kalsyfikatora
- po nauczeniu nie jest potrzebny zbiór uczący
- dodanie nowych danych do zbioru wymusza modyfikację modelu lub jego weryfikację

### Klasyfikatory
#### Klasyfikatiory najbliższych sąsiadów (NN)
- minimalnoodległościowe
- wyznacza sie odległość między obiektem analizowanym a innymi obiektami
- kluczowy jest sposób wyznaczania odległości
- najprostszy

![[klasyfikator_NN.png]]

##### Zalety
- prosta
- brak fazy uczenia

##### Wady:
- czasochłonność, trzeba analizować cały zbiór
- wrażliwość na błędy w zbiorze uczącym
	- punkty czasem są daleko od swojej grupy i może to prowadzić do złej kategoryzacji
	![[Pasted image 20211110105729.png]]

#### Klasyfikator k-najbliższych sąsoadów (k-NN)
- zamiast szukać najblizszego sąsiada to szukamy k-sąsiadów
- jako wynik wybieramy dominującą klasę
- *poziom ufności* $= \frac{l}{k}$ gdzie $l$ to ilość w klasie dominującej a $k$ to ilość sąsiadów

![[klasyfikator_kNN.png]]

##### Dobór $k$
- powinno być nieparzyste
- często dobiera się eksperymentalnie
- im mniej obiektów w poszczególnych klasach tym mniejsze $k$
- gdy mamy po jednym obiekcie w każdej klasie to $k=1$

##### Zalety
- mniejsze ryzyko błędnej kategoryzacji

##### Wady
- wysoki koszt obliczeniowy

#### Klasyfikatopr najbliższego prototypu (NP)
- można zastąpić przedstawicieli klasy prototypem tej klasy
- prototyp jest to wirtualny wzorzec klasy kumulujący jej cechy
- mając prototyp nie trzeba już korzystać ze zbioru uczącego
- wyznaczanie prototypu jest fazą uczenia

![[klasyfikator_NP.png]]

##### Funkcja dyskryminacyjna
![[funkcja_dyskryminacyjna_NP.png]]

$p$ - wektor cech
$w_i$ - wzorce klas (punkty średnie)

#### Klasyfikator Bayesa
- podstawowy klasyfikator statystyczny
- zdarzenia losowe - przynależność do klasy
- modelowanie prawdopodobieństw
- obiekt należy do klasy pod warunkiem, że posiada jakieś cechy (prawdopodobieństwo warunkowe)

![[klasyfikator_bayesa.png]]

##### Twierdzenie Bayesa
![[twierdzenie_bayesa.png]]