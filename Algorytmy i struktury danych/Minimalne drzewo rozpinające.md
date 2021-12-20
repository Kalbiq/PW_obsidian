### Opis
Mając graf ważony, nieskierowany, spójny.

Chcemy stworzyć graf z najmniejszym kosztem ścieżek zachowując spójność.

### Postępowanie
1. Wybieramy dowolny węzeł (A)
2. Budujemy kolejkę priorytetową zawierającą połączenia
3. Wstawiamy A - A o koszcie 0 do kolejki
4. Wyjmujemy z kolejki obiekt o najniższym koszcie
5. Ten węzeł należy teraz do drzewa rozpinającego
6. Wkładamy teraz wszystkie połączenia z A
7. Idziemy do węzła z najmniejszym kosztem i wyjmujemy z kolejki
8. Dodajemy ten węzeł do drzewa rozpinającego
9. Wkładamy połączenia z węzłami jeszcze nie należacymi do drzewa rozpinającego
10. Powtarzamy takie wyjmowanie i wkładanie aż nie będzie więcej możliwości

#todo na kartce do przerysowania