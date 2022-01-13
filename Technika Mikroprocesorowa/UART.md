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