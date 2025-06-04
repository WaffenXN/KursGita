# **Bonus 1 – Tworzenie klucza SSH i łączenie z GitHubem**
Używanie klucza SSH pozwala na bezpieczne i wygodne uwierzytelnianie się w GitHubie bez potrzeby podawania loginu i hasła (lub tokena) przy każdym git push i git pull.

-----
## **📌 Krok 1: Sprawdź, czy masz już klucz SSH**
ls ~/.ssh

Jeśli widzisz pliki takie jak id\_rsa i id\_rsa.pub, możesz przejść do kroku 3.

-----
## **🛠️ Krok 2: Tworzenie nowego klucza SSH**
W terminalu wpisz:

ssh-keygen -t ed25519 -C "twoj@email.com"

Jeśli Twoja wersja SSH nie obsługuje ed25519, użyj:

ssh-keygen -t rsa -b 4096 -C "twoj@email.com"

Naciśnij **Enter**, aby zapisać plik domyślnie w ~/.ssh/id\_ed25519. Możesz też ustawić hasło dla większego bezpieczeństwa.

-----
## **📋 Krok 3: Skopiuj klucz publiczny**
Wykonaj:

cat ~/.ssh/id\_ed25519.pub

Skopiuj cały wygenerowany klucz – zaczyna się od ssh-ed25519 lub ssh-rsa.

-----
## **🌐 Krok 4: Dodaj klucz do GitHuba**
1. Zaloguj się na [https://github.com](https://github.com/)
1. Wejdź w **Settings** (prawy górny róg)
1. Przejdź do **SSH and GPG keys**
1. Kliknij **New SSH key**
1. Wklej swój klucz do pola „Key”, nadaj mu nazwę i kliknij „Add SSH key”
-----
## **🔁 Krok 5: Przetestuj połączenie**
ssh -T git@github.com

Jeśli wszystko działa, zobaczysz komunikat w stylu:

Hi username! You've successfully authenticated...

-----
## **💡 Używanie adresu SSH zamiast HTTPS**
Podczas klonowania repozytorium wybierz opcję **SSH**, a nie HTTPS:

git clone git@github.com:twoja-nazwa/repo.git

Dzięki temu nie będziesz musiał logować się za każdym razem – Git będzie korzystał z Twojego klucza SSH.

-----
## **Podsumowanie**
W tym bonusie nauczyłeś się:

- Tworzyć parę kluczy SSH
- Dodawać klucz do GitHuba
- Testować połączenie SSH
- Klonować i pracować z repozytorium bez hasła

To wygodny i bezpieczny sposób pracy z GitHubem, zwłaszcza w codziennej pracy developerskiej.
