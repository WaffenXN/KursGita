# **04 – Podstawowe operacje w Git**
W tym rozdziale nauczysz się przeglądać różnice między wersjami plików, poprawiać commity, usuwać pliki oraz ignorować niechciane pliki w repozytorium.

-----
## **Przeglądanie zmian**
Aby zobaczyć zmiany w plikach **przed** ich dodaniem do commita:

git diff

Aby zobaczyć zmiany w plikach, które **zostały już dodane** do staging area:

git diff --cached

-----
## **Modyfikowanie ostatniego commita**
Jeśli zapomniałeś czegoś dodać do ostatniego commita lub chcesz poprawić jego treść:

git add plik.ktory.zmieniles

git commit --amend

Uwaga: Nie należy używać --amend w commitach, które zostały już wypchnięte do zdalnego repozytorium!

-----
## **Usuwanie plików**
Aby usunąć plik z katalogu i z Git:

git rm nazwa\_pliku

Jeśli usunąłeś plik ręcznie (z poziomu systemu plików), użyj:

git rm nazwa\_pliku --cached

Uwaga: --cached usuwa plik tylko z Gita, nie z dysku.

-----
## **Przywracanie zmian**
Aby przywrócić zmiany w pliku (cofa zmiany niezapisane w commitach):

git restore nazwa\_pliku

Aby przywrócić plik do wersji ze staging area:

git restore --staged nazwa\_pliku

-----
## **Ignorowanie plików**
Niektóre pliki nie powinny być dodawane do repozytorium (np. pliki tymczasowe, buildy, klucze API). Do tego służy plik .gitignore.

Przykład .gitignore:

\# Ignoruj wszystkie pliki .log

\*.log

\# Ignoruj katalog build/

build/

\# Ignoruj plik z hasłami

.env

Stwórz plik .gitignore w katalogu głównym repozytorium i dodaj do niego odpowiednie wzorce.

-----
## **Podsumowanie**
W tym module nauczyłeś się:

- Przeglądać zmiany w plikach (git diff)
- Modyfikować ostatni commit (git commit --amend)
- Usuwać pliki z repozytorium (git rm)
- Przywracać zmiany (git restore)
- Ignorować pliki za pomocą .gitignore

W kolejnym module połączysz repozytorium lokalne z GitHubem i nauczysz się pracować z repozytorium zdalnym.
