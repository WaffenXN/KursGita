# **Bonus 2 – GitFlow: struktura pracy z Git w zespołach**
GitFlow to popularna konwencja zarządzania gałęziami w projektach Git. Ułatwia organizację pracy zespołowej, wersjonowanie i publikowanie kodu.

-----
## **🗺️ Główna idea GitFlow**
GitFlow opiera się na podziale pracy na gałęzie o określonych rolach:

- **main** – stabilna wersja produkcyjna
- **develop** – bieżąca wersja rozwojowa
- **feature/** – nowe funkcjonalności
- **release/** – przygotowanie do wydania
- **hotfix/** – szybkie poprawki dla produkcji
-----
## **🌱 Gałęzie w GitFlow**

|**Gałąź**|**Przeznaczenie**|
| :-: | :-: |
|main|zawiera tylko kod, który został wydany na produkcję|
|develop|główna gałąź do integracji nowych funkcji|
|feature/nazwa|rozwijanie nowej funkcjonalności|
|release/x.y.z|przygotowanie wersji do wydania|
|hotfix/x.y.z|poprawki błędów w main|
|bugfix/nazwa|poprawka buga/błędu|

-----
## **🔁 Przykładowy cykl pracy w GitFlow**
1. **Start feature**:

   git checkout develop

   git checkout -b feature/logowanie

1. **Po zakończeniu funkcji**:

   git checkout develop

   git merge feature/logowanie

   git branch -d feature/logowanie

1. **Przygotowanie wydania**:

   git checkout develop

   git checkout -b release/1.0.0

1. **Wydanie i powrót zmian**:

   git checkout main

   git merge release/1.0.0

   git tag -a v1.0.0 -m "Wersja 1.0.0"

   git checkout develop

   git merge release/1.0.0

   git branch -d release/1.0.0

1. **Hotfix**:

   git checkout main

   git checkout -b hotfix/1.0.1

   Po poprawce:

   git commit -am "Poprawka krytycznego błędu"

   git checkout main

   git merge hotfix/1.0.1

   git tag -a v1.0.1 -m "Hotfix 1.0.1"

   git checkout develop

   git merge hotfix/1.0.1

   git branch -d hotfix/1.0.1

-----
## **🛠️ Narzędzia wspierające GitFlow**
Możesz zainstalować rozszerzenie do Gita:

brew install git-flow

Lub używać wbudowanych konwencji w narzędziach typu GitKraken, SourceTree, czy IntelliJ.

-----
## **✅ Zalety GitFlow**
- Jasna struktura pracy
- Oddzielenie faz rozwoju, testów i wdrożenia
- Ułatwia planowanie wersji i zarządzanie błędami
-----
## **⚠️ Wady GitFlow**
- Może być zbyt rozbudowany dla małych zespołów
- Wymaga dyscypliny w nazwach i porządku scalania
- Współpraca przez PR może być bardziej elastyczna niż „czysty” GitFlow
-----
## **📘 Ściągawka GitFlow**
Polecamy oficjalną ściągawkę (po polsku):\
👉 <https://danielkummer.github.io/git-flow-cheatsheet/index.pl_PL.html>

-----
## **Podsumowanie**
GitFlow to sprawdzony sposób organizacji pracy zespołowej z Git. Jeśli pracujesz nad większym projektem lub z zespołem – warto znać ten model i stosować go (lub jego uproszczoną wersję).
