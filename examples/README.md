# Examples — before/after

5 par tekstów w różnych domenach. Każdy plik pokazuje:

1. **Przed** — AI-tekst (zwykle wygenerowany albo zaobserwowany w produkcji)
2. **Co skill łapie** — które § wzorca są aktywne
3. **Po** — humanizacja
4. **Flagi do weryfikacji** — fakty/halucynacje do sprawdzenia
5. **Statystyki** — kwantyfikowalna różnica przed/po

## Lista

| # | Plik | Domena | Cel |
|---|---|---|---|
| 01 | [01-blog.md](01-blog.md) | Blog techniczny | Podstawowy use case |
| 02 | [02-marketing.md](02-marketing.md) | Email/LinkedIn marketing | Najgęstsze AI-tellsy |
| 03 | [03-naukowy.md](03-naukowy.md) | Popularnonaukowy | Subtelne tellsy + zachowanie merytoryki |
| 04 | [04-formalny.md](04-formalny.md) | **REGRESSION TEST** — umowa / regulamin | Pokazuje, że skil **NIE** humanizuje formalnego tekstu |
| 05 | [05-mieszany.md](05-mieszany.md) | Tekst mix human+AI | Najtrudniejszy — selektywna humanizacja |

## Jak czytać przykłady

**Najpierw przeczytaj „Przed"** bez patrzenia na resztę. Pomyśl: gdzie są AI-tellsy? Co byś zmienił?

**Potem porównaj** z sekcją „Co skill łapie" — sprawdź, czy zauważyłeś to samo.

**Na końcu „Po"** — zobacz, jak skil to przepisał. Czy zgadzasz się?

## Trudność

```
01-blog        ★★☆☆☆  podstawowy
02-marketing   ★☆☆☆☆  oczywiste tellsy, łatwe do złapania
03-naukowy     ★★★☆☆  subtelne, wymaga osądu
04-formalny    ★★★★☆  regression — nie zepsuć
05-mieszany    ★★★★★  granica human/AI
```

## Note: te przykłady są syntetyczne

„Przed" zostały **wygenerowane** przeze mnie (autora) jako reprezentatywne sample, nie pochodzą z prawdziwych publikacji. „Po" to humanizacja zgodna z SKILL.md.

Real-world examples (z prawdziwych źródeł) planowane w przyszłej wersji po feedbacku użytkowników.

## Contributing

Masz dobry przykład AI-tekstu po polsku z prawdziwego źródła? PR mile widziany. Dodaj plik `examples/06-...md` w tym samym formacie.

Pamiętaj: jeśli tekst pochodzi z czyjejś publikacji, zachowaj atrybucję. Jeśli z Twoich własnych — OK.
