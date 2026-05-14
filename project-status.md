# Min Hund — Project Status

> **Bruk:** Web-Claude / ChatGPT / Perplexity henter denne ved chat-start for å ha fersk kontekst om hvor prosjektet er. For artikkel-research, hent `docs/research-brief.md` (separat kanal).
>
> **Sist generert:** 2026-05-13
> **Mirror:** https://raw.githubusercontent.com/Minhundpet/minhund-project-docs/main/project-status.md (public repo — claude.ai blokkerer gist-domenet)
> **Struktur:** STATUS (snapshot, byttes ut) → BESLUTNINGER (append-only, dato) → SPRINT-LOG (append-only, uke).

---

## STATUS — 2026-05-14

### Innhold
- **54 hundetips-artikler** publisert i `/pages/hundetips`-hubben, fordelt på 5 kategorier:
  - Helse: 20 · Atferd: 16 · Stell: 8 · Aktivitet: 5 · Ernæring: 5
- **5 raseguider** publisert i dedikert `/pages/raseguider`-hub (skilt ut fra hundetips 2026-05-13):
  - Griffon Petit Brabançon · Golden Retriever · Labrador Retriever · Border Collie · Engelsk Cocker Spaniel
- **11 produkter** i katalog. **10 custom PDPs** har nå fått full audit-sweep (cart drawer-fix + produkt-spesifikke trust badges + a11y).

### Produkt-PDP-status
- **Pelsfjerner** — fullt auditert (legal disclaimer, FAQ-accordion + JSON-LD, spec-table, intern lenking, product-specific badges, King quote, variant card a11y). Live.
- **Vannflaske (TurPakken 3-i-1)** — light pass (cart drawer + product-specific badges + a11y carryover). Live.
- **8 andre custom PDPs** — mekanisk sveip (cart drawer-wrap, @import font-fjerning, kontrast-fikser, badge-bytte). Live.
  - hundeseng, andefanten, aktiviseringsleke, aktiviseringsskal (CalmBall), ullgenser, sjampoborste, vannskal, potevasker
- Generisk Horizon-template: dekker resten av katalogen.

### Marketing
- **Google Ads: PAUSED.** Ingen aktive kampanjer. Søkeordforskning ikke prioritert nå.
- **Salgs-baseline:** ~2 salg/uke organisk.
- **Newsletter popup:** KING10 to-stegs flow, 30s scroll trigger. Live siden 2026-05-11.

### Neste fase
**8-ukers sprint** (start: uke etter 2026-05-13)
- Cadence: **1 hundetips-artikkel + 1 raseguide per uke**
- **5 av 9 raseguider levert** (Griffon, Golden, Labrador, Border Collie, Engelsk Cocker Spaniel). 4 gjenstår i sprint:
  1. Cavalier King Charles Spaniel
  2. Chihuahua
  3. Berner Sennen (blokkert av XL donut-seng sourcing)
  4. Tysk Schäferhund (blokkert av XL donut-seng sourcing)
- Mal: følg canonical raseguide-mønster — 12 H2, 9 FAQ, 3 inline product callouts, "Anbefalt for [Rase]" post-FAQ recap-seksjon med rasespesifikk produktrangering, Tips fra King-seksjon, FAQPage JSON-LD 1:1 match. Sidebar er TOC + King-quip (intet produkt-kort). Full spec i `docs/page-patterns.md` "Raseguide Canonical Pattern".
- **In-prose crossover-lenker** mellom raseguider er SEO-vektor: Labrador-guiden lenker til Golden i H2-3 (linje-distinksjon) og H2-4 (temperament); Cocker-guiden lenker til Labrador i H2-3. Treffer "[rase] vs [rase]"-spørringer som er undertargetet av norske dyrebutikker.
- **GA4 product_callout_click tracking** er instrumented på alle 6 product CTAs per raseguide (30 totalt på 5 raseguider). Events fires via `Shopify.analytics.publish` + `dataLayer.push`, men Custom Pixel-forwarding til GA4 er paused (se Paused threads).
- Publiseres til `/pages/raseguider`-hub. llms.txt-kategori: `Raseguide`. Hub-card-mal: badge `Rase`, kategori `Raseguide`.

