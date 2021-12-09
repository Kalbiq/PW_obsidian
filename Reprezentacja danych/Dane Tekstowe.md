### Opis
- większość danych jest w postaci tekstu
- łatwe do gromadzenia

#### Niestrukturyzowana
- tekst bez znaków formatujących (np. pogrubienie, kursywa, akapit, tab)
- czysty ciąg znaków

#### Częściowo ustrukturyzowana
- np. email
	- ma nagłówek który jest jakąś informacją dla aplikacji mailowej
	- ma treść którą my mamy zobaczyć
- część jest formatowana, ale zawiera też fragmenty bez formatu

#### Ustrukturyzowana
- cały dokument ma znaczniki formatujące
- np. HTML, JSON, TOML, XML 
- jest uporządkowany

### Postacie
#### Tekst prosty
- ciąg znaków zgodny z regułami gramatyki, składni itd.
- wykorzystuje znaki zgodne z przyjętym systemem (np. UTF-8)
- różne formy słów: koniugacje, deklinacje itp.

#### Segmentacji / tkenizacja
- przetwarzanei sekwencji znaków w sekwencję tokenów
- token - elementarna część zdania
- prosta tokenizacja to podział zdania na wyrazy
- bardziej zaawansowane metody mogą dzielić słowo na kilka tokenów
- trochę jak tokenizacja w kompilatorze

#### Steming i lematyzacja
- wyciągnięcie rdzenia słowa
- "potop", "potop-ić", "przed-potop-owy"
- usówanie prefiksów i sufiksów
- lematyzacja (hasłowanie) - sprowadzenie słowa do formy podstawowej
- stosowanie modeli języka w celu znalezienia forma podstawowych
- słowinki morfologiczne
	- wszystkie formy dla danego słowa
	- tworzony przez językoznawców i informatyków
	- istotny w przypadku języków fleksyjnych
	- dla danego słowa zwracają jego możliwe interpretacje morfologiczne

#### Reprezentacja dokument-słowo (TDM)
- wktorowa / macierzowa
- słownik słów w alalizowanych dokumentach
- wektor dla dokumentu zawiera liczbę wystąpień poszczególnego słowa
- macierz dla większej ilości dokumentów
	- wiersze - słowa
	- kolumny - dokumenty
	- elementy - liczba wystąpień
- utrata informacji o strukturze zdania!

#### n-gramy
- zbitiki wyrazowe

![[Pasted image 20211209111649.png]]

### Reprezentacja tekstu
- powinna umożliwiać:
	- prawidłowe zrozumienie tekstu (zachowuje zawartość semantyczną)
	- określenie stopnia podobieństwa
- ścisłe odwzorowanie semantyki
- w zadanich eksploracji dopuszcza się niekoniecznie precyzyjne odwzorowanie semantyki

### Zadania
#### wyszukiwanie informacji
- na podstawie słów kluczowych
	- problemy: odmiana, synonimy
	- rozwiązania: dodatkowe zbiory słów kluczowych, warianty, inne odmiany
- na podstawie innych dokumentów
	- konieczne jest znanie miary podobieństwa
	- zdanie-po-zdaniu, słowo-po-słowie tylko w specyficznych przypadkach bo czasem ten sam sens można wyrazić innym szykiem zdania (np. chcemy znaleźć plagiat)
	- metoda worka słów
		- sprawdzamy czy pewne słowa występują w obydwu zdaniach => może być podobieństwo
- na podstawie pożądanych cech (np. poziom emocji)
	- cechy danych wyrazów (zły, głupi vs. dobry, mądry)
	- badamy poziom nasycenia daną cechą
	- poszukujemy dokumentów o odpowiednim poziomie nasycenia

#### porównywanie dokumentów
#### klasyfikacja tekstu
#### transformacja tekstu (np. tłumaczenia)
#### przetwarzanie języka naturalnego
- analiza i modelowanie składni
- rozumienie i tłumaczenie
- generowanie wypowiedzi
- wykracza poza prostą nalizę tekstu - wymaga wiedzy o temacie wypowiedzi i świecie zewnętrznym

### Operacje na tekstach
#### Wyszukiwanie ciągu znaków
- wyszukiwanie podciągu w większym ciągu
- wyszukanie słowa w zdaniu lub dokumencie
- metody przykładowe:
	- brute force
	- algorytm Boyera-Moora

#### Wyszukiwanie tekstowe
- dokument jest traktowany jako zbiór słów kluczowych
- często stosowanie do wyszukiwania danych nietekstowych w oparciu o metadane np. wideo po ich opisie
- problemy:
	- odmiana
	- synonimy
	- polisemia - różne znaczenia słowa w zależności od kontekstu
- rozwiązania:
	- odmiana -> lematyzacja
	- synanim, polisemia -> słownik

#### Miara tf-idf
![[Pasted image 20211209112500.png]]

#### Podobieństwo dokumentów
- reprezentacja wektorowa TDm
- dokumenty podobne powinny mieć podobne częstości wystąpień słów kluczowych
- maiara kosinusowa
	- kosinus kąta między dwoma wektorami opisującymi dokumenty
	- ![[Pasted image 20211209113047.png]]

#### Miary oceny wyszukiwania
![[Pasted image 20211209113319.png]]
![[Pasted image 20211209113259.png]]

### Uczenie maszynowe a dane tekstowe
- wyszukiwanie
	- na podstawie dokumentów referencyjnych
	- na podstawie słów kluczowych
- klasyfikacja
- grupowanie
- rankingi
- odkrywanie wzajemnych zależności

### Grupowanie i klasyfikacja
- mając miarę podobieństwa możemy stosować techniki eksploracji danych

#### Klasyfikacja w analizie tekstu
- statystyki występowania słów
- 
##### filtry antyspamowe
- rozpoznaje wzorce powiązane ze spamem
- kategorie: spam, niespam
- np. Bayesowski filtr antyspamowy
	- różne słowa występują z różną częśtotliwością w normalnych i spoamowych wiadomościach
	- trzeba ręcznie nauczyć klasyfikator
	- ![[Pasted image 20211209113800.png]]
	- zalety:
		- wysoka skuteczxność przy klasycznym spamie
		- uczy się na bieżąco
		- dopasowany do uzytkownika
	- wady:
		- podatność na "zatrucie Bayesowskie" - spamerzy wysyłają wiadomości z dużą ilością normalnego tekstu co osłabia filtr
		- podatność na różnice zapisu

##### analiza sentymentu
- ocena wydźwięku tyekstu
- np. można ocenić jak zadowolony jest użytkownik po recenzji

### Ranking i analiza zależności
#### Algorytm Page Rank
- ocena istotnosci stron internetowych
- opracowany przez L. Page'a (jednego z założycieli Google)
- problem wyszukiwarek - wybiera strony w kolejności według zgodności z wyszukiwanie, najpierw bardziej istotne
- przegląda strony i ocenia przydatność
- ![[Pasted image 20211209114310.png]]
- o popularności strony decyduje po części ilość linków do tej strony

##### Zasada działania
- ile stron linkuje do naszej strony
- jakie rankingi mają linkujące strony
- algorytm jest iteracyjny oraz zbieżny

![[Pasted image 20211209114422.png]]
![[Pasted image 20211209114651.png]]
![[Pasted image 20211209114732.png]]
![[Pasted image 20211209114832.png]]
![[Pasted image 20211209114847.png]]