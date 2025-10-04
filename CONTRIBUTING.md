# Wytyczne współpracy

## Zgłoszenia i zadania

1. Twórz issue dla każdej większej zmiany (feature/bug).
2. Każda gałąź powinna wynikać z numeru zadania – format `feature/<nazwa>` lub `fix/<nazwa>`.
3. Pull requesty opisuj po polsku, z checklistą testów manualnych (desktop/mobile, hero/CTA).

## Standard kodu

- Utrzymuj strukturę HTML w jednej kolumnie, sekcje oznacz komentarzami `<!-- -->`.
- CSS inline w `<style>` – zachowaj kolejność sekcji (layout, komponenty, media queries).
- Nie wprowadzaj zewnętrznych frameworków bez dyskusji (Bootstrap/Tailwind).
- Dla JS: tylko czysty ES6, bez bundlerów.
- Biblioteki zewnętrzne: AOS (scroll animations) i VanillaTilt (tilt efekt) ładowane z CDN – inicjalizację utrzymuj przy końcu `<body>`, pamiętaj o fall-backu offline przy testach.

## Testy manualne

- Przegląd desktop ≥1440px, laptop 1280px, tablet 768px, mobile 375px.
- Sprawdź focus i tab-order na menu mobilnym i formularzu.
- Formularz kontaktowy: walidacja pól wymaganych.

## Grafiki

- Pliki PNG umieszczaj w `images/`. Nazwy w `kebab-case`.
- Po wygenerowaniu materiałów AI użyj `image-prompts.md` (rozdzielczość + proporcje) jako specyfikacji.
- Optymalizuj grafiki (tinypng lub imagemin) przed commitowaniem.

## Copy i język

- Język polski, ton ekspercki ale przyjazny.
- Przy aktualizacji treści bloga pamiętaj o spójności call-to-action („Umów konsultację”, „Czytaj artykuł”).

## Proces review

1. Autor PR odpowiada za krótkie streszczenie zmian oraz screenshoty kluczowych sekcji.
2. Weryfikacja responsywności: reviewer testuje co najmniej w Chrome i Firefox.
3. Nie łącz, jeśli brakuje finalnych grafik lub walidacja WCAG/kontrast nie została przetestowana.

## Release checklist

- Upewnij się, że prompty w `image-prompts.md` odzwierciedlają wszystkie użyte grafiki.
- Zaktualizuj datę w stopce (`&copy; 2025` domyślnie – dostosuj, jeśli wprowadzono zmiany prawne).
- W przypadku dodania nowych sekcji, rozszerz dokumentację w README i niniejszym pliku.
