### Opis
- klucz i wartość


### Implementacja jako Drzewo
- podstawy: [[Kopiec (binary tree)]]
- chcemy by wysokość drzewa była $h=\log_2{n}$
- można mieć 2 wartości w węźle i wtedy są 3 potomkowie albo 3 i 4 potomków

#### 2 - 3
#todo Na kartce do przepisania / zdjęcie
Drzewo 2 - 3 słowo "Kapelusz"

#### Czerwono - czarne
- mamy węzły czerwone i czarne
- każda ścieżka od korzenia do liścia prowadzi przez tylesamo czarnych i czerwonych
- wszystko co wstawiamy jest czerwone a korzeń jest czarny

##### Lewostronnie czerwone
- nie może być po sobie 2 węzłów czerwonych
- węzły są wstawiane jako czerwone
- jeśli mamy 2 po sobie to robimy rotację
- jeśli mamy 2 czerownych potomków to zamieniamy kolory rodzica z dziećmi
- korzeń zawsze musi być czarny
- jeśli narysujemy czerwone węzły na poziomie o jeden wyższym to wygląda ono jak drzewo 2 - 3
- łatwiejsze do zaimplementowania niż 2 - 3, ale trochę gorsze

#todo Na kartce do przepisania / zdjęcie
Drzewo czerowono - czarne (modyfikacja lewostronnie czerwona)

##### Usuwanie elementu największego
- Wariant I:
	- potomkowie korzenia czarni
	- schodzimy do największej wartości zamieniając kolory tak aby iść zawsze po czerwonym
	- usuwamy
	- naprawiamy niezgodności jeśli trzeba
- Wariant II:
	- prawy potomek czarny, lewy potomek czerwony
	- robimy rotację w prawo na korzeniu
	- potem tak jak w wariancie I
	- robimy rotację w lewo na korzeniu
