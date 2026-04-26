# Przykład 05 — Tekst mieszany (human + AI)

**Domena:** post na blog/Substack — pierwszy akapit autorski, reszta poprawiona AI
**Złożoność:** wymaga **selektywnej** humanizacji
**Tellsy:** §1, §2, §10, §13, §43 + regression awareness

## Cel tego przykładu

Pokazuje, że skil **rozpoznaje granicę między fragmentem napisanym przez człowieka a fragmentem AI**. Nie nadgryza pierwszego, koncentruje się na drugim.

To jeden z najtrudniejszych use case'ów — bo wymaga, żeby AI-edytor:
1. Wyczuł rytm autora w pierwszej części
2. Dopasował drugą część do tego rytmu
3. Nie zamienił całego tekstu w „swój" styl

## Przed (mieszanка)

> # Dlaczego rzucam Slacka — relacja z trzeciego tygodnia
>
> Trzeci tydzień bez Slacka i już mam pierwsze obserwacje. Pierwsza: nikt nie umarł. Druga: ludzie piszą emaile, których faktycznie nie wstyd przeczytać — pełne zdania, akapity, ktoś pomyślał zanim napisał. Trzecia: nie tęsknię. To było zaskoczenie. Myślałem, że mi będzie brakowało tych szybkich wymian, ale okazało się, że 80% tych „szybkich wymian" to były pytania, na które każdy mógłby sobie odpowiedzieć po pięciu minutach myślenia.
>
> [tekst dalej kontynuuje pierwotny autor — tu wkracza AI w kolejnym akapicie:]
>
> Nie sposób nie zauważyć, że w dzisiejszym dynamicznie zmieniającym się świecie pracy zdalnej, narzędzia komunikacji asynchronicznej odgrywają kluczową rolę. Na koniec dnia, dedykowane rozwiązania robią różnicę dla zespołów inżynierskich. Email, jako przełomowy sposób komunikacji, dostarcza wartość poprzez umożliwienie głębokiej pracy.
>
> Ponadto, asynchroniczność pozwala na adresowanie potrzeb różnych stref czasowych. Co więcej, redukuje overhead poznawczy. W istocie, jest to gamechanger.

## Co skill **rozpoznaje**

**Pierwszy akapit (HUMAN):**
- ✅ Rytm zmienny: „nikt nie umarł" / „pełne zdania, akapity, ktoś pomyślał" / „nie tęsknię. To było zaskoczenie."
- ✅ Konkretne liczby (`80%`)
- ✅ Autoironia („myślałem, że mi będzie brakowało, ale...")
- ✅ Wtrącenia („— pełne zdania, akapity, ktoś pomyślał zanim napisał")
- ✅ Pierwsza osoba („Myślałem", „nie tęsknię", „mi będzie brakowało")

→ **Decision tree §43, pkt 2: tekst już ma ironię/wtrącenia → NIE dodawaj nic.** Zachować w całości.

**Drugi i trzeci akapit (AI):**
- §1 „Nie sposób nie zauważyć", „w dzisiejszym dynamicznie zmieniającym się świecie"
- §2 „kluczową rolę", „przełomowy", „gamechanger"
- §10 „na koniec dnia", „dedykowane rozwiązania", „robią różnicę", „dostarcza wartość", „adresowanie potrzeb"
- §13 „Ponadto", „Co więcej", „W istocie" — sztywne spójniki
- §9 nadmiar AI-słów

→ **Przepisać całkowicie.**

## Po (humanizacja selektywna)

> # Dlaczego rzucam Slacka — relacja z trzeciego tygodnia
>
> Trzeci tydzień bez Slacka i już mam pierwsze obserwacje. Pierwsza: nikt nie umarł. Druga: ludzie piszą emaile, których faktycznie nie wstyd przeczytać — pełne zdania, akapity, ktoś pomyślał zanim napisał. Trzecia: nie tęsknię. To było zaskoczenie. Myślałem, że mi będzie brakowało tych szybkich wymian, ale okazało się, że 80% tych „szybkich wymian" to były pytania, na które każdy mógłby sobie odpowiedzieć po pięciu minutach myślenia.
>
> [pierwszy akapit zachowany w 100% bez zmian]
>
> Coś jeszcze: emailowanie wymusza na mnie myślenie w blokach. Nie mogę napisać czterech linii i czekać 30 sekund na odpowiedź — bo nie ma takiej dynamiki. Albo opisuję problem porządnie i daje druga stronie 24 godziny na odpowiedź, albo się nie opisuję wcale i robię sam. To zamyka ¾ rozmów, które na Slacku ciągnęłyby się przez cały dzień.
>
> Ze stref czasowych: część zespołu jest w Indiach. Slack robił z tego problem (każda wiadomość o 3 nad ranem zostawała nieprzeczytana albo mnie budziła). Email po prostu czeka. Nikt się nie obraża, bo nikt nie oczekuje natychmiastowej odpowiedzi. To dziwnie ulegające pomysłowi „komunikacja powinna być szybka", ale pracuje się lepiej.

## Kluczowa decyzja AI-edytora

**Co skil zrobił:**
1. **Pierwszy akapit:** zachowany dosłownie. Nie zamieniono ani jednego słowa. Decision tree §43 zatrzymał interwencję.
2. **Drugi akapit AI:** całkowicie przepisany w stylu pierwszego akapitu (rytm zmienny, konkrety, „24 godziny", „¾ rozmów").
3. **Trzeci akapit AI:** kontynuacja w stylu autora, ale z konkretem (`Indie`, `3 nad ranem`).
4. **Nie dodano** „No i", „prawda?", autoironii ponad to, co już było (autor sam w pierwszym akapicie używa autoironii — drugi akapit może naturalnie kontynuować).

## Trudność / co wymaga osądu

To najtrudniejszy przypadek, bo skil musi:
- Wyczuć **głos autora** w pierwszym akapicie (rytm, słownictwo, poziom formalności)
- Odtworzyć ten głos w drugim, przepisanym fragmencie
- Nie dodać własnych „ulubionych" wtrąceń AI-edytora (§44 mówi „nie wciskaj wtrąceń wszędzie")

W praktyce: jeśli AI-edytor pisze „No i jeszcze jedna sprawa..." — to **też** jest AI-tell. Wtrącenia są naturalne, gdy AI je naśladuje, ale stają się sztuczne, gdy są nadużywane.

## Statystyki

|  | Przed (akapit AI) | Po |
|---|---|---|
| Słowa w fragmencie AI | 91 | 162 |
| AI-słowa | 6 | 0 |
| Sztywne spójniki | 3 | 0 |
| Frazeologiczne anglicyzmy | 5 | 0 |
| Konkretne liczby | 0 | 3 (`24 godziny`, `¾`, `3 nad ranem`) |
| Geograficzne konkrety | 0 | 1 (`Indie`) |

## Najważniejsze: pierwszy akapit niezmieniony

| Test | Wynik |
|---|---|
| Słowa w pierwszym akapicie zmienione | 0 ✓ |
| Stylistyczne ingerencje w autorską prozę | 0 ✓ |
| Dodane „skilowe" wtrącenia | 0 ✓ |

To najmocniejszy regression test. Skil **nie nadgryza** dobrego polskiego tekstu.
