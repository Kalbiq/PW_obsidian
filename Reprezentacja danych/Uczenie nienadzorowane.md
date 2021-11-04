### Opis
- nie znamy wyjścia
- odkrywamy strukturę danych i zależności
- grupowanie danych
- detekcja anlomalii
- odkrywanie wzorców

### Idea grupowania
- odkrywanie naturalnych skupisk danych
- podział na podzbiory składające sie z podobnych obiektów
- zawierają atrybuty opisowe, nie mają jeszcze decyzyjnych

#### Grupowanie hierarchiczne
- iteracyjne tworzenie grup obiektów
- grupy tworzą hierarchię, jedne zawierają drugie
- struktura drzewa

##### Podjeście aglomeracyjne
- zakładamy że liczba grup jest równa liczbie obiektów
- iteracyjnie zmniejszamy liczbę grup poprzez łączenie podobnych
- tanie obliczeniowo

##### Podejście rozdzielające
- zakładamy że wszystkie obiekty w jednej grupie
- iteracyjnie oddzielamy najmniej podobne do innych grup
- bardziej kosztowne obliczeniowo

#### Grupowanie k-średnich
- minimalizujemy odległości między obiektami tej samej grupy oraz maksymalizujemy odległości między obiektamy z innych grup
- dzielimy na k grup, niezmienne z góry ustalone

##### Centroidy
- środek skupienia grupy
- w iteracjach może się zmieniać jego położenie