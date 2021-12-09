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