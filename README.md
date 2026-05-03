---
type: pitch-asset
prospect: OX Royal
status: Mock v1.2 — Karte raus, echte Bilder von bestehender Webseite eingebunden
created: 2026-05-03
updated: 2026-05-03
---

# OX Royal — Webseite (Pitch-Mock)

Single-Page-Landing als Pitch-Asset für das Fahro-Gespräch. Brand-konform, ohne Preise, mit echten Bildern aus der bestehenden Webseite.

## So öffnest du die Demo

Doppelklick auf `index.html` → öffnet im Standardbrowser.

Alternativ für Live-Reload:
```bash
cd webseite && python3 -m http.server 8000
```

## v1.2 — Was sich gegen v1.1 geändert hat

- **Speisekarten-Sektion entfernt** (auch aus Nav, Desktop + Mobile) — saubere Struktur, Karte gibt's vor Ort
- **13 echte Bilder eingebunden** aus der bestehenden Webseite (statt Placeholder-Slots)
- **Hero**: Rhein-Tisch-Bild als Background mit dunklem Gradient-Overlay
- **Cuts**: jede der 6 Karten hat jetzt ein passendes Foto + Text
- **Atmosphäre**: 6 echte Galerie-Bilder vom Restaurant
- **Reservierungs-Sektion**: Innenraum-Bild als Background
- **OG-Image** auf hero.jpg gesetzt
- **`fetchpriority="high"`** auf Hero-Bild (Performance)
- **`img-premium`-Filter** (leichte Kontrast-/Sättigungsanpassung) auf allen Bildern

## v1.1 — Was vorher dazu kam

- Reduced-Motion respektiert, Focus-Visible, Skip-Link, ARIA
- Touch-Targets ≥44px überall
- CTA-Hierarchie geschärft (Primary filled, Secondary bordered)
- Motion One Spring-Physics + Stagger
- Theme-Color, Color-Scheme dark, Color-Contrast WCAG AA verifiziert

## Bilder-Mapping

| Slot | Datei | Inhalt |
|---|---|---|
| Hero | `images/hero.jpg` | Tisch am Fenster mit Rheinblick (Vasen, Gläser) |
| Cut: Tomahawk | `images/steak2.jpg` | Tomahawk auf Holzbrett, tranchiert |
| Cut: Chateaubriand | `images/speisen.jpg` | Filet-Mittelstück, aufgeschnitten |
| Cut: Ribeye | `images/essen2.jpg` | Steak mit Bratkartoffeln |
| Cut: Filet | `images/steak1.jpg` | Filet-Stück auf weißem Teller |
| Cut: Carpaccio | `images/essen1.jpg` | Steak mit Kräuterbutter (Platzhalter — Carpaccio gab's nicht) |
| Cut: Tatar | `images/essen3.jpg` | Steak mit Kartoffelpüree (Platzhalter) |
| Atmosphäre 1 | `images/tisch.jpg` | Eingedeckte lange Tafel |
| Atmosphäre 2 | `images/lokal.jpg` | Innenraum mit Blumen |
| Atmosphäre 3 | `images/restaurant.jpg` | Special-Event-Tisch (rote Rosen) |
| Atmosphäre 4 | `images/lokal2.jpg` | Steak in der Pfanne |
| Atmosphäre 5 | `images/oxroyal.jpg` | Hauptgang mit Salat |
| Atmosphäre 6 | `images/steak3.jpg` | Frisches Premium-Fleisch |
| Reservierung BG | `images/lokal.jpg` | Innenraum als atmosphärischer Hintergrund |

## Ehrliche Bewertung der Bilder

**Stark:** hero.jpg (Rhein-Tisch — perfekter Hero), steak2.jpg (Tomahawk-Hero), tisch.jpg (Tafel-Atmosphäre), lokal.jpg (Innenraum)

**Mittel:** essen-Bilder, restaurant.jpg (für Special-Event-Vibe ok)

**Nicht ideal — beim Filmtag ersetzen:**
- steak3.jpg zeigt rohes Fleisch in Edelstahl-Schale — kein Premium-Look
- lokal2.jpg ist ein flach beleuchtetes Pfannen-Steak
- oxroyal.jpg zeigt Pasta + Salat — kein Steakhaus-Hero
- Carpaccio + Tatar fehlen komplett im Bestand
- Roter-Teppich-Aufnahme fehlt
- Dry-Age-Schrank-Aufnahme fehlt
- Außenfassade Blue Hour fehlt

→ Genau die Schwäche, die wir in der Brand-Analyse identifiziert haben. Filmtag 1 löst das.

## Struktur

| Sektion | Zweck |
|---|---|
| Hero | „OX Royal · Ein Tisch am Rhein." + Primary-CTA + Hero-Bild Rhein-Tisch |
| Haus | 3-Säulen-Statement: Familie / Rhein / Handwerk |
| Cuts | 6 Cut-Karten mit Foto + Text + Hover-Scale |
| Atmosphäre | 6-Slot-Galerie mit echten Bildern |
| Reservierung | Tel (primary, filled) + Mail (secondary, bordered), Innenraum-BG |
| Kontakt & Anfahrt | Adresse, Tel, Mail, Öffnungszeiten + Google Maps Embed |
| Footer | IG/TikTok-Links, Impressum-/Datenschutz-Slots |

## Was Mock ist und was später echt wird

| Element | Status | Was später kommt |
|---|---|---|
| Bilder | Existing-Site-Material (mittelmäßig) | Filmtag-1-Material (Caravaggio-Look) |
| E-Mail-Adressen | Annahmen | Tatsächliche Adressen |
| Google Maps | Approx-Koordinaten | Korrekte Pin-Position |
| TikTok-Link | `#` | Account-URL |
| Impressum / Datenschutz | Platzhalter | Rechtliche Texte |
| Reservierungs-Tool | Tel/Mail-Fallback | OpenTable / Quandoo / eigenes Formular |
| Favicon | Fehlt | OX-Wappen als ICO/SVG |

## Pitch-Argumente für Fahro

1. **Premium-Look** — dunkel, editorial, Magazin-Ästhetik
2. **Keine Karte auf der Startseite** — Premium-Move, Gast kommt rein für ein Erlebnis, nicht für eine PDF
3. **Klarer Gast-Pfad:** Hero → Story → Cuts → Atmosphäre → Reservierung → Kontakt
4. **Mobile-First** mit Touch-Targets ≥44px
5. **Accessibility WCAG AA** — Focus-States, Reduced-Motion, Skip-Link
6. **Spring-Physics-Animationen** (Motion One via CDN)
7. **Performance:** Hero-Bild mit `fetchpriority`, alles andere `loading="lazy"`

## Wenn Vertrag kommt

Migration zu Astro + Tailwind + Cloudflare Pages:
- Modulares Komponenten-Setup
- Bilder als optimierte `<picture>` + AVIF/WebP-Varianten
- Cookie-Banner (DSGVO)
- Echtes Reservierungs-Tool
- Analytics (Plausible / Umami)
- Bilder vom Filmtag ersetzen

## Skills, die für diesen Build genutzt wurden

- **ui-ux-pro-max** — Design-System, Color-Contrast, Font-Pairing, UX-Audit
- **motion** — Motion One Spring-Physics, Stagger, hover scale, reduced-motion

## Nächste Schritte

1. Im Fahro-Termin zeigen
2. Feedback notieren
3. Bei Vertrag: Migration zu Astro
4. Bei Filmtag 1: schwache Bilder ersetzen, Hero-Video integrieren
