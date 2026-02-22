# Ralph CLAUDE.md — D.JANC WORKSHOP

## Project
Auto mechanic website for D.JANC WORKSHOP. Polish-language. Astro 5 + Tailwind CSS + Vercel.

## Quality Check Command
```
npm run build
```
Must pass with zero errors before any story is marked complete.

## Framework
- Astro 5.x with Tailwind CSS
- Static output (output: 'static')
- Site: https://djanc.pl
- All pages: .astro files in src/pages/

## Language
Polish throughout ALL content. Zero English content on any page.
Polish characters must work: ą ę ó ś ć ń ł ź ż

## Business Details (Use Exactly)
```
Name: D.JANC WORKSHOP
Address: ul. Toruńska 25, Wielka Nieszawka
Postal: 87-165
Region: kujawsko-pomorskie
Phone display: 451-273-483
Phone href: tel:+48451273483
Geo: 53.0500 N, 18.5833 E
```

## Phone Link Pattern (EVERY page, min 3x on homepage)
```html
<a href="tel:+48451273483" class="...">451-273-483</a>
```

## Design Tokens
```
Primary: #1a2332 (deep navy)
Accent: #e17055 (orange — all CTAs)
BG: #ffffff
BG-alt: #f8f9fa
Text: #2d3436
```

## Layout Pattern
Every .astro page imports Layout.astro which includes:
- html lang="pl"
- Sticky header with tap-to-call button
- JSON-LD schema in <head> (page-specific, passed as prop)
- Open Graph tags
- Tailwind import from src/styles/global.css

## Schema Pattern
Every page has JSON-LD in <head>:
- Homepage: AutoRepair + LocalBusiness
- Service pages: Service + FAQPage
- /faq: FAQPage (20+ Q&As)
- /kontakt: LocalBusiness with openingHoursSpecification

## Service Pages Template (6 pages)
Each service page at /uslugi/[slug]-torun must have:
1. H1 = "[Service Name] Toruń"
2. Opening paragraph: price in PLN + duration (answer-first)
3. Co obejmuje (bullets)
4. Nasz proces (numbered steps)
5. Cennik table
6. FAQ section (min 5 Q&As)
7. CTA: Zadzwoń Teraz button
8. Google Maps embed
9. FAQPage + Service JSON-LD schema

## Acceptance Criteria (All Stories)
- npm run build passes
- H1 contains target keyword in Polish
- href="tel:+48451273483" present
- Schema markup in <head>
- No horizontal scroll on mobile
- All Polish characters render correctly

## PRD Location
scripts/ralph/prd.json
