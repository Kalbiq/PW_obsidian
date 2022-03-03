### Błędy zaokrągleń
Obliczenia na zaokrąglonych wartościach dają inny wynik niż zaokrąglenie na końcu.

#### Operacje zmiennopozycyjne
![[Pasted image 20220224113014.png]]

Pamiętamy o tym że  $\tilde{x} = x(1 + \epsilon)$ co wynika ze wzoru na błąd względny

##### Przykład
![[Pasted image 20220224113607.png]]

#### Przykłady
##### przykład 1
![[Pasted image 20220303111843.png]]
![[Pasted image 20220303112048.png]]

##### inny sposób
Chcemy uniknąć odejmowania ponieważ możliwy jest duży błąd względny

![[Pasted image 20220303112854.png]]

##### przykład 2
![[Pasted image 20220303114434.png]]
![[Pasted image 20220303114536.png]]
![[Pasted image 20220303114552.png]]

W zależności od kolejności działań jest różnica błędów. Lepiej wybrać tu algorytm $y_1$.