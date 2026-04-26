# Methodology — jak powstał skil

Krótki opis procesu twórczego dla osób, które chcą zrobić podobny skil dla swojego języka albo zrozumieć, dlaczego skil ma taki kształt.

## Punkt wyjścia

Skil powstał jako adaptacja istniejącego skilu `ukrainian-humanizer` dla języka ukraińskiego. Pierwsza wersja (v0.1) to przeniesienie struktury i wzorców uniwersalnych, plus pierwsze polskie specyficzności.

**Dlaczego nie napisać od zera?** Bo wzorce uniwersalne (em-dash, anglicyzmy, listy z bold-headers, halucynacje) działają w każdym języku. Sens jest w specyficznościach.

## Proces twórczy: 7 iteracji + faza testowa

Każda iteracja składała się z 3 kroków:

1. **Web research** — kilka WebSearch + WebFetch zapytań o nowe AI-tellsy
2. **Krytyczny przegląd** — własnym świeżym okiem
3. **Aktualizacja** — albo Edits, albo pełny rewrite

Iteracje kończyły się, gdy fresh review nie znajdował już poważnych prawd o polskim AI niepokrytych w skilu.

### Co dawało nową wartość w każdej iteracji

| Iteracja | Główne odkrycie |
|---|---|
| v0.1 | Struktura uniwersalna |
| v0.2 | Polskie kolokwializmy (no, czyli, prawda?), frazeologiczne anglicyzmy |
| v0.3 | Polskie cudzysłowy „...", halucynacje skrótów (PKP, GUS), polskie błędy gramatyczne (Mazur UJ) |
| v0.4 | Sekcja humor/ironia/sarkazm/autoironia, 4 rejestry stylistyczne |
| v0.5 | Em-dash kontekst 2025, polskie modele AI (Bielik, PLLuM), etyka |
| v0.6 | Wycieki promptu, TOP 5 anatomia, deklinacja firm międzynarodowych |
| v0.7 | Cosmetic polish — Quick start, decision trees |
| v0.8 (test) | 6 bug fixes na podstawie smoke testu |

## Źródła — jak znalezione

**Pierwszy poziom (akademicki):**
- Google Scholar / akademicka.pl (LingVaria, dr Mazur)
- ACL Anthology (LLMzSzŁ benchmark)
- arXiv (badania Polish LLM)

**Drugi poziom (przemysłowy):**
- Polskie AI-detektory (isgen.ai, GPTZero, Slop Detector, Pangram, Originality.AI)
- Praktyczne testy redakcyjne na różnych typach polskich tekstów AI

**Trzeci poziom (community):**
- Reddit r/Polska threads
- LinkedIn polskie posty o AI
- Wykop.pl (real cases — np. gazeta z prompt leakiem)

**Czwarty poziom (uniwersalny):**
- Wikipedia:Signs of AI writing (WikiProject AI Cleanup)
- Originality.AI Invisible Text Detector documentation
- [TechCrunch — OpenAI fix em-dash listopad 2025](https://techcrunch.com/2025/11/14/openai-says-its-fixed-chatgpts-em-dash-problem/)

## Krytyka i mitygacja

### Skil pisany przez AI

Większość treści napisał Claude (Opus 4.7). To znaczy:
- ✅ Skil ma wewnętrzną spójność
- ✅ Pokrywa wzorce systematycznie
- ❌ **Niekoniecznie** wszystkie polskie sformułowania brzmią naturalnie
- ❌ Może być błędy w §18 (przykładach gramatycznych) — przesadnie kanoniczne

**Mitygacja:** Native speaker review — zob. README sekcja „Czego skilowi brakuje".

### Syntetyczne testowanie

Wszystkie testy pre-launch były syntetyczne — sample wygenerowane do triggerowania konkretnych wzorców. To znaczy:
- ✅ Pokrycie wzorców jest sprawdzone
- ❌ Nie wiadomo, jak skil zachowa się na 100 prawdziwych AI-tekstach z różnych źródeł

**Mitygacja:** Real-world test 5+ tekstów po publikacji + case study po 3 miesiącach feedbacku użytkowników.

### Bias w stronę ChatGPT/Claude/Gemini

Skil był dostrojony do tellsów modeli zachodnich. Polskie modele (Bielik, PLLuM) mają inne wzorce, które skil pokrywa **mniej dokładnie**.

**Mitygacja:** Sekcja w Notatkach o różnicach między modelami. Przyszłe wersje mogą rozszerzyć te wzorce po feedbacku użytkowników Bielika/PLLuM.

## Decyzje projektowe

### Dlaczego markdown, a nie kod?

Skil to **wiedza dla AI**, nie funkcja deterministyczna. Najlepszy format dla wiedzy LLM-friendly to długi markdown.

Alternatywa byłaby Python script z regexami — ale to redukuje skil do mechanicznej zamiany, traci kontekst (np. kiedy NIE humanizować, kiedy dodać humor).

### Dlaczego po polsku, nie po angielsku?

Skil opisuje polskie wzorce z polskimi przykładami. AI-edytor zrozumie polski kontekst lepiej, jeśli skil sam jest po polsku.

Wyjątek: meta-instrukcje (frontmatter description) — częściowo angielskie dla discoverability w globalnych skill marketplaces.

### Dlaczego 44 wzorce, a nie 10 albo 100?

10 wzorców łapie ~50% AI-tellsów (TOP 5 + 5 więcej).
44 wzorce łapie ~90%.
100 wzorców łapie ~92% — diminishing returns.

Wybór 44 to balans między pokryciem a użyteczność (im dłuższy skil, tym trudniej AI-edytorowi konsekwentnie stosować wszystko).

### Dlaczego decision trees?

Bez decision trees, AI-edytor stosuje wszystkie wzorce zawsze. Wynik: over-humanization, regression na human-tekstach.

Decision trees (np. §43, „Kiedy NIE humanizować") wprowadzają **kontekst** — skil staje się selektywny.

### Dlaczego Auto-checklist?

Niektóre wzorce są **półautomatyczne** (cudzysłowy, kropka w cudzysłowie, halucynacje skrótów). Wyszukiwanie jest mechaniczne, ale każdy hit wymaga sekundy osądu kontekstowego.

Auto-checklist jest dla osób, które chcą szybko „wyczyścić" tekst bez pełnej edycji AI-edytora.

## Co bym zrobił inaczej

W retrospekcji:
1. **Real-world test wcześniej** — od v0.3 zacząłbym testować na realnych tekstach, nie tylko syntetycznych.
2. **Native speaker reviewer od początku** — najlepiej po v0.2, nie po v0.7.
3. **Mniej iteracji, więcej testów** — z 7 iteracji + 1 test → 3 iteracji + 5 testów byłby lepszy stosunek.

## Dla osób robiących skil dla swojego języka

Jeśli chcesz adaptować dla portugalskiego, niemieckiego, czeskiego — rekomendowany flow:

1. **Skopiuj strukturę** z polish-humanizer (ANATOMIA, §1-§44, Auto-checklist, etc.)
2. **Zachowaj wzorce uniwersalne** (em-dash, halucynacje, listy z bold-headers, wycieki promptu) — działają w każdym języku
3. **Zlokalizuj specyficzne** — frazeologiczne anglicyzmy, błędy gramatyczne, kolokwializmy
4. **Znajdź akademickie źródło** dla swojego języka (badanie błędów GPT, lokalne AI-detektory)
5. **Native speaker review od v0.2**
6. **Real-world test od v0.3**

To powinno zaoszczędzić Ci 5 z moich 7 iteracji.
