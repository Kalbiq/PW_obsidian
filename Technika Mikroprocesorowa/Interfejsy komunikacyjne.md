### Opis
![[Pasted image 20211209123604.png]]
![[Pasted image 20211209124344.png]]

### Podział magistrali interfejsów
![[Pasted image 20211209124837.png]]
- szeregowy - przekazujemy bit po bicie
- równoległy - przekazujemy cały bajt naraz

### Linia długa
![[Pasted image 20211209125608.png]]
![[Pasted image 20211209130547.png]]
![[Pasted image 20211209131001.png]]

### Połączenia
![[Pasted image 20211209131706.png]]
- asynchroniczny
	- przy każdym takcie rejestr przesuwa bit w prawo
- RZ - return to zero - przed każdym wysłaniem bitu układ wraca do pewnego punktu
- NRZ - non return to zero - albo jeden albo zero

#### UART
![[Pasted image 20211209134248.png]]

- wynaleziony przeszło 60 lat temu
- rozwiązuje problem asynchronicznego przesyłania
- ramka - transmisja danych wraz z bitami sterującymi

##### Nadajnik
![[Pasted image 20211216121933.png]]

##### Odbiornik
![[Pasted image 20211216122439.png]]
- detektor bróbkujący sprawdza czy sygnał jest stały i nie zmienia się nagle podczas jednego bitu, jeśli conajmniej 2 sąsiadujące próbki są takie same to detektor uznaje je za wartość sygnału

##### Ramka
![[Pasted image 20211216123223.png]]
- dopóki próbki trafiają w ramkę rzeczywistą to można odczytać prawidłowo wartość
- zazwyczaj odchył jest +/- 5%
- ze względów fizycznych ciężko jest ustawić dokładnie taki sam Baud Rate

##### Typowe połączenia
![[Pasted image 20211216124718.png]]
- UART średnio się nadaje do połączeń sieciowych, był projektowany do połączeń jeden do jednego
- Wake-up - wired and (iloczyn na drucie) - TxD są połączone poprzez diode
	- urządzenie uart zaczynając nadawanie nadaje stan niski na linię poprzez diodę i blokuje inne uarty które mają jedynki
	- jest realizowane AND czyli jeśli jeden uart ma zero to cała linia zero i tylko jeśli wszystkie mają jeden to na lini jest jeden
	- nie mogą działać jednocześnie bo sygnał nie będzie miał sensu
	- tylko jedno urządzenie może nadawać na raz
	- master może nadawać do wszystkich i wybiera je poprzez adres urządzenia (8-bitów) i w ostatniej ramce sygnału nadaje on bit sygnalizujący że jest to adres, urządzenia muszą umieć rozpoznać czy sygnał jest do nich

#### SPI
![[Pasted image 20211216133028.png]]
![[Pasted image 20211216134436.png]]
- bardzo rzadkie połączenie (daisy chain)

![[Pasted image 20211216135002.png]]
- zbocze narastające => odbiornik ma zapamiętać to co jest aktualnie na wejściu
- zbocze opadające => nadajnik wysyła na złącze kolejny bit
- transmisje mogą być dowolnie długie ponieważ to my sterujemy momentami odczytu i nadania a nie synchronizacja ramek jak w UART, dzięki temu nie ma problemów z synchronizacją długich transmisji

##### Transmisja slave -> master
- slave ustawia daną na drugiej lini przy zboczu narastającym
- przy zboczu opadającym master odczytuje daną z drugiej lini
- zawsze jest dwustronna komunikacja
- komunikacja jest przesunięta o połowę fazy
- praca w trybie FULL DUPLEX - naraz w 2 strony
- slave sam z siebie nie może czegoś nadać masterowi