### Åpne tråder (ikke besluttet ennå)
- **Meta titles** — strategi for re-write av eksisterende artikkel-meta. Ingen sweep gjort.
- **AggregateRating schema** — vurderes på produkt-PDPs, men avhenger av at vi har reelle reviews.
- **Reviews-strategi** — hvordan vi samler inn ekte produktanmeldelser (Shopify Reviews app? E-post-flow post-purchase? Manuell innsamling?). Ingen valgt vei.
- **Sourcing: XL donut-seng (≥40 kg)** — Beroligende hundeseng maxer på 25 kg (Large). Blokkerer seng-callout på 4 av 6 gjenværende sprint-raseguider: Berner Sennen, Tysk Schäferhund, +2 large breeds TBD (Golden + Labrador allerede levert uten seng-CTA). Sondre må source XL-størrelse før disse rasene får seng-CTA. **Reprioritering anbefalt:** trekk smaller breeds frem i køen (Cavalier King Charles Spaniel, Cocker Spaniel, evt. Bichon Havanais som ny kandidat) mens sourcing pågår — disse trenger ikke XL-seng og kan publiseres uten å vente på blokker-løsning.

---

## Paused threads

- **GA4 product_callout_click tracking** (paused 2026-05-14) — Custom Pixel setup paused. Events fire via `Shopify.analytics.publish` (and `dataLayer.push`, `window.gtag` fallback) on all 24 product CTAs across the 4 raseguider, but no forwarder is configured — events go nowhere. Resume by creating GA4 Measurement Protocol API secret + Shopify Custom Pixel in Admin → Settings → Customer events. Tracking infra commit: `0cb96a4`. Snippet: `snippets/mh-track-product-callouts.liquid`.

---

## BESLUTNINGER — append-only, nyeste først

### 2026-05-14 — Raseguide CRO Pattern C+ låst som canonical (sidebar produktkort fjernet, post-FAQ recap lagt til)
Etter Sondres observasjon at sidebar Pelsfjerner-kortet på Border Collie var begravd under TOC + King-quip på fold (sticky-stack for høy), gjennomført strategisk audit + ship.
- **Fjernet:** sidebar `mh-article__product-box--sidebar` på alle 4 daværende raseguider. Sidebar er nå TOC + King-quip kun.
- **Lagt til:** ny `mh-article__recommend` BEM-blokk mellom Les også og disclaimer — "Anbefalt for [Rase]"-H2 + 80–120 ord rasespesifikk intro + 3-kort grid (1-col mobile, 3-col ≥720px, 48px min tap-target).
- **Breed-tunet rangering:** Border Collie → Aktiviseringsleke/TurPakken/Pelsfjerner; Golden → Pelsfjerner/TurPakken/Aktiviseringsleke; Labrador → TurPakken/Pelsfjerner/Aktiviseringsleke; Griffon → Beroligende-seng/Aktiviseringsleke/Pelsfjerner; Cocker → Pelsfjerner/TurPakken/Aktiviseringsleke. Hero-spot = rasens primær daglig-pain.
- **Skjema uendret:** ingen Product/ItemList JSON-LD lagt til — Article-schema beholdt for å sikre at LLM-er klassifiserer sidene som informational, ikke commercial. AI Overview-citation-kvalitet bevart.
- **Griffon catch-up:** 2 manglende inline-callouts (Pelsfjerner i §Pelsstell, Aktiviseringsleke i §Fôring) lagt til så Griffon matcher canonical.
- **Canonical mønster dokumentert** i `docs/page-patterns.md` (ny "Raseguide Canonical Pattern"-seksjon).
- **Hvorfor:** Bottom-CTA etter FAQ er peak-trust + peak-intent moment som var helt fraværende. Sidebar-produkt-kort lå under fold og leverte 0 konverteringsmomenter. Bytte = behold informational tonefall, åpne én tydelig konverteringsmoment der leseren har bygget tillit.
- **Måleimplikasjon:** Skalert-effekt målbar via GA4 `product_callout_click` per posisjon (inline-1/2/3 vs recommend-1/2/3) per breed_page — *forutsatt Custom Pixel-forwarding gjenopptas* (se Paused threads).

