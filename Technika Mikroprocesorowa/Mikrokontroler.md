### Schemat
![[mikrokontroler.png]]
![[mikrokontroler_2.png]]

Dekoder pamięci - zna adresy urządzeń
ADC, DAC, ... - urządzenia peryferyjne
CPU - [[Procesor|procesor]]

### Opis działania
- urządzenia są podłączone równolegle do szyny danych
	- trzeba wiedzieć w jakim czasie czytać z szyny bo mogą się zmienić na nim dane
	- jeśli urządzenia naraz będą nadawać na szynę to mogą się zewrzeć i uszkodzić
	- przed takimi rzeczami zabezpieczas bramka trójstanowa [[Bramka trójstanowa|3-state]]
- 