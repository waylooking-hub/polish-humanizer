# Przykład 04 — Tekst formalny (REGRESSION TEST)

**Domena:** umowa, regulamin, dokumentacja techniczna
**Złożoność:** *odwrotna* — tu skil **NIE** powinien usuwać formalności
**Tellsy:** §8 (halucynacje skrótów), §24 (wersaliki), `Etyka humanizacji`

## Cel tego przykładu

Pokazuje, że skil ma **kontekst awareness**. W tekstach formalnych:
- ✅ Zachowuje stronę bierną
- ✅ Zachowuje konstrukcje typu „Strony zobowiązują się"
- ✅ Zachowuje paragrafy i numerację
- ❌ Nie dodaje autoironii
- ❌ Nie wsadza wtrąceń typu „no i"
- ✅ Usuwa **tylko** czyste AI-tellsy: halucynacje, błędne wersaliki, kalki anglicyzmów

## Przed (AI z drobnymi błędami)

> # § 5. Zobowiązania Stron
>
> 5.1. Strony Niniejszej Umowy zobowiązują się do wzajemnego informowania o Wszelkich Okolicznościach mogących Wpływać na realizację niniejszej umowy. Wszelkie zmiany niniejszej umowy wymagają formy pisemnej pod rygorem nieważności.
>
> 5.2. W przypadku, gdy Strona dowie się o naruszeniu, niezwłocznie powiadomi drugą Stronę zgodnie z procedurą określoną w § 7. Adresowanie kwestii powinno nastąpić w terminie 14 dni roboczych.
>
> 5.3. Niniejsza umowa wchodzi w życie z dniem podpisania przez obie Strony i obowiązuje przez okres 24 miesięcy. Według raportu Ministerstwa Cyfryzacji RP z 2024 roku, około 67% umów o tej strukturze jest renegocjowane przed upływem terminu.
>
> 5.4. Wszelka korespondencja będzie kierowana na adresy wskazane w preambule. Strony zobowiązują się do informowania o zmianach adresu w terminie 7 dni od dnia ich nastąpienia.

## Co skill **łapie**

- §24 wersaliki w środku tekstu: „Niniejszej Umowy", „Wszelkich Okolicznościach", „Wpływać", „Stron"
- §10 anglicyzm „adresowanie kwestii" → „odniesienie się do kwestii" / „rozwiązanie kwestii"
- §8 halucynacja statystyki: „raport Ministerstwa Cyfryzacji" + „67% umów" — w umowie to nie ma sensu, bo dokument prawny nie cytuje statystyk
- §37 wypełniacz: „W przypadku, gdy" → można skrócić („Jeśli"), ale w prawnym kontekście „W przypadku" jest często wymagane przez konwencję redakcyjną — **ZACHOWAĆ**

## Co skill **NIE** powinien zmieniać

- ❌ „Strony zobowiązują się" — strona bierna jest tu częścią rejestru
- ❌ „pod rygorem nieważności" — termin prawny
- ❌ „§ 5.1, 5.2..." — numeracja
- ❌ „Niniejsza umowa" — formuła prawna
- ❌ Nie dodawać humoru, autoironii, „no i", „prawda?" itp.

## Po (humanizacja kontekstowo-świadoma)

> # § 5. Zobowiązania Stron
>
> 5.1. Strony niniejszej umowy zobowiązują się do wzajemnego informowania o wszelkich okolicznościach mogących wpływać na realizację niniejszej umowy. Wszelkie zmiany niniejszej umowy wymagają formy pisemnej pod rygorem nieważności.
>
> 5.2. W przypadku, gdy Strona dowie się o naruszeniu, niezwłocznie powiadomi drugą Stronę zgodnie z procedurą określoną w § 7. Odniesienie się do kwestii powinno nastąpić w terminie 14 dni roboczych.
>
> 5.3. Niniejsza umowa wchodzi w życie z dniem podpisania przez obie Strony i obowiązuje przez okres 24 miesięcy.
>
> 5.4. Wszelka korespondencja będzie kierowana na adresy wskazane w preambule. Strony zobowiązują się do informowania o zmianach adresu w terminie 7 dni od dnia ich nastąpienia.

## Co konkretnie zmieniono

| Zmiana | Powód |
|---|---|
| `Niniejszej Umowy` → `niniejszej umowy` | §24 — wersaliki w środku zdania |
| `Wszelkich Okolicznościach` → `wszelkich okolicznościach` | §24 |
| `mogących Wpływać` → `mogących wpływać` | §24 |
| `Stron` → `Strony` (gdzie stosowne) | §24 (zachowano wielką literę gdzie odnosi się do oznaczenia w preambule) |
| `Adresowanie kwestii` → `Odniesienie się do kwestii` | §10 — anglicyzm „adresować" |
| Usunięto „Według raportu Ministerstwa..." z 5.3 | §8 — halucynacja + irrelevant w umowie |

## Czego **NIE** zmieniono (zachowane formalności)

- ✅ „Strony zobowiązują się" (strona bierna — feature)
- ✅ „pod rygorem nieważności" (termin prawny)
- ✅ „w przypadku, gdy" (konwencja prawna; §37 mówi że to wypełniacz, ale w umowie OK)
- ✅ Numeracja paragrafów § 5.1, 5.2, 5.3, 5.4
- ✅ „Niniejsza umowa" jako formuła
- ✅ Czas przyszły „będzie kierowana"

## Uwaga: skil zostawił „W przypadku"

W prawym kontekście (umowy, regulaminy, statuty), niektóre formalne konstrukcje są **wymagane** przez konwencję redakcyjną i nie powinny być zamieniane na „Jeśli". §37 (wypełniacze) **nie stosuje się** do tekstów prawnych — tylko do tekstów stylistycznie luźnych.

## Etyka — ważne

Tego przykładu **nie** powinno się traktować jako szablonu „jak humanizować umowę, żeby ukryć użycie AI". Cel jest inny:
- Usunięcie błędów AI (halucynacji, kapitalizacji)
- Zachowanie poprawności prawnej
- Pomoc redaktorowi/prawnikowi przeczytać szybciej

W kontekście dokumentu prawnego — **zawsze** finalna wersja powinna przejść przez prawnika.

## Statystyki

|  | Przed | Po |
|---|---|---|
| Słowa | 144 | 122 |
| Wersaliki w środku zdań | 6 | 0 |
| Halucynacje | 1 | 0 |
| Strona bierna (zachowana) | 4 | 4 |
| Numeracja paragrafów | 4 | 4 |
| Wprowadzona autoironia | 0 | 0 ✓ |
| Wprowadzone wtrącenia („no i", „prawda?") | 0 | 0 ✓ |
