### Opis
- standard testowania
- Joint Test Action Grup
- można debugować hardware i software

![[Pasted image 20220120121932.png]]

### Starsze metody testowania
- automat z igłami testującymi połączenia na płytce
- łoże igłowe, płytka jest dociskana do igieł i można sprawdzić wszystkie połączenia (tak jak metoda z igłami tylko że masowa)
- automatyczny przegląd optyczny
- automatyczne prześwietlenia x-ray

### BGA
![[Pasted image 20220120122157.png]]

- obudowa z wyprowadzeniami
- zrobiona żeby nie wyprowadzać pinów na krawędzie płytki tylko na dół gdzie jest więcej miejsca
- nie da się testować igłowo

#### Zastosowanie JTAG do BGA
![[Pasted image 20220120123000.png]]

![[Pasted image 20220120123305.png]]

### TAP
![[Pasted image 20220120123139.png]]

![[Pasted image 20220120123202.png]]

### Instrukcje
![[Pasted image 20220120123041.png]]

- jest wiele możliwych poleceń które zmieniają test
- można testować w zasadzie wszystko (trzeba tylko znać jakie są polecenia)

![[Pasted image 20220120123453.png]]

- testowana jest tu płytka z 3 diodami
- kidy BSC jest w trybie testowym to odcina od świata zewnętrznego, wtedy dane są podawane przez nas i zbierane przez nas poprzez TAP

![[Pasted image 20220120123622.png]]

- testowanie 2 układów ze sobą

### Wady i zalety
![[Pasted image 20220120124002.png]]

