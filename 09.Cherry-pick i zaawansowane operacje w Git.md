# **09 – Cherry-pick i zaawansowane operacje w Git**
W tym module poznasz bardziej zaawansowane techniki pracy z historią commitów, takie jak cherry-pick, interaktywny rebase, tagowanie i inne operacje wykorzystywane w codziennej pracy profesjonalnych zespołów developerskich.

-----
## **🍒 git cherry-pick**
git cherry-pick pozwala **przenieść pojedynczy commit** z jednej gałęzi do drugiej, bez scalania całej historii.
### **Przykład:**
1. Przejdź na gałąź docelową:

   git checkout main

1. Wybierz commit do przeniesienia:

   git cherry-pick <hash\_commita>

To narzędzie jest przydatne, gdy np. chcesz wprowadzić poprawkę z develop do main, ale nie cały zestaw zmian.

-----
## **🧠 Rebase interaktywny (git rebase -i)**
Służy do porządkowania historii commitów (np. łączenia, zmieniania kolejności, edytowania wiadomości).

git rebase -i HEAD~3

Pojawi się lista ostatnich commitów. Możesz je:

- pick – zostawić bez zmian
- reword – zmienić wiadomość
- edit – edytować zawartość commita
- squash – połączyć kilka commitów w jeden

📌 Używaj tego tylko w lokalnej historii – **nie rebase'uj commitów, które zostały już wypchnięte do zdalnego repozytorium!**

-----
## **🏷️ Tagowanie commitów**
Tagi to "znaczniki" przypisane do commitów – zwykle używane do oznaczania wersji (np. v1.0.0).
### **Tworzenie taga:**
git tag v1.0.0
### **Tag z opisem:**
git tag -a v1.0.0 -m "Pierwsza wersja stabilna"
### **Wysyłanie tagów do zdalnego repozytorium:**
git push origin v1.0.0

lub wszystkich tagów:

git push origin --tags

-----
## **📦 Stash – tymczasowe zapisywanie zmian**
git stash pozwala tymczasowo zapisać zmiany bez commitowania – przydatne, gdy musisz szybko przełączyć się na inną gałąź.
### **Zapisanie zmian:**
git stash
### **Wyświetlenie listy:**
git stash list
### **Przywrócenie ostatniego stasha:**
git stash pop

-----
## **🧹 Czyszczenie nieśledzonych plików**
Aby usunąć wszystkie nieśledzone pliki z katalogu roboczego:

git clean -f

Uwaga – ta operacja jest nieodwracalna!

-----
## **📌 git bisect – znajdowanie błędu**
Pomaga znaleźć commit, który wprowadził błąd. Git automatycznie testuje commity w połowie zakresu, aż znajdzie problematyczny.
### **Przykład użycia:**
git bisect start

git bisect bad # obecny (zły) commit

git bisect good <hash\_dobrego\_commita>

Git będzie prosił o oznaczanie kolejnych commitów jako good/bad, aż zawęzi zakres.

-----
## **Podsumowanie**
W tym module nauczyłeś się:

- Przenosić pojedyncze commity między gałęziami (cherry-pick)
- Porządkować historię (rebase -i)
- Tworzyć i wypychać tagi
- Tymczasowo zapisywać zmiany (stash)
- Używać bisect do szukania błędów

To potężne narzędzia Git – warto je znać, by jeszcze efektywniej pracować z historią kodu.
