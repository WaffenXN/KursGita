# **06 – Branchowanie i praca zespołowa**
W tym module nauczysz się, jak tworzyć i używać gałęzi (*branches*) w Git. Gałęzie pozwalają pracować nad różnymi funkcjonalnościami niezależnie od głównej wersji projektu. Dowiesz się też, jak scalać zmiany i rozwiązywać konflikty.

-----
## **Tworzenie nowej gałęzi**
git branch nazwa-galezi

Przykład:

git branch funkcja-logowania

-----
## **Przełączanie się między gałęziami**
git checkout nazwa-galezi

Połączenie tworzenia i przełączania:

git checkout -b funkcja-rejestracji

-----
## **Wyświetlanie wszystkich gałęzi**
git branch

Dodaj -a, aby zobaczyć także zdalne gałęzie:

git branch -a

-----
## **Scalanie gałęzi (merge)**
Aby scalić gałąź z aktualnie aktywną:

1. Przejdź na gałąź docelową (np. main):

   git checkout main

1. Wykonaj merge:

   git merge funkcja-logowania

-----
## **Rozwiązywanie konfliktów**
Podczas mergowania może dojść do konfliktów. Git oznaczy fragmenty plików, które wymagają Twojej interwencji.

Po ręcznym rozwiązaniu konfliktu:

git add nazwa\_pliku

git commit

-----
## **🛑 Anulowanie operacji scalania (merge)**
Jeśli chcesz wycofać się z nieudanego lub przerwanego merge'a, możesz anulować operację:

git merge --abort

To polecenie przywraca repozytorium do stanu sprzed rozpoczęcia scalania. Działa tylko wtedy, gdy proces scalania jest w toku (nie został jeszcze zakończony git commit).

-----
## **Usuwanie gałęzi**
Po scaleniu możesz usunąć gałąź lokalną:

git branch -d funkcja-logowania

Wymuszenie usunięcia:

git branch -D funkcja-logowania

-----
## **Porównywanie gałęzi**
Zobacz różnice między dwiema gałęziami:

git diff main..funkcja-logowania

-----
## **Gałęzie zdalne**
Pobierz wszystkie gałęzie z repozytorium zdalnego:

git fetch

Utwórz lokalną gałąź na podstawie zdalnej:

git checkout -b lokalna-nazwa origin/zdalna-nazwa

-----
## **Podsumowanie**
W tym module nauczyłeś się:

- Tworzyć, przełączać i usuwać gałęzie
- Scalać zmiany między gałęziami
- Rozwiązywać konflikty merge
- Anulować nieudane scalanie (git merge --abort)
- Pracować z gałęziami zdalnymi

W kolejnym module poznasz podstawy pull requestów i przegląd kodu na GitHubie.
