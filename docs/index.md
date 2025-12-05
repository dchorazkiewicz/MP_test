# Publikacja strony na GitHub Pages za pomocą MkDocs

Ten przewodnik krok po kroku pokaże Ci, jak opublikować Twoją stronę stworzoną w MkDocs na GitHub Pages. Zakładamy, że pracujesz w Visual Studio Code.

## Krok 1: Przygotowanie środowiska w Visual Studio Code

1.  **Otwórz terminal:** Otwórz zintegrowany terminal w VS Code, używając skrótu `Ctrl+`` (lub przechodząc do `Terminal > Nowy Terminal`).

2.  **Stwórz wirtualne środowisko:** Aby odizolować zależności projektu, stwórz wirtualne środowisko dla Pythona.

    ```bash
    python -m venv .venv
    ```

3.  **Aktywuj środowisko:**
    *   Na systemach Linux/macOS:
        ```bash
        source .venv/bin/activate
        ```
    *   Na systemie Windows (w terminalu Command Prompt lub PowerShell):
        ```bash
        .venv\Scripts\activate
        ```
    Po aktywacji, nazwa Twojego środowiska `(.venv)` powinna pojawić się na początku linii w terminalu.

## Krok 2: Instalacja MkDocs

Z aktywnym środowiskiem, zainstaluj MkDocs. Dobrą praktyką jest również instalacja popularnego motywu `material`.

```bash
pip install mkdocs mkdocs-material
```

## Krok 3: Inicjalizacja projektu i tworzenie treści

Jeśli zaczynasz od zera, możesz stworzyć nowy projekt:

```bash
# Stwórz projekt w bieżącym katalogu
mkdocs new .
```

Teraz możesz edytować plik `mkdocs.yml` oraz dodawać lub modyfikować pliki `.md` w katalogu `docs/`.

## Krok 4: Publikacja na GitHub Pages

To najważniejszy krok. MkDocs posiada wbudowane narzędzie, które automatyzuje cały proces.

1.  **Upewnij się, że Twój projekt jest repozytorium Git:**
    *   Zainicjuj repozytorium: `git init`
    *   Dodaj zdalne repozytorium GitHub: `git remote add origin https://github.com/TWOJA_NAZWA_UŻYTKOWNIKA/NAZWA_REPOZYTORIUM.git`
    *   Wypchnij zmiany na gałąź `main` (lub `master`): `git push -u origin main`

2.  **Użyj komendy `gh-deploy`:** Ta komenda zbuduje Twoją stronę i automatycznie umieści ją na gałęzi `gh-pages` w Twoim zdalnym repozytorium.

    ```bash
    mkdocs gh-deploy
    ```

    Podczas wykonywania polecenia MkDocs zbuduje dokumentację, utworzy gałąź `gh-pages` (jeśli nie istnieje), zatwierdzi zmiany i wypchnie je do zdalnego repozytorium `origin`.

## Krok 5: Konfiguracja GitHub Pages

Po wykonaniu komendy `gh-deploy`, przejdź do swojego repozytorium na stronie GitHub.

1.  Wejdź w `Settings` (Ustawienia).
2.  W menu po lewej stronie wybierz `Pages`.
3.  W sekcji `Build and deployment` jako źródło (`Source`) wybierz `Deploy from a branch`.
4.  Upewnij się, że wybrana jest gałąź (`Branch`) **`gh-pages`** z folderem `/ (root)`.
5.  Zapisz zmiany.

Twoja strona powinna być dostępna po kilku minutach pod adresem:
`https://<TWOJA_NAZWA_UŻYTKOWNIKA>.github.io/<NAZWA_REPOZYTORIUM>/`