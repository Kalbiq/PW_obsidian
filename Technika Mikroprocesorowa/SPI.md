#### SPI
![[Pasted image 20211216133028.png]]
![[Pasted image 20211216134436.png]]
- bardzo rzadkie połączenie (daisy chain)

![[Pasted image 20211216135002.png]]
- zbocze narastające => odbiornik ma zapamiętać to co jest aktualnie na wejściu
- zbocze opadające => nadajnik wysyła na złącze kolejny bit
- transmisje mogą być dowolnie długie ponieważ to my sterujemy momentami odczytu i nadania a nie synchronizacja ramek jak w UART, dzięki temu nie ma problemów z synchronizacją długich transmisji

##### Rodzaje
![[Pasted image 20220113122224.png]]
![[Pasted image 20220113122256.png]]

##### Transmisja slave -> master
- slave ustawia daną na drugiej lini przy zboczu narastającym
- przy zboczu opadającym master odczytuje daną z drugiej lini
- zawsze jest dwustronna komunikacja
- komunikacja jest przesunięta o połowę fazy
- praca w trybie FULL DUPLEX - naraz w 2 strony
- slave sam z siebie nie może czegoś nadać masterowi

##### Zalety
- komunikacja full-duplex - można jednocześnie nadawać i odbierać
- dowolny format transmisji
- bardzo prosty wybór slave'ów
- nadajniki push-pull - duża szybkość
- dane nie są ograniczone do słów 8-b
- prosta implementacja programowa
- brak bitów sterujących - szybsza transmisja, brak strat czasu na przesyłanie ich
- jednokierunkowe linie przesyłowe - łatwa izolacja galwaniczna

##### Wady
- dużą ilość pinów i połączeń
- tylko jeden master
- brak formalnego standardu
- brak hot-swap
- brak kontroli przepływu danych
- transmisja tylko na krótkich odległościach
- wiele wariantów