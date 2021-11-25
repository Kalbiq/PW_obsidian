### Opis
- rejestr liczący jakieś impulsy

![[timer.png]]

### Schemat
![[Pasted image 20211104124003.png]]
![[Pasted image 20211104125457.png]]
![[Pasted image 20211104132256.png]]

### Program
#### 1
![[Pasted image 20211104132632.png]]

#### 2
![[Pasted image 20211118125053.png]]
![[Pasted image 20211118130353.png]]

### Zegary systemowe MSP430
![[Pasted image 20211118123053.png]]

### DCO (digital clock oscilator)
- dryfty (zmiany częstotliwości)
	- dryft temperaturowy - zmiana temperatury rezystora
	- dryft czasowy - starzeje się rezystor

![[Pasted image 20211118124044.png]]

### Watchdog Timer
- zabezpiecza system przed nieprawidłowym działaniem programu, program powinien wyzerować timer zanim się przepełni
- po przepełnieniu resetuje procesor
- uruchomienie i wyłączenie watchdoga musi być intencjonalne
- w trakcie działania może być wyzerowany
- timer ustawia flagę po dokonaniu resetu procesora

![[Pasted image 20211118132507.png]]
![[Pasted image 20211118133736.png]]
