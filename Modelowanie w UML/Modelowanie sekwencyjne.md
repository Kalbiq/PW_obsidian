### Opis
![[Pasted image 20220310142717.png]]

**Linia życia** - pionowa przerywana linia, na niej są belki operacji (poziome linie ze strzałką)

Czas płynie z góry na dół.

Komunikaty odpowiadają operacjom klas. I **są one wykonywane przez cel** tego komunikatu, czyli obiekt na końcu strzałki.

Obiekt wysyłający komunikat musi wiedzieć obiekcie do którego wysyła. Oznacza to że musi być tam jakaś relacja na diagramie klas.

![[Pasted image 20220310143930.png]]

### Zagadnienia
- [[Cykl życia]]
- [[Nieliniowe przebiegi (Ramki)]]
- [[Komunikaty synchroniczne]]
- [[Komunikaty asynchroniczne]]

### Etykiety komunikatów
Wywołanie:
- Format: *nazwa komunikatu* ( *lista argumentów* )
- Format argumentów: *nazwa* = *wartość*, ... 

Zwrot:
- Format: *cel przypisania* = *nazwa komunikatu* ( *lista argumentów* ) : *wartość*
	- cel przypisania gdzie przypisać wartość zwracaną
- Format argumentów: *nazwa* : *wartość*, ... 

Nie zawsze trzeba podawać jakie są argumenty.

![[Pasted image 20220310145347.png]]

### Wywołania zwrotne (callback) i własne
W takim wypadku belki mogą się nakładać.

![[Pasted image 20220310150203.png]]

### Modelowanie kodu
Przypomnienie: [[Techniki i zasady#Kod | Zasady modelowania kodu]]

Wzorzec: Model View Presenter (MVP)
![[Pasted image 20220310150947.png]]

![[Pasted image 20220310151518.png]]

![[Pasted image 20220310151733.png]]

Na podstawie takich diagramów można dość łatwo wywnioskować strukturę kodu.

### Typowe błędy w modelowaniu
- Komunikat zwrotny do niewłaściwej linii, żeby sobie skrócić ![[Pasted image 20220310153328.png]]
- Komunikat zwrotny do asynchronicznego ![[Pasted image 20220310153401.png]]
- Inna nazwa komunikatu zwrotnego niż synchronicznego
- Brak ciągłości sterowania ![[Pasted image 20220310153649.png]]
- Zwracanie wartości dla komunikatu asynchronicznego ![[Pasted image 20220310153754.png]]
- Przecięcie się 2 ramek (nie chodzi o zagnieżdżenie)
- Przecięcie ramki z komunikatem
- komunikat zwrotny nie zawarty w tej samej ramce co komunikat synchroniczny

### Sekwencja interakcji z użytkownikiem
Realizowane z pomocą [[Architektura warstwowa|architektury warstwowej]]

![[Pasted image 20220317145349.png]]

### Komunitakty vs. kod
![[Pasted image 20220317150909.png]]

### Stosowanie komunikacji synchronicznej i asynchronicznej
![[Pasted image 20220317151727.png]]

### Fragment włączony
![[Pasted image 20220317154321.png]]

![[Pasted image 20220317154334.png]]
![[Pasted image 20220317154351.png]]

