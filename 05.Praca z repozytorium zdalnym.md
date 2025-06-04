# **05 – Praca z repozytorium zdalnym**
W tym rozdziale nauczysz się, jak połączyć swoje lokalne repozytorium z repozytorium zdalnym, wysyłać i pobierać zmiany oraz klonować istniejące projekty.

-----
## **Tworzenie konta na GitHubie**
1. Wejdź na: [https://github.com](https://github.com/)
1. Zarejestruj się i utwórz konto
1. Po zalogowaniu możesz tworzyć nowe repozytoria zdalne
-----
## **Tworzenie nowego repozytorium na GitHubie**
1. Kliknij przycisk **"New repository"**
1. Podaj nazwę repozytorium, opcjonalnie opis
1. Zaznacz opcję "Public" lub "Private"
1. Nie zaznaczaj opcji „Initialize this repository with a README” jeśli masz już lokalne repo

Po utworzeniu repozytorium, GitHub pokaże Ci link do repozytorium, np.:

https://github.com/twoja-nazwa/moj-projekt.git

-----
## **Łączenie lokalnego repozytorium z GitHubem**
W terminalu:

git remote add origin https://github.com/twoja-nazwa/moj-projekt.git

Następnie wypchnij zmiany:

git push -u origin master

lub jeśli używasz main jako głównej gałęzi:

git push -u origin main

-----
## **Wysyłanie zmian (push)**
Aby wypchnąć nowe commity do zdalnego repozytorium:

git push

-----
## **Pobieranie zmian (pull)**
Aby pobrać i automatycznie zaktualizować lokalną kopię:

git pull

-----
## **Klonowanie istniejącego repozytorium**
Jeśli chcesz pobrać repozytorium z GitHuba:

git clone https://github.com/uzytkownik/projekt.git

Git utworzy lokalny katalog z nazwą repozytorium i automatycznie skonfiguruje zdalne połączenie origin.

-----
## **Sprawdzanie repozytoriów zdalnych**
git remote -v

To pokaże aktualne zdalne repozytoria, z którymi masz połączenie.

-----
## **Podsumowanie**
W tym module nauczyłeś się:

- Jak założyć konto i repozytorium na GitHubie
- Jak połączyć lokalne repozytorium zdalnym
- Jak wypychać i pobierać zmiany
- Jak klonować inne repozytoria

W następnym module poznasz tworzenie gałęzi i pracę zespołową w Git.
