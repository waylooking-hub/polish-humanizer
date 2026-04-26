# Instalacja i użycie

Skill nie ma kodu — to długi markdownowy dokument, który czyta AI-edytor. Można go używać w 4 sposobach.

## 1. Claude Code (zalecane)

Jeśli używasz [Claude Code](https://claude.com/claude-code):

```bash
mkdir -p ~/.claude/skills/polish-humanizer
cp SKILL.md ~/.claude/skills/polish-humanizer/SKILL.md
```

Po restarcie Claude Code skill staje się dostępny jako `/polish-humanizer` (jeśli włączysz w settings).

W rozmowie z Claude:
```
/polish-humanizer

[wklej AI-tekst]
```

## 2. Claude Project (Claude.ai web/desktop)

1. Otwórz Claude.ai → Projects → Create Project
2. W "Project knowledge" → Add files → wgraj `SKILL.md`
3. W "Custom instructions" wklej:

```
Stosuj zasady z polish-humanizer/SKILL.md do każdego polskiego tekstu, który dostajesz do humanizacji. Stosuj proces redakcji zgodnie z sekcją "Proces redakcji" w SKILL.md.
```

4. Wszystko, co wklejasz w tym Projekcie, będzie humanizowane.

## 3. ChatGPT Custom Instructions / Custom GPT

**Custom Instructions:**
- Settings → Personalization → Custom Instructions
- W polu "How would you like ChatGPT to respond?" wklej:

```
Gdy dostajesz polski tekst do humanizacji, stosuj 44 wzorce z polish-humanizer (https://github.com/waylooking-hub/polish-humanizer). Najważniejsze: usuń frazeologiczne anglicyzmy ("na koniec dnia", "drugi po nikim"), zamień cudzysłowy na polskie „...", sprawdź halucynacje (skróty PKP, GUS, statystyki bez źródła), zachowaj sens i fakty. Humor, autoironię i osobiste wtrącenia dodawaj tylko wtedy, gdy tekst jest osobisty/blogowy/felietonowy, autor ma taki głos w próbce i żart wynika z treści. Zob. SKILL.md.
```

**Custom GPT** (lepszy dla regularnego użycia):
- Create a GPT → Configure → wklej zawartość SKILL.md jako instructions
- Knowledge → upload SKILL.md jako pliku
- Test, share

## 4. Manual prompt (jednorazowe użycie)

Bez konfiguracji, ad hoc:

```
Jesteś redaktorem polskich tekstów. Stosuj zasady z polish-humanizer (skill do humanizacji AI-tekstu). Najważniejsze:

1. Usuń frazeologiczne anglicyzmy: "na koniec dnia" → "ostatecznie", "robić różnicę" → "mieć znaczenie", "dedykowany" → "skierowany do"
2. Zamień cudzysłowy "..." na polskie „..."
3. Sprawdź halucynacje: PKP = Polskie Koleje Państwowe (NIE "Polska Kolej Prywatna"), GUS = Główny Urząd Statystyczny (NIE "Generalny")
4. Usuń: "W dzisiejszym dynamicznie zmieniającym się świecie", "Mam nadzieję, że to pomocne", sekcję "Podsumowanie"
5. Nie dodawaj humoru ani autoironii automatycznie. Dodaj je tylko wtedy, gdy tekst jest osobisty/blogowy/felietonowy, autor ma taki styl w próbce, a humor wynika z istniejącego napięcia w tekście. W copy firmowym, B2B, landing page, krótkim produktowym, emailu służbowym, regulaminie i instrukcji technicznej — nie dodawaj humoru.

Zhumanizuj ten tekst:

[wklej tekst]
```

To minimum, ale działa dla prostych przypadków.

## Sprawdzanie wyniku

Po humanizacji:
1. **Czytaj na głos** — jeśli się zacinasz, popraw
2. **Detektory** (opcjonalnie):
   - [isgen.ai](https://isgen.ai) — polski
   - [GPTZero](https://gptzero.me) — multilingual
   - [Slop Detector](https://slop-detector.com) — polski
3. **Native speaker** (jeśli to ważny tekst — np. publikacja)

## Limitacje

- Skill nie modyfikuje semantyki — tylko styl
- Halucynowane fakty wymagają **ręcznej** weryfikacji (skil tylko flaguje)
- Dla bardzo długich tekstów (>3000 słów) zalecane podzielenie na sekcje
- Nie działa idealnie na tekstach z polskich modeli (Bielik, PLLuM) — patrz sekcja Notatki w SKILL.md

## Troubleshooting

**Q: Tekst po humanizacji brzmi sztucznie / wymuszone**
A: Możliwe over-humanization. Sprawdź After-action review w SKILL.md (8 pytań). Często problem to nadmiar autoironii — zob. decision tree §43.

**Q: Skil nie usunął jakiegoś AI-tellsa**
A: Zgłoś jako issue z tagiem `false-negative`. Może to być nowy wzorzec, który warto dodać do skilu.

**Q: Skil zepsuł human-tekst (regression)**
A: Zgłoś jako issue z tagiem `false-positive`. Pokaż fragment + pokaż, jak skil go zmienił.
