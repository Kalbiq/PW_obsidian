## Właściwości
- drzewo binarne
- własność relacji
- składa się z węzłów
	- kazdy węzeł ma relacje parent - child
	- ma 2 dzieci (np. right, left)

## Implementacja
##### Java:
```Java
public class Node {
	Object data; 	// jakieś dane przechowywane w węźle
	Node left; 		// dziecko 1
	Node right; 	// dziecko 2
	...
}

public class BTree {
	Node root; 		// korzeń drzewa binarnego
	...
}
```

##### Rust:
```Rust
struct Node<T> {
	left: Node<T>,	// dziecko 1
	right: Node<T>,	// dziecko 2
	data: <T>		// jakieś dane przechowywane
}

struct BTree<T> {
	root: Node<T>,	// korzeń drzewa binarnego
}
```

## Szukanie po drzewie
Używa się do tego *Binary Search Tree* w, którym zachodzi relacja `left < parent < right` lub na odwrót `left > parent > right`

```
			10
		   /  \
		  7    15
		 / \   / \
		3   9 12  22
```

### Dodawanie elementów
Trzeba używając tego drzewa poszukać miejsca dla nowego elementu.

### Liczenie idexów
Rodzic, Lewy, Prawy, Dziecko

R = 1
L = R * 2 + 1
P = R * 2 + 2

R = (D - 1)/2

## Kopiec maksymalny
```
			6
		   /  \
		  6    5
		 / \   / \
		4   5   
```

Wstawiamy na pierwsze wolne miejsce

!!Rysunki na kartkach (kształt kopca)