### 2026-05-14 — Pelsfjerner-hansken copy må eksplisitt navngi textile-target (ikke "fjerner pels" alene)
Identifisert mønsterfeil i raseguide-template: short-form "Pelsfjerner-hansken vår fjerner pels på sekunder" kan misleses som on-dog use og bryter med dokumentert produktregel "TEXTILES ONLY — NEVER for use on dogs" (`docs/products.md`).
- **Approved fraseringer:** "fjerner hundehår fra tekstiler", "fjerner [hundehår/hår/det] fra sofa, klær og bilseter", "tar pels fra sofa, klær og bil".
- **Forbidden short forms:** "fjerner pels", "fjerner hundehår" (uten eksplisitt textile-target).
- **Fix scope:** 4 recommend-card descs reframet med textile-first lead (Sondres exact copy), 1 inline §7 callout på Griffon strammet ("fjerner pels på sekunder" → "fjerner hundehår fra tekstiler"), 8 øvrige mentions auditert + bekreftet OK.
- **Gotcha dokumentert** i `docs/gotchas.md` ("Pelsfjerner Ambiguous 'Fjerner Pels' Framing") så fremtidig raseguide-generering ikke reintroduserer mønsteret.
- **Konsekvens:** Regelen gjelder alle raseguider og hundetips-artikler. Cocker-guide (shipped samme dag) følger denne fra start.

### 2026-05-13 — Raseguider får top-level nav-placering (sibling til Hundetips)

`/pages/raseguider` skal være top-level menyvalg, ikke kun discovery-via-cross-link. Begrunnelse: (1) internal-link-equity fra hver side på sitet treffer raseguider-hubben → bedre SEO på "[rase] raseguide"-spørringer; (2) serverer kjøpsbeslutnings-publikummet som hundetips ikke når; (3) skalerer til 8 raseguider og videre uten å begraves; (4) konkurransefortrinn — norske dyrebutikker underinvesterer i breed-content. Implementeres som "Guider"-dropdown med Hundetips + Raseguider som submenyer (alternativ: rene sibling-menypunkter; valgt for kompakthet).

### 2026-05-13 — Raseguider får dedikert hub (/pages/raseguider), separat fra hundetips

**Hva endret seg:** Raseguider (breed guides) flyttet ut av `/pages/hundetips`-hubben til ny dedikert `/pages/raseguider`-hub. Eksisterende breed-guide URLs (`/pages/golden-retriever`, `/pages/griffon-petit-brabancon`) er uendret — kun hub-listingen flyttes.

**Why:** Raseguider og hundetips har fundamentalt forskjellig brukerintensjon. Hundetips = problem-driven (general care, atferd, helse). Raseguider = purchase-decision-driven (skal jeg kjøpe denne rasen?). SEO-targeting, schema og bruker-flow blir tydeligere når de splittes. Sprintens 8 raseguider hadde gjort hundetips-hubben uoverskuelig.

**Tekniske endringer:**
- Ny template: `page.raseguider.json` (cloned struktur fra page.hundetips.json)
- Nye seksjoner: `sections/raseguider-hero.liquid`, `sections/raseguider-grid.liquid`
- Fjernet kort fra `page.hundetips.json`: card_8 (Griffon), card_56 (Golden) — totalt går fra 56 → 54 kort
- Back-button + breadcrumb i begge raseguider oppdatert til `/pages/raseguider`
- llms.txt: `Stell` → `Raseguide` for begge breed-guide entries
- Hundetips-hub H1 retargeted fra "Hundeguider — komplett kunnskapsbase" til "Hundetips — praktiske guider for stell, atferd, helse og ernæring"
- ItemList JSON-LD nå auto-derived fra `section.blocks` på begge hubs — ingen mer stale hardcoded handle-arrays

