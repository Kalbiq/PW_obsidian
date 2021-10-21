### Schematy
![[Pasted image 20211014122253.png]]
![[Pasted image 20211014122312.png]]
![[uklad_sterowania.png]]

### Rodzaje architektury
#### Harvardzka
- bardziej skomplikowana
- przeciętnie [[Assembler|assembler]] ma 100+ instrukcji
- ![[architektura_harvardzka.png]]
- ![[mod_architektura_harvardzka.png]]
- rozdzielona szyna danych i rozkazów
- pamięć programów i danych może mieć różne długości słowa
- konieczność stosowania różnych rozkazów dla pamięci programów i danych
- pokrywające się adresy [[Pamięć stała|ROM]] i [[Pamięć o dostępie swobodnym|RAM]]
- zmodyfikowana wersja ma oddzielne pola adresowe ale muszą one mieć tą samą długość słowa

#### Von Neumanna
- przeciętnie [[Assembler|assembler]] ma poniżej 100 instrukcji
- ![[architektura_neumanna.png]]
- jednolita przestrzeń adresowa
- umowny podział na pamięć programu, danych
- wspólna szyna umożliwia dostęp do pamięci przez te same tryby adresowania

#### CISC (Complex Instruction Set Computers)
- występują złożone operacje wymagające kilku cykli procesora
- długa lista rozkazów
- dużo trybów adresowania
- wady:
	- długa lista rozkazó, niewszystkie są często używane
	- dużo czasu na przepisanie z pamięci do rejestrów i na odwrót

#### RISC (Reduced Instruction Set Computers)
- zredukowana liczba rozkazów do minimum
- mniej trybów adresowania, dzięki czemu kody rozkazów są prostsze, bardziej zunifikowane
- np. MSP430 ma tylko 27 instrukcji

### Przestrzeń adresowa
- zbiór wszystkich adresów które procesor może wygenerować na szynie
- mapa pamięci - adresy przestrzeni przyporządkowane do urządzeń fizycznych
- ![[mapa_pamieci_harvard.png]]
- ![[mapa_pamieci_neumann.png]]