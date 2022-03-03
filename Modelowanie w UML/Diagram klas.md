### Klasa
- wzorzec do budowy obiektu
- obiekt zewnętrzny prosi o wyprodukowanie obiektu
- po produkcji mozna korzystać z funkcji klasy

### Diagram UML
- ma prostą nazwę
- zawiera przegródki (np. nazwa, atrybuty, operacje)
- można przedstawiać na diagramie mniej lub wiecej szczegółów

#### Przykłady
rózne warianty przedstawienia klasy samochodu
![[Pasted image 20220303142455.png]]

### Atrybuty
#### Składnia:
- " nazwa : typ \[krotność\] "
- typ nie jest obowiązkowy
- typy nie są standaryzowane w UML
- typem może być nazwa innej klasy

#### Dobre praktyki:
- model rzeczywistości:
	- nazwy i typy powinny być zrozumiałe dla klienta
- model kodu:
	- nazwy typów zgodne z danym językiem programowania

#### Typy wyliczeniowe
![[Pasted image 20220303143700.png]]

### Operacje
Elementarna usługa dostarczana przez obiekty danej klasy innym obiektom

#### Składnia
- " nazwa (lista parametrów) : zwracany typ "
- lista parametrów ma rozdzielone je przecinkami
- zapis parametrów tak jak w atrybutach

### Stereotyp
Umożliwia dopasowanie elementu UML do danej platformy lub dziedziny.

![[Pasted image 20220303144910.png]]

### Asocjacje
Relacje między obiektami klas. W danej relacji klasy pełnia różne role i jest to też zaznaczone.

#### Przykłady
##### Sama z sobą
![[Pasted image 20220303145403.png]]
![[Pasted image 20220303145543.png]]
##### Z inną klasą
![[Pasted image 20220303145624.png]]

### Krotności
Dopuszczalna liczba obiektów klasy w relacji z obiektem drugiej klasy.

Zapis:
- od 2 do 2 => 2
- od 0 do 5 => 0..5
- od 0 do $\infty$ => 0..* lub samo *

![[Pasted image 20220303150149.png]]

### Agregacje i kompozycje
Asocjacje grupowania czyli całość - części.

- rąb jest po stronie całości
- czarny rąb to kompozycja
- w kompozycji obiekty nie moga być dzielone między różne całości
	- np. silnik - samochód
- w agregacji obiekty mogą być w różnych agregacjach na raz
	- np. osoba - stowarzyszenie

![[Pasted image 20220303150820.png]]

### Nawigowalność asocjacji
Obiekty jednej klasy wiedzą o innej klasie.

Rodzaje:
- nawigowalność bez atrybutu
- nawigowalność poprzez atrybut
- brak nawigowalności (można daź X żeby podkreślić)

- strzałka po stronie asocjacji która wie (dowód wie, samochód nie)

![[Pasted image 20220303151409.png]]

### Elementarne atrybuty a klasy
- obiekt posiada tożsamość
- obiekt można zdekomponowac na pod-obiekty
- obiekty wchodzą w dalsze relacje

### Asocjacje a atrybuty
Asocjacje lepiej stosować kiedy obydwie klasy wiedzą o sobie.

Atrybuty lepiej stosować kiedy nie ma potrzeby pokazywania klasy, lub chcemy uprościć siec połączeń.

![[Pasted image 20220303152010.png]]

### Klasy asocjacyjne
Tak jakby asocjacja z atrybutami i operacjami.

![[Pasted image 20220303152408.png]]

### Asocjacje wielokrotne


### Generalizacje
- klasy ogólne i specjalizowane
- może być dziedziczenie
- klasy abstrakcyjne (nie istnieją w rzeczywistości, np. pojazd)

### Notacja obiektów
![[Pasted image 20220303153631.png]]
![[Pasted image 20220303153757.png]]

#### Relacja zawierania
![[Pasted image 20220303153851.png]]

#### Typ obiektu
![[Pasted image 20220303153918.png]]