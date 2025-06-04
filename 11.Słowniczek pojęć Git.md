# **11 – Słowniczek pojęć Git**
Ten moduł zawiera wyjaśnienie najważniejszych pojęć używanych w kursie. Warto wracać do tego słowniczka w razie wątpliwości.

-----
## **📂 Repository (repozytorium)**
Zbiór plików zarządzany przez Git. Może być **lokalne** (na Twoim komputerze) lub **zdalne** (np. na GitHubie).

-----
## **🔄 Commit**
Zapisanie stanu plików w repozytorium. Commit zawiera:

- informacje o autorze,
- datę,
- unikalny identyfikator (hash),
- opis zmian.
-----
## **📝 Commit message**
Krótki opis w commicie, który wyjaśnia, jakie zmiany zostały wprowadzone.

-----
## **🧪 Staging area (obszar roboczy / indeks)**
Tymczasowe miejsce, w którym umieszczasz pliki przed wykonaniem commita. Umożliwia selektywne zapisywanie zmian.

-----
## **➕ git add**
Dodaje pliki do staging area.

-----
## **🧾 git commit**
Tworzy commit z plików znajdujących się w staging area.

-----
## **📥 git pull**
Pobiera zmiany ze zdalnego repozytorium i scala je z lokalnym.

-----
## **📤 git push**
Wysyła lokalne commity do repozytorium zdalnego.

-----
## **🌿 Branch (gałąź)**
Równoległa wersja projektu. Gałęzie pozwalają pracować nad różnymi funkcjami niezależnie. Główna gałąź to zazwyczaj main lub master.

-----
## **🔀 Merge**
Scalanie zmian z jednej gałęzi do drugiej.

-----
## **⚔️ Merge conflict**
Konflikt, który powstaje, gdy te same fragmenty kodu zostały zmienione w różnych gałęziach i Git nie wie, którą wersję wybrać.

-----
## **🧠 Rebase**
Przenosi (reaplikuje) commity na nową bazę. Umożliwia zachowanie liniowej historii. Wymaga ostrożności w projektach zespołowych.

-----
## **🧰 Interaktywny rebase (rebase -i)**
Tryb rebase, który pozwala łączyć, edytować, usuwać i zmieniać kolejność commitów.

-----
## **✂️ Autosquash**
Automatyczne połączenie commitów typu --squash lub --fixup podczas git rebase -i --autosquash.

-----
## **🍒 Cherry-pick**
Przenosi wybrany commit z jednej gałęzi do drugiej bez scalania całej historii. Użyteczny przy selektywnym kopiowaniu zmian.

-----
## **📦 Stash**
Tymczasowe zapisanie zmian, które nie są gotowe do commita. Pozwala wrócić do nich później.

-----
## **🧹 git clean**
Usuwa nieśledzone pliki i katalogi z katalogu roboczego.

-----
## **🔍 git diff**
Pokazuje różnice między wersjami plików lub commitami.

-----
## **🧾 .gitignore**
Plik zawierający listę wzorców plików i katalogów, które Git ma ignorować (np. pliki tymczasowe, node\_modules, .env).

-----
## **🧠 git reflog**
Pokazuje historię wszystkich działań Git – również tych, które nie są już widoczne w git log. Umożliwia odzyskiwanie commitów.

-----
## **🧯 git reset**
Cofa zmiany lub usuwa commity z historii. Może działać w trzech trybach:

- --soft: zachowuje staging,
- --mixed: czyści staging, ale nie pliki,
- --hard: usuwa wszystko – ostrożnie!
-----
## **⏪ git revert**
Tworzy nowy commit, który odwraca działanie wskazanego commita. Nie usuwa historii – bezpieczny w pracy zespołowej.

-----
## **🔗 Remote**
Zdalne repozytorium, np. na GitHubie, z którym możesz synchronizować zmiany.

-----
## **🔄 Pull Request (PR)**
Wniosek o scalenie gałęzi – tworzony na GitHubie. Umożliwia przegląd, komentarze i zatwierdzenie zmian przed ich połączeniem.

-----
## **📊 git bisect**
Narzędzie do znajdowania problematycznego commita – Git przeprowadza "binarne przeszukiwanie" historii.

-----
## **✅ CI/CD**
Automatyzacja testów i wdrożeń. Często zintegrowana z pull requestami, aby upewnić się, że zmiany nie psują projektu.

-----
Ten słowniczek możesz poszerzać o własne terminy i przykłady. To dobry punkt odniesienia podczas pracy z Gitem.
