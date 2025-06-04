# **08 – Częste problemy i cofanie zmian**
W tym module nauczysz się, jak cofać zmiany w Git, przywracać poprzednie wersje plików oraz radzić sobie z typowymi błędami, które mogą wystąpić podczas pracy z repozytorium.

-----
## **Cofanie commitów**
### **git reset – zmiana historii lokalnej**
Cofa ostatni commit, zachowując zmiany w plikach roboczych:

git reset --soft HEAD~1

Cofa commit i usuwa zmiany ze staging area:

git reset --mixed HEAD~1

Cofa commit i usuwa wszystkie zmiany:

git reset --hard HEAD~1

📌 Uwaga: reset jest ryzykowny — zmiany mogą zostać bezpowrotnie usunięte!

-----
## **Odwracanie commitów**
Jeśli commit został już wysłany do zdalnego repozytorium, użyj git revert:

git revert <hash\_commita>

Tworzy nowy commit, który odwraca skutki wskazanego commita — bez zmiany historii.

-----
## **Reflog – historia wszystkiego**
Jeśli coś poszło źle, a commit „zniknął”, sprawdź reflog:

git reflog

Zobaczysz listę wszystkich ostatnich działań (checkouty, commity, resety itd.). Możesz odzyskać utracony commit:

git checkout <hash\_z\_refloga>

-----
## **Usuwanie zmian w plikach**
Cofnij zmiany w pliku (niezapisane w commitach):

git restore nazwa\_pliku

Cofnij zmiany już dodane do staging area:

git restore --staged nazwa\_pliku

-----
## **Konflikty przy git pull lub merge**
Jeśli pojawi się konflikt:

1. Git zaznaczy problematyczne fragmenty w plikach (np. <<<<<<<, =======, >>>>>>>)
1. Ręcznie wybierz poprawną wersję
1. Zapisz plik i wykonaj:

git add nazwa\_pliku

git commit

-----
## **Typowe błędy i ich rozwiązania**
### **1. Błąd przy pushu: *non-fast-forward***
git pull --rebase

git push
### **2. Błąd: *detached HEAD***
Nie pracuj bezpośrednio na commitach – utwórz gałąź:

git checkout -b nowa-galaz

-----
## **Podsumowanie**
W tym module nauczyłeś się:

- Różnicy między reset i revert
- Jak korzystać z reflog do odzyskiwania zmian
- Jak rozwiązywać konflikty merge
- Jak naprawiać typowe błędy push/pull

W kolejnym module dowiesz się, jak pisać dobre commity i stosować dobre praktyki w pracy z Gitem.
