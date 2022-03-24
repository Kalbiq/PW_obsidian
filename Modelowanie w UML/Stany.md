### Operacje klas obiektów

![[Pasted image 20220324143139.png]]

### Zmiana stanów
- Stan - stabilny zestaw wartości atrybutów
- Przejście - zmiana stanu np. poprzez zdarzenie
- Pseudo stan początkowy - przejście do stanu po rozpoczęciu działania (bez zdarzenia)
- Pseudo stan terminalny - bezwarunkowe zakończenie całej aktywności

![[Pasted image 20220324143330.png]]

![[Pasted image 20220324143712.png]]

Koniec (kółko z kropką mniejszą) oznacza zakończenie tylko tej maszyny stanów, inne mogą nadal działać.

w nawiasach "\[...\]" umieszczone są warunki przejścia. 

### Stany złożone
![[Pasted image 20220324144053.png]]

Czerwony "żeton" oznacza aktualny stan.

Jeśli nastąpi np. zezłomowanie a jesteśmy w stanie wewnętreznym Użytkowanego to odrazu wychodzimy z niego.

#### Regiony
![[Pasted image 20220324144418.png]]

Są to równolegle wykonywane maszyny stanów.

#### Przykład
![[Pasted image 20220324144853.png]]

