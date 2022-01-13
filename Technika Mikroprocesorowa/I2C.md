#### $I^2C$ (I2C)
##### Opis
![[Pasted image 20220113130400.png]]

- tylko jedna linia przesyłowa
- jest sformalizowana specyfikacja
- tranzystory w konfiguracji open-dren - cały układ jest wolniejszy ponieważ zmiany z zero na jeden są wolniejsze

![[Pasted image 20220113131851.png]]

![[Pasted image 20220113133108.png]]

##### Transmisja Master -> Slave
![[Pasted image 20220113132600.png]]

- najlepiej sprawdza się przy przesyłaniu dużych ilości

##### Transmisja Slave -> Master
![[Pasted image 20220113132950.png]]

##### Arbitraż
![[Pasted image 20220113134158.png]]

- jak master przegrywa to ustawia odpowiednią flagę, którą możemy jakoś zinterpretować

![[Pasted image 20220113134656.png]]

