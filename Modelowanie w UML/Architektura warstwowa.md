### Opis
Górna warstwa - frontend, prezentuje dane
Dolna warstwa - backend, przetwarza dane

### Wielowarstwowość
- każda warstwa komunikuje się tylko z jedną niżej lub wyżej
- górne warstwy są szybko zmienne
- dolne warstwy zmieniają się woniej i wraz z technologią
- warstwy środkowe zmieniają się wraz z wymaganiami funkcjonalności problemu

### Rodzaje warstw
- Prezentacja i Adaptacja - odbiera dane od użytkownika lub innego systemu lub też je podaje
- Logika Aplikacji - odpowiada za funkcjonalność
- Logika Dziedziny - przetwarzanie informacji i danych
- Dane - implementuje już bazę danych lub inny taki system

### Interfejsy w kodzie
![[Pasted image 20220317144747.png]]

notacja alternatywna ma kółko przy nazwie interfejsu

### Wzorzec MVP
#### Model:
- reprezentuje i przetwarza dane

#### Widok:
- przekazuje zdarzenia do Prezentera
- przezentuje dane
- reaguje na polecenia Prezentera

#### Prezenter:
- steruje interakcjami z uzytkownikiem
- obsługuje zdarzenia z Widoku
- przesyła do modelu prośby o wykonanie usług
- przesyła do widoku prosby o wyświetlenie danych
- może obsługiwać kilka widoków

### Relacje zależności
Po stronie grota jest dostawca a klient po stronie bez

![[Pasted image 20220317145023.png]]

### Przykład
#### Model MVP
![[Pasted image 20220317143012.png]]

#### Przykładowy widok
![[Pasted image 20220317151958.png]]

#### Przykładowy prezenter
![[Pasted image 20220317152242.png]]

#### Przykładowy model
![[Pasted image 20220317152447.png]]

