# **07 – Pull requesty i przegląd kodu (GitHub)**
W tym module poznasz, czym są pull requesty (PR), jak je tworzyć i przeglądać na GitHubie oraz jak wygląda proces recenzji i scalania zmian w pracy zespołowej.

-----
## **Co to jest pull request?**
**Pull request** (PR) to prośba o włączenie zmian z jednej gałęzi do innej (najczęściej z gałęzi funkcjonalnej do main lub develop).

Jest to podstawowy element współpracy na GitHubie – umożliwia recenzję kodu, komentowanie i kontrolę jakości przed scaleniem.

-----
## **Tworzenie pull requesta**
1. Wypchnij swoją gałąź na GitHub:

   git push origin nazwa-galezi

1. Wejdź na stronę repozytorium na GitHubie – pojawi się przycisk **"Compare & pull request"**.
1. Kliknij, uzupełnij tytuł i opis zmian.
1. Zatwierdź przyciskiem **"Create pull request"**.
-----
## **Recenzowanie i komentowanie zmian**
W ramach PR:

- Możesz przeglądać zmiany plik po pliku.
- Zostawiać komentarze do konkretnych fragmentów kodu.
- Zaznaczać sugestie lub zadawać pytania.
- Zatwierdzać PR lub zgłaszać potrzebę poprawek.
-----
## **Scalanie pull requesta**
Jeśli PR został zatwierdzony:

1. Kliknij przycisk **"Merge pull request"**.
1. Wybierz metodę scalenia (merge commit, squash, rebase).
1. Po scaleniu możesz usunąć gałąź.
-----
## **Statusy i integracje**
GitHub PR może być powiązany z:

- Testami automatycznymi (CI/CD)
- Wymaganymi recenzjami
- Zablokowaniem scalania bez akceptacji

To wszystko zwiększa jakość i bezpieczeństwo kodu.

-----
## **Dobre praktyki przy PR**
- Rób PR-y z małej liczby commitów – łatwiej je recenzować
- Nazywaj gałęzie czytelnie, np. feature/logowanie
- Pisząc opis PR – wyjaśnij *co* i *dlaczego* zmieniasz
- Odpowiadaj na komentarze recenzentów
-----
## **Podsumowanie**
W tym module nauczyłeś się:

- Czym jest pull request i do czego służy
- Jak go utworzyć i przeglądać na GitHubie
- Jak wygląda recenzja i scalanie kodu
- Jakie są dobre praktyki przy pracy zespołowej z PR-ami

W kolejnym module dowiesz się, jak cofać zmiany i rozwiązywać typowe problemy w Git.
