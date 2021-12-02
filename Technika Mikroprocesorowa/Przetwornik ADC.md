### Przetwornik ADC
#### bezpośredni równoległy
![[Pasted image 20211125134906.png]]

#### z kompensacją liniową
- mirzy się napięcie poprzez inne napięcie
- nie obciążamy źródła które mierzymy
- czas konwersji zależy od sygnału wejściowego, nie jest to dobre bo chcemy stały mieć
- już się ich raczej nie stosuje, ale nadal się stosuje kiedy potrzeba dostać wartość chwilową sygnału

![[Pasted image 20211202122520.png]]
![[Pasted image 20211202123556.png]]

#### z kompensacją wagową - SAR
- czas konwersji nie jest już zależny od sygnału
- poprzez ustawianie $\frac{1}{2}$ zakresu mierzenia na początku i stwierdzenie czy sygnał większy czy mniejszy aproksymuje takimi połówkami (na wykresie widać) wartość sygnału
- przy każdym etapie proksymacji wstawia do wyniku 1 albo 0 w zależności czy sygnał > czy < niż wartość aproksymowana
- problem pojawia się gdy sygnał zmieni mocno swoją wartość podczas pomiaru ponieważ odczyt będzie nieprawidłowy

![[Pasted image 20211202123739.png]]
![[Pasted image 20211202125821.png]]

##### układ próbkująco - pamiętający
- rozwiązuje problem zmiany sygnału podczas pomiaru
- przechowuje sygnał na czas pomiaru w stałej wartości
- 2 wzmacniacze mające świetną wydajność, mają wzmocnienie = 1 żeby nie zmienić sygnału
- kondensator też jest wysokiej klasy, ale musi być bardzo szybko ładowany
- drugi wzmacniacz ma ogromną impedancję wejściową żeby nie obciążać kondensatora
- przy takim rozwiązaniu wartość pomiarowa jest równa chwilowej w momencie rozpoczęcia pomiaru

![[Pasted image 20211202125128.png]]
![[Pasted image 20211202125710.png]]