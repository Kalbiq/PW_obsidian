### Opis
- inna nazwa: Hash Table
- bardzo szybie szukanie w tablicy
- notacja $O(1)$

### Działanie
- hashujemy obiekt i robimy **hash % n** i wstawiamy na index tej wartości
- przy szukaniu w takiej tablicy hashujemy szukaną liczbę % przez długość tablicy i patrzymy co jest pod tym adresem

### Sytuacja z takimi samymi hashami
#### Problem
Jest możliwe że dostaniemy 2 takie same hashe z różnych danych (raczej 2 takie same wyniki **hash % n**).

#### Rozwiązanie - metoda łańcuchowa
- zamiast mieć tylko jeden obiekt w tabeli pod danym hashem mamy listę obiektów
- złożoność się zmienia ponieważ musimy jeszcze przeszukać listę pod hashem
- może się zdarzyć że przez słabą funkcję mieszającą będziemy mieli wiele obiektów pod tymi samymi hashami przez co stracimy dużo szybkości
- staramy się dbać o poziom wypełnienia naszej tablicy
	- współczynnik wypełnienia $f=\frac{m}{n}$ gdzie m to ilość elementów zajętych w tablicy

#### Metody adresowania w adresowaniu otwartym
##### Liniowe
$$f_{(k,i)}=(f_{(k)}+i)\%m$$

##### Kwadratowe
$$f_{(k,i)}=(f_{(k)}+a*i+b*i*i)\%m$$
$a,b$ są dobierane przez nas

##### Hashowanie podwójne
$$f_{(k,i)}=(f_{(k)}+i*g_{(k)})\%m$$

##### Ogólnie
Gdy mamy kolizję to zwiększamy $i$ zaczynając od $i=0$

$$f_{(k)}=k\%m$$
$$g_{(k)}=2+k\%(m-3)$$

##### Problem z usuwaniem
Kidy usuwamy to jest problem bo nie da się odtworzyć wkładania innego elementu przez co nie można go znaleźć w tablicy.

Trzeba zamiast usuwać wstawiać specjalny obiekt który mówi że jest pusto w tym miejscu ale nadal da się odszukać inne obiektów bo wtedy mówi on że coś tam jest ale wartość nie równa temu co szukamy.