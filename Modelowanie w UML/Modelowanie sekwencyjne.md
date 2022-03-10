### Opis
![[Pasted image 20220310142717.png]]

**Linia życia** - pionowa przerywana linia, na niej są belki operacji (poziome linie ze strzałką)

Czas płynie z góry na dół.

Komunikaty odpowiadają operacjom klas. I **są one wykonywane przez cel** tego komunikatu, czyli obiekt na końcu strzałki.

Obiekt wysyłający komunikat musi wiedzieć obiekcie do którego wysyła. Oznacza to że musi być tam jakaś relacja na diagramie klas.

![[Pasted image 20220310143930.png]]

### Cykl życia
Linia życia określa czas życia obiektu.

Długość wykonywania operacji jest określony przez długość belki na lini życia.

X na lini życia oznacza usunięcie obiektu.

![[Pasted image 20220310143514.png]]

### Komunikaty synchroniczne
Obiekt wysyła komunikat i czeka na odpowiedź.

Ważne: **grot strzałki jest wypełniony**

![[Pasted image 20220310144258.png]]

Na diagramie synchronicznym musi być ciągłość sterowania, czyli da się przejść strzałka po strzałce i sterowanie zawsze wraca do wysyłającego.
Jak nie ma komunikatu zwrotnego to wraca odrazu.

![[Pasted image 20220310145757.png]]
![[Pasted image 20220310150122.png]]

### Komunikaty asynchroniczne
Obiekt wysyła komunikat i wraca do pracy. Procedura wywołująca nie czeka na odpowiedź.

Zwrot jest oddzielnym komunikatem (jeśli jest).

Ważne: **grot strzałki jest otwarty**

![[Pasted image 20220310144434.png]]

Nastepuje podział sterowania na różne wątki. Może być wykonywane kilka operacji na raz przez różne obiekty.

![[Pasted image 20220310150653.png]]

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