**Manual steps for Sondre:**
1. Opprett ny Shopify Admin-side `Raseguider` (handle: `raseguider`, template: `page.raseguider`, Visible)
2. Sett meta-title + description på begge hubs (begge mangler eller skal retargetes)
3. Legg til "Raseguider" i hovedmenyen (Shopify Admin → Navigation)

### 2026-05-13 — Web-Claude project memory flow (via public repo)
Opprettet `Minhundpet/minhund-project-docs` (public GitHub repo) som kanonisk kilde for prosjekt-status. Erstatter Gist-kanalen som viste seg ubrukbar.
- **Fil:** `project-status.md` (i repo-roten)
- **Raw URL:** https://raw.githubusercontent.com/Minhundpet/minhund-project-docs/main/project-status.md
- **Hvorfor:** `gist.githubusercontent.com` er blokkert av claude.ai sin `robots.txt`-håndhevelse — web-Claude kan ikke `web_fetch` Gist-URLer uansett om de er public eller secret. `raw.githubusercontent.com` fungerer.
- **Web-Claude memory-regel:** Når Sondre sier "vi fortsetter" i en ny chat, må han **paste raw URL-en i samme melding**. `web_fetch` krever bruker-oppgitt URL og kan ikke hente fra memory alene.
- **Anbefaling til Sondre:** Lagre snippet som bokmerke / text-expander:
  ```
  vi fortsetter — hent https://raw.githubusercontent.com/Minhundpet/minhund-project-docs/main/project-status.md
  ```
- **Konsekvens:** Gist-kanalen for project-status nedlagt. Research-brief Gist beholdes inntil videre (testet OK tidligere — overvåk).

### 2026-05-13 — Trust badges blir produkt-spesifikke (ikke generiske)
Alle 10 custom PDPs hadde identiske generiske badges (Norsk eierskap, Trygg handel, etc). Erstattet med 4 produkt-spesifikke badges per PDP, formulert ut fra hvert produkts kjernenytte.
- **Hvorfor:** Generiske badges sier ingenting unikt. Produkt-spesifikke gir konkret salgsverdi og forsterker USP per produkt.
- **Konsekvens:** Trust-strip på `/collections/all` og footer fortsatt generisk — bare PDP-badges er produkt-spesifikke.

### 2026-05-13 — Cart drawer-fix krever `product-form-component`-wrap (HARD)
Horizon-temaets cart drawer fungerer ikke uten at ATC-formen er wrappet i `<product-form-component>`. Alle 10 custom PDPs hadde mistet denne wrapperen — re-wrappet i dag.
- **Hvorfor:** Horizon JS binder eventer mot `product-form-component`-Web Component. Uten wrap = silent failure (knapp gjør ingenting).
- **Konsekvens:** Alle nye custom PDPs MÅ wrappes. Lagt til som hard regel i `.claude/rules/horizon-cart.md`.

### 2026-05-13 — Pelsfjerner FAQ-pattern blir kanonisk for product-PDPs
6 hardkodede Q&As i `<details>/<summary>`-accordion + FAQPage JSON-LD med 1:1 match. INGEN metafield-basert FAQ.
- **Hvorfor:** Metafield-FAQ koblet til Shopify Admin = vanskelig å versjonere, schema-mismatch-risiko. Hardkodet = git-historikk + lett å revidere.
- **Konsekvens:** Mønster gjelder ALLE custom PDPs framover. Dokumentert i `CLAUDE.md`.

### 2026-05-13 — King quote som "punchline" på pelsfjerner-PDP
Korte King-sitat lagt inn som avsluttende menneskelig touch over CTA. Brand voice signaliseres tydeligere uten å bli sentimentalt.
- **Hvorfor:** Differensiering mot generiske Shopify-PDPer. King er en troverdig "stemme" for målgruppen.
- **Konsekvens:** Vurderes for andre PDPer der det passer naturlig — ikke et must.

