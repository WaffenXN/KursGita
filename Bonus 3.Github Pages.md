
# Jak korzystać z GitHub Pages — krok po kroku

## Krok 1 — Załóż konto na GitHub (jeśli jeszcze nie masz)

1. Wejdź na: [https://github.com](https://github.com)
2. Kliknij **Sign up** i załóż darmowe konto.

## Krok 2 — Utwórz nowe repozytorium

1. Po zalogowaniu kliknij w prawym górnym rogu przycisk **+** -> **New repository**.
2. Wpisz nazwę repozytorium, np. `mojastrona`.
3. (Opcjonalnie) Możesz zaznaczyć checkbox **Add a README file** — łatwiej będzie zacząć.
4. Kliknij **Create repository**.

## Krok 3 — Przygotuj pliki do publikacji

1. Przygotuj plik `index.html` — to będzie strona startowa.
2. Jeśli nie masz lokalnie, możesz dodać plik bezpośrednio w przeglądarce przez GitHub:
   - Wejdź w swoje repozytorium.
   - Kliknij **Add file** -> **Create new file**.
   - Wpisz `index.html`.
   - Dodaj prosty kod HTML, np.:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Moja strona na GitHub Pages</title>
</head>
<body>
    <h1>Witaj na mojej stronie!</h1>
    <p>Strona działa na GitHub Pages 🚀</p>
</body>
</html>
```

3. Kliknij **Commit changes**.

## Krok 4 — Włącz GitHub Pages

1. Wejdź w ustawienia repozytorium: **Settings**.
2. Po lewej stronie znajdź zakładkę **Pages** (czasem jest pod **Code and automation -> Pages**).
3. W sekcji **Build and deployment**:
   - Wybierz **Deploy from a branch**.
   - Wybierz branch, np. `main`.
   - Wybierz folder: `/(root)` (czyli katalog główny).
4. Kliknij **Save**.

## Krok 5 — Gotowe! Twoja strona działa

- Po kilku sekundach GitHub wygeneruje link do Twojej strony. Będzie wyglądał mniej więcej tak:

  ```
  https://twojanazwa.github.io/mojastrona/
  ```

- Możesz wejść pod ten adres i zobaczyć swoją stronę!

## Dodatkowe wskazówki

- **Aktualizacje** strony robisz przez commit nowych wersji plików do repo.
- GitHub Pages obsługuje również strony budowane np. w Jekyll, Hugo, czy generowane statycznie.
- Możesz podłączyć własną domenę przez ustawienia Pages.
