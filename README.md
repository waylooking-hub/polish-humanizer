# Polish Humanizer

> Skill do redakcji polskich tekstów, które brzmią sztucznie, szablonowo albo jak surowy szkic AI. Pomaga poprawić naturalność, rytm, rejestr, frazeologię i typografię bez zmiany sensu oraz bez obchodzenia zasad ujawniania użycia AI.
>
> A skill for editing Polish texts that sound stiff, generic, or like raw AI drafts. It improves naturalness, rhythm, register, phrasing, and typography without changing meaning or bypassing AI disclosure rules.

[![Version](https://img.shields.io/badge/version-0.1.0-blue.svg)](CHANGELOG.md)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## ⚠️ Etyka i zakres użycia / Ethics and scope of use

**[PL]** Ten skill służy do edycji stylu — żeby teksty brzmiały naturalnie po polsku. **Nie używaj go do ukrywania AI-pochodzenia tam, gdzie ujawnienie jest wymagane:**

- W **kontekście akademickim** (eseje, prace dyplomowe, artykuły naukowe) — wiele polskich uczelni (UW, SGH, UMCS, UAM) wymaga oświadczenia o zakresie użycia AI. Humanizacja w celu obejścia detektora może być traktowana jako plagiat.
- W **dziennikarstwie** — wiele redakcji wymaga ujawnienia AI w pipeline.
- W **marketingu, copywritingu, social mediach** — humanizacja jest zwykłą redakcją stylu, o ile nie służy tworzeniu fałszywych opinii, podszywaniu się pod realne osoby, ukrywaniu sponsorowania ani manipulacji odbiorcą.
- W **regulaminach, umowach, dokumentach prawnych i instrukcjach technicznych** — używaj tylko trybu cautious/minimal: poprawiaj jasność, błędy, kalki i typografię, ale nie dodawaj potoczności, humoru ani autorskiego głosu (modalność prawna i bezosobowość są wymagane).

Cel skilu to **naturalny, dobrze brzmiący tekst** — nie niski AI-score za wszelką cenę.

**[EN]** This skill is for style editing — making texts sound natural in Polish. **Do not use it to hide AI authorship where disclosure is required:**

- In **academic contexts** — many Polish universities (UW, SGH, UMCS, UAM) require AI usage disclosure. Humanizing to bypass detection may be treated as plagiarism.
- In **journalism** — many editorial boards require AI disclosure in the workflow.
- In **marketing, copywriting, social media** — humanization is standard editing, **as long as** it does not serve to fabricate fake opinions, impersonate real people, hide sponsored content, or manipulate audiences.
- In **legal documents, contracts, regulations and technical specifications** — use only cautious/minimal mode: fix clarity, errors, calques and typography, but do not add informality, humor or authorial voice (legal modality and impersonal style are required).

The goal is **natural-sounding text**, not low AI-score at any cost.

---

## Co to jest / What it is

**[PL]** Polish Humanizer to długi (1000+ linii) markdownowy dokument-przewodnik, który czyta AI-edytor i wykonuje na podanym tekście. Skill rozpoznaje **44 wzorce** charakterystyczne dla AI-tekstu po polsku i opisuje, jak je naprawić. Bazuje na:

- Polskiej publikacji akademickiej (Mazur 2024, [LingVaria 19(1)](https://doi.org/10.12797/LV.19.2024.37.08))
- Polskich AI-detektorach (isgen.ai, GPTZero, Slop Detector, Originality.AI)
- [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) (WikiProject AI Cleanup)
- Praktycznej obserwacji tysięcy AI-tekstów po polsku z Claude / ChatGPT / Gemini / Bielik / PLLuM

> Note: część obserwacji ma charakter praktyczny, nie korpusowo-statystyczny. Konkretne daty, wersje modeli AI i przykłady medialne należy okresowo weryfikować przy aktualizacji skilu.

**[EN]** Polish Humanizer is a long (1000+ line) markdown guide that an AI editor reads and applies to provided text. The skill recognizes **44 patterns** typical of AI text in Polish and describes how to fix them.

---

## Co skill łapie / What the skill catches

- **Frazeologiczne anglicyzmy:** „na koniec dnia", „drugi po nikim", „robić różnicę"
- **Halucynacje:** wymyślone rozwinięcia skrótów (PKP, GUS), daty, statystyki
- **Strukturalne AI-tellsy:** wstępy „W dzisiejszym świecie", listy z bold-headers, sekcje „Podsumowanie"
- **Typografia:** polskie cudzysłowy `„..."`, kropka po cudzysłowie, em-dash, hidden Unicode
- **Polskie błędy gramatyczne:** niezgoda przypadku, kolokacje, deklinacja nazw własnych
- **Mieszanie rejestrów:** Pan/Pani vs ty, korpomowa vs slang
- **Wycieki promptu:** „Sure, here is the article you requested..."
- **Brak humoru/ironii** — z polskimi sygnałami kulturowymi (Mrożek, Bareja)
- **+30 kolejnych wzorców** — patrz [SKILL.md](SKILL.md)

---

## Quick start

1. Skopiuj zawartość [SKILL.md](SKILL.md) do swojego AI-edytora (Claude Project, ChatGPT Custom Instructions, Gemini Gem)
2. Wklej AI-tekst do edycji
3. Poproś: „Zhumanizuj ten tekst po polsku zgodnie z polish-humanizer"
4. Sprawdź **flagi do weryfikacji** w output (fakty, daty, skróty)
5. Przeczytaj na głos — to ostateczny test

Szczegóły: [docs/INSTALL.md](docs/INSTALL.md)

---

## Przykłady / Examples

5 par before/after na różnych typach tekstu — patrz [examples/](examples/):

- [01-blog.md](examples/01-blog.md) — blog techniczny
- [02-marketing.md](examples/02-marketing.md) — email marketing / LinkedIn
- [03-naukowy.md](examples/03-naukowy.md) — popularnonaukowy
- [04-formalny.md](examples/04-formalny.md) — tekst formalny (regression test)
- [05-mieszany.md](examples/05-mieszany.md) — tekst z mixem human/AI

---

## Use cases

✅ **Dobre zastosowania:**
- Redakcja własnych AI-szkiców do publikacji (blog, newsletter, social media)
- Sprawdzanie czystości tekstu copywritera, który mógł wspomóc się AI
- Nauka rozpoznawania AI-style w polskich tekstach
- Punkt wyjścia dla własnych humanizerów / detektorów

❌ **Zastosowania, dla których skill NIE jest przeznaczony:**
- Obchodzenie detektorów AI w akademickim kontekście
- Generowanie fake-human contentu w celu manipulacji
- Tłumaczenia (skill operuje na poziomie stylu, nie semantyki)
- Edycja tekstów w innych językach niż polski

---

## Stan projektu / Project status

**Wersja 0.1.0** — pierwsza publiczna wersja po internal QA. Używalna na co dzień, ale **przed native review** i przed feedbackiem z prawdziwego użycia. Versioning od 0.x, bo jeszcze nie ma stabilnego API patternów.

### Co skil już ma:
- ✅ 44 wzorce AI-tellsów po polsku
- ✅ 4-trybowy preflight (`normal` / `cautious` / `minimal` / `refuse`)
- ✅ Auto-checklist (półautomatyczne kontrole)
- ✅ Decision tree dla humoru / ironii / wtrąceń
- ✅ After-action review (8 pytań kontrolnych)
- ✅ Mierzalne proxies AI-tekstu
- ✅ 2 pełne przykłady + 5 standalone examples
- ✅ Refusal-route dla: detector bypass, fake testimoniali i ukrytego sponsorowania

### Czego skilowi brakuje (i czego szukam):

> 🔎 **Szukam native polish-speaking testerów i recenzentów.**
>
> Skil powstał z dużą pomocą AI (Claude). Ja sam nie jestem native PL — czuję, że niektóre przykłady mogą brzmieć sztucznie albo „z innej Polski". Native review jest największą rzeczą blokującą tę wersję przed prawdziwym dojrzeniem.
>
> **Najprzydatniejsze, co możesz zrobić:**
> 1. Przetestuj skil na prawdziwym AI-tekście (LinkedIn/blog/email) i powiedz, co brzmi nienaturalnie
> 2. Wskaż błędy w §18 (polskie błędy gramatyczne) — niektóre przykłady mogą być przesadne
> 3. Daj znać o false positives (skil błędnie identyfikuje human-tekst jako AI)
> 4. Zaproponuj nowy wzorzec, którego brakuje
>
> Issue: [github.com/.../issues](../../issues) | albo napisz na Threads / X / DM.

### Czym polish-humanizer NIE jest:
- Nie jest kompletny — AI-tellsy zmieniają się co kilka miesięcy, skil wymaga aktualizacji
- Nie jest narzędziem do obejścia detektorów AI ([refusal-route](SKILL.md))
- Nie jest tłumaczeniem ani korektą stylistyczną tekstu już napisanego przez człowieka

---

## Contributing

Cieszę się z każdym feedbackiem. Najprzydatniejsze kontrybucje:

1. **Native speaker review** — wskaż błędy, niefortunne kolokacje, nienaturalne przykłady
2. **Nowe wzorce** — AI-style ewoluuje, znajdź wzorzec, którego skil nie pokrywa
3. **False positives** — przykład tekstu, gdzie skil błędnie identyfikuje human-tekst jako AI

Issue templates: [.github/ISSUE_TEMPLATE/](.github/ISSUE_TEMPLATE/)

---

## Acknowledgments / Źródła

Skill opiera się na:

- [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) — WikiProject AI Cleanup
- Mazur, R. (2024) — *O poprawności językowej tekstów generowanych przez SI na przykładzie ChatuGPT*, [LingVaria 19(1)](https://doi.org/10.12797/LV.19.2024.37.08), s. 119–138
- Polskie AI-detektory: [isgen.ai](https://isgen.ai), [GPTZero](https://gptzero.me), Slop Detector, [Pangram](https://www.pangram.com), [Originality.AI](https://originality.ai)
- [TechCrunch — OpenAI fix em-dash (listopad 2025)](https://techcrunch.com/2025/11/14/openai-says-its-fixed-chatgpts-em-dash-problem/)
- Praktyczna obserwacja tekstów AI po polsku oraz testy redakcyjne

> Część obserwacji ma charakter praktyczny, nie korpusowo-statystyczny. Konkretne daty, przykłady medialne i wersje modeli należy weryfikować przy aktualizacji skilu.

---

## License

[MIT](LICENSE) — feel free to use, modify, distribute.

---

## Disclaimer

Skill jest dostarczany **as-is**. Nie gwarantuje, że tekst po humanizacji nie będzie wykrywany jako AI. Nie zastępuje profesjonalnej redakcji tekstu. Zob. [Etyka](#-etyka-i-zakres-użycia--ethics-and-scope-of-use).
