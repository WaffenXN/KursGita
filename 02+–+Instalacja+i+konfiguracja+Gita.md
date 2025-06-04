# **02 – Instalacja i konfiguracja Gita**
## **Instalacja Gita**
### **🪟 Windows**
1. Przejdź na stronę:

   https://git-scm.com/download/win

1. Instalator pobierze się automatycznie.
1. Uruchom plik .exe i przejdź przez kolejne kroki instalacji.
1. Zalecane ustawienia podczas instalacji:
   1. Wybierz edytor tekstu (np. Notepad++ lub Visual Studio Code)
   1. Zaznacz: **"Git from the command line and also from 3rd-party software"**
   1. Pozostaw pozostałe opcje domyślne
1. Po zakończeniu instalacji, otwórz **Git Bash** lub **PowerShell** i wpisz:

   git --version

-----
### **🍎 macOS**
#### **Instalacja przez Homebrew (zalecana)**
1. Zainstaluj Homebrew (jeśli jeszcze go nie masz):

   https://brew.sh

1. Następnie zainstaluj Git:

   brew install git
#### **Alternatywa – instalator graficzny**
- Możesz pobrać instalator z oficjalnej strony:

  https://git-scm.com/download/mac

3. Po instalacji sprawdź wersję:

   git --version

-----
### **🐧 Linux (Debian/Ubuntu)**
1. Otwórz terminal i wykonaj:

   sudo apt update

   sudo apt install git

1. Po instalacji sprawdź wersję:

   git --version

📌 Na innych dystrybucjach użyj odpowiedniego menedżera pakietów, np. dnf, yum, pacman.

-----
## **Konfiguracja Gita**
Po zainstalowaniu Gita skonfiguruj podstawowe dane użytkownika, które będą dołączane do każdego commita.
### **👤 Ustawienie imienia i adresu e-mail**
git config --global user.name "Twoje Imię"

git config --global user.email "twoj@email.com"
### **🔍 Sprawdzenie konfiguracji**
git config --list

-----
## **Opcjonalne ustawienia**
### **✅ Domyślny edytor (np. Visual Studio Code)**
git config --global core.editor "code --wait"
### **🧩 Przydatne aliasy (skróty komend)**
git config --global alias.st status

git config --global alias.co checkout

git config --global alias.br branch

git config --global alias.cm commit

Aliasów możesz utworzyć dowolną liczbę, według własnych preferencji.

-----
## **🔐 Gdzie zapisywana jest konfiguracja?**
- **Globalna konfiguracja** (dla całego systemu / użytkownika):

  ~/.gitconfig

- **Lokalna konfiguracja** (dla konkretnego repozytorium):

  .git/config

Możesz edytować te pliki ręcznie lub za pomocą poleceń git config.

-----
✅ **Gotowe!**\
Masz teraz zainstalowanego i poprawnie skonfigurowanego Gita. W kolejnym rozdziale rozpoczniesz pracę z repozytorium lokalnym i zapiszesz pierwsze zmiany.
