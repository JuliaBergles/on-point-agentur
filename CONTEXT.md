# On Point — Projektkontext

Kompakter Überblick für die Agentur-Website unter **agentur.juliabergles.de**.
Bei jeder Sitzung zuerst hier reinschauen.

**Stand: 10. August 2026 · Ende Session** — nach vollständigem mymiapage-Umbau, Reichweite-Dashboard, Neu-Layouts sitewide.

---

## Julia

- Julia Bergles, 20 Jahre, aus Wehringen bei Augsburg
- Rollen: Social Media Managerin, Mediendesignerin, Webdesignerin
- Agentur: **On Point**
- Instagram: [@julia_bergles](https://www.instagram.com/julia_bergles/)
- App-Projekt: **TerraLuna** (ganzheitlich für Frauen mit chronischen Beschwerden — Histamin, Reizdarm, Zöliakie, Fructose, Laktose, Zyklus, Allergien)
- Persönliche Geschichte: Darmverschluss, 2 Jahre Isolation, Fahrrad als mentale Rettung. Nur teilen wenn passend, sonst zurückhaltend.
- Ausbildung: **Fachabitur Gestaltung**. Rest autodidaktisch (Malen, Design, Nähen).
- Kontakt: julia@bergles.net · [Calendly 30min](https://calendly.com/julia-bergles/30min) · +49 1511 8515 394

## Team

- Julia macht Social Media (Konzept, Dreh, Sprache), Mediendesign (Konzept in Canva), Webdesign
- Cutter/Schnitt wird abgegeben
- Für Mediendesign ggf. Studenten hinzugezogen
- Kein „wir/Team" so tun als wären sie viele. Ehrlich als kleine Struktur auftreten.

---

## Repo & Hosting

- Lokal: `/Users/juliabergles/Desktop/On Point Website/`
- Remote: `github.com/JuliaBergles/on-point-agentur`
- Domain: `agentur.juliabergles.de` (CNAME-Datei im Repo)
- Deploy: Push auf `main` → GitHub Pages baut in ca. 1 Minute
- **Julia testet live am Handy**, nicht lokal. Kein Preview-Setup.
- Alternativ-Domain `juliabergles-onpoint.de` bei Cloudflare (wrangler.toml + .assetsignore für 25 MiB-Grenze)

---

## Aktuelle Seitenstruktur

### Hauptnavigation

| # | Seite | Datei | Zweck |
|---|---|---|---|
| 1 | **Warum On Point ▾** | `warum-onpoint.html` | 3 Versprechen, Tool-Badges, Reichweite-Editorial mit Cutouts, About-Portrait, CTA mit Julia-Foto. Sub-Menü: Erklärtag / Alle Vorteile. |
| 1a | · Erklärtag | `erklaertag.html` | 2 – 3h vor Ort, Ablauf-Timeline, 450 € pauschal. Sub-Menü unter Warum. |
| 2 | Social Media | `social-media.html` | Sprech-Formate, Vogue-Tab-Selector „Wählen Sie Ihre Branche" (4 Branchen, nur Bilder — keine Text-Kästen mehr), FAQ, CTA. |
| 3 | Mediendesign ▾ | `mediendesign.html` | Leistungen (hell), Handschrift-Editorial (3 Text-Bild-Blöcke: Konsistenz / Canva ohne KI / Malerei-Herkunft), CTA mit Foto. Kein Portfolio-Grid mehr. |
| 3a | · Visitenkarten | `visitenkarten.html` | Sub-Menü |
| 3b | · Flyer | `flyer.html` | Sub-Menü |
| 3c | · Verpackungsdesign | `verpackungsdesign.html` | Sub-Menü |
| 4 | Video & Foto | `videografie.html` | Phones-Hero mit 3 Videos, mymiapage-Editorial-Splits „Meine Haltung" + „Nach dem Dreh", helle Leistungen, Anlässe, Showcase, FAQ, CTA. |
| 5 | Webdesign | `websites.html` | Prozess-Timeline (helle Beige-Zeitleiste, Shimmer-Fortschritt, Nummern über Bubbles), Editorial-Sektion mit 3 Julia-Cutouts (rund/blob/oval) + Text-Wrap, Referenzen, FAQ, CTA. |
| 6 | **Meine Kunst** (top-level) | `kunst.html` | 9 Werke Masonry-Galerie, Story (Malerei als Ausgleich + zweites Standbein), Konditionen 80 €/h + 50 % Anzahlung, CTA mit Julia-Foto. |
| 7 | Reichweite | `reichweite.html` | Dashboard-Übersicht mit **animierten Countern** + **SVG-Donut** für Follower-Split, 3 Themengruppen für Screenshots, Demographie-Bars, PDF-CTA. Stand 10.08.2026. |
| 8 | Über mich | `ueber-mich.html` | Hero-Split, Werdegang-Cards, „Julia im Alltag"-Masonry (8 Bilder — 1 rund, 1 oval, 1 blob), Wissen-Split (portrait-neu-2), Werte, CTA. |

### Weitere Seiten (nicht in Hauptnav)

- `index.html` — Startseite mit Landing-Overlay (nur EIN Wort „Ihr Timing. Entscheidet alles."), Hero, Value-Marquee, Cutout-Editorial mit Julia, Brand-Story, 4 Bausteine, Kundendashboard-Preview, Branchen-Tabs, FAQ-Widget
- `anfrage.html` — 8-Fragen-Anfrageformular
- `angebot.html` — Angebots-Seite
- `hotel-guide.html` — private Landing (noindex/nofollow)
- `mealbites.html` — Landing für Mealbites-Projekt
- `impressum.html`, `datenschutz.html`, `agb.html`
- `old-index.html` — Archiv, alter Stand

---

## Design-System

### Farb-Palette (finaler Stand 10.08.2026)

Basis, Ink, Muted (`css/onpoint.css:root`):

```
--bg:          #ede6d9   /* warmes helles Greige, Haupt-Basis */
--bg-warm:     #ECEAE6   /* Cream für Sektions-Wechsel (FAQ, Referenzen etc.) */
--bg-soft:     #f5f0e6   /* sehr helles Cream */
--bg-mint:     #ECEAE6
--card:        #ffffff

--ink:         #2a2a2a   /* Anthrazit — Body-Text und Buttons */
--ink-soft:    #4a4a4a
--muted:       #6f6a63
--muted-lite:  #a49f97
```

Akzente:

```
--bordeaux:      #be7676   /* weiche Rose als Neben-Akzent (nicht dominant) */
--bordeaux-hi:   #d29999
--bordeaux-deep: #8b5555

--oxblood:     #4a1418   /* HIGHLIGHT — nur Headline-Italics, Micro-Akzente, CTA-em */
--oxblood-hi:  #6d1e24

--copper:       #C48B6C   /* Shimmer-Gradient-Ton */
--copper-dark:  #A0705A
--copper-light: #E8C4A8
--gold:         #C48B6C (Alias)
```

Landing-Farbtrio (nur `index.html` Snap-Flip-Overlay):

```
Cream   #ECEAE6
Orange  #ff8854
Oxblood #500011
```

Form-Utilities:

```
--radius-round: 50%
--radius-oval:  50% / 60%
--radius-soft:  20px
--radius-blob:  60% 40% 55% 45% / 55% 45% 60% 40%  (animiert via .shape-blob)
```

**Farb-Regel:** Nichts plakativ. Anthrazit für Text/Buttons, Oxblood NUR für dramatische Highlights (h1/h2/cta em), Kupfer für Shimmer-Gradients, Rose als sanfter Neben-Akzent. Keine Rot-Hintergründe, keine dunklen Sektionen mehr (alle section-dark wurden umgebaut).

### Landing (index.html)

- **Nur EIN Wort:** „Ihr Timing." mit Sub „Entscheidet alles." (4-Wörter-Version war zu lang — Kunden bounced)
- **Snap-Flip:** 2 Farbstände (Cream/Orange/Oxblood-Kombis)
- **Font:** Archivo Black, uppercase, clamp(72px – 260px)
- **Dauer:** ca. 2.2s bis Choice-Screen
- **Kein Fade** (`transition: none` auf .lo-stage)
- **Value-Marquee** direkt nach Hero: Oxblood-BG mit 10 Wert-Props („Kunden gewinnen · Sichtbar werden · Alles außer KI · Social Media · Reels · Webdesign · Mediendesign · 1 Mio+ Aufrufe · Vor-Ort-Erklärtag · Handgemachte Kunst")
- **Cutout-Editorial-Sektion** nach Marquee: fließender Text mit 3 Julia-Portraits als Cutouts (rund/blob/oval) die text umfließen, kein Karten-Container

### Typografie

- **Headlines & UI:** Raleway 500–900
- **Landing-Display:** Archivo Black (nur Landing-Overlay)
- **Body:** Quicksand 300–700
- Fallbacks: Rubik, Space Grotesk, Playfair Display, Object Sans

Google-Fonts-Import in `css/onpoint.css` + gespiegelt in allen HTML-Heads: Space Grotesk 400-700, Clash Display 600-700, Bricolage Grotesque, Rubik 400-900, Archivo Black, Quicksand 300-700, Raleway 500-900.

### Design-Muster (mymiapage.de + Soul-of-Women-Club inspiriert)

Wiederkehrende Bausteine sitewide:

1. **Editorial-Split** — Text + großes Foto nebeneinander (`.wo-cta-split`, `.um-hero-inner`, `.um-wissen-split`, `.split-julia`, `.md-block`, `.cta-block.with-photo`, `.v-split`, `.k-cta-split`)
2. **Transparente Text-Overlay auf Foto** — cream 94% backdrop-blur, Oxblood-Text, Muted-Small-Cap-Label. Sitewide-Signature auf allen CTAs und Split-Blocks.
3. **Masonry-Grid** mit .tall/.wide/.square/.default (`um-gallery-grid`, `k-gallery-grid`)
4. **Alternierendes Text-Bild-Layout** — `.reverse`-Modifier (`md-block`, `v-split`)
5. **Tab-Selector Vogue-Style** — Oxblood-BG aktiv, Fade-In-Content (social-media Branchen-Tabs)
6. **Screenshot-Grid** — iPhone-9:19.5-Aspect (Reichweite)
7. **KENNENLERNEN-CTA mit Julia-Foto** — `.cta-block.with-photo` sitewide (erklaertag, mediendesign, social-media, reichweite, websites, videografie). Warum-onpoint hat eigene `.wo-cta-split`, ueber-mich `.um-cta`, kunst `.k-cta-split`.
8. **Cutouts + Text-Wrap** (Magazin-Layout) — Julia-Portraits als runde/blob-Formen mit `shape-outside: circle()` bzw. `margin-box`, Text fließt drumrum (`.cutout-editorial` auf Startseite, `.w-float-*` auf websites, `.re-cutout-*` auf warum-onpoint Reichweite-Editorial)
9. **Form-Utilities** — `.shape-round` / `.shape-oval` / `.shape-soft` / `.shape-blob` (mit 12s Morph-Animation) — sitewide einsetzbar
10. **Animierte Counter** — `data-count` Attribute, IntersectionObserver-getriggered, 0 → Zielwert in 1.8s (ease-out cubic), Copper-Shimmer-Text-Gradient
11. **SVG-Donut** — Follower/Nicht-Follower-Split, stroke-dashoffset animiert von 100% auf 7.3% in 2.5s, Copper-Gradient-Stroke
12. **Prozess-Timeline** — helle Beige-Zeitleiste, Nummern ÜBER den Bubbles (nicht drin), kleine Dot-Bubbles auf Linie, Linie mit Shimmer-Gradient (Oxblood→Kupfer→Oxblood 6s-Loop), staggered Reveal-Delay

### Text-Regeln

- **Sie-Form durchgängig** (im Gegensatz zu juliabergles.de)
- Kein „Wusstest du...", keine KI-Sprache
- Keine Bindestriche als Trenner
- Jeder Satz auf neue Zeile (`<br>` in HTML)
- Zahlen sauber schreiben
- Konditionen und Preise klar zeigen
- **Julia schreibt alle Prosa selbst.** Claude macht Placeholder + strukturelles/faktisches Scaffolding.

### Content-Regeln

- Kein Heilversprechen
- Kein „wir sind ein großes Team" — Julia ist Solo mit Freelancer-Netzwerk
- Peer-Support = Erfahrungsaustausch, nicht Beratung (Heilpraktiker-Gesetz-relevant)
- Julia arbeitet in **Canva** (nicht Illustrator/InDesign/Figma). Kein KI in Design.
- Kunst / Design / Nähen — alles autodidaktisch gelernt, außer Fachabitur Gestaltung

---

## Aktuelle Zahlen (Stand 10.08.2026)

Aus Instagram Insights, Zeitraum 10. Juli – 8. August 2026:

- **1.020.876** Aufrufe in 30 Tagen (davon 925.946 Reels, 54.510 Stories, 38.116 Beiträge)
- **22.384** Interaktionen (20.571 auf Reels)
- **+484** Netto neue Follower — total **6.070 Follower**
- **7.749** Profilaufrufe
- **92,7 %** Nicht-Follower
- **506.191** Betrachter (unique accounts reached)

### Zielgruppe

- **Frauen 73,7 %** / Männer 26,3 %
- Alter dominant: **25–34 mit 34,7 %**, 35–44 25,3 %, 18–24 14,9 %, 45–54 13,4 %
- Länder: **Deutschland 85,4 %**, Österreich 7,6 %, Schweiz 3,4 %
- Sprache: 96,8 % deutschsprachig

**Screenshots** liegen unter `img/reichweite/IMG_3460.PNG` bis `IMG_3467.jpg` (8 Dateien).

---

## Konditionen

| Leistung | Preis | Anmerkung |
|---|---|---|
| Social Media Beitrag | 220 € | |
| Social Media Reel + Videodreh | 250 € | zzgl. Fahrtpauschale außerhalb Augsburg |
| Social Media Story | 50 € | |
| Webdesign | 80 €/h | Landing 400–640 €, mittlere Website ca. 1.120 €, komplex 1.760–2.560 € |
| Kunst-Auftrag | 80 €/h | 50 % Anzahlung, Farben inklusive |
| **Erklärtag** | **450 € pauschal** | 2–3h vor Ort, Content-Plan + 1–2 Reels inklusive |
| Kilometer | 0,30 €/km | Ab 20 km von Wehringen |
| Retainer | auf Anfrage | 3 Monate Mindestlaufzeit, 1 Monat Kündigung |

Alle Preise zzgl. MwSt.

---

## Bilder-Struktur

```
Desktop/On Point Website/
├── img/                          # website-Bilder (in Repo, versioniert)
│   ├── portraits/                # julia-1..julia-8.jpeg (julia-4 ist Aquarell-Stillleben, NICHT verwenden für Julia-Kontext)
│   ├── landing/                  # webdesign, ueber-julia
│   ├── mediendesign/             # visitenkarten, flyer, verpackung, kunstwerke
│   ├── kunst/                    # 9 Werke (aquarell, acryl, modellieren, werk-neu, werk-farbe)
│   ├── reichweite/               # 8 IG-Insights-Screenshots (IMG_3460–3467)
│   ├── videografie/              # 3 MP4-Videos + Weihnachtskarte
│   ├── mymia-refs/               # Referenzbilder mymiapage (intern, nicht öffentlich)
│   ├── fitness-1..4.png          # Kunde Fitnessstudio
│   ├── kitchen-1..6.png          # Kunde Bruckner Einrichtungshaus
│   ├── mental-1..10.png          # Kunde Nicole Schleer Mediale Beratung
│   ├── idea-1..7.png             # generische Content-Ideen
│   ├── portrait-3.jpg            # Julia mit Handy + rosa Pfingstrosen (Social-Media-CTA, Warum-About)
│   ├── portrait-neu-2.jpg        # Julia-Portrait (Über-mich Wissen-Split)
│   ├── portrait-hero.jpg         # Alternativer Hero-Portrait
│   ├── portrait-about.jpg
│   ├── sprech-julia-kamera.jpg   # Julia hinter Kamera (Videografie-Editorial)
│   ├── IMG_5738.jpeg             # Julia weißes Top (Mediendesign-CTA)
│   ├── bild-2.jpg, bild-3.jpg    # Julia in verschiedenen Situationen
│   └── ref-*.jpg                 # Referenz-Fotos
├── Bilder /                      # Julias Rohbilder (unversioniert, Staging)
└── css/onpoint.css               # Shared Stylesheet (Design-Tokens, Nav, Footer, Buttons, Shape-Utilities, CTA-Block)
```

### Foto-Verteilung Julia-Portraits (kein Duplikat pro Sektion)

| Datei | Wo verwendet |
|---|---|
| julia-1.jpeg | ueber-mich Hero |
| julia-3.jpeg | mediendesign Handschrift (nicht mehr CTA), landing cutout, websites editorial |
| julia-4.jpeg | ⚠️ Aquarell-Stillleben, KEIN Julia-Portrait — nicht verwenden für Julia-Kontext |
| julia-5.jpeg | erklaertag CTA + Split, landing cutout, warum-onpoint Reichweite-Editorial |
| julia-6.jpeg | ueber-mich Gallery (shape-round), websites editorial, warum-onpoint reichweite cutout, landing cutout |
| julia-7.jpeg | ueber-mich Gallery, videografie Editorial |
| julia-8.jpeg | ueber-mich Gallery, reichweite CTA |
| portrait-3.jpg | social-media CTA, warum-onpoint About-Portrait |
| portrait-neu-2.jpg | ueber-mich Wissen-Split |
| sprech-julia-kamera.jpg | ueber-mich Gallery (shape-oval), videografie Editorial + CTA |
| bild-3.jpg | landing Hero-BG, ueber-mich Gallery (shape-blob) |
| IMG_5738.jpeg | mediendesign CTA |

**Cross-Nutzung erlaubt:** Blog-Bilder aus juliabergles-Website-Repo dürfen auch hier verwendet werden.

---

## Was Julia NICHT will

- ❌ Alte Bordeaux #660e30 / Petrol / Champagner
- ❌ Playfair / Nunito / Fraunces / Inter als Primary-Fonts
- ❌ Marquee-Bänder mit unruhigen iPhone-Mockups
- ❌ Zu volle Sektionen — Weißraum ist Signature
- ❌ Erfundene Zitate und Testimonials
- ❌ Rose als Hauptton (zu weiblich-verspielt) — nur als sanfter Akzent OK
- ❌ Reines Rot als Hintergrund (zu plakativ) — Oxblood nur als Highlight-Punkt
- ❌ Reines Blau/Maritime (kalt, off-brand)
- ❌ Reines Salbeigrün
- ❌ Bindestriche als Satz-Separator
- ❌ „Wir sind ein großes Team"-Sprache
- ❌ Prosa-Absätze in Julias Stimme (Julia schreibt selbst)
- ❌ Heilversprechen
- ❌ Nicht-Julia-Bilder in Personen-Kontext (nur Julia auf Julia-Fotos, keine Blumen/Landschaften wo Portrait hingehört)
- ❌ Dark Section-Backgrounds (alle wurden auf hell/beige umgebaut)
- ❌ KI-Illustrationen / Illustrator / InDesign / Figma — Julia arbeitet in Canva

## Was Julia will

- ✅ Editorial-Look Richtung mymiapage.de + Metropolregion-München-Kraft
- ✅ Text und Bilder gemischt, versetzte Layouts, transparente Overlays
- ✅ Viele Julia-Bilder sichtbar, in variablen Größen und Formen (rund/oval/blob)
- ✅ Cutouts + Text-Wrap (Magazin-Layout, Text direkt auf Cream)
- ✅ Klare Farb-Highlights sparsam einsetzen (Oxblood + Copper-Shimmer)
- ✅ Live-Push zu GitHub Pages, direkt am Handy testen
- ✅ Rot + Gold als Zielfarben (aus Visitenkarten-Kontinuität) — aktuell durch Oxblood-Highlight + Copper-Shimmer umgesetzt
- ✅ Referenzen konkret zeigen (nicht anonymisieren wo möglich)
- ✅ Auf jeder Seite: Julia-Foto neben dem KENNENLERNEN-CTA
- ✅ Animationen: Shimmer-Effekte auf Nummern/Linien, Counter, Donut, Timeline-Fortschritt

---

## Iteration-Log 10.08.2026 (~35 Commits diese Session)

Major Umbauten:
1. **Landing** metropolregion-Snap-Flip → radikal auf EIN Wort reduziert (Bounce-Fix)
2. **Sitewide Sie-Form** (perl-Konvertierung ~50 Verb-Konjugationen)
3. **Farbe:** Bordeaux #660e30 → mehrere Iterationen → Greige-Base + Rose-Neben-Akzent + Oxblood-Highlight + Copper-Shimmer + neuer --bg-warm #ECEAE6
4. **Schrift:** Nunito → Raleway sitewide
5. **social-media** aufgeräumt: ManyChat/Einzelleistungen/Referenzen raus, Vogue-Tabs (jetzt ohne Text-Kästen)
6. **Reichweite** komplett neu mit Dashboard-Übersicht (animierte Counter + SVG-Donut) + 8 IG-Screenshots in 3 Themengruppen + Stand 10.08.
7. **Erklärtag** neue Seite (450 €) mit Nav-Integration als Sub-Menü von Warum On Point
8. **Kunst** ausgebaut auf 9 Werke, top-level Nav, CTA mit Julia-Foto, Story-Text von Julia
9. **Über-mich** Julia-Bilder-Masonry (8 Bilder, 3 mit Shape-Utilities: rund/oval/blob)
10. **Mediendesign** Handschrift-Editorial (3 Text-Bild-Blöcke: Konsistenz / Canva ohne KI / Malerei-Herkunft), Portfolio-Karten raus, CTA mit Foto
11. **Warum-onpoint** CTA Split-Layout + Reichweite komplett neu als Magazin-Layout mit runden Julia-Cutouts + Fachabitur/TerraLuna-Kontext
12. **CTA-Block sitewide** Julia-Foto daneben (`.cta-block.with-photo`)
13. **Websites** Prozess-Timeline hell/beige mit Shimmer + Nummern über Bubbles + Editorial-Sektion mit 3 Julia-Cutouts (float + shape-outside)
14. **Videografie** dark → hell, mymiapage-Editorial-Splits (Meine Haltung + Nach dem Dreh), Leistungen hell
15. **Shape-Utilities** (`.shape-round/-oval/-soft/-blob` mit Morph-Animation) — sitewide verfügbar
16. **Landing Cutout-Editorial** direkt aufs Cream, 3 Julia-Portraits als Cutouts mit Text-Wrap
17. **Oxblood** in Headline-Italics (h1/h2/cta em)
18. **Value-Marquee** auf Startseite mit 10 Wert-Props
19. **Nav-Restructuring:** Kunst top-level, Erklärtag als Sub-Menü von Warum On Point
20. **Content-Updates:** Reichweite-Zahlen aktualisiert (706k → 1 Mio+), Julia's Canva-Copy, Selbst-beigebracht-Zusatz, Kunst-Story neu

---

## Offene Punkte / Nächste Iterationen

- **Kundenprojekte fortführen:** relax Fitness & Vital Lounge (Daniel Hartmann), Hotel-Kooperationen (Panorama Hotel Niedermair)
- **Kooperations-Mails:** MyMense, Selenacare, Ooia, Dilling
- **SSL/HTTPS** auf agentur.juliabergles.de finalisieren
- **Google Search Console** für juliabergles-onpoint.de
- **Foto-Doppel-Checks:** einige Foto-Duplikate zwischen Seiten könnten aufgelöst werden falls Julia mehr Fotos schickt
- **PRIVATE Website juliabergles.de** — separater Redesign-Auftrag im Design-System dieser Site geplant (mit du-Ansprache, WhatsApp-Community-Button, App-Anleitung, E-Book-Downloads). Prompt existiert.

---

## Deployment / Externe Tools

- **GitHub Pages:** Hosting agentur.juliabergles.de
- **Cloudflare Workers:** juliabergles-onpoint.de (wrangler.toml, .assetsignore)
- **Calendly:** `calendly.com/julia-bergles/30min`
- **IONOS:** DNS
- **Google Search Console:** verifiziert, sitemap.xml + robots.txt vorhanden

### Standard-Stack für Kunden-Websites (nicht für On Point)

- Astro als Framework
- Decap CMS
- Vercel oder Netlify
- Kunden-Ownership: Domain, Code, Hosting im Kunden-Account
- Kein Lock-in

---

## Prinzipien für Änderungen

1. **CONTEXT.md ist die Wahrheit.** Bei jeder neuen Sitzung erst hier reinschauen.
2. **Keine erfundenen Zitate oder Testimonials.**
3. **Fokus:** Kunden-Gewinnung, nicht Content-Produktion.
4. **Kein reines Rot, kein Fraunces, kein Nunito, kein plakatives Blau, kein Dark-Background.**
5. **Weniger Text ist mehr.**
6. **Julia schreibt Prosa selbst** — Claude scaffoldet nur.
7. **Push-first, live testen am Handy.** Kein lokaler Preview-Flow.
8. **Ein Task = ein Commit.** Deutsche Commit-Messages mit warum/was.
9. **Bei Farb-/Design-Fragen:** Julia entscheidet, Claude gibt Meinung + Empfehlung, dann tut.
10. **Julia-Fotos:** Nur echte Julia-Portraits in Personen-Kontext. julia-4.jpeg ist ein Aquarell-Stillleben — NICHT verwenden.

---

## Wenn du diese Datei liest…

…dann arbeitest du gerade an On Point Website (Agentur, Sie-Form).
**Verwechsle sie nicht mit juliabergles.de** (Personal Brand, du-Form) — das ist ein anderes Repo unter `~/Library/Mobile Documents/.../juliabergles Website/`.

Zuerst hier reinschauen, dann Änderung planen. Direkt und knapp arbeiten. Live-Push mit klarer deutscher Commit-Message.
