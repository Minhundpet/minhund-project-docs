# Min Hund — Project Status

> **Bruk:** Web-Claude / ChatGPT / Perplexity henter denne ved chat-start for å ha fersk kontekst om hvor prosjektet er. For artikkel-research, hent `docs/research-brief.md` (separat kanal).
>
> **Sist generert:** 2026-05-13
> **Mirror:** https://raw.githubusercontent.com/Minhundpet/minhund-project-docs/main/project-status.md (public repo — claude.ai blokkerer gist-domenet)
> **Struktur:** STATUS (snapshot, byttes ut) → BESLUTNINGER (append-only, dato) → SPRINT-LOG (append-only, uke).

---

## STATUS — 2026-05-13

### Innhold
- **55 hundetips-artikler** publisert, fordelt på 5 kategorier:
  - Helse: 20 · Atferd: 16 · Stell: 9 · Aktivitet: 5 · Ernæring: 5
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
- **8 raseguider planlagt** (rekkefølge ikke fastlåst):
  1. Golden Retriever
  2. Labrador
  3. Border Collie
  4. Cocker Spaniel
  5. Cavalier King Charles Spaniel
  6. Chihuahua
  7. Berner Sennen
  8. Tysk Schäferhund
- Mal: følg eksisterende `griffon-petit-brabancon` raseguide (Stell-kategori, ~2600 ord, canonical hundetips-struktur).

### Åpne tråder (ikke besluttet ennå)
- **Meta titles** — strategi for re-write av eksisterende artikkel-meta. Ingen sweep gjort.
- **AggregateRating schema** — vurderes på produkt-PDPs, men avhenger av at vi har reelle reviews.
- **Reviews-strategi** — hvordan vi samler inn ekte produktanmeldelser (Shopify Reviews app? E-post-flow post-purchase? Manuell innsamling?). Ingen valgt vei.

---

## BESLUTNINGER — append-only, nyeste først

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

### Uke 19 — 2026-05-11 til 2026-05-13 (pågående)

**Tema: PDP-audit + custom product page sweep**

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

**Uke-status:** PDP-audit-fase nær ferdig. Klart for 8-ukers content sprint fra og med uke 20.

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