### 2026-05-12 — llms.txt-arkitektur omlagt (Shopify magic-route)
Shopify rullet ut native `/llms.txt` + `/llms-full.txt`. URL-redirects funker ikke lenger. Vi overrider via `templates/llms.txt.liquid` som rendrer self-sufficient snippets med inline artikkel/produkt-data.
- **Hvorfor:** Shopify-restriksjon (kun `request` + `settings` tilgjengelig i magic-route Liquid). Vi MÅ inline-hardkode.
- **Konsekvens:** Nye artikler/produkter må manuelt legges i `snippets/llms-articles-data.liquid` + `snippets/llms-products-data.liquid`.

### 2026-05-12 — Pages-only arkitektur (blogg fjernet permanent)
"News"-bloggen slettet fra Shopify Admin. `/blogs/news` = 404. Alle "artikler" er Shopify Pages.
- **Hvorfor:** Forenkler URL-struktur, schema og navigasjon. Pages gir mer fleksibilitet på templates.
- **Konsekvens:** Aldri foreslå blogg-løsninger eller `/blogs/news/*`-URLer. Alt nytt = Page + template.

### 2026-05-11 — Legal-risk-audit gjennomført (Fase A-serien)
Stor sveip: prescription-merkenavn fjernet, "forskning viser"-claims kildebelagt eller mykere formulert, named competitors fjernet, absolute superlativer mykere, prisinfo dato-stemplet, brand-genericization.
- **Hvorfor:** Markedsføringsloven + Legemiddelforskriften kap. 13 + Forbrukertilsynet. Risiko-reduksjon før vi skalerer trafikk.
- **Konsekvens:** Voice-regler i `docs/research-brief.md` + harde regler i `CLAUDE.md` reflekterer dette. Aldri "best i Norge", alltid "etter vår vurdering", `ca. XX kr` på alle priser.

---

## SPRINT-LOG — append-only, nyeste øverst

### Uke 19 — 2026-05-11 til 2026-05-14 (pågående)

**Tema: PDP-audit + raseguide sprint + CRO-optimering**

