---
name: False positive / błędna identyfikacja
about: Skil błędnie traktuje human-tekst jako AI
title: '[FALSE POSITIVE] '
labels: 'false-positive, bug'
assignees: ''
---

## Fragment tekstu (human, nie AI)

Wklej tekst, który był napisany przez człowieka, a skil go „poprawia":

```
[wklej tekst]
```

**Źródło / autor:** (np. „mój własny blog", „artykuł z Polityki", „kabaret Mrożka"). Ważne: skąd wiesz, że to nie AI?

## Co skil zrobił z tym tekstem

Wklej output skilu (po humanizacji):

```
[wklej zhumanizowany output]
```

## Który paragraf SKILL.md jest „winny"

Konkretny § albo sekcja, na podstawie której skil źle zdiagnozował:

- §...

## Dlaczego to jest false positive

Krótko: czemu Twoim zdaniem skil nie powinien tu interweniować?

## Proponowana naprawa

(opcjonalne)

- [ ] Dodać caveat do § ...
- [ ] Rozszerzyć decision tree
- [ ] Inne: ...

## Środowisko

- AI-edytor: (Claude / ChatGPT / Gemini / inne)
- Wersja skilu: (np. v1.0.0 — sprawdź w CHANGELOG.md)
