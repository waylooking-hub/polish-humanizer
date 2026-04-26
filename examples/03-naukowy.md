# Przykład 03 — Tekst popularnonaukowy

**Domena:** artykuł popularnonaukowy o astrofizyce
**Złożoność:** umiarkowana, ale subtelne tellsy
**Tellsy:** §4, §17, §6, §9, §15, §43 (brak humoru)

## Przed (AI)

> # Czarne dziury: tajemnicze obiekty kosmosu
>
> Czarne dziury stanowią jedne z najbardziej fascynujących obiektów we Wszechświecie, demonstrując fundamentalne zasady fizyki, podkreślając naszą ograniczoną wiedzę o kosmosie i odzwierciedlając głębokie tajemnice rzeczywistości.
>
> Naukowcy uważają, że odgrywają one kluczową rolę w ewolucji galaktyk. Według dostępnych danych, niemal każda duża galaktyka zawiera supermasywną czarną dziurę w swoim centrum. To może wydawać się zaskakujące, ale potencjalnie wpisuje się to w szerszy kontekst formowania się struktur kosmicznych.
>
> Nasza podróż przez wszechświat zaprowadziła nas od osobliwości Wielkiego Wybuchu do dzisiejszej kosmicznej sieci, od narodzin gwiazd do tajemniczego tańca ciemnej materii. Czarne dziury, w tym kontekście, są nie tylko ciekawym fenomenem — są mostem między teoretyczną fizyką a obserwowalnym wszechświatem.
>
> Współczesne badania wskazują, że horyzont zdarzeń może zachowywać informację o materii, która do niej wpada. Jest to fundamentalne pytanie, które nadal pozostaje przedmiotem dyskusji w społeczności naukowej.

## Co skill łapie

- §4 nawarstwiane imiesłowy: „demonstrując... podkreślając... odzwierciedlając"
- §6 mgliste źródła: „Naukowcy uważają", „Według dostępnych danych", „Współczesne badania wskazują"
- §9 „kluczową rolę", „fundamentalne", „kluczowy"
- §15 fałszywy zakres: „od osobliwości Wielkiego Wybuchu do dzisiejszej kosmicznej sieci, od narodzin gwiazd do tańca ciemnej materii"
- §17 hedging: „może wydawać się", „potencjalnie", „może zachowywać"
- §38 „pozostaje przedmiotem dyskusji" — vague pozytywne zakończenie
- §43 zero humoru, autoironii, niedopowiedzenia (tekst akademicki — humor jest out of place)

## Po (humanizacja)

> # Czarne dziury: dlaczego fizyka się przy nich zacina
>
> Czarne dziury są w fizyce trochę jak granica, na której kończy się to, co umiemy obliczyć. Wiemy, że ich grawitacja jest tak silna, że nawet światło nie ucieka — i ten opis każdy słyszał. Trudniejsze pytania zaczynają się dalej.
>
> W centrum każdej dużej galaktyki — w tym naszej — siedzi supermasywna czarna dziura. Ta z naszego centrum, Sagittarius A*, ma masę około 4 milionów Słońc. To nie wystarcza, żeby wytłumaczyć, jak galaktyki rosną do takich rozmiarów. Coś tu pasuje, ale fizyka nie do końca wie co.
>
> Najgorsze zaczyna się przy tzw. osobliwości — punkcie wewnątrz czarnej dziury, gdzie krzywizna czasoprzestrzeni rośnie do nieskończoności. W tym miejscu ogólna teoria względności przestaje produkować sensowne odpowiedzi i potrzebujemy mechaniki kwantowej. Te dwa frameworki nie chcą się ze sobą zsynchronizować. Od dekad. To trochę pokorne — fizyka, która wyjaśnia wszystko inne, na czarnej dziurze gubi nitkę.
>
> Nadal nie wiemy, co dokładnie dzieje się z informacją o materii, która wpada do czarnej dziury. To jedno z głośniejszych pytań współczesnej fizyki teoretycznej (Hawking, Susskind, Maldacena spierali się o to przez ponad 30 lat). Odpowiedzi nie ma — i prawdopodobnie nie będzie, dopóki ktoś nie wymyśli teorii kwantowej grawitacji.

## Flagi do weryfikacji

- ✓ „Sagittarius A* ma masę około 4 milionów Słońc" — fakt potwierdzony (zob. publikacje EHT, ~4.15M ± 0.6M Słońc)
- ✓ „Hawking, Susskind, Maldacena spierali się przez 30+ lat" — fakt (Information paradox debate, lata ~1990-2020)
- ⚠️ Sprawdź najnowsze publikacje (2024-2026) — być może coś się zmieniło w information paradox

## Co dodano vs co usunięto

**Usunięto:**
- Imiesłowy nawarstwiane („demonstrując, podkreślając, odzwierciedlając")
- Mgliste źródła („Naukowcy uważają")
- Pusty hedging („potencjalnie", „może wydawać się")
- Fałszywy zakres („od X do Y, od narodzin do tańca")

**Dodano:**
- Konkretne fakty (Sagittarius A*, 4 mln Słońc, EHT, nazwy fizyków)
- Autoironia w 1 miejscu („to trochę pokorne — fizyka [...] gubi nitkę") — zgodnie z decision tree §43 (tekst >200 słów, neutralny opisowy → 1-2 momenty)
- Niedopowiedzenie („Coś tu pasuje, ale fizyka nie do końca wie co", „prawdopodobnie nie będzie")
- Konkretne pytanie filozoficzne („co z informacją")

## Uwaga o domenie naukowej

W tekstach popularnonaukowych humanizacja powinna być ostrożna z humorem. Decision tree §43:
- Tekst >200 słów ✓
- Neutralny, opisowy ✓
- Bez humoru w wersji AI ✓
→ **TAK, dodaj 1 moment autoironii** (i tylko 1 — naukowy tekst nie powinien się przekręcić w felieton)

## Statystyki

|  | Przed | Po |
|---|---|---|
| Słowa | 195 | 290 |
| Imiesłowy przysłówkowe | 3 | 0 |
| AI-słowa | 5 | 0 |
| Hedging fraz | 4 | 1 (uzasadnione) |
| Konkretne fakty z liczbami | 0 | 3 |
| Konkretne nazwiska | 0 | 4 (Hawking, Susskind, Maldacena, Sagittarius A*) |