**2026-05-14 (Pattern C+ CRO sweep + Cocker raseguide-launch — 6 commits)**
- `6bcae46` Pattern C+ CRO ship på alle 4 daværende raseguider: sidebar produktkort fjernet, `mh-article__recommend` post-FAQ recap-seksjon lagt til med breed-tunet 3-kort grid; Griffon catch-up med 2 manglende inline-callouts; canonical mønster dokumentert i `docs/page-patterns.md`. word_counts oppdatert i llms-data (BC 3400→3800, Griffon 2600→2700, mindre justeringer på Golden/Lab). 6 filer endret, +452/-73 linjer.
- `0cb96a4` GA4 product_callout_click tracking-layer: ny snippet `snippets/mh-track-product-callouts.liquid` (delegated click handler via dataLayer + Shopify.analytics.publish + window.gtag fallback). 24 product CTAs på 4 raseguider tagget med `data-mh-event/product/position/breed/placement` attrs. Idempotent re-init guard. 5 filer endret, +84/-24 linjer.
- `4fe7377` Pelsfjerner copy clarification: alle 4 "Anbefalt for"-recommend-cards reframet textile-first per Sondres exact copy; Griffon inline §7 callout ambiguity ("fjerner pels på sekunder" → "fjerner hundehår fra tekstiler") fikset. 4 filer endret, +5/-5 linjer.
- `62d66e4` `docs/gotchas.md` oppdatert med ny "Pelsfjerner Ambiguous 'Fjerner Pels' Framing"-gotcha + approved/forbidden frasering så fremtidig copy-generering unngår mønsterfeil.
- `2c4c51a` `docs/project-status.md` "Paused threads"-seksjon lagt til: GA4 product_callout_click tracking Custom Pixel-setup paused etter Chrome-extension audit avslørte at GT-NGS3DWB9 er Shopify Channel App-destinasjon (ikke ekte GTM container). Events fire via Shopify.analytics.publish men ingen forwarder configured ennå.
- `4cbf107` Engelsk Cocker Spaniel raseguide live (sprint guide #5): `sections/hundetips-cocker-spaniel.liquid` (1073 linjer, ~3650 ord), `templates/page.cocker-spaniel.json`, hub card_5 lagt til `templates/page.raseguider.json`, llms-data entry inserted alphabetisk mellom border-collie og golden-retriever (entry-count 58→59). Canonical 12 H2 + 9 FAQ + 3 inline callouts + Anbefalt-for recap (Pelsfjerner/TurPakken/Aktiviseringsleke). H2-6 ørebetennelser-info-box som rase-definerende helse-utfordring; H2-7 ear-cleaning danger box; H2-3 cross-link til Labrador; "Rage Syndrome" intentionally omitted. Hero CDN-image verifisert 200 pre-commit. Admin-step (Online Store → Pages → Add page med template `page.cocker-spaniel`, handle `cocker-spaniel`) pending Sondre.

**2026-05-13 natt (Labrador raseguide-launch — 1 commit)**
- `9921d54` Labrador Retriever raseguide publisert — ~3500 ord, 12 H2, 8 FAQ, 3 product callouts (TurPakken, Pelsfjerner, Aktiviseringsleke). 3. raseguide totalt; mønster fra Golden speilet 1:1 (CSS+JS byte-identisk). Helse-dekning: HD/AD, EIC (DNA-test), CNM (DNA-test), arvelige øyelidelser (PRA/katarakt/grønn stær), POMC-mutasjonen (Raffan et al. 2016) framet som forskningsfunn, kreft, hud/øre, korsbånd, GDV. **In-prose crossover-lenker til Golden i H2-3 og H2-4** — første implementering av SEO-vektoren for "Golden vs Labrador"-norske spørringer. Hub card_3 lagt til `/pages/raseguider` med image_url. llms.txt entry count: 56 → 57 (header-comment off-by-1 korrigert).

**2026-05-13 kveld (raseguide-launch + hub-restruktur + header-polish — 9 commits)**
- `7b95eec` Header dropdown containment-fix: top gradient nå `background-image` (ikke separat `::before`), hover-bar bruker `top: 11px / bottom: 11px` inset (kan ikke overflowe link-bounds)
- `7ce0166` Header dropdown: skjuler `.overflow-menu::after` phantom panel (full-bredde hvit strip som lakk gjennom bak compact dropdowns)
- `9f1d906` Header dropdown visual polish: 3px brand-green gradient stripe, modernere 2-lags skygge, hover-state med animert left-bar, parent-link grønn når dropdown er åpen
- `7b3a605` Header dropdown positioning fix: dropdown-paneler aligned under parent items (Guider, Om oss), ikke flush mot viewport-kanten. CSS-only override per Horizon cart rule.
- `7c24672` llms.txt: `Raseguide` lagt til som ny kategori i renderer (uten dette ble breed-guide-entries usynlige i `/llms.txt`)
- `d43dc63` Hub-restruktur: `/pages/raseguider` skilt ut fra `/pages/hundetips`. Egen template + 2 nye section-filer. Tilbakekobling-knapper + breadcrumbs i begge raseguider oppdatert. ItemList JSON-LD nå auto-derived fra `section.blocks` på begge hubs (retiret stale hardcoded handle-array). Hundetips-hub H1 + meta retargeted mot problem-solving intent.
- `3a4af0a` Golden raseguide: hub card_56 image swappet til `golden.png` (midlertidig — venter dedikert square crop)
- `4c9e939` Golden raseguide: hero-bilde swappet til `golden.png` (live)
- `18b4827` Golden Retriever raseguide publisert — ~3050 ord, 12 H2, 8 FAQ, 3 product callouts (TurPakken, Pelsfjerner, Aktiviseringsleke). 2. raseguide totalt; mal låst for resterende 6.

**2026-05-13 (i dag — 11 commits)**
- `6237273` Pelsfjerner: legal disclaimer, dry-use guidance, a11y-fikser
- `aafb84c` Pelsfjerner: ATC-form wrappet i `product-form-component` (cart drawer-fix)
- `084dd19` Pelsfjerner: 6 hardkodede FAQ Q&As + matching FAQPage JSON-LD
- `98ed6a3` Variant cards: radio-group a11y + bundle price anchoring (på tvers av PDPs)
- `95c7ad6` Pelsfjerner: spec-table + intern lenking + llms.txt-oppdatering
- `ff3f5b5` Pelsfjerner: produkt-spesifikke trust badges + King quote-punchline
- `50edf51` docs: product marketing context oppdatert
- `bd75f9b` Vannflaske: cart drawer-fix + trust badges + a11y carryover
- `3af6dda` Sweep: 4 mekaniske fixes på 8 gjenværende custom PDPs (@import, kontrast, cart-wrap)
- `4377e02` Produkt-spesifikke trust badges på 8 PDPs + ullgenser size disclaimer
- `e98f7bb` Vannskal: badge 4 byttet ("Bra for kort snute" → "For ivrige drikkere")

**2026-05-13 (process / infrastructure)**
- Opprettet public repo `Minhundpet/minhund-project-docs` for cross-chat-kontinuitet
- Pushet `project-status.md` (kanonisk prosjekt-state) til root
- Verifisert at `web_fetch` fungerer på `raw.githubusercontent.com`-URL
- Gist-kanal for project-status nedlagt (robots.txt blokkerer claude.ai-bots på gist-domenet)
- Memory: `feedback_update_dagens_fremdrift_shorthand.md` lagret — kommandoen "oppdater dagens fremdrift" trigger full update-flow

**2026-05-12**
- 3 nye hundetips-artikler publisert: `hund-spiser-for-fort` (Helse), `hund-vil-ikke-spise` (Helse), `hund-spiser-gress` (Atferd)
- llms.txt-arkitektur omlagt (Shopify magic-route override)
- "News"-bloggen slettet — pages-only arkitektur
- Terminologi-standardisering: brakycefal → brachycefal (NVF-standard)
- `research-brief.md` opprettet for web-Claude-kontekst

**2026-05-11**
- Newsletter popup live (KING10, to-stegs, 30s scroll)
- `/collections/all` + kategori-landingssider refactored (norsk H1, ItemList schema, LCP-fix, quick-add)
- Legal-risk-audit Fase A1–A5 gjennomført på hele hundetips-corpus
- Homepage audit: lang=nb, JSON-LD WebSite+SearchAction, brand fonts oppdatert til Playfair Display + DM Sans

**Uke-status:** PDP-audit-fase ferdig. Content sprint i gang — **3 av 9 raseguider levert** (Griffon, Golden, Labrador). Raseguider-hub-infrastruktur etablert (ny template, section-filer, llms.txt-kategori, top-level nav-plassering). Crossover-link-SEO-vektoren mellom raseguider aktivert med Labrador↔Golden. Klart for 6 gjenværende raseguider + 1 hundetips/uke, men XL-donut-seng-sourcing er blokker for Berner Sennen og Schäfer — reprioritering mot small breeds anbefalt.

---

## Hvordan oppdatere denne fila

- **STATUS:** Byttes ut i sin helhet ved hver oppdatering. Reflekter dagens snapshot.
- **BESLUTNINGER:** Append-only. Ny beslutning øverst i listen. Inkluder dato + kort begrunnelse + konsekvens.
- **SPRINT-LOG:** Append-only per uke. Ny uke øverst. Commits + tema + uke-status.

**Update-flyt (git-basert):**
1. Edit canonical kilde: `docs/project-status.md` i `Minhundpet/minhund-theme`
2. Commit + push i theme-repo
3. Sync til public mirror:
   ```bash
   cp "/Users/sondreuleberg/Downloads/Min hund nettside/docs/project-status.md" ~/Downloads/minhund-project-docs/project-status.md
   cd ~/Downloads/minhund-project-docs && git add project-status.md && git commit -m "sync: <reason>" && git push
   ```
4. Raw URL serverer ny versjon innen ~5 min (cache). URL endres aldri, så gamle web-Claude-chatter fungerer fortsatt.

Source of truth = theme-repo. Public repo er mirror-only — aldri rediger direkte der.
