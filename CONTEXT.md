# On Point Kontext

Kompakter Ueberblick fuer Website, Design, Konditionen und offene Punkte.
Bei jeder Sitzung zuerst hier reinschauen.

Ersetzt die vorige Version (Petrol/Champagner/Inter, alte Preise) vollstaendig.
Aktueller Stand: Juli 2026.

---

## Julia

- Julia Bergles, 20 Jahre, aus Wehringen bei Augsburg
- Rollen: Social Media Managerin, Mediendesignerin, Webdesignerin
- Agentur: On Point
- Instagram: @julia_bergles
- App-Projekt: TerraLuna (ganzheitlich fuer Frauen mit chronischen Beschwerden. Histamin, Reizdarm, Zoeliakie, Fructose, Laktose, Zyklus, Allergien. Reisen-Bereich aktiv)
- Persoenliche Geschichte: Darmverschluss, 2 Jahre Isolation, Fahrrad als mentale Rettung. Nur teilen wenn passend, sonst zurueckhaltend
- Kontakt: julia@bergles.net, https://calendly.com/julia-bergles/30min, +49 1511 8515 394

## Team

- Julia macht Social Media (Konzept, Dreh, Sprache), Mediendesign (Konzept), Webdesign
- Cutter/Schnitt wird abgegeben
- Fuer Mediendesign ggf. Studenten hinzugezogen
- Kein "wir/Team" so tun als waeren sie viele. Ehrlich als kleine Struktur auftreten

---

## Website On Point

### Seitenstruktur

- `index.html` — Startseite. Hero mit Julia-Bild, Auswahl-Modal "Weswegen sind Sie hier?", 4 Bausteine, Branchen, Ueber Julia, Testimonial
- `warum-onpoint.html` — 3 Versprechen. Nebenkosten, Ohne Drehbuch, Nur eine Marke pro Branche
- `social-media.html` — Beitrag 220 EUR, Reel 250 EUR, Story 50 EUR. Sprech-Optionen mit Bildern
- `mediendesign.html` — Visitenkarten, Print/Flyer, Workbooks/E-Books/Praesentationen, Logo/CD
- `websites.html` — 80 EUR/h. Landing 400 bis 640 EUR. Uebliche Website ca. 1.120 EUR. Komplex 1.760 bis 2.560 EUR
- `pakete.html` — Retainer als Accordion. Wachstum als Empfehlung. Prozess "So starten wir"
- `reichweite.html` — aktuelle Instagram-Zahlen (heller Look, Bordeaux-Boxen)
- `hotel-guide.html` — private Landing (noindex/nofollow, robots.txt disallow), Hybrid Design hell mit dunklen Akzenten

### Design System

- Farben:
  - `--bordeaux: #8B2E3A`
  - `--bordeaux-deep: dunkler Bordeaux fuer Backgrounds`
  - `--gold: #C5A46D`
  - `--off-white: #FBF2ED`
  - `--ink: #2D1F22`
- Schriften: Playfair Display (Serif Headlines) + Object Sans (Sans, Body und Zahlen)
- Shared Styles: `css/onpoint.css` fuer neue Seiten, teils inline styles auf Startseite
- Look: dark editorial mit hellen Sektionen im Wechsel, klare Kontraste

### Design-Regeln

- Sektionen nicht starr wirken lassen. Klare Background-Wechsel und spuerbare Motion
- Zahlen NIEMALS in Playfair-Italic (schlecht lesbar). Immer Object Sans Bold
- Kein "6 von 8 Bildern" pro Panel. Kompakt halten
- Bordeaux dominant, Gold als Akzent
- Hero-Bilder gross und ruhig, keine ueberladenen Overlays

### Text-Regeln

- Keine Bindestriche als Separator (weder — noch – als Trenner). Stattdessen Punkt, Komma oder neue Zeile
- Jeder Satz auf neue Zeile (bei Fliesstexten mit `<br>` trennen)
- Zahlen sauber schreiben, nicht verschnoerkeln
- Keine Werbe-Phrasen wie "Kein Verkaufs-Pitch" oder "Ihr Argument". Direkt zur Sache
- Konditionen und Preise klar zeigen, nicht verstecken

### Was Julia NICHT will

- Alte Petrol/Champagner-Palette (ersetzt durch Bordeaux/Gold)
- Fraunces und Inter (ersetzt durch Playfair und Object Sans)
- Marquee-Baender und iPhone-Mockups (weg, wirkt unruhig)
- Zu volle Sektionen
- Erfundene Zitate und Testimonials
- Kupfer, Salbeigruen, reines Rot

---

## Deployment

- Repo: `https://github.com/JuliaBergles/on-point-agentur`
- `agentur.juliabergles.de` auf GitHub Pages (CNAME auf juliabergles.github.io)
- `juliabergles-onpoint.de` auf Cloudflare Workers Static Assets
  - `wrangler.toml` und `.assetsignore` schliessen `.git`, `dashboard/`, `Hotel-Guide/`, `On-Point-Bilder/` aus
  - Grund: .git-Ordner (96 MiB) sprengt Cloudflare 25 MiB Limit
- Nameserver bei Cloudflare: `keenan.ns.cloudflare.com`, `tia.ns.cloudflare.com`
- Visitenkarten mit `www.agentur.juliabergles.de`. DNS-Record dafuer setzen falls neu

