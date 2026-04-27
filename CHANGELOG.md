# Changelog

Format wzorowany na [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), wersjonowanie [SemVer](https://semver.org/lang/pl/).

Skil jest w fazie 0.x — API patternów (struktura sekcji, format wyjścia, decision trees) może się jeszcze zmienić na podstawie feedbacku z prawdziwego użycia. Wersja 1.0.0 będzie po:
- Native polish-speaking review
- Real-world testach na 20+ tekstach z różnych źródeł
- Stabilizacji formatu wyjścia po pierwszych issues od użytkowników

> **Uwaga o historii wersji:** w commit logu zobaczysz pierwszy commit z napisem „Initial public release v1.2.4". To było źle — podczas 2 dni intensywnej iteracji (7 wersji wewnętrznych + 6 self-audit rund) zacząłem numerować je jako v1.0.0 → v1.2.4, co wyglądało na sztuczne (3 commity, ale wersja 1.2.4 sugeruje wiele wydań). Po feedbacku obniżyłem do v0.1.0 jako honest „first public release". Stare wpisy v1.0.0 — v1.2.4 były w istocie internal QA iteracjami, nie prawdziwymi releasami, dlatego nie mają osobnych entry w tym CHANGELOG.

---

## [0.1.1] — 2026-04-27 — fix typografii myślnika §20

### Naprawione

- **§20 (Pauza, półpauza, łącznik)** — kompletna przeróbka po external review wskazującym faktologiczne błędy:
  - Dodano cytat dr. hab. Adama Wolańskiego (PWN poradnia 16280): myślnik ma DWIE alternatywne formy (pauza/półpauza), nie jedną
  - Dodano regułę konsekwencji w obrębie tekstu (PWN binding rule)
  - Dodano cytat prof. Mirosława Bańki (PWN poradnia 1528): pauza primary, półpauza fallback
  - Dodano **najważniejszą regułę**: spacje wokół myślnika obowiązkowe (była pominięta w v0.1.0)
  - Spaceless `tekst—tekst` (angielski styl) podniesiony do **najsilniejszego AI-tella**
  - Dodano wyjątek: półpauza w zakresach liczbowych (`1939–1945`) BEZ spacji
  - Usunięto nieprawidłowe sformułowanie „AP-style nadużycie"
  - Dodano „mieszanie pauzy/półpauzy w jednym tekście" jako AI-tell
  - Cytaty PWN bezpośrednio zastępują opinion blogs

### Weryfikacja

Zmiany potwierdzone przez 2 niezależne fact-checki na PWN/Wikipedia/eKorekta24. Reviewer's sugestia „default do półpauzy dla webu" została **świadomie złagodzona** — to nie PWN-norm, tylko opisowy trend Wikipedii (która sama flag-uje „normatywny status nieuregulowany").

---

## [0.1.0] — 2026-04-26 — pierwsza publiczna wersja

Pierwsza publikacja na GitHubie. Treść skiła powstała w trakcie ~2 dni intensywnej pracy: 7 iteracji wewnętrznych + 6 rund self-audit z pomocą zewnętrznego AI review. To dużo na krótki czas i znaczna część tych iteracji to były regression-by-leftover fixes (jak audit znajdował, że poprzedni audit nie dosięgnął wszystkich plików).

### Co zawiera

- **SKILL.md** (1139 linii, 44 wzorce AI-tellsów po polsku)
- **4-trybowy preflight:** `normal` / `cautious` / `minimal` / `refuse`
- **Refusal-route** dla: detector bypass, fake testimoniali, ukrytego sponsorowania, akademickiej nieuczciwości
- **§8 fact rule:** nie tworzyć wymyślonych nazwisk, dat, statystyk, anegdot osobistych
- **§19 ostrzeżenie** o modalności prawnej w regulaminach
- **§29 emoji caveat** dla socialmedia/CTA
- **§43 humor decision tree** (4 AND-gate)
- **§44 wtrącenia gating** (te same warunki co humor)
- **Mandatory 4-sekcji output** + idle case
- **Auto-checklist** (półautomatyczne kontrole — cudzysłowy, diakrytyki, halucynacje skrótów)
- **5 examples** + **2 pełne przykłady w-skilu**
- **README, INSTALL, METHODOLOGY, CONTRIBUTING, .github/ templates**

### Czego NIE ma jeszcze

- Native polish-speaking review (główny blocker)
- Real-world test na tekstach z prawdziwych źródeł (na razie tylko syntetyczne)
- `tests/` folder z golden examples (planowane na 0.2.0)
- Konsolidacja paralelnych algorytmów (`Twoje zadanie` / `Workflow` / `Proces redakcji`)

### Atrybucja

Skil powstał z dużą pomocą Claude (Anthropic). Autor (Oleh Hryniv) nie jest native polish — dlatego ta publikacja to **explicit zaproszenie do native review**, nie deklaracja gotowego produktu. Niektóre przykłady w §18 (polskie błędy gramatyczne) mogą być przesadne; niektóre kolokacje w pełnych przykładach mogą brzmieć „z innej Polski". Issues i PR'y mile widziane.

### Roadmap

- **0.2.0** — fixes z native review + real-world test feedbacku
- **0.3.0** — `tests/` folder + konsolidacja algorytmów
- **1.0.0** — po stabilizacji formatu i 20+ real-world tekstach
