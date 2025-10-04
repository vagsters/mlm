# MLM Legal – Strona wizytówka

Static marketing site for the MLM Legal law office (Polish language). This repository contains a hand-crafted HTML/CSS build optimised for quick local preview and deployment to static hosts (GitHub Pages, Netlify, Vercel, etc.).

## Struktura projektu

```
./
├── index.html                 # Strona główna
├── blog.html                  # Listing główny bloga
├── blog-omnibus.html          # Artykuł: dyrektywa Omnibus
├── blog-rodo-bledy.html       # Artykuł: RODO w praktyce
├── blog-whistleblowing.html   # Artykuł: Whistleblowing
├── images/                    # Grafiki (placeholders PNG)
└── image-prompts.md           # Prompty AI do wygenerowania grafik
```

## Wymagania

- Przeglądarka wspierająca HTML5/CSS3.
- Brak zależności npm – projekt działa jako statyczny bundle.
- CDN: [AOS 2.3.4](https://michalsnik.github.io/aos/) (animacje przewijania), [VanillaTilt 1.7.3](https://micku7zu.github.io/vanilla-tilt.js/) (efekt tilt kart). Dostęp wymagany przy podglądzie online – w środowisku offline pobierz assety lokalnie.

## Uruchomienie lokalne

1. Sklonuj repozytorium.
2. Uruchom dowolny serwer statyczny (np. `python3 -m http.server 8000`) w katalogu projektu.
3. Wejdź na `http://localhost:8000/index.html`.

## Deployment

Strona może być hostowana na dowolnej infrastrukturze statycznej. Zalecane kroki:

1. Zbuduj finalny pakiet (opcjonalnie minifikuj HTML/CSS).
2. Wdróż pliki `*.html`, katalog `images/` oraz ewentualne zasoby dodatkowe.
3. Skonfiguruj nagłówki cache (np. dla grafiki dłuższy TTL, dla HTML krótszy).

## Konwencje stylistyczne

- Język UI: polski.
- Typografia: `Playfair Display` (nagłówki), `Inter` (tekst). Czcionki pobierane z Google Fonts (link w każdej stronie).
- Paleta: granaty (`#0F1F35`, `#0B1728`), złoto (`#C9A05C`), krem (`#F5F1EA`), akcenty bieli.
- Rozmiary sekcji dostosowane do układu 12 kolumn na desktopie, układ jednokolumnowy na ≤1024px.

## Grafiki

Wszystkie obrazy (placeholders) znajdują się w folderze `images/` i są w formacie PNG. Docelowe grafiki należy wygenerować według promptów opisanych w `image-prompts.md`. Zalecania:

- `hero-abstract.png`: tło hero 1600×900.
- `about-collage.png`: collage 900×1200.
- Ikony specjalizacji: `expertise-*-icon.png`, 256×256.
- `testimonials-pattern.png`: tło sekcji rekomendacji 1400×900.
- `contact-map.png`: stylizowana mapa 1200×800.

## Struktura komponentów

- **Nawigacja**: Sticky header z menu burger na <768px.
- **Hero**: Tekst + karta z portretem, dynamiczne metryki.
- **About**: Trzy kolumny (grafika, opis, statystyki).
- **Specjalizacje**: Karty z ikonami.
- **Brand Assets**: Kolory, typografia, wartości komunikacyjne.
- **Blog preview**: Teasery 3 wpisów + link do bloga.
- **Process**: Kroki współpracy.
- **Testimonials**: Cytaty na tle wzorca.
- **CTA**: Baner z przyciskami.
- **Kontakt**: Dane, mapka, formularz.

## Blog

- `blog.html` – listing z trzema teaserami + CTA.
- Każdy artykuł ma własny plik (`blog-*.html`). Linki „poprzedni/następny” spajają treści.
- Treści artykułów zawierają placeholdery do podmiany po przygotowaniu materiałów z mlm-legal.pl.

## Wsparcie RODO i dostępność

- Formularz kontaktowy posiada checkbox zgody RODO (walidacja HTML5).
- Kontrast: ciemne tło + jasny tekst, alt na obrazach dekoracyjnych ustawiony pusty.
- Menu mobilne dostępne poprzez `aria-labels` i `role` w linkach.

## Jak rozwijać dalej

- Dodanie pipeline’u (np. GitHub Actions) do walidacji HTML/CSS (np. `htmlhint`, `stylelint`).
- Rozważ wdrożenie bundlera (Vite/Rollup) jeśli planowane są większe rozszerzenia JS.
- W przypadku rozbudowy bloga o dynamiczne dane – rozważyć headless CMS lub generowanie statyczne (11ty, Astro).
- Uzupełnić grafiki docelowymi renderami oraz wprowadzić optymalizację (kompresja, WebP).

## Licencja

Do ustalenia z klientem (domyślnie wszystkie prawa zastrzeżone).
