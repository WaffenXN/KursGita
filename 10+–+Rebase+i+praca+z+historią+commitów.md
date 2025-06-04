# **10 – Rebase i praca z historią commitów**
W tym module nauczysz się, jak korzystać z git rebase, aby porządkować historię commitów, synchronizować gałęzie i upraszczać log zmian. Poznasz też techniki takie jak rebase interaktywny i autosquash.

-----
## **Co to jest git rebase?**
rebase przenosi jedną serię commitów na inny punkt w historii. Zamiast łączyć zmiany (merge), rebase przepina je na nową bazę, tworząc liniową historię.

-----
## **Rebase w praktyce**
### **Rebase feature do main**
1. Przejdź na gałąź, którą chcesz zaktualizować:

git checkout feature

2. Zrób rebase względem main:

git rebase main

Git "przeniesie" commity z feature na koniec main.

-----
## **Interaktywny rebase (git rebase -i)**
Pozwala na edycję, łączenie, usuwanie i zmianę kolejności commitów.

git rebase -i HEAD~3

Opcje:

- pick – pozostaw commit
- reword – edytuj opis commita
- edit – przerwij rebase, by zmodyfikować commit
- squash – połącz z poprzednim commit
- fixup – połącz z poprzednim commit bez opisu
-----
## **Autosquash**
Przydatne do łączenia poprawek (fixup/squash) ze starszymi commitami.

1. Dodaj --fixup do commita:

git commit --fixup=<hash\_celu>

2. Wykonaj interaktywny rebase z opcją autosquash:

git rebase -i --autosquash HEAD~n

Git automatycznie ustawi fixup/squash przy odpowiednich commitach.

-----
## **Rebase a merge – różnice**

|**Cecha**|**merge**|**rebase**|
| :-: | :-: | :-: |
|Historia|Drzewiasta|Liniowa|
|Konflikty|Przy łączeniu gałęzi|Podczas rebase|
|Zachowanie hashy|Nie zmienia commitów|Tworzy nowe commity|
|Praca zespołowa|Bezpieczna|Niebezpieczny dla publicznych commitów|

-----
## **Przerywanie i cofanie rebase**
Przerwij rebase w dowolnym momencie:

git rebase --abort

Jeśli chcesz kontynuować po rozwiązaniu konfliktów:

git rebase --continue

-----
## **Rebase z --onto**
Zaawansowana forma rebase — przenosi commity między trzema punktami.

git rebase --onto nowa-baza stara-baza gałąź

Przykład:

git rebase --onto main feature-start feature

Przenosi commity od feature-start do końca feature na main.

-----
## **Kiedy (nie) używać rebase**
✅ Używaj rebase, gdy:

- chcesz uporządkować lokalną historię przed wysłaniem
- scalasz często z main i chcesz uniknąć commitów merge

❌ Nie używaj rebase na publicznych commitach (takich, które ktoś inny już pobrał).

-----
## **Podsumowanie**
W tym module nauczyłeś się:

- Używać git rebase do przenoszenia historii
- Porządkować commity dzięki rebase -i
- Wykorzystywać --autosquash do czystych historii
- Rozumieć różnicę między rebase i merge

W kolejnym module poznasz techniki cherry-pick, stash, bisect i inne narzędzia do zaawansowanej pracy z Git.