---

## Konditionen

### Social Media (Einzelbuchung)

- Beitrag: 220 EUR
- Reel: 250 EUR
- Story: 50 EUR

### Webdesign

- Stundensatz: 80 EUR/h
- Landing Page: 5 bis 8 h (400 bis 640 EUR)
- Uebliche Website: ca. 14 h (rund 1.120 EUR, inkl. Astro-Setup)
- Komplex: 22 bis 32 h (1.760 bis 2.560 EUR)

### Kilometer

- Ab 20 km von Wehringen: 0,30 EUR/km

### Retainer

- 3 Monate Mindestlaufzeit, 1 Monat Kuendigung
- Preisanpassung nach 8 Monaten
- Freigabe innerhalb 24 h, 1 Follow-up inklusive
- Referenznutzung durch Julia erlaubt

Alle Preise zzgl. MwSt.

---

## Reichweite (Case Study Zahlen)

Stand aktuell:
- 1.393.620 Aufrufe / Monat
- 581.274 erreichte Konten
- 22.435 Interaktionen
- 16.830 Profilaufrufe
- 5.675 Follower gesamt
- 91,6 Prozent Nicht-Follower Reichweite
- Demografie: 75,9 Prozent Frauen, 24,1 Prozent Maenner
- Alter: 25-34 (35,5 Prozent), 35-44 (25,2 Prozent)
- Land: DE 85,1 Prozent, AT 7,6 Prozent
- Accounts: @julia_bergles, @Smacado_

---

## Kundenprojekte

- **relax Fitness und Vital Lounge e.K.** (Daniel Hartmann). Retainer laeuft, Vertragsentwurf existiert auf Desktop (`Vertrag-relax-Fitness.html`)
- **Hotel-Kooperationen**. Anreise gratis, kein Cash-Honorar bei Erst-Kooperation. Guide fuer Hotels als HTML (Desktop `/Hotel-Guide/`)
  - Angeschrieben: Panorama Hotel Niedermair, Partschins (Familie Kuen)
- **Kooperations-Anfragen an Marken**. Periodenunterwaesche (MyMense, Selenacare, Ooia), allergikerfreundliche Kleidung (Dilling). Mail-Vorlagen auf Desktop `/Kooperations-Mails/`

---

## Externe Tools

- Calendly (Standard, 30 Min Kennenlerngespraech): https://calendly.com/julia-bergles/30min
- Google Search Console: HTML-Tag Verifizierung, Sitemap.xml und robots.txt vorhanden
- IONOS: DNS-Verwaltung fuer juliabergles.de Subdomains
- Cloudflare: Nameserver und Workers-Hosting fuer juliabergles-onpoint.de
- GitHub Pages: Hosting fuer agentur.juliabergles.de

---

## Standard-Stack fuer Kunden-Websites

Fuer NEUE Kundenprojekte (nicht On Point selbst):

- Astro als Framework
- Decap CMS fuer Kunden-Redaktion
- Vercel oder Netlify als Hosting
- Kunden-Ownership: Domain, Code, Hosting im Kunden-Account
- Kein Lock-in, alles gehoert dem Kunden

---

## Offene Todos

- Kooperations-Mails an MyMense und Selenacare senden
- Mail an Familie Kuen (Panorama Hotel Niedermair) senden
- SSL/HTTPS auf agentur.juliabergles.de pruefen (falls noch offen)
- Google Search Console fuer juliabergles-onpoint.de: Property anlegen und Sitemap einreichen
- Cloudflare Pages Custom Domain fuer juliabergles-onpoint.de und www abschliessen
- Optional: Redirect agentur.juliabergles.de nach juliabergles-onpoint.de

---

## Naechstes Projekt: Dashboard On Point

- Eigenes Tool fuer Julias Agentur-Betrieb
- Noch keine konkreten Specs
- Im neuen Chat starten (nicht hier weiter)
- Vor Implementation klaeren:
  1. Was soll das Dashboard koennen (Kunden, Rechnungen, Content-Kalender, KPIs, Termine)
  2. Fuer wen (nur Julia oder auch Kunden-Login)
  3. Wo hosten (Cloudflare, Vercel, Supabase)
  4. Datenspeicher (Datenbank oder erstmal Frontend-Skizze)
- Design-Sprache muss zur Website passen: Bordeaux/Gold/Off-white/Ink, Playfair und Object Sans, dark editorial

---

## Arbeitsweise (aus CLAUDE.md)

- Sauber und strukturiert, kein Quick-and-Dirty
- Bestehenden Code erst verstehen bevor geaendert wird
- Gute UX mitdenken
- Langfristig sinnvoll bauen, keine kurzfristigen Hacks
- Aenderungen klein und nachvollziehbar
- Bei Unklarheiten nachfragen statt raten
- Tests und Dokumentation gehoeren dazu

---

## Prinzipien fuer Aenderungen

1. CONTEXT.md ist die Wahrheit. Bei jeder neuen Sitzung erst hier reinschauen.
2. Keine erfundenen Zitate oder Testimonials.
3. Fokus bleibt: Kunden-Gewinnung, nicht Content-Produktion.
4. Kein Kupfer, kein reines Rot, kein Fraunces.
5. Weniger Text ist mehr.
