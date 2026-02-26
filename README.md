# D.JANC WORKSHOP — Strona Internetowa

Strona internetowa warsztatu samochodowego **D.JANC WORKSHOP** w Wielkiej Nieszawce k. Torunia.

**Strona (live):** [djanc-workshop.vercel.app](https://djanc-workshop.vercel.app) | Docelowo: djanc.pl

---

## Szybki start dla Tino

### 1. Pobierz na swój komputer

Zainstaluj najpierw: [Node.js](https://nodejs.org) + [Git](https://git-scm.com) + [VS Code](https://code.visualstudio.com)

```bash
git clone https://github.com/kowalcg/D.JANC-WORKSHOP.git
cd D.JANC-WORKSHOP
npm install
npm run dev
```

Otwórz przeglądarkę: **http://localhost:4321**

### 2. Edytuj treść

Wszystkie strony są w folderze `src/pages/`:

| Plik | Strona |
|------|--------|
| `index.astro` | Strona główna |
| `kontakt.astro` | Kontakt |
| `cennik.astro` | Cennik |
| `faq.astro` | FAQ |
| `o-nas.astro` | O nas |
| `opinie.astro` | Opinie |
| `uslugi/diagnostyka-komputerowa-torun.astro` | Diagnostyka |
| `uslugi/mechanika-ogolna-torun.astro` | Mechanika |
| `uslugi/wulkanizacja-torun.astro` | Wulkanizacja |
| `uslugi/klimatyzacja-samochodowa-torun.astro` | Klimatyzacja |
| `uslugi/wymiana-oleju-torun.astro` | Wymiana oleju |
| `uslugi/naprawa-hamulcow-torun.astro` | Hamulce |

Edytuj tekst między tagami HTML — nie musisz rozumieć kodu.

### 3. Wyślij zmiany na serwer

```bash
git add .
git commit -m "opis co zmieniłem"
git push
```

Vercel automatycznie zaktualizuje stronę w ~2 minuty.

---

## Wdrożenie na Vercel

**Strona jest już wdrożona:** [djanc-workshop.vercel.app](https://djanc-workshop.vercel.app)

Każdy `git push` do gałęzi `main` automatycznie aktualizuje stronę na Vercel (~2 minuty).

Aby podpiąć domenę `djanc.pl`: Wejdź na [vercel.com](https://vercel.com) → **Settings → Domains** → dodaj `djanc.pl` → ustaw rekord DNS u rejestratora domeny.

---

## O projekcie

| Pole | Wartość |
|------|---------|
| **Technologia** | Astro 5.x + Tailwind CSS v4 |
| **Hosting** | Vercel (strona statyczna) |
| **Język** | Polski (zero angielskiego) |
| **Adres** | ul. Toruńska 25, Wielka Nieszawka, 87-165 |
| **Telefon** | 451-273-483 / +48 451 273 483 |
| **Obsługiwany obszar** | Wielka Nieszawka + Toruń + powiat toruński |

---

## Wszystkie strony (15 stron)

| URL | Opis | Słowo kluczowe |
|-----|------|----------------|
| `/` | Strona główna | warsztat samochodowy Toruń |
| `/uslugi` | Hub wszystkich usług | usługi warsztatu Toruń |
| `/uslugi/diagnostyka-komputerowa-torun` | Diagnostyka OBD — od 80 PLN | diagnostyka komputerowa Toruń |
| `/uslugi/mechanika-ogolna-torun` | Mechanika ogólna | mechanik Toruń |
| `/uslugi/wulkanizacja-torun` | Wymiana opon — od 36 PLN/szt | wulkanizacja Toruń |
| `/uslugi/klimatyzacja-samochodowa-torun` | Klimatyzacja — od 150 PLN | klimatyzacja samochodowa Toruń |
| `/uslugi/wymiana-oleju-torun` | Wymiana oleju — 150–350 PLN | wymiana oleju Toruń |
| `/uslugi/naprawa-hamulcow-torun` | Hamulce — od 200 PLN | naprawa hamulców Toruń |
| `/cennik` | Cennik wszystkich usług | cena warsztatu Toruń |
| `/kontakt` | NAP, mapa, formularz, dojazd | kontakt warsztat Toruń |
| `/faq` | 21 pytań i odpowiedzi | pytania mechanik Toruń |
| `/o-nas` | Damian Janc, filozofia, sprzęt | |
| `/blog` | Blog motoryzacyjny | |
| `/blog/kiedy-wymieniac-opony-na-zimowe` | Poradnik wymiany opon | |
| `/opinie` | Opinie klientów | |

---

## Co zawiera każda strona usługi

Każda strona usługi (`/uslugi/...`) zawiera:
- **H1** z dokładnym słowem kluczowym (np. "Wulkanizacja Toruń")
- **Cena w pierwszym zdaniu** — format answer-first dla AI (ChatGPT, Perplexity, Google AI)
- **Co obejmuje** — lista punktowana
- **Nasz proces** — 5 kroków
- **Tabela cenowa** w PLN
- **FAQ** — min. 5 pytań i odpowiedzi
- **Przycisk telefonu** — `tel:+48451273483`
- **Google Maps** — iframe z adresem ul. Toruńska 25
- **Schema JSON-LD** — Service + FAQPage w `<head>`

---

## SEO i schematy

Strona jest zoptymalizowana pod lokalne SEO i widoczność w AI:

- **LocalBusiness + AutoRepair** schema na stronie głównej
- **Service + FAQPage** schema na każdej stronie usługi
- **FAQPage** schema z 21 pytaniami na `/faq`
- **sitemap-index.xml** — generowany automatycznie przy buildzie
- **robots.txt** — `Allow: /`, link do sitemap
- **Open Graph** meta tagi na każdej stronie
- **hreflang="pl"** + `lang="pl"` na całej stronie
- **Canonical URL** na każdej stronie

---

## Co zrobić po wdrożeniu

1. **Google Business Profile** — zarejestruj na google.com/business (najważniejszy krok SEO)
2. **Prawdziwe zdjęcia** — zastąp placeholder zdjęciami warsztatu, Damiana, samochodów
3. **Godziny otwarcia** — zaktualizuj godziny w `src/layouts/Layout.astro` (stopka) i na `/kontakt`
4. **Google Analytics** — dodaj GA4 tracking ID w `src/layouts/Layout.astro` (placeholder `<!-- GA4 -->`)
5. **Opinie Google** — zbieraj od każdego klienta, aktualizuj `/opinie`
6. **Aktualizuj ceny** — jeśli zmienią się ceny, edytuj pliki usług i `/cennik`

---

## Jak to zostało zbudowane

Strona powstała w lutym 2026 przy użyciu:

1. **Badania rynku** — analiza konkurentów (Celmer, AutoSerwis Toruń, Żurek, Auto Dna), research słów kluczowych dla rynku polskiego, analiza luk w treści
2. **Strategia pozycjonowania** — "Uczciwy warsztat: znasz ceny zanim przyjedziesz"
3. **PRD (Product Requirements Document)** — 18 user stories z kryteriami akceptacji
4. **Ralph** — autonomiczny agent AI, który zbudował całą stronę automatycznie na podstawie PRD
5. **Claude Code** — nadzorowanie procesu, konfiguracja, debug

**Stack techniczny:**
- [Astro](https://astro.build) 5.x — framework (szybkie strony statyczne, idealne dla SEO)
- [Tailwind CSS](https://tailwindcss.com) v4 — stylowanie
- [Vercel](https://vercel.com) — hosting (darmowy plan wystarczy)

**Całkowity czas budowy:** ~1 noc (Ralph zbudował wszystkie 18 stron w jednej sesji)

---

## Komendy

```bash
npm run dev      # uruchom lokalnie na localhost:4321
npm run build    # zbuduj do folderu dist/
npm run preview  # podejrzyj build lokalnie
```

---

*Zaprojektowane przez Grega Kowalczyka | Zbudowane przez Ralph (AI) + Claude Code | Luty 2026*
