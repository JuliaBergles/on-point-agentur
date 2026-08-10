# On Point — Projektkontext

Kompakter Überblick für die Agentur-Website unter **agentur.juliabergles.de**.
Bei jeder Sitzung zuerst hier reinschauen.

**Stand: 10. August 2026.** Ersetzt alle vorherigen Stände (Juli-Version mit Bordeaux #8B2E3A + Playfair war Vorgänger).

---

## Julia

- Julia Bergles, 20 Jahre, aus Wehringen bei Augsburg
- Rollen: Social Media Managerin, Mediendesignerin, Webdesignerin
- Agentur: **On Point**
- Instagram: [@julia_bergles](https://www.instagram.com/julia_bergles/)
- App-Projekt: **TerraLuna** (ganzheitlich für Frauen mit chronischen Beschwerden — Histamin, Reizdarm, Zöliakie, Fructose, Laktose, Zyklus, Allergien)
- Persönliche Geschichte: Darmverschluss, 2 Jahre Isolation, Fahrrad als mentale Rettung. Nur teilen wenn passend, sonst zurückhaltend.
- Kontakt: julia@bergles.net · [Calendly 30min](https://calendly.com/julia-bergles/30min) · +49 1511 8515 394

## Team

- Julia macht Social Media (Konzept, Dreh, Sprache), Mediendesign (Konzept), Webdesign
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
- Alternativ-Domain `juliabergles-onpoint.de` bei Cloudflare (Workers Static Assets, mit wrangler.toml + .assetsignore für die 25 MiB-Grenze)

---

## Aktuelle Seitenstruktur

### Hauptnavigation (aktive Menü-Punkte)

| # | Seite | Datei | Zweck |
|---|---|---|---|
| 1 | Warum On Point | `warum-onpoint.html` | 3 Versprechen: Nebenkosten, Ohne Drehbuch, Nur eine Marke pro Branche. Tool-Badges. KENNENLERNEN mit Julia-Foto-Split. |
| 2 | Social Media | `social-media.html` | Sprech-Formate, Vogue-Tab-Selector „Wählen Sie Ihre Branche" (4 Branchen: Fitness/Einrichtung/Mediale/Gastro), FAQ. |
| 3 | Mediendesign ▾ | `mediendesign.html` | Leistungen dark, „Meine Handschrift" (3 alternierende Text-Bild-Blöcke Soul-of-Women-Stil), Referenzen. |
| 3a | · Visitenkarten | `visitenkarten.html` | Sub-Menü |
| 3b | · Flyer | `flyer.html` | Sub-Menü |
| 3c | · Verpackungsdesign | `verpackungsdesign.html` | Sub-Menü |
| 3d | · Meine Kunst | `kunst.html` | 9 Werke (Acryl, Aquarell, Modellieren), Stundensatz 80 €, 50 % Anzahlung. |
| 4 | Video & Foto | `videografie.html` | Phone-Mockups-Hero, Videos & Fotos, Referenzen. **Umbau in mymiapage-Stil noch offen.** |
| 5 | Webdesign | `websites.html` | Prozess, Preise 80 €/h, Beispiel-Referenzen. |
| 6 | **Erklärtag** *(neu 08/2026)* | `erklaertag.html` | 2 – 3h vor Ort. Ablauf-Timeline, Preis 450 € pauschal. |
| 7 | Reichweite | `reichweite.html` | 8 Instagram-Insights-Screenshots + Zahlen. **Stand 10.08.2026:** 1.020.876 Aufrufe / 30 Tage, 92,7 % Nicht-Follower, 6.070 Follower. |
| 8 | Über mich | `ueber-mich.html` | Hero-Split, Werdegang, „Julia im Alltag"-Masonry-Galerie (8 Bilder), Wissen, Werte. |

### Weitere Seiten (nicht in Hauptnav)

- `index.html` — Startseite mit Landing-Overlay (jetzt EIN Wort: „Ihr Timing. Entscheidet alles.")
- `anfrage.html` — 8-Fragen-Anfrageformular
- `angebot.html` — Angebots-Seite
- `hotel-guide.html` — private Landing (noindex/nofollow, robots.txt disallow)
- `mealbites.html` — Landing für Mealbites-Projekt
- `impressum.html`, `datenschutz.html`, `agb.html`
- `old-index.html` — alter Stand, archiv

---

## Design-System

### Farb-Palette (Stand 10.08.2026 — reduziert-neutral)

Basis, Ink, Muted (in `css/onpoint.css`):

```
--bg:          #d8cfc0   /* warmes tieferes Greige */
--bg-warm:     #c9bfaf   /* deeper greige für Sektionen */
--bg-soft:     #ddd4c5
--bg-mint:     #d2c9ba
--card:        #ffffff
--ink:         #2D1F22   /* Body-Text: warmes Pflaume-Braun */
--ink-soft:    #4a3236
--muted:       #8a6f72
--muted-lite:  #b09a9c
```

Hauptakzent (Buttons, Nav-Aktiv, Borders) — nach mehreren Iterationen jetzt weiche Rose als sanfter Akzent:

```
--bordeaux:      #be7676   /* Rose — Hauptakzent */
--bordeaux-hi:   #d29999
--bordeaux-deep: #8b5555
```

Highlight (sparsam, nur in Headline-Italics und CTA-em):

```
--oxblood:     #4a1418   /* sehr dunkles Rot — Highlight-Punkt */
--oxblood-hi:  #6d1e24
```

Landing-Rotation (nur index.html Overlay):

```
Cream  #ECEAE6   /* Landing-BG 1 */
Orange #ff8854   /* Landing-BG 2 */
Oxblood #500011  /* Landing-Highlight */
```

Kupfer/Gold-Legacy (in einzelnen Sektionen noch vorhanden):

```
--copper:       #C48B6C
--copper-dark:  #A0705A
--copper-light: #E8C4A8
--gold:         #C48B6C (Alias von --copper)
```

**Iteration-Historie:** Bordeaux #660e30 (Juli) → Rose #be7676 → Copper #a67150 (verworfen) → Rose zurück + Greige-Base + Oxblood-Highlight. Julia will Kunden-Kontinuität mit ihren roten Visitenkarten — deshalb Oxblood #500011 als Highlight statt hellem Rot. Rot+Gold ist die Zielrichtung, aber nicht plakativ, sondern sparsam.

### Landing (index.html) — Stand 10.08.

- **Nur EIN Wort:** „Ihr Timing." mit Sub „Entscheidet alles."
- **Grund:** 4-Wörter-Version war zu lang, Kunden bounced ab
- **Snap-Flip:** 2 Farbstände (Oxblood-BG + Orange-Text ↔ Orange-BG + Oxblood-Text)
- **Font:** Archivo Black, uppercase, clamp(72px – 260px)
- **Dauer:** ca. 2,2 Sekunden bis Choice-Screen
- **Kein Fade** (`transition: none` auf .lo-stage)

### Typografie

- **Headlines & UI:** Raleway 500–900
- **Landing-Display:** Archivo Black (nur Landing-Overlay)
- **Body:** Quicksand 300–700
- Legacy als Fallbacks: Rubik, Space Grotesk, Playfair Display, Object Sans

**Fonts-Import (in `css/onpoint.css`, gespiegelt in allen HTML-Heads):**

```
Space Grotesk 400-700
Clash Display 600-700
Bricolage Grotesque 12..96, 600..800
Rubik 400-900
Archivo Black
Quicksand 300-700
Raleway 500-900
```

### Design-Muster (mymiapage.de / Soul-of-Women-Club inspiriert)

Wiederkehrende Layout-Bausteine sitewide:

1. **Editorial-Split** — Text + großes Foto nebeneinander (`.wo-cta-split`, `.um-hero-inner`, `.um-wissen-split`, `.split-julia`, `.md-block`, `.cta-block.with-photo`)
2. **Transparente Text-Overlay auf Foto** — cream 94 % backdrop-blur, Oxblood-Text, Muted-Small-Caps-Label. Konsistente Signature auf: über-mich, warum-onpoint, erklärtag, social-media, mediendesign, cta-block sitewide.
3. **Masonry-Grid** mit versetzten Bildgrößen (`.tall`, `.wide`, `.square`) — z.B. `um-gallery-grid` (Julia im Alltag), `k-gallery-grid` (Kunst)
4. **Alternierendes Text-Bild-Layout** — Bild links/rechts wechselnd mit `.reverse`-Modifier (`md-block` auf mediendesign)
5. **Tab-Selector** — Vogue-Editorial-Stil, aktiv = Oxblood-BG + Cream-Text, Fade-In-Content (Branchen-Tabs auf social-media)
6. **Screenshot-Grid** — iPhone-9:19.5-Aspect, Hover-Lift (Reichweite)
7. **KENNENLERNEN-CTA mit Julia-Foto** — `.cta-block.with-photo` Modifier sitewide: Text links + Portrait rechts mit „24h Antwortversprechen"-Overlay. Aktiv auf erklaertag/mediendesign/social-media/reichweite/websites/videografie. warum-onpoint hat eigene `.wo-cta-split`-Variante.

### Text-Regeln

- **Sie-Form durchgängig.** Diese Site siezt (im Gegensatz zu juliabergles.de).
- Kein „Wusstest du...", keine KI-Sprache
- Keine Bindestriche als Trenner. Punkt oder neue Zeile.
- Jeder Satz auf neue Zeile (`<br>` in HTML)
- Zahlen sauber schreiben, nicht verschnörkeln
- Konditionen und Preise klar zeigen
- **Julia schreibt alle Prosa selbst.** Claude macht Placeholder + strukturelles/faktisches Scaffolding (Header, Button-Labels, Nav, kurze Beschreibungen).

### Content-Regeln

- **Kein Heilversprechen** (auch nicht für TerraLuna-App-Bezug)
- **Kein „wir sind ein großes Team"** — Julia ist Solo mit Freelancer-Netzwerk
- **Peer-Support = Erfahrungsaustausch**, nicht Beratung (Heilpraktiker-Gesetz-relevant)

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
- Alter dominant: **25–34 mit 34,7 %**, 35–44 mit 25,3 %, 18–24 mit 14,9 %, 45–54 mit 13,4 %
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
| Retainer | auf Anfrage | 3 Monate Mindestlaufzeit, 1 Monat Kündigung, Preisanpassung nach 8 Monaten |

Alle Preise zzgl. MwSt.

---

## Bilder-Struktur

```
Desktop/On Point Website/
├── img/                          # website-Bilder (in Repo, versioniert)
│   ├── portraits/                # julia-1 bis julia-8 (verwendet auf ueber-mich, cta-blocks)
│   ├── landing/                  # webdesign, ueber-julia
│   ├── mediendesign/             # visitenkarten, flyer, verpackung, kunstwerke
│   ├── kunst/                    # 9 Werke (aquarell, acryl, modellieren, etc.)
│   ├── reichweite/               # 8 IG-Insights-Screenshots (IMG_3460–3467)
│   ├── mymia-refs/               # Referenzbilder mymiapage (nur intern, nicht öffentlich zeigen)
│   ├── fitness-1..4.png          # Kunde Fitnessstudio
│   ├── kitchen-1..6.png          # Kunde Bruckner Einrichtungshaus
│   ├── mental-1..10.png          # Kunde Nicole Schleer Mediale Beratung
│   ├── idea-1..7.png             # generische Content-Ideen
│   └── ref-*.jpg                 # Referenz-Fotos
├── Bilder /                      # Julias Rohbilder (unversioniert, Staging)
│   ├── Reichweite aktuell/       # Screenshot-Vorlage
│   ├── Meine Kunst/              # Kunst-Rohbilder
│   └── Social Media Bilder /
└── css/onpoint.css               # Shared Stylesheet
```

**Cross-Nutzung erlaubt:** Blog-Bilder aus dem juliabergles-Website-Repo (`~/Library/Mobile Documents/.../juliabergles Website/blog-bilder/`) dürfen auch hier verwendet werden — sind Julias eigene Fotos.

---

## Was Julia NICHT will

- ❌ Alte Petrol/Champagner-Palette
- ❌ Fraunces und Inter als Primary-Fonts
- ❌ Nunito als Headline-Font (durch Raleway ersetzt)
- ❌ Marquee-Bänder und iPhone-Mockups die unruhig wirken
- ❌ Zu volle Sektionen — Weißraum ist Signature
- ❌ Erfundene Zitate und Testimonials
- ❌ Rose als Hauptton (zu weiblich-verspielt)
- ❌ Reines Rot (zu plakativ) — deshalb Oxblood-Highlight statt dominantem Rot
- ❌ Reines Blau/Maritime (kalt, off-brand)
- ❌ Reines Salbeigrün
- ❌ Bindestriche als Satz-Separator
- ❌ „Wir sind ein großes Team"-Sprache
- ❌ Prosa-Absätze in Julias Stimme (Julia schreibt selbst)
- ❌ Heilversprechen
- ❌ Nicht-Julia-Bilder in Personen-Kontext (nur Julia auf Julia-Fotos, keine Blumen/Landschaften wo Portrait hingehört)

## Was Julia will

- ✅ Editorial-Look Richtung mymiapage.de + Metropolregion-München-Kraft
- ✅ Text und Bilder gemischt, versetzte Layouts, transparente Overlays
- ✅ Viele Julia-Bilder sichtbar (nicht inszeniert, aus der Praxis)
- ✅ Klare Farb-Highlights sparsam einsetzen (Oxblood-Signature)
- ✅ Live-Push zu GitHub Pages, direkt am Handy testen
- ✅ Rot + Gold als Zielfarben (aus Visitenkarten-Kontinuität) — aktuell durch Oxblood-Highlight umgesetzt
- ✅ Referenzen konkret zeigen (nicht anonymisieren wo möglich)
- ✅ Auf jeder Seite: Julia-Foto neben dem KENNENLERNEN-CTA

---

## Iteration-Log 10.08.2026

Diese Session (rund 20 Commits) hat komplett umgebaut:

1. **Landing** metropolregion-Snap-Flip (Cream/Orange/Oxblood, Archivo Black) → auf EIN Wort reduziert
2. **Sitewide Sie-Form** (mechanisch via perl, alle Du/dein/dir → Sie/Ihr/Ihnen mit ~50 Verb-Konjugationen)
3. **Farbe** von Bordeaux #660e30 → durch mehrere Iterationen → Greige-Base + Rose + Oxblood-Highlight
4. **Schrift** von Nunito → Raleway sitewide
5. **social-media** aufgeräumt: ManyChat/Einzelleistungen/Referenzen raus, dafür Vogue-Tabs
6. **Reichweite** komplett neu mit 8 IG-Screenshots + Stand 10.08.
7. **Erklärtag** neue Seite (450 €) mit Nav-Integration
8. **Kunst** ausgebaut auf 9 Werke
9. **Über-mich** Julia-Bilder-Masonry (8 Bilder mymiapage-Grid)
10. **Mediendesign** neue Handschrift-Sektion (3 alternierende Text-Bild-Blöcke)
11. **Warum-onpoint CTA** Split-Layout mit Julia-Foto
12. **CTA-Block sitewide** Julia-Foto daneben (`.cta-block.with-photo`)
13. **Oxblood** in Headline-Italics (h1/h2/cta em)

---

## Offene Punkte / Nächste Iterationen

- **videografie.html** komplett-Redesign im mymiapage-Stil mit eingebetteten Videos
- **Kunst als eigener Menüpunkt** (aktuell nur Sub-Menü unter Mediendesign — Julia will es top-level)
- **Erklärtag als Unterpunkt bei Warum On Point** (Nav-Restructuring)
- **Landing:** mehr Bilder in unterschiedlichen Größen nebeneinander, Cutouts, Text-wrap-around
- **Runde/ovale Rahmen** bei Bildern sitewide als Design-Element
- **Reichweite-Screenshots** systematischer gruppieren (nach Übersicht / Content-Art / Zielgruppe)
- **Kundenprojekte fortführen:** relax Fitness & Vital Lounge (Daniel Hartmann), Hotel-Kooperationen (Panorama Hotel Niedermair), Kooperations-Mails (MyMense, Selenacare, Ooia, Dilling)
- **SSL/HTTPS** auf agentur.juliabergles.de finalisieren
- **Google Search Console** für juliabergles-onpoint.de

---

## Deployment / Externe Tools

- **GitHub Pages:** Hosting agentur.juliabergles.de (Push auf main → live in ~1 min)
- **Cloudflare Workers:** juliabergles-onpoint.de (wrangler.toml, .assetsignore für 25 MiB-Limit)
- **Calendly:** `calendly.com/julia-bergles/30min` (30-Min Kennenlerngespräch)
- **IONOS:** DNS für juliabergles.de-Subdomains
- **Google Search Console:** HTML-Tag verifiziert, sitemap.xml + robots.txt vorhanden

### Standard-Stack für Kunden-Websites (nicht für On Point selbst)

- **Astro** als Framework
- **Decap CMS** für Kunden-Redaktion
- **Vercel oder Netlify** als Hosting
- **Kunden-Ownership:** Domain, Code, Hosting im Kunden-Account
- **Kein Lock-in**, alles gehört dem Kunden

---

## Prinzipien für Änderungen

1. **CONTEXT.md ist die Wahrheit.** Bei jeder neuen Sitzung erst hier reinschauen.
2. **Keine erfundenen Zitate oder Testimonials.**
3. **Fokus:** Kunden-Gewinnung, nicht Content-Produktion.
4. **Kein reines Rot, kein Fraunces, kein Nunito, kein plakatives Blau.**
5. **Weniger Text ist mehr.**
6. **Julia schreibt Prosa selbst** — Claude scaffoldet nur.
7. **Push-first, live testen am Handy.** Kein lokaler Preview-Flow.
8. **Ein Task = ein Commit.** Deutsche Commit-Messages mit warum/was.
9. **Bei Farb-/Design-Fragen:** Julia entscheidet, Claude gibt Meinung + Empfehlung + Direction, dann tut.

---

## Wenn du diese Datei liest…

…dann arbeitest du gerade an On Point Website (Agentur, Sie-Form).
**Verwechsle sie nicht mit juliabergles.de** (Personal Brand, du-Form) — das ist ein anderes Repo unter `~/Library/Mobile Documents/.../juliabergles Website/`.

Zuerst hier reinschauen, dann Änderung planen. Direkt und knapp arbeiten. Live-Push mit klarer deutscher Commit-Message.
