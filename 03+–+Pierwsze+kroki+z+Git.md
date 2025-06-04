# **03 – Pierwsze kroki z Git**
W tym rozdziale nauczysz się tworzyć nowe repozytorium Git, dodawać pliki do śledzenia, zapisywać zmiany (commitować) oraz przeglądać historię zmian.

-----
## **Tworzenie nowego repozytorium**
Aby rozpocząć pracę z Gitem, przejdź do katalogu projektu lub utwórz nowy:

mkdir moj-projekt

cd moj-projekt

git init

To polecenie utworzy ukryty katalog .git, w którym Git będzie przechowywał całą historię projektu. Od tej pory katalog jest repozytorium Git.

-----
## **Dodawanie plików do śledzenia**
Utwórz nowy plik, np.:

echo "# Mój pierwszy projekt" > README.md

Sprawdź status repozytorium:

git status

Dodaj plik do tzw. „staging area” (obszaru przygotowania do zapisu):

git add README.md

Dodanie wszystkich plików:

git add .

-----
## **Zapisywanie zmian – commit**
Commit to trwałe zapisanie aktualnego stanu śledzonych plików.

git commit -m "Dodano plik README"

Każdy commit powinien mieć czytelny i zwięzły opis (komunikat).

-----
## **Przeglądanie historii commitów**
Zobacz pełną historię commitów:

git log

Skrócona wersja (tylko skrócone hashe i opisy):

git log --oneline

-----
## **Sprawdzanie statusu repozytorium**
git status

To polecenie pokazuje, które pliki zostały zmodyfikowane, dodane, usunięte lub nie są jeszcze śledzone przez Git.

-----
## **Podsumowanie**
Do tej pory nauczyłeś się:

- Tworzyć lokalne repozytorium
- Dodawać pliki do śledzenia
- Wykonywać commity
- Przeglądać historię commitów
- Sprawdzać aktualny stan repozytorium

W kolejnym module nauczysz się przeglądać zmiany, modyfikować commity i korzystać z .gitignore.
