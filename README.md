# git-notatki-lekcje
`git merge` to polecenie służące do łączenia niezależnych linii rozwoju (gałęzi/branchy) w jedną. Najczęściej używamy go, aby dołączyć zmiany z gałęzi roboczej (np. `feature-branch`) do gałęzi głównej (`main`).
**Przydatne komendy:**
* `git branch <nazwa>` - tworzy nową gałąź.
* `git checkout <nazwa>` lub `git switch <nazwa>` - przełącza na daną gałąź.
* `git merge <nazwa>` - łączy podaną gałąź z tą, na której obecnie się znajdujemy.

## 2. Czym są konflikty (Conflicts)?
Konflikt w Gicie pojawia się podczas operacji `merge`, gdy te same linie w tym samym pliku zostały zmienione w obu łączonych gałęziach. Git nie wie wtedy, którą wersję ma zachować i prosi programistę o ręczne rozwiązanie problemu.

**Jak rozwiązać konflikt?**
1. Otwieramy plik z konfliktem. Git oznacza sporne miejsca znacznikami: `<<<<<<<`, `=======`, `>>>>>>>`.
2. Decydujemy, którą wersję chcemy zostawić (lub łączymy je w jedną logiczną całość) i usuwamy znaczniki Gita.
3. Zapisujemy plik.
4. Dodajemy zmiany do stage'a: `git add <nazwa_pliku>`.
5. Kończymy łączenie komendą: `git commit`.