# Contributing to Polish Humanizer

Cieszę się z każdego feedbacku i kontrybucji. Oto co jest najprzydatniejsze.

## Najwartościowsze kontrybucje

### 1. Native speaker review

Skill został napisany z pomocą AI. Native speaker polski może wyłapać:
- Niefortunne kolokacje w przykładach
- Nienaturalne sformułowania
- Błędy w §18 (polskie błędy gramatyczne) — niektóre przykłady mogą być przesadne
- Stare lub regionalne sformułowania, które już się nie używa

**Jak zgłosić:** Issue z tagiem `language-error`, podaj sekcję i konkretne zdanie.

### 2. Nowe wzorce AI

AI-tellsy ewoluują. Jeśli zauważyłeś wzorzec, którego skil nie pokrywa, zgłoś.

**Wymagania na nowy wzorzec:**
- Co najmniej 3 przykłady AI-tekstu zawierające wzorzec (z linkami do źródła, jeśli to możliwe)
- Naturalne polskie alternatywy (jak człowiek by to napisał)
- Argumentacja, czemu to AI-tell, a nie po prostu styl konkretnego autora

**Jak zgłosić:** Issue z tagiem `new-pattern`, użyj template w `.github/ISSUE_TEMPLATE/new-pattern.md`.

### 3. False positives

Tekst napisany przez człowieka, gdzie skil błędnie identyfikuje AI-tell.

**Jak zgłosić:** Issue z tagiem `false-positive`, podaj fragment + który paragraf skilu spowodował problem.

### 4. Aktualizacja źródeł

Skill cytuje akademickie i przemysłowe źródła z lat 2024-2025. Nowsze badania mile widziane.

## Czego NIE potrzebuję

- Tłumaczeń skilu na inne języki — skil jest specyficzny dla polskiego, nie należy go uniwersalizować. Dla innych języków: forki.
- Generycznych „popraw stylistycznie" PR — bez konkretnego problemu do rozwiązania.
- Refactor dla refactor's sake — formatowanie SKILL.md jest celowo długie i powtarzalne.

## Process

1. **Issue najpierw** — przed PR otwórz issue, opisz problem i proponowane rozwiązanie. Pozwala uniknąć rozjazdów.
2. **Branch** — `fix/short-description` albo `feat/short-description`
3. **PR** — krótki opis: co zmieniasz, dlaczego, jak testowałeś
4. **Versioning** — semver (MAJOR.MINOR.PATCH); w PR opisz, jakiej wersji oczekujesz

## Code of conduct

Bądź konstruktywny. Skill ma podwójne zastosowanie (zob. README — sekcja Etyka), więc dyskusje o etyce są mile widziane. Ataki personalne — nie.

## Kontakt

Jeśli wolisz prywatnie: zostaw email w issue albo otwórz discussion w GitHub.
