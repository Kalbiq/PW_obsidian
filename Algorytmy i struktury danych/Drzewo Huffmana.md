### Opis
- na początku z lasu wyjmujemy po dwa drzewa z najmniejszą wartością i dodajemy do nich węzeł z ich sumą
- pozwala zakodować znaki które występowały wcześniej jako krótsze słowa kodowe korzystając z drzewa Huffmana
- żadne słowo kodewe nie jest prefixem innego czyi nie ma np. 01 i 011 więc można bardzo łatwo stwierdzić jaki jest znak za danym kodem
- każdy wierzchołek który nie jest lisciem ma 2 potomków, jest to drzewo regularne
- znaków w drzewie jest $C$ a innych (sum) jest $C - 1$

### Złożoność
$$\sum a_z * d_{kz}$$
$a_z$ - ilość wystąpień znaku
$d_{kz}$ - dłogość kodu znaku

### Problemy
- plik można odkodować tylko przy pomocy naszego drzewa więc trzeba je dołączyć do kompresji co skutkuje zwiększeniem rozmiaru pliku

#todo na kartce do przepisania