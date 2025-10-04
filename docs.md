# Dokumentacja projektowa

## Cel projektu

Stworzenie nowoczesnej, responsywnej strony wizytówki MLM Legal – kancelarii radcy prawnego rozpoczynającej działalność, z sekcją blogową i elementami brandingowymi.

## Architektura

- **Brak backendu**: wyłącznie statyczne HTML + inline CSS + odrobina JS (menu mobilne).
- **Pliki**: 5 stron (home + blog + 3 artykuły). Każda zawiera kompletny layout.
- **Fonty**: Google Fonts (Playfair Display, Inter) ładowane per strona.
- **Skrypty**: menu mobilne (toggle klasy `open`), brak frameworków.

## Przepływ pracy

1. **Planowanie**: Issue → PR → review → merge.
2. **Styl graficzny**: oparty na palecie granat/złoto/krem. Wzorce i prompty w `image-prompts.md`.
3. **Biblioteki UI**: AOS (animacje on scroll), VanillaTilt (efekt 3D kart) – ładowane z CDN, planuj fall-back offline.
4. **Treści**: Strona główna + blog + 3 artykuły (placeholders). Docelowe teksty z mlm-legal.pl.

## Dalszy rozwój

- **SEO**: dodać meta tagi (tytuły/description per strona), strukturalne dane JSON-LD.
- **Analityka**: wpięcie Google Analytics lub innego narzędzia (skrypt z consentem).
- **Formularz**: integracja z backendem (np. Netlify Forms, formspree) lub dedykowane API.
- **Blog**: migracja do generatora (11ty/Astro) aby zarządzać większą liczbą wpisów.
- **WCAG**: przeprowadzić szczegółowy audyt dostępności (kontrast, focus, ARIA).

## Konwencje commitów

- `[feat]`, `[fix]`, `[docs]`, `[style]`, `[refactor]`, `[chore]` – prefixy w summary.
- Maks 72 znaki w pierwszej linii, opis w czasie teraźniejszym.

## Checklist przed PR

- [ ] Responsywność na 1440 / 1280 / 768 / 375 px.
- [ ] Form validation i focus states.
- [ ] Zgodność z design systemem (kolory, typografia).
- [ ] Aktualizacja dokumentacji (README/CONTRIBUTING/image-prompts) gdy wymagane.

## Media guidelines

- Format: PNG (względnie WebP opcjonalnie), brak SVG inline.
- Nazwy: `sekcja-opis.png`.
- Rozdzielczości określone w `image-prompts.md`.
- Produkcja grafiki: generacja AI + ręczna edycja (Photoshop/Figma), następnie optymalizacja.

## Plan release v1.0

1. Uzupełnić finalne grafiki.
2. Zweryfikować treści bloga (pobrać z serwisu źródłowego).
3. Dodać politykę prywatności / cookies (linki w stopce).
4. Zrobić smoke test na urządzeniach (iOS Safari, Android Chrome).
5. Opublikować na wybranej platformie statycznej.
