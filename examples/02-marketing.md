# Przykład 02 — Email marketing / LinkedIn post

**Domena:** sales email + sponsorowany post LinkedIn
**Złożoność:** wysoka (najgęstsze AI-tellsy)
**Tellsy:** §36, §1, §2, §9, §10, §29, §26, §8, §13, §35

## Przed (AI mailing)

> 🚀 **Witaj [Imię]!**
>
> Nie uwierzysz, co się właśnie wydarzyło! 🎉
>
> Wiesz, co Cię czeka? Mam dla Ciebie coś naprawdę specjalnego — produkt, który zmieni zasady gry w Twoim biznesie. W dzisiejszym dynamicznie zmieniającym się świecie e-commerce, dedykowane rozwiązania robią różnicę.
>
> Aż 92% naszych klientów już czerpie korzyści z naszych innowacyjnych technologii! Nie pozwól sobie przepuścić tej okazji!
>
> 💡 **Oszczędność czasu:** Automatyzujemy procesy.
> ✅ **Niska cena:** Konkurencyjne stawki.
> 🚀 **Wzrost sprzedaży:** Średnio o 47%.
> 🔥 **Wsparcie 24/7:** Zawsze do dyspozycji.
>
> Na koniec dnia, liczy się dla nas Twój sukces. Adresujemy każdą potrzebę. Dostarczamy wartość.
>
> **Działaj teraz! Tylko dziś specjalna oferta — 50% zniżki!** ⏰
>
> Pozdrawiam serdecznie,
> Anna Kowalska
> Senior Marketing Manager
> XYZ Solutions Sp. z o.o.
> [LinkedIn] [Twitter] [Strona]

## Co skill łape

- §29 emoji w nagłówkach (🚀, 🎉, 💡, ✅, 🔥, ⏰)
- §36 fake urgency („Nie uwierzysz", „Tylko dziś", „Działaj teraz")
- §36 wykrzykniki w temacie/otwarciu
- §36 placeholder `[Imię]` w gotowym tekście (leak template)
- §1 „W dzisiejszym dynamicznie zmieniającym się świecie"
- §2 „zmieni zasady gry"
- §9 „dedykowane", „innowacyjnych"
- §10 „robią różnicę", „na koniec dnia", „adresujemy", „dostarczamy wartość"
- §8 „92% naszych klientów" + „47% wzrost" — niepotwierdzone
- §26 listy z bold-headers + emoji
- §35 wazeliniarski ton („Pozdrawiam serdecznie")
- §36 overformatting podpisu (4 linie z linkami)

## Po (humanizacja)

> Cześć Anno,
>
> dwa tygodnie temu uruchomiliśmy nowy moduł raportów retencji. Zwraca dane, których nie widać w standardowym dashboardzie — np. że ⅓ klientów odpada w drugim tygodniu, nie w pierwszym, jak się powszechnie zakłada.
>
> Pokazuję to firmom, które już mają większą skalę i poszukują, gdzie tracą — bo na małych zbiorach to się chowa w szumie.
>
> Jeśli chcesz, mogę przesłać krótki opis (1 strona PDF) albo umówić się na 15 minut, żeby zobaczyć, czy to ma sens dla Twojego setupu.
>
> Anna
> XYZ Solutions

## Flagi do weryfikacji

- ❗ „92% klientów czerpie korzyści" — z palca, usunięto
- ❗ „47% wzrost sprzedaży" — z palca, usunięto
- ⚠️ „⅓ klientów odpada w drugim tygodniu" — przykład; w prawdziwym mailingu sprawdź realne liczby
- ⚠️ Fake urgency („50% zniżka tylko dziś") — usunięto, zastąpiono niskim-ciśnieniowym CTA

## Co zostało zachowane / dlaczego

**Zachowano:**
- Personalizacja przez imię
- Konkretna oferta (PDF + 15-min call)
- Sygnatura imię + firma

**Usunięto:**
- Wszystkie emoji
- Wszystkie wykrzykniki (poza zerem)
- Title/Senior Manager — irrelevant dla CTA
- Linki w stopce — dystraktor

**Dodano:**
- Konkretną liczbę („dwa tygodnie temu", „1 strona PDF", „15 minut")
- Opinię/observację (`⅓ klientów w 2. tygodniu, nie w 1.`)
- Niepewność/uczciwość (`bo na małych zbiorach to się chowa w szumie`)
- CTA dwa-stopniowe (PDF *albo* call) zamiast jednego natarczywego

## Statystyki

|  | Przed | Po |
|---|---|---|
| Słowa | 130 | 84 |
| Wykrzykniki | 8 | 0 |
| Emoji | 7 | 0 |
| AI-słowa | 5 | 0 |
| Niepotwierdzone statystyki | 2 | 1 (oznaczona) |
| Konkretne mierzalne fakty | 0 | 4 |
