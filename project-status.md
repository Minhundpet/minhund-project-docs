# Min Hund — Project Status

> **Bruk:** Web-Claude / ChatGPT / Perplexity henter denne ved chat-start for å ha fersk kontekst om hvor prosjektet er. For artikkel-research, hent `docs/research-brief.md` (separat kanal).
>
> **Sist generert:** 2026-08-12 morgen (vann-pilar utvidet; se BESLUTNINGER 2026-08-12). Forrige: 2026-08-11 kveld (**SEO-sveip: 32 lekkasjesider fikk ny title + meta, og to strukturelle GSC-bugs ble lukket.** GSC 90d: 4 480 klikk / 393 972 visninger / CTR 1,14 % / posisjon 8,7 — 96,9 % av årets visninger falt i dette kvartalet. Raseguidene underpresterer som segment (0,85 % mot hundetips' 1,23 %) på samme posisjon, altså et snippet-problem, ikke et rangeringsproblem. **Metodefunn:** GSC-sidedata må filtreres for anker-URL-er (`excludingRegex: "#"`) — 353 av 499 rader var jump-lenker som spiste opp 500-radstaket. **Bug 1 FIKSET:** `/pages/<handle>/<hva-som-helst>` svarte 200 og selv-kanonikaliserte under alle 129 sider; `mh_canonical` i `snippets/meta-tags.liquid` peker nå på ekte side-URL for både canonical og og:url. **Bug 2 DELVIS:** noindex på `/collections/frontpage` er bekreftet tilsiktet og beholdt; sitemap-oppføringen krever avpublisering fra Online Store — manuelt Admin-steg, `write_publications` mangler i `shopauth`. **Én faktafeil fanget før publisering:** vizsla «kan ikke være mye alene» → «trives dårlig alene». **Intern sjargong funnet live i meta:** «TRIPPEL helsemoat» og «storrase-helse-trilogi» fjernet. **Nedjustert anslag:** ~1 900 gjenvinnbare klikk var for høyt — ingredienssidene taper til AI Overviews uansett meta; realistisk 400–700/kvartal.)
>
> **Forrige (2026-08-07 formiddag):** Meta-sporet — prosjektets arbeidsminne restrukturert i fem prosjekt-level skills under `.claude/skills/`; CLAUDE.md 175 → 127 linjer.
> **Mirror:** https://raw.githubusercontent.com/Minhundpet/minhund-project-docs/main/project-status.md (public repo — claude.ai blokkerer gist-domenet)
> **Struktur:** STATUS (snapshot, byttes ut) → BESLUTNINGER (append-only, dato) → SPRINT-LOG (append-only, uke).

---

## STATUS — 2026-05-27 morgen (**4-sprint serien #60→#63 etablerer TRIPPEL-moat-format som korpus-standard** når 3 navngitte primær-studier finnes. **Sprint #63 WHWT deployed i morges** — raseguide #60, åpner skotsk terrier-cluster. TRIPPEL breed-eksklusiv health-moat: Craniomandibular Osteopathy (Hytönen 2016 PLoS Genet — autosomalt DOMINANT m/ufullstendig penetrans, oppdatert fra eldre recessive) + Canine Idiopathic Pulmonary Fibrosis «Westie Lung Disease» (Heikkilä 2011 J Vet Intern Med + Clercx 2018 Vet J palliasjon-balanse: orale/inhalerte kortikosteroider + pirfenidone/nintedanib under utprøving) + atopisk dermatitt CAD (Salzmann 2011 BMC Genet + Favrot 2019 Vet Dermatol). 2645 ord canonical i target-band 2550–2650. §6 hand-stripping vs klipping CRYSTAL CLEAR med «permanent damage»-warning (pelsen mister vannavstøtende tekstur + pigmentet svekkes til grålig skjær) + FAQ3 echo — en av få «wrong info → permanent damage»-fakta i hele korpuset. **§9 17,2/100 manuell claim-density = NYTT KORPUS-REKORD** (Legg-Calvé-Perthes + patellaluksasjon NKK-grad 1–4 + Cushings polyuri/polydipsi/polyfagi/pendelmage + ACTH-stimulasjonstest + deksametason-suppresjonstest + Krabbe disease GALC-gen). Anti-anakronisme «landrace-pool»-formulering LÅST som canonical pattern for skotsk terrier-cluster (Cairn 1910 etter WHWT 1907 — eldre kilders «Cairn som forfar» er kronologisk umulig). 8-fil single-commit `e1abc4b` pushet live `#148333264974` med inbound back-links fra jack-russell-terrier + yorkshire-terrier + dvergschnauzer. Pending admin page-creation. **Tidligere i dag:** Sprint #62 Samojedhund deployed (raseguide #59) — polar spisshund-cluster opener; TRIPPEL SHG/COL4A5 (Zheng 1994 PNAS + Jansen 1987 Can J Vet Res) + diabetes mellitus (Catchpole 2013 Vet J, OR 35,84 vs 0,09 % generell) + FEH/SLC24A4 (Pedersen 2017 CAHG) -moat; 2559 ord; commit `80fc622`; FAQ7 hypoallergen-debunk + §6 echo; inbound back-links fra sibirsk-husky + finsk-lapphund. **Tidligere 2026-05-26:** Sprint #61 Greyhound deployed (raseguide #58, mynde-cluster #3) TRIPPEL CYP2B11-anestesi-deficiency (Martinez 2020) + osteosarkom (Rosenberger 2007 + Nationwide 2017) + breed-specific blodverdier (IDEXX + Lefebvre 2011) -moat; 2641 ord; commit `fb5fd92`. Sprint #60 Italiensk Mynde deployed (raseguide #57, mynde-cluster #2) DOBBEL ENAM+DLA-moat; 2793 ord; commit `76a8a06`. **Validert mønstre fra 4-sprint serien:** (1) Buffer-strategi 3× validert (Phase 1 → Phase 3 trim/pad konsistent innen ±100 — sprint #61 +31, #62 −81, #63 −25); (2) Manuell §9 claim-density LÅST som standard metode (regex undertelder veterinær-fagtermer ~30 % konsekvent i 3 sprinter på rad — HD/AD/SAS/T4/TSH/ACTH/auskultasjon/ekkokardiografi); (3) TRIPPEL-moat-format pusher §8-budsjett naturlig over 435 ord til 480–520 (sprint #63 §8 landet 521); (4) Anakronisme-flag for cluster-opener-raseguider: alle «X-rase som forfar»-formuleringer må verifiseres mot kennel-anerkjennelse-årstall. **Åpent funn C2:** root `/llms.txt` server UCP-boilerplate — kuratert liste kun på `/pages/llms-txt`. 🏁 50/50-milepæl nådd 2026-05-20. **60/100 raseguider live; 40 gjenstår.** Polar spisshund-cluster + skotsk terrier-cluster begge etablert med opener-guide + første crossover-links.)

### Innhold
- **59 hundetips-artikler** publisert i `/pages/hundetips`-hubben, fordelt på 5 kategorier (nyeste: hund-sover-mye #59, Helse, 2026-05-29 — fyller Beroligende hundeseng-content-gap; pending admin page-creation):
  - Helse: 23 · Atferd: 18 · Stell: 8 · Aktivitet: 5 · Ernæring: 5
- **60 raseguider** publisert i dedikert `/pages/raseguider`-hub (🏁 50/50-målet nådd 2026-05-20; **Italiensk Mynde #57 + Greyhound #58 + Samojedhund #59 + West Highland White Terrier #60** lagt til 2026-05-26/27 (mynde-cluster #2–#3 + polar spisshund-cluster opener + skotsk terrier-cluster opener); **Strihåret Vorstehhund #51** lagt til 2026-05-21; **Irsk Setter #52** (irsk stående fuglehund, CLAD/PRA-rcd1-moat + Nansen/NISK-historikk) lagt til 2026-05-22 som første guide under nytt 2400–2800-canonical — hub-card + llms-entry live, **pending admin page-creation + hero-bilde**; **Gordon Setter #53** (skotsk stående fuglehund, DOBBEL breed-exclusive HA-CA + PRA-rcd4-moat + hertug Gordon/NGK-historikk) lagt til 2026-05-22 som andre guide under canonical — hub-card_53 + llms-entry + back-links irsk/engelsk live, **pending admin page-creation**; **Jämthund #54** (svensk jaktspisshund, HONEST health-moat — ingen breed-eksklusiv DNA-test; jämthundstriden 1893–1946 + gråhund-differensiering) lagt til 2026-05-24 som tredje guide under canonical — første non-setter, åpner spisshund-nordisk cluster (back-links nge-gra/nge-sort), pending admin page-creation; **Whippet #55** (kortpelset mynde, DOBBEL breed-eksklusiv health-moat — MSTN-mutasjon (Mosher 2007 PLoS Genet, whippet-eksklusiv) + MVD-loci kromosom 15 (Stern 2015 PLoS One); «the poor mans racehorse» + NWK avlsanbefalinger 20.04.2026) lagt til 2026-05-25 som fjerde guide — åpner mynde-cluster med single cross-cluster back-link (jack-russell-terrier), første sprint med Beroligende seng i recap-grid, pending admin page-creation; **Weimaraner #56** (sølvgrå tysk fuglehund, DOBBEL breed-eksklusiv health-moat — HOD-rasespesifikk form Crosse 2013 JAVMA + CNP-mutasjon Keller 2024 Genes; «sølvhunden fra hertughoffet» Carl August + Weimaraner Klub e.V. 1897 + NWK 1981) lagt til 2026-05-25 som femte guide — tysk fuglehund-cluster nesten komplett (Korthåret + Strihåret + Weimaraner cross-linked), 8-fil sprint scope (4 inbound back-links fra tysk + ungarsk + britisk fuglehund-cluster: kortharet-vorstehhund, strihaaret-vorstehhund, vizsla, pointer), recap-grid Pelsfjerner-swap (vs Whippets Beroligende seng) fordi 30–40 kg overstiger 25 kg Large-cap, 2771 ord canonical i DEFAULT-bånd uten moat-override, pending admin page-creation) — **topp 10 norske hunderaser + BOAS-trio + norsk nasjonalrase-trio + tysk brukshund-cluster + britisk fuglehund-cluster + vannhund-trio (Pudel + Lagotto Romagnolo + Yorkshire single-coat-bridge)** etablert. Nyeste sprinter 2026-05-19 (kveld) leverte 3 nye raseguider + 1 Trigger B-omdefinering: **Pudel** (#42, single-coat-rase med fransk vannapportør-arv + Stanley Coren-intelligens + autoimmune-moat Addison/SA + NPK 1956), **Yorkshire Terrier** (#43, toy-format single-coat med britisk yorkshire-arbeider-arv 1860-tallet + patellaluksasjon + LCP + tracheal collapse-moat), **Lagotto Romagnolo** (#44, italiensk trøffelhund + ATG4D/LSD Helsinki/Bern 2015 + LGI2/BFJE 2011 + SLC2A9/HUU + NLK 1956 — single-coat-cluster komplett). Sprint #41 var Trigger B-omdefinering av Labrador Retriever (POMC-moat + chocolate-lifespan-gap + Working vs Show-divergens, ikke ny rase). Tidligere sprinter 2026-05-18/19 (formiddag): #32 Sibirsk Husky · #33 Sankt Bernhardshund · #34 Rhodesian Ridgeback · #35 Korthåret Vorstehhund · #36 Cane Corso · #38 Engelsk Springer Spaniel · #39 Pointer. Sprint #37 var Trigger B Engelsk Cocker Spaniel. Sprint #40 var canonical migration av 20 legacy-filer (4163 ins / 6370 del):
  - **Topp 10 norske raser:** Labrador Retriever · Golden Retriever · Border Collie · Cocker Spaniel · Cavalier King Charles Spaniel · Chihuahua · Norsk Elghund Grå · Tysk Schäferhund · Pomeranian · Finsk Lapphund
  - **Supplerende populære raser:** Griffon Petit Brabançon · Staffordshire Bull Terrier · Bichon Havanais · Engelsk Setter · Dansk-svensk Gårdshund · Mops · Jack Russell Terrier · Berner Sennenhund · Fransk Bulldog · Engelsk Bulldog · Shetland Sheepdog · Norsk Elghund Sort · Norsk Buhund · Beagle · Boxer · Rottweiler · Dachshund · Tibetansk Spaniel · Australian Shepherd · Welsh Corgi Pembroke · Shiba Inu · Sibirsk Husky · Sankt Bernhardshund · Rhodesian Ridgeback · Korthåret Vorstehhund · Cane Corso · Engelsk Springer Spaniel · Pointer · **Pudel** · **Yorkshire Terrier** · **Lagotto Romagnolo** · **Malteser** · **Newfoundland** · **Dvergpinscher** · **Dvergschnauzer** · **Mellomschnauzer** · **Riesenschnauzer** · **Vizsla** · **Coton de Tulear** · **Strihåret Vorstehhund** · **Gordon Setter** · **Jämthund** · **Whippet**
- **15 produkter** i katalog (var 11 → 12 med Valpepakken 04.08 → 15 med slikkematte-trioen 05.–06.08). **13 custom PDPs.** Nyeste: `slikkematte-hund`, `slikkematte-roterende-ball` og `puslespill-hund`, alle med «Nyhet»-badge på kolleksjonssidene.

### Produkt-PDP-status
- **Pelsfjerner** — fullt auditert (legal disclaimer, FAQ-accordion + JSON-LD, spec-table, intern lenking, product-specific badges, King quote, variant card a11y). Live.
- **Vannflaske (TurPakken 3-i-1)** — light pass (cart drawer + product-specific badges + a11y carryover). Live.
- **8 andre custom PDPs** — mekanisk sveip (cart drawer-wrap, @import font-fjerning, kontrast-fikser, badge-bytte). Live.
  - hundeseng, andefanten, aktiviseringsleke, aktiviseringsskal (CalmBall), ullgenser, sjampoborste, vannskal, potevasker
- **Valpepakken** — NY 04.08.2026, katalogens 12. produkt. Custom PDP etter kanonisk mønster + swatch-basert fargevelger (Rosa/Blå) med krysstonende galleribilde. Live. Se BESLUTNINGER 2026-08-04 kveld.
- **Slikkematte (E52 6-i-1)** — NY 05.08.2026, handle `slikkematte-hund`. Custom PDP. Live.
- **Slikkematte m/ roterende ball** — NY 05.08.2026, handle `slikkematte-roterende-ball` (Limited Edition). Custom PDP. Live. Bygget mens Friday endret fem produktfelt i Admin midt i økta — opphavet til gotcha #21.
- **Puslespill for hund** — NY 06.08.2026, handle `puslespill-hund` (het `puslematte-hund` til samme kveld). Custom PDP. Live. Reposisjonert fra måltidsmatte til godbitprodukt samme dag. Se BESLUTNINGER 2026-08-06.
- Generisk Horizon-template: dekker resten av katalogen.

### Marketing
- **Google Ads: PAUSED.** Ingen aktive kampanjer. Søkeordforskning ikke prioritert nå.
- **Salgs-baseline:** ~2 salg/uke organisk.
- **Newsletter popup:** redesignet 2026-07-28, **strukturfikset 2026-08-11** (`7c6c439`, live + verifisert). To varianter (A kommersiell/`KING15`, B innhold/`KINGTIPS15`), tre steg med mikro-ja-segmentering. Trigger nå **12 s timer, eller 50 % scroll tidligst etter 8 s** — scroll-sperren er ny og gjorde timeren reell for første gang (se gotcha #26). Måling via Custom Pixel `150765646` til GA4. **Første frys (28.07–11.08) ga 96,0 % frafall før steg 1** — 620 av 646 visninger lukket uten å velge. Fire strukturårsaker funnet og rettet. **Ny frys til ~5.–8. september 2026** (se MÅLEKONTRAKT 2026-08-11). ⚠️ Avlesningen forutsetter at GA4-blokkerne i gotcha #25 er ryddet — de er det ikke ennå.

### Neste fase
**🏁 Raseguide-sprint MÅLET NÅDD: 50 av 50 (Flat Coated Retriever #50 levert 2026-05-20 sen kveld, commit 2434ddf). Neste: cleanup-sprint #54 (aktiviseringsleke 404-fix globalt + `last_updated` framtidsdato-fix + wordcount-target-justering) + post-#50 crossover-link-audit (`docs/link-audit-2026-05-20.md`). Komplett Schnauzer-trio levert sprint #48–#50 (Dvergschnauzer/Mellomschnauzer/Riesenschnauzer) med "stamfar-rase"-moat-arkitektur; Vizsla #51 + Coton de Tulear #52 med rasespesifikke moat (polymyositt/BNAt).** (Historikk #44 nedenfor uendret:) **Raseguide-sprint utvidet til 41 av 50-milepælen (9 igjen). Single-coat-cluster fullført 2026-05-19 kveld: Pudel (#42) + Yorkshire Terrier (#43) + Lagotto Romagnolo (#44) deler hypoallergen single-coat-vinkel og krysslenker hverandre. Sprint #44 Lagotto Romagnolo deployed 2026-05-19 kveld — italiensk trøffelhund med tre kommersielt testbare rasespesifikke mutasjoner (ATG4D/Lagotto Storage Disease Helsinki/Bern 2015; LGI2/BFJE Helsinki 2011; SLC2A9/hyperurikosuri), vannapportør-arv fra Comacchio-myrene, eneste rase i verden avlet for trøffeljakt. Venter på manuell admin-step (page-creation i Shopify Admin) før `/pages/lagotto-romagnolo` går fra 404 til 200. Sprint #43 Yorkshire Terrier + #42 Pudel levert samme dag (begge NEW). Sprint #41 var Trigger B-omdefinering av Labrador Retriever (POMC-moat, ikke ny rase).

**Ny HARD-regel etablert (effective Sprint #45+):** Raseguide wordcount-disiplin 3700–3950 ord (se BESLUTNINGER 2026-05-19 kveld). Cane Corso 4777 + Lagotto 4726 markert som pre-regel-unntak. CLAUDE.md refactored til path-scoped rules (`.claude/rules/raseguide-canonical.md` + `template-deletion.md`). To pre-eksisterende platform-funn dokumentert i `docs/gotchas.md`: `/llms.txt` → `/agents.md` Shopify-redirect (custom article-data ikke synlig på magic-route; page-route `/pages/llms-txt` fungerer), og `/products/aktiviseringsleke` 404 (44 raseguider linker hit, batch-fix etter Sprint #50).

**Historikk (uendret):** Britisk fuglehund-cluster fullført 2026-05-19 (sprint #37 Cocker + #38 Springer + #39 Pointer + Engelsk Setter etablert tidligere = full britisk stående/støtende-dekning). Sprint #39 Pointer levert 2026-05-19 formiddag — britisk stående fuglehund med spansk pointer-arv via War of Spanish Succession 1714, foredlet av britene 1700-tallet med Foxhound/Greyhound/Bloodhound/Setter-kryssing, NPK stiftet 1907 (én av Norges eldste raseklubber, 9 år yngre enn NKK selv), helse-tetralogi (HD/PRA/chondrodysplasi/AMN — den siste rasespesifikk nevropatisk lidelse med SCN9A-parallell og DNA-test). NKK direkte-sitat «egner seg ikke som ren selskapshund» som tonet rammen for hele guiden — ikke en kosereklame.

Tidligere i dag: Sprint #38 Engelsk Springer Spaniel levert 2026-05-19 02:00–02:05 (britisk støtende fuglehund, Fant 1992-arven). Sprint #37 Engelsk Cocker Spaniel Trigger B-omdefinering 2026-05-19 02:00. Sprint #36 Cane Corso (italiensk vakthund), #35 Korthåret Vorstehhund (tysk allsidig jakthund), #34 Rhodesian Ridgeback, #33 Sankt Bernhardshund, #32 Sibirsk Husky alle levert 2026-05-18. Raseguider-totalen er nå 38 av målet 50.**

**Tidligere milepæler (uendret):** Raseguide-sprint utvidet til 27 av 27 levert i sprint #22–#27. Topp 10 norske hunderaser-milestone fullført 2026-05-16. BOAS-trioen-milestone fullført 2026-05-16 (sen kveld). Norsk nasjonalrase-trio-milestone fullført 2026-05-17 formiddag (sprint #22 + #23). Tysk brukshund-cluster fullført 2026-05-17 ettermiddag (sprint #25 Boxer + sprint #26 Rottweiler). Sprint #27 Dachshund levert 2026-05-17 kveld — tysk grevling-hund med chondrodystrofisk arv (CDDY/FGF4-mutasjonen identifisert 2017, kort-bein-bygning gir disc-degenerasjon) og IVDD-moat etter norsk Stigen 1991-protokoll (327 unge norske dachser røntget; Standard-Strihår 27,1 %, Korthår 16,4 %, Langhår 9,1 %, Dverg-Langhår 36 %; etablerte rygg-røntgen som avls-screening i Norden) + tre størrelser × tre pelstyper (Standard/Dverg/Kanin × Strihår/Korthår/Langhår = ni varianter med ulik helse-profil) + IDC 0–3 grading-skala med Jensen 2008-anbefaling (4+ kalsifiseringer ved 2 år = ikke i avl).** Sprint kjørte opprinnelig på 9 raseguider; Sondre forlenget den i åtte runder (SBT/Bichon/Engelsk Setter 11–12, så DSG/Pomeranian/Mops/Finsk Lapphund 13–16 som fullførte topp 10-dekningen, så Jack Russell Terrier/Berner Sennenhund 17–18 som supplerende populære raser, så Fransk Bulldog/Engelsk Bulldog/Shetland Sheepdog 19–21 som BOAS-trioen-fullføring + gjeterhund-utvidelse, så Norsk Elghund Sort 22 og Norsk Buhund 23 som norsk nasjonalrase-trio-fullføring, så Beagle 24, så Boxer 25, så Rottweiler 26, så Dachshund 27 som småhund-jakthund-cluster-utvidelse). 9 nye guider levert 2026-05-16 — 3 sprinter på sen kveld alene. 2026-05-17 leverte 6 guider på én dag (sprint #22+#23 formiddag, sprint #24+#25+#26 ettermiddag, sprint #27 kveld). **Sprint #23+24+25+26+27 anvender nytt back-link audit-regelverk** (CLAUDE.md effective sprint #23+) — sprint #23 ga NEG+NES back-link til Buhund; sprint #24 ga Cocker Spaniel + Engelsk Setter back-link til Beagle; sprint #25 ga Berner Sennen + Stafford back-link til Boxer; sprint #26 ga 4 back-links (rekord); sprint #27 ga Beagle (body + les-også) + JRT (les-også) — kvalitets-fokus over rekord (Cocker REJECT for cluster-koherens).

**Etablerte mønstre på tvers av alle 21:**
- Canonical raseguide-mønster: 12 H2 + FAQ, **kun bunn-recap-grid** (inline callouts fjernet 2026-05-14, se BESLUTNINGER), Tips fra King-seksjon, FAQPage JSON-LD 1:1 match. Sidebar er TOC + King-quip. Full spec i `docs/page-patterns.md` "Raseguide Canonical Pattern".
- **Default word-count: 2800–3200 ord** (oppdatert 2026-05-16, se BESLUTNINGER) — med moat-override på §2 (rasens unike vinkel), §8 og §9 (helse-fagseksjoner).
- **FAQ canonical: 40–60 ord per svar** (oppdatert 2026-05-16) — featured-snippet sweet spot per Backlinko/SEMrush.
- **Vinkel A locked for sensitive helse-tunge raseguider** (Berner Sennen kreft/levealder, Mops BOAS, Cavalier MMVD): ærlig faktabasert tone, kildebare statistikker, eksisterende eiere respekteres, ingen moraliserende språk.
- **Editorial rule (ny 2026-05-16):** Ingen spesifikke års-tall uten kildebelegg (E-E-A-T-prinsipp, analog til pris-tall-regelen). Lærdom fra Finsk Lapphund-sprint.
- **In-prose crossover-lenker** mellom raseguider treffer "[rase] vs [rase]"-spørringer (eksempler: Labrador↔Golden, Cocker→Labrador, Bichon↔Chihuahua/Pomeranian via NBHK-patella, Engelsk Setter↔Norsk Elghund Grå+Schäferhund via HD-indeksavl, JRT↔DSG visuell forveksling, Finsk Lapphund↔Schäfer+Norsk Elghund Grå nordisk dobbeltpels-trio, Berner↔Mops+Cavalier ærlig-helsedebatt).
- **GA4 product_callout_click tracking** instrumented på recap-CTAs og **forwarding LIVE fra 2026-05-17** — events fire via `Shopify.analytics.publish` + `dataLayer.push`, og Shopify Custom Pixel forwarder dem til GA4 (`G-TR8MTY1BSE`) via Measurement Protocol med per-posisjon/per-produkt/per-breed-parametere. Verifisert i DebugView 01:11:51 på `/pages/border-collie`. Se BESLUTNINGER 2026-05-17.
- llms.txt-kategori: `Raseguide`. Hub-card-mal: badge `Rase`, kategori `Raseguide`. Hub-card støtter `description`-felt fra 2026-05-15.
- llms-data alfabetisk plassering bekreftet som strikt regel etter Berner-sprint (skulle ligge før bichon-havanais, ikke etter — brief-feil korrigert).

**Åpne valg etter sprint:**
- Cadence-pause anbefalt for å samle GSC-data (~4–8 uker fram til Q3 2026) på de 21 publiserte guidene før eventuell videre raseguide-produksjon. Topp 10 + BOAS-trioen-milestoner gir naturlig pausepunkt.
- Eventuelle nye raseguider bør baseres på faktisk søketrafikk/keyword-research, ikke gjetninger.
- XL-seng-blokker fortsatt aktiv for de tre storrasene (Schäferhund, Finsk Lapphund, Berner Sennen) — seng-CTA droppet på alle tre, recap-grid bruker pelsfjerner/aktivisering/vannskål i stedet.

### Åpne tråder (ikke besluttet ennå)
- **REN AVLESING ~2026-08-14 → v2-korpus GO/NO-GO** — 28d-vindu **17.07–14.08 = 100 % post-retrofit** (isolerer v2-effekt fra baseline-dager). **Sammenlign mot DAGENS 28d-tall (avlesing 20.07), IKKE 90d-baselinen** — apples-to-apples 28d-vindu. **Beslutningskriterium for GO:** median-CTR-løft på tvers av pilotene med **maks 1–2 sider som faller**, ELLER **konsistent posisjonsløft utover organisk modning**. Hold ellers. **Bakgrunn:** første avlesing 20.07 ga **NO-GO** (se BESLUTNINGER 2026-07-20) — for tidlig + konfundert av bred impresjons-surge (1,5–5,7× på ALLE sider, inkl. ulikt-behandlet hund-i-bil = ikke v2-signal) + 28d-vindu var ~40 % pre-retrofit. August-vinduet har **9 piloter** å dømme på (6 batch #1 + 3 batch #2). Mega-sidene (`hund-kaster-opp`, `hvor-mye-mat`) + 60 raseguider forblir gated til GO.
- **⏳ Checkout-locale default-flip (Admin UI, manuelt)** — nb er enabled+published via API (2026-07-21 kveld), men **en er fortsatt primær** → checkout rendrer engelsk til Sondre flipper default til Norsk (Bokmål) i Admin → Settings → Languages og deretter fjerner English. Rekkefølge kritisk (aldri disable en mens primær). Se BESLUTNINGER 2026-07-21 (kveld). API-gap: primær-flip går IKKE via Admin API.
- **Meta titles** — **KORRIGERT 2026-08-10: det er IKKE kjørt noe korpusbredt CTR-sveip.** Formuleringen «ingen sweep gjort» sto uendret her mens 13 målrettede Admin-endringer var utført, og ble derfor lest som at ingenting var gjort. Faktisk utført: **4 raseguide-meta-rewrites** (Batch A, 22.07 — `australian-shepherd`, `newfoundland`, `italiensk-mynde`, `weimaraner`) + **9 v2-pilot title+meta** (02.–19.07 — `hva-kan-hund-spise`, `giftig-mat`, `hund-oeyne`, `hvor-mye-vann-hund`, `hund-spiser-gress`, `hund-sover-mye`, `valp-biter-pa-alt`, `bandtvang-norge`, `hund-slikker-ansikt`). **Avlesing 90d (12.05–09.08, 121 sider fra `article_map`): 11 av de 13 ligger fortsatt under korpussnitt-CTR (1,11 %).** Kun `hund-oeyne` (1,36 %) og `valp-biter-pa-alt` (1,34 %) er over. **Forbehold: 90d-vinduet er ikke rent post-sveip** (starter 12.05, blander inn pre-sveip-dager for alle 13) → **28d-vinduet ~12.08 er fortsatt hovedmålet**, jf. GSC page-2 round 2-tråden under. De 82 sidene under snittet (62 % av korpusets visninger, 52 av dem raseguider) er kandidatlisten for et reelt sveip. Se BESLUTNINGER 2026-08-10.
- **⏳ Hundeseng-tilbudet: HARD FRIST 09.09.2026** — 639/799 med overstreket 799/999 ble satt 10.08.2026. Prisopplysningsforskriften § 9-10: overstreket førpris må være laveste faktisk brukte pris siste 30 dager. Når 639/799 har vært prisen i 30 dager, er 799/999 ikke lenger gyldig førpris → både strikethrough og «(–20 %)» i meta-beskrivelsen blir falsk tilbudspåstand. **Handling: enten en reell prisøkning tilbake til 799/999 før fristen, eller fjern `compare_at_price` på begge varianter (Medium 43401578446926, Large 43401578479694) og strip «Nå» + «(–20 %)» fra meta.** Sky-påminnelse satt: routine `trig_016qx7e1tqtgBaDCsxT8jNB7`, fyrer 05.09.2026 kl. 09:00 Oslo, se https://claude.ai/code/routines/trig_016qx7e1tqtgBaDCsxT8jNB7 — den har hverken repo- eller Admin-tilgang, så den rapporterer status og hva som må gjøres; selve endringen er manuell.
- **⏳ Avpubliser `frontpage`-kolleksjonen (Admin UI, manuelt)** — «Home page»-kolleksjonen er tom (0 produkter), ikke referert av temaet, og noindex er bekreftet tilsiktet. Den ligger likevel i den auto-genererte sitemap.xml fordi den er publisert til Online Store. **Handling: Admin → Produkter → Samlinger → Home page → Salgskanaler → fjern Online Store.** Krever `write_publications`, som ikke er i `shopauth` — kan alternativt gis ved å utvide scope-settet og kjøre `shopauth` på nytt. Lav prioritet: noindex vinner uansett, oppføringen gir bare en «Ekskludert av noindex»-rad i dekningsrapporten. Se BESLUTNINGER 2026-08-11 kveld + gotcha #30.
- **AggregateRating schema** — vurderes på produkt-PDPs, men avhenger av at vi har reelle reviews.
- **Reviews-strategi** — hvordan vi samler inn ekte produktanmeldelser (Shopify Reviews app? E-post-flow post-purchase? Manuell innsamling?). Ingen valgt vei.
- **Sourcing: XL donut-seng (≥40 kg)** — Beroligende hundeseng maxer på 25 kg (Large). Forhindret seng-CTA på Schäfer (publisert uten), og blokkerer fremtidige large-breed-guider (Berner Sennen, Vorsteh, Setter, etc.) hvis sprint forlenges. Sondre må source XL-størrelse før disse rasene får seng-CTA.
- **GSC page-2 round 2 (~64 gjenstående opps) — GATED på avlesing ~2026-08-12** — top-15-effekten fra page-2-sprinten (Batch A/D/C/B, live 2026-07-22) måles i GSC rundt 12.08 (samordnet med v2-avlesingen 14.08). Virker CTR/posisjon-mønsteret → round 2 (dypere mining under top-15) godkjennes da. Hold til da.
- **King→griffon sitewide link-equity (deferred)** — «Tips fra King» er hardkodet i **118 filer** (ikke shared snippet); 15 lenker allerede til griffon-guiden. Sitewide King→`/pages/griffon-petit-brabancon` krever FØRST refactor av «Tips fra King» til delt snippet, deretter mass-link. Egen scoped sprint. (Batch C fylte companion-cluster-gapene i stedet.)
- **2 weak-fit Batch-D-links holdt (Sondre-beslutning utestående)** — `aktivisere-hund-pa-tur`→potevasker (ingen pote/gjørme-kontekst) + `hundehar-bilen`→«fjerne hundehår fra sofa»-anchor (bil-artikkel, off-topic). Ikke shippet; force-add hvis ønsket.
- ~~**llms.txt H2-drift på hund-kaster-opp (månedlig audit)**~~ — **LUKKET 05.08.2026** som del av H2-liste-driften (19 oppføringer, commit `ad28542` + `pointer`-tillegg). «Oppkast vs. rygning» → «oppgulping» rettet. **Korreksjon til den opprinnelige noten: «Bilsyke»-halvdelen var aldri reell** — «Bilsyke — når hunden kaster opp i bil» matchet seksjonsfila eksakt hele tiden. Bare rygning/oppgulping var drift.

---

## BESLUTNINGER — append-only, nyeste først

### 2026-08-12 — Vann-pilar: utvidet eksisterende side i stedet for ny artikkel; to stille defekter rettet (`671fd87`)

**Bestillingen var en ny pilar-artikkel «Hundens vann». Den ble ikke skrevet.** GSC 90d viste at `/pages/hvor-mye-vann-hund` allerede ER vann-pilaren: 5 169 visninger, posisjon 6,9, og rangering på nøyaktig måltermene («hvor mye vann skal en hund drikke» 158 visn./pos. 7,1 · «hund drikker mye vann» 114 · «valp drikker mye vann» 99 · «hund drikker lite vann» 45 · «hunden vil ikke drikke vann» 35). Åtte av ni foreslåtte H2-er var allerede dekket. En ny side ville kannibalisert en side som alt rangerer på side 1.

**Reell flaskehals er CTR, ikke dekning:** 0,95 % på posisjon 6,9 mot forventet 2,5–3 %. Det er ~90–110 tapte klikk per kvartal, og det er et snippet-problem — samme diagnose som raseguide-segmentet fikk 2026-08-11.

**Levert i stedet:** siden utvidet 1 750 → ~2 720 ord med tre nye H2-er (valp/voksen/senior · blågrønnalger · kran- vs flaskevann), TurPakken 3-i-1 som `--featured` produktkort inline (Batch 6/7), nytt hero-bilde, FAQ 7 → 9 med verifisert 1:1 mot JSON-LD. Kilder: Veterinærkatalogen + Veterinærinstituttet (alger), drikkevannsforskriften + Mattilsynet (kranvann). Se `docs/health-claims-register.md`.

**To defekter som lå live og som ingen sjekk fanget:**

1. **Kalkulatoren motsa både prosaen og tabellen i samme fil.** `basePerKg` var 80/65/55/50; en hund på 3 kg fikk 240 ml mot tabellens 150–180. Batch 4 (2026-07-29) registrerte dette som lukket etter å ha justert prosaens *ordlyd* mot kalkulatoren — uten å regne på hva kalkulatoren faktisk returnerte, og uten å se på tabellen. Rettet til 60/58/55/52, verifisert innenfor tabellen i alle ni vektklasser.
2. **TOC-ankrene var indeksbaserte og forskjøvet.** Kalkulator-H2-en ligger utenfor `.mh-article__body`, så hver lenke fra og med nr. 2 pekte på feil seksjon — inkludert `#faktorer`, `#dehydrering` og `#paa-tur`, som Google har indeksert med visninger. Erstattet med eksplisitte `id`-er.

**Tre nye gotchas dokumentert:** #34 `theme pull --only` krever repeterte flagg (mellomromsform henter stille null filer og gir falsk PASS) · #35 `sha256 live == HEAD` holder aldri for `templates/*.json` fordi Shopify injiserer en kommentar-header · #36 indeksbaserte TOC-ankere.

**Verifisert live:** sha256 live == HEAD for begge `.liquid`-filene; normalisert JSON-sammenligning for hub-templaten. Alle tre llms-URL-er bærer ny tittel og de nye H2-ene. Reindeksering sendt (men jf. gotcha #31 — `✅` er ikke bevis).

**Åpent Admin-steg:** SEO-tittel og meta-description er ikke oppdatert; det er nettopp det steget som skal lukke CTR-gapet. Forslag levert til Sondre.

**Pre-eksisterende funn, ikke rørt:** to ekte hub ↔ `article_map` tittel-drift (`hund-lukter-vondt`, `aktivisere-hund-pa-tur`).

### 2026-08-11 kveld — SEO-sveip: 32 lekkasjesider + to strukturelle GSC-bugs (`ff94037` → `a9ddbae`)

**Utløser:** full GSC-avlesing 90d (13.05–10.08). **Korpus: 4 480 klikk / 393 972 visninger / CTR 1,14 % / snittposisjon 8,7.** 12-månederstallet er 4 793 / 406 678 — **96,9 % av alle visninger siste år falt i dette kvartalet**, så per-URL-sammenligning mot 12 mnd er meningsløs; det finnes ingen historikk å måle mot.

**Metodefunn som endret hele avlesingen: anker-URL-er må filtreres bort.** Google indekserer innholdsfortegnelsenes jump-lenker som egne URL-er. En rå `page`-spørring ga 499 rader hvorav **353 var ankre** — `/pages/bandtvang-norge` alene hadde 7 stk à ~1 250 visninger. Ankrene spiste opp 500-radstaket, så alt under ~490 visninger falt ut av datasettet. Med `excludingRegex: "#"` ble det 157 rader = komplett. Se gotcha #28.

**Segmentbildet:** hundetips 65 sider / 3 324 klikk / 1,23 % CTR · raseguider 60 sider / 1 040 klikk / **0,85 %** · produkt+kolleksjon 21 sider / 76 klikk / 1,50 % på snittposisjon 12,4. Raseguidene tar 31 % av visningene og gir 23 % av klikkene, på praktisk talt samme posisjon som hundetips (8,5 vs 8,0). **Forskjellen er snippet, ikke rangering.** Produktsidene er nesten usynlige organisk: 1,3 % av all eksponering, hvorav `/products/pelsfjerner` er en firedel.

**Indeksering er i praksis komplett:** 148 av 150 sitemap-URL-er har eksponering. De to unntakene er `puslespill-hund` (indeksert og frisk, bare ny) og `collections/frontpage` (noindex, se bug 2). Merk at Sider-rapporten **ikke** finnes i GSC-API-et — full ekskluderingsliste med årsak kan bare eksporteres fra UI-et; per-URL-status hentes med URL-inspeksjon.

**Sveipen: 32 sider med posisjon ≤10, CTR <1 % og ≥1 000 visninger fikk ny title + meta** (64 metafelt, `metafieldsSet` i tre kall, ingen `userErrors`). Mønsteret ble utledet ved å analysere de tre høy-CTR-sidene på samme posisjonsnivå — `hund-vil-ikke-ga-tur` (4,97 %), `vaske-hundeseng` (5,30 %), `hundehar-i-bilen` (3,14 %):

1. **Metaen skal svare, ikke beskrive.** «Komplett guide til X» er en innholdsfortegnelse; vinnerne oppgir svaret («skyldes oftest smerte … ikke vrangvilje»).
2. **Motsi antakelsen søkeren kom med.** Debunk-vinkelen er den sterkeste enkeltmekanismen — `malteser` fikk «Er malteser hypoallergen? Nei — her er hvorfor» i title, hentet opp fra metaen.
3. **Tall slår adjektiver:** «hver 4.–8. uke», «40–60 ml per kg», «55–80 kg og 9,3 års levetid».
4. **Ingen akronymer i meta.** `SAS/HD` → «hjerte- og hofteproblemer», `IVDD` → «skiveprolaps», `emaljehypoplasi` → «svak tannemalje».
5. **«komplett raseguide» sto i 14 av de 32 titlene** — droppet i alle. Samme med «Alt du trenger å vite om».

**Funn som burde vært fanget tidligere: intern prosjektsjargong lå live i meta.** `samojedhund` hadde «TRIPPEL helsemoat» og `kortharet-vorstehhund`/`cane-corso` hadde «storrase-helse-trilogi» ute på Google. Det er ord fra vår egen raseguide-protokoll, ikke fra hundeverdenen. Fjernet.

**Faktakontroll før publisering — én reell feil fanget.** Alle nye påstander ble verifisert mot seksjonsfilene. Utkastet for `vizsla` sa «kan ikke være mye alene»; kilden sier eksplisitt at rasen **kan** være alene i perioder, men trives ikke med det. Rettet til «trives dårlig alene» i både title og meta. Tre andre metaer (`beagle`, `norsk-elghund-gra`, `bade-hund`) ble skrevet om til å bruke kildens egne formuleringer; `bade-hund` fikk inn det verifiserte intervallet «hver 4.–8. uke» som ikke var med i utkastet. De øvrige 28 gikk uendret fra forslag til publisering.

**Verifisert i to trinn:** 64/64 metafelt lest tilbake via Admin API uten avvik, deretter 32/32 sider mot live-HTML på `<title>`, `description`, `og:description` **og** `twitter:description` (port 8 i pre-publiseringsporten). `docs/ROLLBACK-seo-2026-08-11.json` holder alle 64 gamle verdier med metafelt-type.

**Bug 1 — canonical-lekkasje under alle 129 sider (FIKSET).** Shopify svarer HTTP 200 på ett ekstra path-segment etter en side-handle, og `canonical_url` returnerer da søppelstien. `/pages/hundetips/hva-som-helst` selv-kanonikaliserte, altså et uendelig URL-rom under hver eneste side. GSC hadde indeksert tre: `hund-stresset` (47 visninger), `tannhelse-hund` (8), `eldre-hund` (3), alle på posisjon 42–52, alle meldt som «Duplicate, Google chose different canonical than user». Kun `page_type == 'page'` er rammet — produkter kanonikaliserer riktig selv, kolleksjoner 301-redirecter, blogger 404-er. `snippets/meta-tags.liquid` beregner nå `mh_canonical` fra `page.handle` og mater både `<link rel="canonical">` og `og:url` (sistnevnte leste `canonical_url` separat og hadde samme feil). **301-redirect var ikke et alternativ — Shopifys URL-redirects støtter ikke wildcards.** Live-verifisert: 14 URL-er, 0 feil, inkl. 9 regresjonssjekker. Gotcha #29.

**Bug 2 — `/collections/frontpage` noindex vs. sitemap (DELVIS: noindex bekreftet riktig, sitemap-oppføring gjenstår).** Undersøkelsen viser at noindex er **tilsiktet og skal stå**: kolleksjonen er Shopifys auto-opprettede «Home page», har **0 produkter**, er sist endret 21.01.2026 og refereres ikke av temaet i det hele tatt — eneste treff på «frontpage» i hele temaet var noindex-regelen selv. `layout/theme.liquid` er byttet fra streng-match på `canonical_url` til resurs-basert sjekk, som ikke lenger treffer handles som bare *begynner* med «frontpage» (effektnøytralt i dag: butikken har 6 kolleksjoner og bare én slik handle). **Sitemap-oppføringen kan ikke fjernes fra repoet** — Shopifys sitemap er auto-generert og tar med alle kolleksjoner publisert til Online Store. Eneste vei er å avpublisere kolleksjonen fra salgskanalen, som krever `write_publications` — ikke i `shopauth`-scopene, `publications`-spørringer feiler med `ACCESS_DENIED`. **Manuelt Admin-steg, se Åpne tråder.** `Disallow` i robots.txt er bevisst valgt bort: det hindrer Google i å se noindex-taggen. Gotcha #30.

**Forbehold om gevinsten.** Det opprinnelige anslaget på ~1 900 gjenvinnbare klikk er **for høyt og ble nedjustert**. `hva-kan-hund-spise` har 490 ulike søkeord dominert av «kan hunder spise \<ingrediens\>»; toppsøket ga 300 visninger på posisjon 9,2 med **null klikk**, og tittelen speilet allerede søket ordrett. Det er enkeltfakta-spørsmål som besvares i AI Overview — der er søketypen problemet, ikke teksten. Realistisk: **400–700 klikk per kvartal**, konsentrert om raseguidene der intensjonen er vurderende. Ingredienssidene trenger egne sider per høyvolum-ingrediens, ikke bedre meta.

**Ikke rørt:** ingen seksjonsfil, ingen H1, ingen brødtekst. llms.txt trengte ingen synk — `article_map` speiler hub-korttitler og H2-er, ikke SEO-title-tags, og ingen H2, produktreferanse eller tall er endret.

### 2026-08-11 — Nyhetsbrev-popup: fire strukturfikser LIVE etter 96 % frafall før steg 1 (`7c6c439`)

**Utløser:** første frysperiode (28.07–11.08) er over. Avlesningen viste **620 av 646 visninger lukket før steg 1 — 96,0 % frafall**. Kun 26 brukere nådde det første valget. Hypotesen «tekst/rabatt er feil» ble forkastet tidlig: dette var strukturelt.

**Først utelukket — det var ikke en målefeil.** `mh_popup_step1` går gjennom nøyaktig samme `#fire()`-funksjon og samme kanaler som `mh_popup_view`. Verifisert ved å hooke `dataLayer`, åpne popupen og klikke et valg: begge eventene fyrer, med korrekt `step1_choice`, og steg 2 vises. Det finnes ingen asymmetri som kunne blåst opp view-tallet. Tallene er direkte sammenlignbare.

**Fire strukturårsaker, alle rettet:**

**1. Timer vs scroll-race — `delay_seconds` var død kode.** Scroll-lytteren ble armet uten forsinkelse, så den vant alltid over 12-sekunderstimeren. Målt fyring: **1 532–5 286 ms** etter landing på alle fem sidetyper. Popupen avbrøt folk før de rakk å lese noe, og `scroll-lock` frøs siden midt i en tommelflikk. Ny `data-scroll-arm-ms` (default 8 s) + hardt gulv i `#open()`. Terskel hevet 40 → 50 %. **Etter: 8 495–12 931 ms på live**, timeren vinner nå på 4 av 5 sidetyper. Egen gotcha #26.

**2. Mobilarket klippet innhold.** `max-height: 55dvh` skjulte valg #3 og **begge** nødutgangene på iPhone SE (139 px skjult, 2/3 valg), vanlig Android 360 (99 px, 2/3) og liggende mobil (381 px, **0/3**). «Bare send meg alt» — utgangen for alle som ikke vil velge tema — var skjult på **samtlige** målte skjermer, inkludert laptop 1280×720 og iPhone 14. Tak hevet til 92dvh, bildet gradert ned (2/1 under 820 px høyde, skjult under 620 px), egen to-kolonners layout for liggende mobil, scroll-gradient som sikkerhetsnett.

**3. Steg 1 hadde ingen klikk-affordanse.** Valgkanten var `rgba(45,106,53,0.14)` = **1,23:1** mot hvit — WCAG-kravet for en UI-kant er 3:1 — mens lukk-X-en lå på **17,43:1**. Det eneste elementet som skulle konvertere var det svakeste på skjermen. Nå 2 px `#4b8353` = **4,50:1**, pil i fylt grønn disk 6,51:1, høyde 56 px, vekt 600, hover fyller knappen grønn. Bevisst **ikke** `.mh-nl__cta` på alle tre: tre identiske primærknapper fjerner lesbarheten av at det er et valg, og gjør «Nei takk» til den eneste visuelt distinkte utveien.

**4. Bakteppe-klikk dominerte.** Bakteppet var **17,3× større** enn alle tre valgene til sammen på desktop og **2,8×** på mobil — den enkleste handlingen på skjermen, og på mobil nøyaktig der tommelen står midt i en scroll. Klikk-utenfor-for-å-lukke fjernet. `assets/dialog.js` er **urørt** (deles av 12 andre flater — søk, filtre, buy-buttons, password); bakteppe-klikk fanges i stedet i capture-fasen på `<dialog-component>` før stock-handleren ser dem, med presis treff-test så klikk inni boksen slipper uendret gjennom. `.mh-nl__grabber` slettet — det lovet en sveipegest som aldri var implementert.

**Verifisert på live etter push:** 12 skjerm/variant-kombinasjoner, alle med 3/3 valg synlige **og** klikkbare (`elementFromPoint`, ikke bare geometri), begge nødutganger synlige, 0 px skjult, null overlapp mot lukk-X. Akkumulerende cache-buster-sjekk: **30 hentinger (6 runder × 5 URL-er), 30 ny / 0 gammel**. sha256 pull-back fra live matcher lokal fil bit for bit på begge filer. Regresjon: Esc, lukk-X, «Nei takk», tilbake-knapp, steg 2 (488 px) og steg 3 (684 px) uten overflyt, e-postfokus intakt.

**Bug fanget underveis:** to-kolonners layouten lot lukk-X-en ligge oppå første valgknapp. Fanget av `elementFromPoint`-sjekken, ikke av synlighetsmåling — ren geometri hadde godkjent den.

**Merk om CDN vs temafil:** den minifiserte JS-en på CDN har ikke samme hash som temafilen (10 009 vs 17 454 bytes). Det er Shopifys minifiser (`'`→`"`, samlede `const`-kjeder, `8_000`→`8e3`, `0.5`→`.5`), ikke et avvik. Temafilen er autoritativ. Samme gjelder CSS: `[data-overflow='true']` serveres som `[data-overflow=true]`.

---

### 2026-08-11 — MÅLEKONTRAKT #2: nyhetsbrev-popup etter strukturfiksene (satt FØR data)

Samme mal som 28.07 — satt før første datapunkt for å hindre etterrasjonalisering.

**Ny baseline fra 11. august 2026.** Tallene fra frys #1 (28.07–11.08) er **ikke sammenlignbare** med frys #2: popupen fyrte etter 1,5–5,3 s, og halve steg 1 var utenfor skjermen på de fleste enheter. Frys #1 målte i praksis en annen popup.

**Avlesning: ~5.–8. september 2026** (3–4 uker). Periode `2026-08-12` → avlesningsdato. **12.08 som startdato, ikke 11.08** — da faller dagens egne verifiseringsevents (force-modus, ~30+ view/step1 fra Playwright) utenfor perioden av seg selv, og skal ikke trekkes fra i tillegg. Samme fallgruve som DebugView-eventene 28.07; se gotcha #25.

**Hovedtall 1 — steg 1-passering: `mh_popup_step1` / `mh_popup_view`**

| Rate | Dom |
|---|---|
| **< 15 %** | Fiksene traff ikke — årsaken er noe annet enn struktur, grav på nytt |
| **15–30 %** | Reell forbedring, men fortsatt et strukturproblem igjen |
| **> 30 %** | Godkjent — steg 1 fungerer som et valg |
| **> 45 %** | Mikro-ja-premisset er bekreftet |

Forrige måling: **4,0 %** (26/646). Alt under 15 % betyr at de fire fiksene ikke var hovedårsaken.

**Hovedtall 2 — påmelding: `mh_popup_submit` / `mh_popup_view`** — samme terskler som 28.07 så tallene er sammenlignbare på tvers av begge frysene:

| Rate | Dom |
|---|---|
| **< 2 %** | Noe er fortsatt strukturelt galt |
| **2–4 %** | Virker, men under det redesignet skulle levere |
| **> 4 %** | Godkjent |
| **> 6 %** | Over e-handelssnittet |

**Sekundært — diagnostikk, ikke mål:**
- **Andel `step1_choice = alle`.** Over 40 % ⇒ mikro-ja-premisset er feil, vurder ettstegs. Merk: «Bare send meg alt» var *skjult på alle skjermer* i frys #1, så dette tallet er reelt sett umålt før nå.
- **`dismiss_method`-fordeling.** Mye `close` mot lite `decline` ⇒ refleksiv lukking. Bakteppe-klikk finnes ikke lenger som avvisningsvei, så fordelingen er ikke sammenlignbar med frys #1.
- **Variant A vs B.** Ingen vinner kåres på 3–4 uker; vi ser kun etter om den ene er dramatisk dårligere.
- **`trigger_type`-fordeling (ny).** Andelen `scroll` vs `timer` viser om 8-sekunderssperren treffer i ekte trafikk slik den gjør i test.

**FRYS: ingen endringer på popupen før avlesningen**, uansett hva tallene viser underveis.

**🔴 Blokker som må ryddes FØR avlesningen kan kjøres:** GA4 Data API + Admin API er deaktivert i GCP-prosjekt `744067514649`, service-kontoen er GSC-scopet og ikke lagt til på GA4-propertyen, og den numeriske property-ID-en er ikke kjent (`G-TR8MTY1BSE` er en measurement ID og godtas ikke). Full beskrivelse i gotcha #25. Avlesningsskriptet finnes: `~/google-ads-script/ga4_popup_report.py`. **Ryddes dette ikke innen begynnelsen av september, må tallene hentes manuelt fra GA4 Utforsk** — en avlesning uten faktisk API-svar er ikke en avlesning.

---

### 2026-08-10 kveld — Beroligende hundeseng −20 % + Bestselger-badge fjernet (`4e3cb44` + `e9c95ae`)

**Utløser:** Sondre: sengen selger 0. Beslutning: permanent prisnedsettelse med synlig førpris — ikke rabattkode.

**Prisendring (Shopify Admin API, `productVariantsBulkUpdate` via MCP):**
- Medium `MH-HS-M`: 799 → **639 kr**, compare-at **799**
- Large `MH-HS-L`: 999 → **799 kr**, compare-at **999**
- Begge rundet ned til hel krone → 20,0 % avslag. Ingen compare-at var satt fra før, så førprisene er de faktisk brukte prisene (prisopplysningsforskriften § 9-10 oppfylt på endringstidspunktet).
- Verifisert live i sidens HTML: `"price":63900` / `"price":79900`.
- `snippets/llms-products-data.liquid`: «Fra 799 kr» → «Fra 639 kr» (llms.txt Trigger C). Eneste hardkodede sengpris i korpuset — grep på `799 kr`/`999 kr` ga 1 treff totalt.

**Badge-opprydning:** `<span class="hs-bestseller-badge">Bestselger</span>` fjernet fra `sections/product-hundeseng.liquid`. Full live-sveip av alle 15 produktsider + `/collections/all` viste at kun **to** flater hadde ordet: hundesengen (usann påstand — 0 solgt) og pelsfjerner (reell bestselger, beholdt). Forsidens hero-badge «BESTSELGER · TESTET AV KING» er bundet til `mh_bestseller_handle = 'pelsfjerner'` og er urørt. CSS-regelen `.hs-bestseller-badge` beholdt for gjenbruk (f.eks. SALG-merke).

**Funn:** de øvrige `*-bestseller-badge`-klassene (calmball, valpepakken, slikkematte, vannflaske, aktiviseringsleke) er samme badge-slot med *beskrivende* tekst («Mental aktivisering», «6-i-1 multifunksjonell», «Sett på TikTok») — ingen salgspåstand, ingen endring nødvendig.

**Cache:** page-cache serverte den gamle badgen i minst 2 min etter push selv om live-temafila var verifisert ren (`shopify theme pull --live` → 0 treff). Kjent mønster, ikke ny gotcha.

### 2026-08-10 — CTR-avlesing 90d + første ekte title/meta-sveip: 15 sider endret via Admin API

**Utløser:** GSC-avlesing (service-account, 90d 12.05–09.08, dimensjon `page`) av alle 121 handles i `article_map`. **Korpus: 4 283 klikk / 384 744 visninger / snitt-CTR 1,11 %.** Alle 121 fikk treff; ingen falt under 50-visningsterskelen, så «under snittet» = 82 sider = **62 % av korpusets visninger**. Raseguidene underpresterer som segment: **0,86 % mot hundetips' 1,23 %**, og ingen raseguide er inne på topp 15 målt i klikk.

**Avlesing av juli-endringene: 11 av 13 ligger fortsatt under snittet.** Kun `hund-oeyne` (1,36 %) og `valp-biter-pa-alt` (1,34 %) er over. Se korrigert Åpne tråder-punkt «Meta titles» — formuleringen «ingen sweep gjort» hadde stått uendret mens 13 målrettede endringer var utført, og ble derfor lest som at ingenting var gjort.

**Ny kanal bekreftet: page-SEO kan skrives via Admin API.** Tidligere antakelse i prosjektet var at title/meta for pages måtte settes manuelt i Admin. Det er feil. `Page`-typen har ikke noe `seo`-felt (`Field 'seo' doesn't exist on type 'Page'`), men «Search engine listing»-feltene ligger som metafelt `global.title_tag` / `global.description_tag` og skrives med `metafieldsSet` + `--allow-mutations` på det eksisterende `write_content`-scopet. Alle 15 sider ble satt i tre kall uten `userErrors`. **Dette fjerner Friday/manuelt-Admin-steget for all framtidig meta-arbeid.** Merk at `type` går fra legacy `string` til `single_line_text_field` ved skriving — uten synlig effekt på rendering.

**Steg 1 — formatfeil rettet (7 felt / 6 sider):**

| Side | Felt | Før | Etter |
|---|---|---|---|
| `hvor-mye-vann-hund` | title | Hvor mye vann skal hunden drikke? Kalkulator + guide (52) | Hvor mye vann skal hunden drikke? Kalkulator \| Min Hund (55) |
| `hund-spiser-gress` | title | Hund spiser gress — hvorfor, og når du bør reagere (50) | Hund spiser gress — hvorfor, og er det farlig? \| Min Hund (57) |
| `giftig-mat` | title | Giftig mat for hund — komplett liste + hva du gjør \| Min Hund (61) | Giftig mat for hund — sjokolade, druer, xylitol \| Min Hund (58) |
| `giftig-mat` | meta | 162 tegn | 127 tegn |
| `labrador-retriever` | meta | 171 tegn | 137 tegn |
| `engelsk-bulldog` | meta | 169 tegn | 138 tegn |
| `pointer` | meta | 166 tegn | 132 tegn |

**Gotcha #23 oppdaget her:** `hvor-mye-vann-hund` og `hund-spiser-gress` hadde Admin-titler på 50–52 tegn — godt innenfor 60 — men live-`<title>` var 61–63 tegn med en-dash-suffiks. `snippets/meta-tags.liquid:132` legger på ` – Min Hund` (`&ndash;`) **når Admin-titelen ikke selv inneholder «Min Hund»**. Diagnosen «en-dash i Admin-feltet» fra rapporten var altså feil: feltet var rent, temaet la på suffikset. **Konsekvens: 60-tegnsgrensen må måles på live-HTML, aldri på Admin-feltet.** `hund-sover-mye` har samme mekanisme men landet på 59 tegn og passerte stille — ikke rørt.

**Steg 2 — raseguide-titler, «komplett raseguide»-formelen droppet (9 sider):** formelen `[Rase] — komplett raseguide | Min Hund` sier ingenting en søker ikke visste, og alle 9 lå på 0,37–1,04 % CTR. Erstattet med konkret krok verifisert ordrett mot brødteksten i hver seksjonsfil:

| Side | Ny title | Krok hentet fra |
|---|---|---|
| `whippet` | Whippet — 64 km/t ute, rolig sofahund inne \| Min Hund (53) | «toppfart anslått til rundt 64 km/t» + «typisk rolig sofahund inne og veddeløpshest ute» |
| `staffordshire-bull-terrier` | Staffordshire Bull Terrier forbudt i Norge? Nei \| Min Hund (58) | «Nei — Staffordshire Bull Terrier er ikke forbudt». Følger husets debunk-mønster (spørsmål + «Nei») fra hypoallergen-bolken, og **beholder head-termen først** i stedet for å lede med spørsmålet |
| `griffon-petit-brabancon` | Petit Brabançon — raseguide fra en eier \| Min Hund (50) | «King er en Petit Brabançon. Vi vet hva denne rasen krever» |
| `golden-retriever` | Golden Retriever — Norges mest registrerte rase \| Min Hund (58) | «Norges mest registrerte hunderase i NKKs statistikk for 2024» — **årstallet bevisst utelatt**, se forbehold |
| `flat-coated-retriever` | Flat Coated Retriever — «Peter Pan blant hundene» \| Min Hund (60) | «Peter Pan blant hundene». Kreftvinkelen (histiocytisk sarkom) **bevisst ikke brukt** i title |
| `cavalier-king-charles-spaniel` | Cavalier King Charles Spaniel etter avlsforbudet \| Min Hund (59) | «Høyesterettsdommen fra 2023» |
| `gordon-setter` | Gordon Setter — tyngste av de tre setterne \| Min Hund (53) | «den tyngste av de tre setterne» — **tre, ikke fire**; gammel meta sa «tyngste setter-rase» uten antall |
| `weimaraner` | Weimaraner — «sølvhunden» trenger 2 timer daglig \| Min Hund (59) | «kjent som sølvhunden» + «1,5–2 timer aktiv mosjon daglig» |
| `samojedhund` | Samojedhund — polarforskerens hvite hund \| Min Hund (51) | «polarforskerens hund» + «Den hvite spisshunden Fridtjof Nansen valgte». **Sykdomslista (TRIPPEL helsemoat) holdt ute av title** etter samme vurdering som flat-coated |

`gordon-setter` fikk title + meta i **samme** skriveoperasjon for å unngå å røre siden to ganger. `irsk-setter` **ikke rørt** — blokkert på NKKs 2024-registreringstall.

**Verifisering.** Admin API-relesning av alle 15: **15/15 korrekt, 0 avvik** (autoritativ kilde — metafeltene er ikke temafiler, så `sha256`-mot-HEAD gjelder ikke). Live-rendering henger etter per gotcha #19: `curl -I` viser `etag: W/"page_cache:70826557518:PageDetailsController:…"` og `theme;desc="148333264974"` på de forsinkede sidene, altså riktig tema + Shopifys fullside-cache, ikke feilet skriving. Cachen roterte per side og ujevnt — sider som verifiserte OK i én runde viste gammelt innhold i neste.

**⚠ FORBEHOLD 1 — steg 1 kontaminerer den gatede 28d v2-avlesingen.** `giftig-mat`, `hvor-mye-vann-hund` og `hund-spiser-gress` er **3 av de 9 v2-pilotene**, og fikk ny title/meta 10.08 — inne i 28d-vinduet 17.07–14.08 som Åpne tråder-punktet «REN AVLESING ~2026-08-14» skulle dømme v2-korpusutrullingen på. De siste ~4 av 28 dager er dermed ikke lenger ren v2-effekt for disse tre. **GO/NO-GO-kriteriet («median-CTR-løft med maks 1–2 sider som faller») bør derfor avgjøres på de 6 urørte pilotene**, med de 3 rapportert separat. Alternativt utsettes avlesingen til et vindu som er rent for begge endringene.

**⚠ FORBEHOLD 2 — `golden-retriever`-titelen hviler på samme datasett som blokkerer `irsk-setter`.** «Norges mest registrerte rase» er artikkelens egen påstand (intro + factstrip, «NKKs statistikk for 2024»). Årstallet er utelatt fra titelen nettopp fordi 2024-tallene er den uverifiserte flaten — påstanden holder over flere år og er ikke pinnet til den disputerte figuren. Verifiseres 2024-tallene og viser noe annet, må titelen byttes.

**Ikke utløst:** llms.txt Trigger B. `article_map`s Title-felt speiler **hub-kort-titelen**, ikke SEO-titelen, og verken H1, H2-struktur eller ordantall er endret. Ingen temafiler rørt i det hele tatt — endringene er rene Admin-metafelt.

**Måledato: endringene er live 2026-08-10 → CTR-sammenligning ~2026-09-07** (4 uker). Sammenlign 28d-vinduet 10.08–07.09 mot 28d før 10.08, ikke mot 90d-baselinen.

**Live-verifisering fullført: 15/15.** Akkumulerende sjekk over fire runder — hver side bekreftet med live-`<title>` + alle tre description-taggene i synk, sha256 loggført. Rundefordeling: 11 sider i runde 1–2, `hvor-mye-vann-hund` i runde 3, `labrador-retriever` i runde 4. Cachen roterte per side og per henting: en side kunne verifisere OK i én runde og servere gammelt innhold i neste. **Enkelthenting mot live er derfor ikke et gyldig porttrinn** — bruk akkumulerende sjekk over flere runder, eller Admin API som autoritativ kilde.

**Utvidet funn — gotcha #23 rammer ni sider, ikke to.** Sveip av alle 121 artikkelsiders `title_tag` via Admin API:

| Side | Tilstand | Visninger |
|---|---|---|
| `aktivisere-hund-pa-tur` | **dobbelt merkenavn** — Admin-title slutter på «Min hund» med liten h, `contains` er case-sensitiv, temaet legger på sitt eget suffiks → live-title = `… Min hund – Min Hund` (68 tegn) | 2 394 |
| `orebetennelse-hund` | mangler suffiks → 68 tegn live | 1 969 |
| `hund-kaster-opp` | mangler suffiks → 64 tegn live. **Korpusets #1-side** (282 klikk) | 16 757 |
| `hund-sover-mye` | mangler suffiks → 59 tegn (under grensen) | 9 647 |
| `tannhelse-hund` · `hund-graver-i-hagen` · `valpe-utstyr-sjekkliste` · `mellomschnauzer` · `strihaaret-vorstehhund` | **ingen `title_tag`** → Shopify faller tilbake til `page.title` (H1-tekst, ikke SEO-optimert) + en-dash-suffiks | 1 018–3 590 |

**To av dem rettet samme dag** (se under). De øvrige sju står — sveipkommandoen ligger i gotcha #23-tillegget.

**Oppfølging 2026-08-10 (kveld) — de to prioriterte gotcha #23-sidene rettet:**

| Side | Før (Admin → live) | Etter (Admin = live) |
|---|---|---|
| `hund-kaster-opp` | `Hund kaster opp gult skum? Slik vet du når det haster` (53) → **64 tegn** live med en-dash-suffiks | `Hund kaster opp gult skum? Når det haster \| Min Hund` (**52**) |
| `aktivisere-hund-pa-tur` | `Aktivisere hund på tur — slik gjør du det riktig Min hund` (57) → **68 tegn** live, `… Min hund – Min Hund` | `Aktivisere hund på tur — slik gjør du det riktig \| Min Hund` (**59**) |

`hund-kaster-opp` er korpusets største side (16 757 visn / 282 klikk / 1,68 % CTR) og hadde avkortet SERP-title. Nøkkelbudskapet er beholdt — symptomet «gult skum» og triage-vinkelen — men «Slik vet du» er trimmet bort for å komme under 60. **Meta description ikke endret** på noen av de to: 151 og 144 tegn, begge i bånd, og `hund-kaster-opp`-metaen bærer allerede «gult skum eller gult slim» + «når det er alvorlig», altså samme budskap som den nye titelen.

`aktivisere-hund-pa-tur` er bekreftet fri for dobbelt merkenavn i live-HTML: én forekomst av «Min Hund», ingen tema-appendet en-dash. Bare case-rettingen alene fjernet suffiks-bugen, akkurat som mekanismen forutsier.

**Verifisering:** Admin API 2/2, akkumulerende live-sjekk 2/2 (`hund-kaster-opp` runde 1, `aktivisere-hund-pa-tur` runde 2 — cachet på 68 tegn i runde 1). Alle tre description-tagger i synk på begge. sha256 loggført.

**Gjenstår etter dette: 11 tilfeller i hele page-settet** (129 sider, ikke bare de 121 artikkelsidene) — `orebetennelse-hund` (68 tegn) og `hund-sover-mye` (59) mangler suffiks; ni sider mangler `title_tag` helt: `contact`, `om-oss`, `om-king`, `tannhelse-hund`, `llms-txt`, `hund-graver-i-hagen`, `valpe-utstyr-sjekkliste`, `mellomschnauzer`, `strihaaret-vorstehhund`. `llms-txt` er en utility-side uten SEO-verdi og kan ignoreres. `orebetennelse-hund` er den eneste som faktisk avkortes.

**Måledato for disse to: live 2026-08-10 → les av ~2026-09-07**, samme klokke som de 15 andre.

**Tredje retting samme kveld — `orebetennelse-hund`:**

| | Admin-felt | Live-`<title>` |
|---|---|---|
| Før | `Ørebetennelse hos hund — symptomer, årsaker og behandling` (57) | **68 tegn** med en-dash-suffiks |
| Etter | `Ørebetennelse hos hund — symptomer og behandling \| Min Hund` (59) | **59 tegn** |

«årsaker» droppet fra titelen for å komme under 60; meta description (131 tegn, i bånd) bærer den fortsatt sammen med «forebygging» og vet-linja, så budskapet er ikke tapt. Meta uendret. Live-bekreftet runde 1, sha256 `b90916d2fe7019c6…`, alle tre description-tagger i synk.

**⚠ KORRIGERING av min egen «ingen flere avkortinger»-konklusjon — det er 23 igjen, ikke 0.**

Gotcha #23-sveipet svarte på spørsmålet *«mangler Admin-titelen «Min Hund», slik at temaet legger på suffiks?»*. Det er **ikke** samme spørsmål som *«er den effektive live-titelen over 60 tegn?»*. Etter at de tre en-dash-tilfellene var rettet, konkluderte jeg med at korpuset var rent. Det var feil: de aller fleste for lange titlene har suffikset korrekt satt i Admin og er rett og slett for lange i seg selv, og de var usynlige for sveipet mitt.

Fullt sveip av alle 129 sider (effektiv live-lengde = `len(title_tag)` hvis den inneholder «Min Hund», ellers `len+11`; tom `title_tag` → `len(page.title)+11`): **26 sider over 60 tegn — 23 artikkelsider + 3 hub/utility-sider.** De største etter visninger:

| Side | Live-tegn | Visninger | Klikk |
|---|---|---|---|
| `hvor-mye-mat` | 64 | 16 320 | 271 |
| `hund-bader-ute` | 67 | 7 620 | 124 |
| `valp-de-forste-ukene` | 62 | 6 281 | — |
| `hund-kroppsspraak` | **71** | 5 923 | 94 |
| `hund-lukter-vondt` | 62 | 4 784 | 125 |
| `hund-smerte-tegn` | 64 | 4 746 | — |
| `hund-graver-i-hagen` | 68 (tom `title_tag`) | 3 590 | 91 |
| `klippe-klor-hund` | **74** | 2 767 | — |
| `kennelhoste-hund` | **74** | 1 862 | 15 |

`hvor-mye-mat` er korpusets #2 på både visninger og klikk. `klippe-klor-hund` og `kennelhoste-hund` er de verste med 74 tegn — 14 over grensen.

**Bifunn:** tre titler har trailing whitespace før eller etter suffikset (`klippe-klor-hund`, `hund-og-varmen`, `hund-klor-seg`). Harmløst for rendering, men det gjør eksakt strengsammenligning upålitelig — normaliser med `.strip()` i alle framtidige sveip.

**Lærdom (samme klasse som gotcha #14 og #20):** et sveip svarer bare på spørsmålet det faktisk stiller. «Mangler suffiks» og «for lang» overlapper delvis, og jeg leste dekning på det første som dekning på det andre. Riktig audit for title-lengde er den effektive live-lengden for **alle** sider, uavhengig av suffiks-tilstand — kommandoen ligger i gotcha #23-tillegget.

**Ikke rettet** — 23 sider er et eget scoped pass, ikke en hale på denne økta.

### 2026-08-07 — Skuff-restrukturering: fem prosjekt-level skills med STATUS-filer; CLAUDE.md 175 → 127 linjer (`7a8bae3` → `ca08840`)

**Utløser:** CLAUDE.md var 175 linjer / 17,4 KB og ble lastet i sin helhet i hver eneste sesjon — også når arbeidet var en cart-bug. 34 % av fila var raseguide-sprint-innhold (4-fase-protokoll, sprint-workflow, lærdommer fra #60–63). Fire antatt eksisterende skills (`min-hund`, `raseguider`, `google-ads-min-hund`, `negative-keywords-min-hund`) viste seg **ikke å finnes** — søk i `~/.claude/skills/`, `~/.agents/skills/`, prosjektets `.claude/skills/` og hele hjemmemappa ga null treff. Den eneste ekte prosjekt-skillen var `hundetips-article-creator` på user-level.

**Besluttet (Sondre):** prosjekt-level `.claude/skills/`, git-versjonert og speilet. `hundetips-article-creator` flyttet inn fra user-level så alt ligger samlet. STATUS-filene fylles med ekte data ved opprettelse, ikke tomme maler.

**Fem skuffer opprettet** (`7a8bae3`, 1235 linjer):

| Skuff | Dekker | Filer |
|---|---|---|
| `min-hund` | drift: deploy, produktfakta, legal, GSC/MCP, mirror-synk | SKILL + STATUS |
| `raseguider` | 4-fase-protokoll, ordbudsjett, back-link-audit | SKILL + STATUS + `references/sprint-lessons.md` |
| `hundetips-article-creator` | nye hundetips-artikler | SKILL (flyttet inn) |
| `google-ads-min-hund` | konto, kampanjer, skriptbibliotek | SKILL + STATUS |
| `negative-keywords-min-hund` | negative søkeord | SKILL + STATUS + `NEGATIVES.md` |

**To mekanismer, ulike triggere — dette er kjernen i beslutningen.** Skills laster på **intensjon** (hva Sondre ber om) og har en `STATUS.md` som leses først og skrives sist i hver økt. Rules i `.claude/rules/` laster på **filkontekst** (hvilken fil du åpner). Raseguide-4-fase-protokollen trigges på «start sprint #64» før noen fil er åpnet — derfor skill, ikke rule. Ads-arbeid rører aldri en fil i repoet, så rules kunne per definisjon ikke fange det.

**CLAUDE.md redusert 175 → 127 linjer / 17,4 → 9,4 KB (46 %)** (`ca08840`). Alt flyttet, ingenting slettet — verifisert med dekningssjekk på 25 nøkkelregler: **0 tapt**. Beholdt som pekere fordi de må gjelde selv når skillen ikke er lastet: STOP-gate-regelen inkl. auto-approve-unntaket, at back-link-audit og pre-publiseringsporten er obligatoriske, service-konto-kravet for GSC, `sc-domain`-formen, og de tre produktfaktaene som oftest blir feil.

**Funn dokumentert i STATUS-filene underveis:**

1. **🔴 Google Ads MCP er nede** — `invalid_grant: Bad Request`, verifisert med et faktisk `execute_gaql`-kall mot konto 2198068625. Rotårsak: OAuth `refresh_token` i `~/google-ads-script/google-ads.yaml` sist skrevet **21.04.2026**. Samtykkeskjermen står trolig i *Testing*, som gir 7-dagers utløp. Fiks: `generate_refresh_token.py` (krever nettleser). Service-konto er ikke et alternativ — Google Ads krever Workspace-domenedelegering, og kontoen er en Gmail-konto. Permanent fiks: publiser samtykkeskjermen til «In production».
2. **NEGATIVES.md dekker 26 av ~50** negative søkeord. `add_negative_keywords.py` er **dynamisk** — leser søketermrapporten ved kjøring og lagrer ingenting, så repoet kan ikke gjenskape listen. GAQL-spørringen som lukker gapet ligger i fila. Dedup ga 0 duplikater (6 BROAD / 20 PHRASE).
3. **Seks av åtte rasespesifikke negativer blokkerer raser med live raseguide** — `jack-russell-terrier`, `finsk-lapphund`, `flat-coated-retriever`, `labrador-retriever`, `cocker-spaniel`, `golden-retriever` (alle 200). Satt i april for å skjerme et produktbudsjett mot infosøk; i dag er de samme søkene innholdssatsingens kjernemålgruppe. Krever bevisst avgjørelse per kampanjetype før Ads restartes.
4. **`dyrehår` BROAD kan blokkere kampanjens eget betalte søkeord** «fjerne dyrehår sofa». Uverifisert (auth nede) — står som kontrollpunkt.
5. **Sprintnummer ≠ raseguidenummer, offset +3.** Commit-meldinger bruker sprintnr, project-status bruker raseguidenr. Sprint #63 = raseguide #60. Offsetet kommer av at sprint #37/#41/#54 var Trigger B / cleanup.
6. **«Pending admin page-creation» i denne fila er stale** — WHWT, Samojedhund, Greyhound, Italiensk Mynde, Weimaraner, Whippet og Jämthund svarer alle **200**.
7. **`docs/link-audit-2026-05-20.md` finnes ikke**, men refereres som hjemmel for post-#50 crossover-link-auditen. Auditen må kjøres på nytt hvis den fortsatt er ønsket.
8. **Talldrift mot denne fila:** PDP-er 13 vs 15 på disk, hundetips-hub-kort 59 vs 61. Ikke overskrevet — flagget i `min-hund/STATUS.md` for reconciliation.
9. **Raseguide-sprintsporet har vært pauset siden 27.05** (~10 uker). Siste `feat(raseguide)` er `e1abc4b`.

**Metodefunn — parallelle økter committer i samme tre.** `sections/hundetips-hund-slikker-ansikt.liquid` lå ucommittet med +142 linjer da økta startet, og forsvant fra `git diff` midt i arbeidet fordi en parallell økt committet den som `318f4d7`. **Kjør `git log --oneline -3` før du beskriver treets tilstand** — `git status` fra sesjonsstart er ikke nok. Regelen er lagt i `min-hund/STATUS.md`.

### 2026-08-07 — Produktkort-hullet var i hovedsak en måle-artefakt; productduo bekreftet som forward-mønster (`318f4d7`)

**Utløser:** trafikkrapport for siste 30 dager (GSC 07.07–05.08: 2 282 klikk / 198 919 visn / CTR 1,15 % / pos 7,8 — +64,9 % klikk mot forrige periode) flagget «topp 10 mye trafikk, lite konverterende» basert på en `grep -c product-box`-proxy. Proxyen var feil.

**Tre måle-feil funnet og rettet:**
1. `grep -c 'product-box'` traff **CSS-regelnavn, ikke HTML**. `hvor-mye-mat` og `hund-kaster-opp` ble rapportert med «2» og «0» bokser — begge har i realiteten et `productduo`-kort. Samme fellen som obs 12723 (`hundetips-livreddende`).
2. Telling av `class="mh-article__productduo` fanget **sub-element-klasser** (`-intro`, `-card`, `-desc` …), så filer fikk «13 kort». Wrapper-tellingen er 9 i hele korpuset.
3. Første telling overså **`mh-article__recommend`** helt — en tredje produktkomponent. `hund-vil-ikke-ga-tur` og `hund-lukter-vondt` ble derfor feilaktig meldt som udekket.

**Riktig metode (bruk denne):** parse `class`-attributtet og match på **eksakt token** (`tok in c.split()`), ikke delstreng, og sjekk alle tre komponentene: `mh-article__recommend`, `mh-article__product-box--featured`, `mh-article__productduo`.

**Korpus-fasit:** 37 filer `--featured` (Batch 1–7) · 9 filer `productduo` · 8 hundetips-sider helt uten kort (172 klikk/mnd, alle med 0 prosalenker).

**Beslutning 1 — ikke konverter productduo → `--featured`.** `docs/page-patterns.md` sin retrofit-standard (effective 2026-07-02) gjør `productduo` til målmønsteret: ETT kort, maks 2 produkter, maks ett kort-touchpoint per produkt. De 9 productduo-filene er de *allerede retrofittede*. En konvertering ville vært en regresjon. Sondre godkjente å droppe den.

**Beslutning 2 — «produktkort-mulighet» er overvurdert som CRO-kategori.** Av de 8 kortløse sidene har **1** en ærlig produktkobling. De øvrige 7 handler om problemer katalogen ikke løser: lufttett beholder/målebeger, bånd, kloklipper, øremiddel (×2), flåttmiddel, førstehjelp. På `oppbevaring-torrfor-hund` (51 klikk — størst av dem) sier artikkelen eksplisitt at matskålen *aldri* skal brukes som måleredskap, så en aktiviseringsskål der ville motsagt teksten. Reell oppside ligger i CTR-arbeid på sider som allerede rangerer, ikke i flere kort.

**Levert:** `hund-slikker-ansikt` fikk `productduo--single` → CalmBall, plassert etter «7 regler for trygg kos» (regel 6 = «Tren hunden til å hilse uten å slikke» er kroken). v2-scopet CSS portert fra kanonisk `hundetips-hva-kan-hund-spise.liquid`; `--single`-regler fra `hvor-mye-mat`. Filen manglet base-`.mh-article__product-btn`, så knappen styles i sin helhet scopet. Lager verifisert live før lenking (gotcha #12). +33 ord (1,4 %) → llms.txt ikke trigget.

**Meta-fiks (Friday, Admin):** `bandtvang-norge` og `hva-kan-hund-spise` fikk nye title + description. Verifisert live med cache-buster, alle tre tagger i synk. Ett kosmetisk avvik: bandtvang-title har en-dash `–` der em-dash `—` ble sendt. `rips` (88 visn/mnd) ble bevisst holdt UTE av hva-kan-hund-spise-metaen — ordet finnes ikke i artikkelen; det er et innholdshull, ikke et meta-hull.

**Metodefunn — falske nuller ved live-verifisering (gjentakelse av obs 12721).** Første live-sjekk av CalmBall-kortet ga 0 treff på alle seks markørene fordi regexet antok `class="…"` med doble anførselstegn i Shopifys rendrede HTML. Kortet var live hele tiden. Samme klasse feil rammet meta-sjekken tidligere samme dag: `<meta name="description" content="…">` skrives **flerlinjet** av `snippets/meta-tags.liquid`, så et enlinjes regex meldte «(ingen)» på sider som hadde velformede metaer. **Regel: live-verifisering skal alltid være quote-agnostisk og `DOTALL`.**

**Åpent:** Google Ads-refresh-token er dødt (`invalid_grant`, både MCP og `~/google-ads-script/google-ads.yaml`) — Ads-pausen fra 06.08 kunne ikke bekreftes. Fikses med `python3 ~/google-ads-script/generate_refresh_token.py`. GA4 og Shopify Analytics har ingen tilgang i CLI-miljøet, så sesjoner/produktvisninger/trafikkilder/bounce mangler fortsatt.

### 2026-08-06 — Puslespill-PDP: bygget, faktarettet ×3 og reposisjonert på én dag (`97c99b6` → `126a03d`)

**Produktet.** Bygget som «Puslematte for hund – interaktiv aktiveringsmatte» (`97c99b6`), endte kvelden som **`Puslespill for hund – godbitleke med lokk og skiver`**, handle **`puslespill-hund`**. Tittel og handle satt av Sondre i Admin etter forslag; 301 fra gammel URL verifisert. Tema-filnavnene (`product-puslematte.liquid`, `product.puslematte.json`, suffiks `puslematte`) er med vilje **ikke** endret — å røre templateSuffix er den kjente stille-fallback-risikoen fra `626e101`.

**Tre faktarettingsrunder mot produktbildene, i denne rekkefølgen:**

1. **Farge** (`8ac6ef5`). Setningen «Kommer i blått med fôrrom i plomme; taupe og mørk blå» var både ugrammatisk og faktisk feil — den tilskrev aksentfargene til fôrrommene. Fôrrommene er umalte nedsenkninger i grunnplaten og har samme mintblå farge som resten. Det er lokkene og midtskivene som er farget. Malen fra `product-slikkematte*.liquid` var fylt ut med feil del. «Mørk blå» rettet til «mørk petrolblå».
2. **Deletall** (`b173d4a`). Copyen sa seks lokk og fire kileskiver; bildene viste fem og tre. Bekreftet av Sondre. **Fôrrom-tallet måtte følge med, tolv → ti** — ytterringen er fem peanøttformede fordypninger med to rom i hver og ett lokk som skyves mellom dem, så «dekker halvparten om gangen» hadde blitt matematisk usant med 5 lokk / 12 rom. Peanøtt-strukturen bekrefter uavhengig at fem er riktig: fem fordypninger, ett lokk i hver, ingen manglende deler i fotosesjonen.
3. **Posisjonering** (`0af5857`). Fra måltidsmatte til godbitprodukt. 33 flater: brand-tag, badge, hero, sonekort, feature-grid, King-sitat, spec-tabell, bruksanvisning, sikkerhet, juridisk og FAQ ×11 — hver FAQ-endring på både synlig HTML og FAQPage-schema.

**Ny HARD-regel: «Produktfamilie-termer»** (`e593f96`, `docs/products.md`). Hvert produkt får sin egen head-term, samme disiplin som CalmBall-regelen. `puslespill-hund` = **aktiviseringspuslespill** / kortform **puslespill**. Avvist: *snuseleke/snusematte* (korpuset bruker det om et stoff-produkt vi ikke selger — samme form-factor-feil som slikkeball/slikkematte), *aktiviseringsleke* (head-term for `aktiviseringsleke-for-hund`, ville gitt PDP-mot-PDP-kannibalisering), *godbitdispenser* (mekanisk feil — produktet dispenserer ikke, hunden avdekker statiske rom).

**🔴 Regelen spiste sin egen begrunnelse — verdt å merke seg.** Valget av «puslespill» ble begrunnet med at korpuset allerede brukte ordet om denne mekanikken, blant annet i `hundetips-hund-hopper-pa-folk` og `aktivisering-article`. Batch 4-økta oppdaget at nettopp de to forekomstene beskrev **det andre produktet** (Godbitballen), og at den nye regelen derfor tvang dem omskrevet til «Godbitball». Regelen står seg — forekomstene var feilmerkede og ble korrigert — men to av bevisene som ble sitert for den, forsvant idet den ble håndhevet. Ved framtidige term-valg: sjekk hvilket produkt en korpusforekomst faktisk omtaler før den brukes som presedens.

**🔴 Handle-bytte stryker hardkodede handle-lister stille** (`126a03d`, gotcha #22 utvidet). Da handelen ble byttet, forsvant «Nyhet»-badgen fra produktet: `mh_nyhet_handles` matcher på `product.handle` og sluttet å treffe. `/collections/all` gikk fra tre til to badges uten feilmelding, og 301-redirecten gjorde at produktsiden så helt normal ut. Rettet begge steder. Grep-sjekkliste lagt inn — hardkodede handle-lister finnes minst i `mh_nyhet_handles` (×2), `mh_king_handles`/`mh_king_tested_handles` (×2), `mh_curated`, `mh-product-readmore` og `llms-products-data`.

**Metodefunn: samme påstand overlever i annen tegnkoding.** Deletall-sveipen traff først ni flater; en tiende («alle tolv rommene … alle seks lokkene … de fire skivene» i bruksanvisningen) overlevde fordi den brukte annen ordlyd, og FAQ-svaret + JSON-LD-tvillingen bruker literal `ô` der resten av fila bruker `&ocirc;`. Søk alltid på begge kodinger, og kjør FAQ↔FAQPage 1:1-verifisering etter enhver tallendring.

**Åpent.** SEO-tittel og meta-description for `puslespill-hund` er foreslått, men ikke satt i Admin: `Puslespill for hund – godbitleke | Min Hund` + «Godbitene ligger gjemt under fem lokk og tre dreibare skiver — hunden må jobbe for snacksen. Kan også fylles med tørrfôr.» `snippets/llms-products-data.liquid` mangler fortsatt de tre nye produktene (Trigger C — 12 → 15). Google Ads MCP er nede (`invalid_grant`, utløpt OAuth) — samme mønster som GSC hadde før service-account-migreringen, så navnevalget er tatt uten søkevolum-støtte.


### 2026-08-04 kveld — NYTT PRODUKT: Valpepakken PDP + fargevelger + valpe-artikkel-integrasjon (`21a8117` → `0154120`, 8 commits)

Parallelt spor ved siden av raseguide-sporet (C3c-18/19 gikk samtidig i samme repo). Alt live på `#148333264974`, alt pushet til GitHub main.

**Produktet.** Valpepakken, handle `valpepakken`, 449 kr, ingen compare-at. Innhold: CalmBall + tyggering i silikon + drikkeflaske i rustfritt stål/silikon. Sondre opprettet produktet, bildene, opsjonen `Farge` (Blå/Rosa), variantbilder, SKU (`MH-VP-BLAA`/`MH-VP-ROSA`) og alt-tekster i Admin underveis i økta. `templateSuffix = valpepakken` (ett av få som matcher URL-handle). Lager per 05.08: **5 Blå + 5 Rosa**, begge InStock i Product-schemaet. (Var kortvarig 9/0 natten mellom 04. og 05.08 mens oppsettet pågikk — rettet i Admin 02:14.)

**Levert.**
1. `sections/product-valpepakken.liquid` + `templates/product.valpepakken.json` — kanonisk PDP-mønster (hero-galleri, trust-badges, ATC via `product-form-component` urørt, King-sitat, accordions, readmore, related, sticky mobil-ATC). BEM-prefiks `vp-`. FAQPage JSON-LD inline (snippeten `mh-product-faq-schema` krever en objekt-array Liquid ikke kan bygge uten metafelt).
2. Swatch-basert fargevelger — datadrevet, rendres kun ved nøyaktig én opsjon med flere verdier (fail-safe). Grønn ring på valgt, hover-glow, `aria-pressed`, piltaster, `aria-live`. Galleribildet krysstoner (`opacity .35s`), `prefers-reduced-motion` sjekkes i JS. Swatch-farge utledes av variant-tittel — **nye fargenavn må legges inn i `case`-en, ellers blir prikken grå**.
3. Produktkort i alle fire valpe-artiklene (`valp`, `valp-biter-pa-alt`, `valp-tisser-inne`, `valpe-utstyr-sjekkliste`) etter `--featured`-mønsteret fra `hundetips-aktivisere-hund-pa-tur`. Bilde og pris hentes via `all_products['valpepakken']`.
4. Valpepakken er nå **eneste produktanbefaling** på de fire sidene — 5 produktbokser, 3 bunn-CTA-er og 5 inline prose-lenker fjernet. De resterende produktlenkene på sidene ligger i **sidefoten**, som er global og ikke ble rørt.
5. `snippets/llms-products-data.liquid` — Valpepakken inn (Trigger C), 11 → 12 produkter.
6. `snippets/mh-product-readmore.liquid` — nytt `valpepakken`-case med tre valpe-artikler.

**To feil funnet og rettet underveis.**
- *Sammenlimte HTML-attributter.* `{%- … -%}` rundt betingede attributt-blokker spiste mellomrommet MELLOM attributter (`data-media-type="image"data-image-url=…`). 14 tilfeller på valpepakken-PDP-en, og samme arvede mønster i `product-vannflaske` (8), `product-calmball` (12) og `product-pelsfjerner` (20). Alle rettet — grenene starter nå med eksplisitt mellomrom. **Mønsteret finnes trolig i flere PDP-er som ikke ble sjekket.**
- *Claim-brudd i llms.txt.* CalmBall-linja påsto «aktiverer parasympatisk nervesystem. Reduserer stress under separasjon» og Andefanten «Trygg for supervised lek og alenetid» — begge i strid med HARD-reglene i `docs/products.md`. Erstattet. Hundeseng-linja står med vilje («beroligende» kommer fra produktnavnet).

**Bildezoom — metode verdt å gjenbruke.** Bildene er portrett 1512×2016 med mye hvit luft; produktene fyller bare 30 % av bildehøyden. Målt ved å konvertere kilden til BMP og analysere piksler (`sips -s format bmp` + ren python — PIL finnes ikke på maskinen): solide produktpiksler ligger x 14–84 %, y 35–65 %. PDP endte på `scale(1.44)` av beregnet maks 1.90; artikkelkortet på `scale(1.5)` av maks 1.99, samme sikkerhetsmargin (0.758). Kortet trengte også `overflow: hidden` på `.mh-article__product-media` — uten det maler det oppskalerte bildet inn i tekstspalten.

**Verifiseringsmetode (ny).** Visuell verifisering før push løst ved: lokal `shopify theme dev` → hente det rendrede kortet + seksjonens egen CSS → isolert HTML-fil → skjermbilde i headless Chrome → beskjære og forstørre 2×. Headless Chrome henger på dev-server-URL-en direkte (eksterne Shopify-ressurser blokkert), men fungerer på lokale filer. `getBoundingClientRect` injisert via `--dump-dom` ga eksakte layout-tall. Første lille rendring så ut som produktet var klippet — 2×-utsnittet viste at det var slagskyggen. **Lærdom: ikke konkluder på lavoppløste utsnitt.**

**Gjenstår.**
- ~~Lagerfordeling Rosa/Blå~~ — løst 05.08: 5 + 5. Merk at PDP-ens lagervarsel («Kun N igjen på lager») trigges under 6 og derfor vises fra dag én på begge farger. Korrekt, men ikke et faktisk knapphetssignal.
- Bildefilene bør beskjæres ved kilden; zoom er en midlertidig kompensasjon for hvit luft i eksporten.
- Tre `.mh-article__cta-wrap`-CSS-regler står igjen som død CSS i valpe-artiklene etter at HTML-blokkene ble fjernet.
- Attributt-mønsteret bør sveipes i de resterende PDP-ene.

### 2026-07-30 kveld — NYTT SPOR: strukturert data + produktidentifikatorer (`b413927`, `e0936c2`, `c1bb03f`)

Første rene teknisk-SEO-økt siden raseguide-sporet startet. Utløst av en kartlegging Sondre bestilte på fem punkter: Product-schema, Organization-schema, GTIN/MPN, alt-tekster, dobbel H1.

**Kartleggingsfunn (11 produkter, ikke 20 — det tallet stammet fra en eldre Merchant Center-audit):**
- Product-schema fantes og virket (`snippets/mh-product-schema.liquid`, rendres av alle 11 custom PDP-seksjoner), men manglet alt Merchant Center etterlyser: `priceValidUntil`, `itemCondition`, `shippingDetails`, `hasMerchantReturnPolicy`, `gtin`/`mpn`. `aggregateRating` virket allerede via Judge.me sitt `reviews.rating`-metafelt.
- **To konkurrerende org-noder** på hver side: `OnlineStore` i `layout/theme.liquid` og en Horizon-stock `Organization` i `sections/header.liquid`. Ingen av dem hadde org.nr eller legalName. Stock-noden hadde i tillegg feil `url` (`request.origin | append: page.url` → tom `page.url` utenfor sidemaler).
- **GTIN og SKU tomme på alle 20 varianter.** Bekreftet, ikke antatt.
- **12 av 56 produktbilder uten alt-tekst** — pelsfjerner 7 av 10, potevasker 3 av 4. Ingen filnavn-/placeholder-tekst; rent fravær.
- **Dobbel H1 kun på forsiden** (header-fallback + hero). Produkt- og kolleksjonssider hadde korrekt 1.

**Levert live:**
- `b413927` — Product-schema utvidet, Organization konsolidert til én node med `@id`/`legalName`/org.nr 935457017/`sameAs`, forside-H1 2 → 1. `vatID` bevisst utelatt (ikke MVA-registrert).
- `c1bb03f` — `hei@` → `kontakt@minhundpet.no` i llms.txt-trioen + `docs/research-brief.md` (Trigger D). `hei@` var aldri verifisert; `kontakt@` er adressen `/policies/refund-policy` oppgir.
- **20 av 20 SKU-er satt** etter konvensjon `MH-<produktkode>[-<variantkode>]` via `mcp__shopify__manage-product-variants`. Priser og varianttitler urørt — verifisert mot storefront.

**Beslutninger som ble tatt underveis:**
- `price` byttet fra `money_without_currency | replace: ',', '.'` til `divided_by: 100.0`. Den gamle kjeden gav riktig output under 1000 kr, men norsk tusenskille ville gjort `1.234,00` til `"1.234.00"`. Dyreste variant i dag er 999 kr — altså 1 kr fra bruddet.
- `merchantReturnDays: 30`, ikke 14. Vilkårssiden gir 14 d lovpålagt angrerett **pluss** 30 d utvidet returrett på ubrukte varer; 30 er det bredeste korrekte tallet.
- Frakt beregnes **per variant** mot 250 kr-terskelen (0 kr over, 79 kr under) i stedet for ett fast tall.
- `shippingDetails`/`hasMerchantReturnPolicy` gjentas per variant framfor `@id`-referanse — Google leser dem på Offer-nivå.

**Metodefunn (gotcha #16, `e0936c2`):** `shopify theme dev` renderer lokale filer mot ekte butikkdata på localhost. Det er den eneste ekte pre-push-verifiseringen av rendret Liquid, og lukker hullet gotcha #11 etterlot. Fanget at `image_url` gir protokoll-relativ URL som må prependes `https:` for å være gyldig i Product-schema. Etter push gjelder fortsatt gotcha #9/#10: edge-cachen brukte ~4 min og svingte 8 → 5 → 7 → 9 av 11 ferske mellom målinger.

**Ikke gjort — venter:**
- **GTIN/EAN på alle 20 varianter.** Må komme fra leverandør. Schemaet skriver ut `gtin13` betinget, så det dukker opp av seg selv når `barcode` fylles. Ullgenseren er egenprodusert og skal trolig markeres `identifier_exists: no` i feeden i stedet.
- **De 12 alt-tekstene.** Kan ikke settes med `mcp__shopify__*` — `update-product` har ikke media-felt og MCP-serveren har ingen media-mutasjon. Krever Admin GraphQL `productUpdateMedia` med et `write_products`-token. Ferdig skript med alle media-GID-er og godkjente tekster: `~/minhund-set-alt-texts.sh`. Tekstene er også dokumentert i `docs/products.md`.


### 2026-07-29 — Kildesettings-prosjektet startet: faktafeil + topp-4 kildesatt live (`2a6b938` + `6ec8107`)

Nytt spor etter popup-compliance-funnet 28.07 (35 av 59 generelle hundetips uten navngitt kilde). Kartlegging reproduserte 35-tallet, men fant **to feilklassifiseringer**: `oppbevaring-torrfor-hund` har FDA+AAFCO (falt utenfor norsk regex-mønster), og `hund-liker-ikke-bading` siterer Hill's Pet + Orvis — kommersielle aktører som bryter kildepolicyen. **Reell status: 33 uten kilde + 2 med problematisk kilde.** Prioritert på GSC-klikk 30 d (GA4 ikke tilgjengelig i sesjonen).

**Batch 1 — faktafeil (`2a6b938`), skilt ut fordi det er feil info, ikke kildemangel:** Mehrabian-myten «80 % av menneskelig kommunikasjon er kroppsspråk» **fjernet** (ikke kildesatt — en myte skal ikke få kilde) ×2 i `hund-kroppsspraak`; utdatert «druetoksinet er uidentifisert» → vinsyre, Wegenast et al. 2022 (JVECC 32(6):812-816); ubelagt «belønning 10× mer effektivt enn straff» → Ziv 2017 (J Vet Behav 19:50-60) uten multiplikator. `giftig-mat` bevisst urørt — «eksakte **dosen** er ukjent» er fortsatt korrekt.

**Batch 2 — topp 4 + sikkerhetsfiks (`6ec8107`, 5 filer live):**
- **⚠ Kastrering-underfôring.** Prosa sa «20–30 % færre kalorier» OG **kalkulatoren i samme fil brukte faktor 1,4 mot 1,8** (~22 % lavere). Rettet til 10–15 % i tekst og faktor **1,6** i kalkulator (NRC 2006/WSAVA/AAHA). En 20 kg kastrert hund får nå ~14 % høyere anbefaling. **Lærdom: tall som finnes både i prosa og i et interaktivt verktøy må sveipes begge steder — verktøyet er det brukeren handler på.**
- **Bulldog-«motsigelsen» var ingen motsigelse.** 49,07 (`hund-lukter-vondt`) og 38,1 (`engelsk-bulldog`) er to O'Neill-2022-studier med ulik referansegruppe — blandingsraser (Scientific Reports 12:10553, 905 553 hunder) mot alle andre hunder (Canine Medicine and Genetics). Begge kildesatt og kryss-lenket. **Lærdom: sjekk studiedesign før du «harmoniserer» bort et riktig tall.**
- **Feil tall:** otitis externa 10 % → **7,30 %** (O'Neill et al. 2021, CMG 8:7). **Periodontitt «minst 80 %» har ingen primærkilde** (Niemiec-lærebok) → erstattet med O'Neill et al. 2021 JSAP 12,52 % ettårsprevalens + eksplisitt merking av 80 %-tallet som lærebokanslag. Lå også i ingressen.
- **Kildesatt:** NRC 2006 (RER-formel), Kealy et al. 2002 JAVMA (levetid), Glickman et al. 2000 (GDV, gjenbruk), Čonková et al. 2011 Acta Vet Brno (Malassezia, n=147 Slovakia — symptomatisk utvalg presisert), Veterinærinstituttet (blågrønnalger).
- **Myket opp uten sporbar kilde:** «1 dl saltvann», «70 % Malassezia i otitt», hud-pH-spennet, «særlig på Sørøstlandet».
- **Harmonisering:** fôrbytte → 7–10 dager (fra 5–7 i hvor-mye-mat, eldre-hund ×2, valpe-utstyr). Løser B4/E2 i registeret.

**Prinsipp fastsatt (Sondre):** *et presist tall uten kilde er verre enn et upresist tall som er sant* — myk opp framfor å sitere noe usikkert. **Aldri oppdikt en sitering:** en feil sitering er mer villedende enn ingen, og består alle automatiske sjekker. Alle nye siteringer slås opp mot primærkilde før de skrives inn (Wegenast-årstallet 2021→2022 ble fanget slik).

**Verifisering:** 21/21 preview-kontrollpunkter PASS; live pre/post-pull 711→711 filer med **kun de 5 forventede endret, 0 kollateral**; sha256 live == HEAD på alle 5; 5 URLer sendt til GSC. `hund-bader-ute` viste page_cache-rotasjon på live (gotcha #10) — kildefil og ucachet render verifisert korrekte. **Metodefelle fanget:** første live-kontroll ga falskt PASS fordi preview-cookien ble gjenbrukt, så «live»-hentingen rendret preview (identisk bytestørrelse avslørte det). Live-kontroll må kjøres **uten cookie-jar**.

**Batch 3 — punkt 3 (`7580f19`, 9 filer live):** Kendal Shepherd kreditert for aggresjonsstigen (BSAVA 2001 — modellen har vært brukt uten opphavskreditering); Herron/Shofer/Reisner 2009 og Mariti et al. 2017 inn i `hund-kroppsspraak`; Adams & Johnson 1993 i `hund-sover-mye`; Axelsson et al. 2013 (AMY2B) i `hva-kan-hund-spise`; Scott & Fuller 1965 i `valp-biter-pa-alt`. Godbiter 10–15 % → **10 %** (5 steder). «15 000 år» → «minst 15 000 år». **`hund-vil-ikke-spise` hadde samme ukildede 80 %-tannpåstand** som ble fjernet fra `hund-lukter-vondt` i batch 2 — tatt ut på 3 steder inkl. schema, ellers ville to av våre sider motsagt hverandre live. **Søvnspriket var større enn flagget:** tre aldersbånd i strid på tvers av fem filer, ikke bare valpetallet — standardisert til valp 18–20 / voksen 12–14 / senior 18–20, kryss-sjekket på seks sider med 0 avvik igjen. Live: 711→711 filer, kun de 9 forventede endret, 0 kollateral, sha256 == HEAD, 9 URLer til GSC.

**Verifiseringen trenger egen disiplin.** To batcher på rad hadde feil i kontrollmetoden, aldri i innholdet: batch 2 brukte `38,1` som «gammel»-markør, som er delstreng av nye `38,12` og derfor alltid slo til; batch 3 verifiserte `hundetips-valp.liquid` mot `/pages/valp`, som ikke er artikkelens handle (`valp-de-forste-ukene`). Sistnevnte ga FAIL på både ny og gammel verdi — et **umulig resultat**, og det er nettopp det som avslørte feilen. Begge fellene er nå formalisert som faste sjekkpunkter.

**Ny permanent arbeidsrutine: `docs/artikkel-sjekkliste.md`** — HARD, kjøres ved hver artikkel som skrives eller redigeres (hundetips, raseguider, produktsider). Inneholder de to grunnreglene, tall- og kildekrav (inkl. lærebokanslag-fella og multiplikator-/referansegruppe-sjekken), sveip av interaktive verktøy og speilinger, og verifiseringsdisiplinen med substreng-selvtest og «umulig resultat»-invariant.

**Batch 4 — punkt 4 bolk 1 (`52409ed`, 11 filer live):** **Første feil funnet i en eksisterende sitering.** `hund-spiser-avforing` siterte Hart et al. 2018 ved navn, men gjenga funnet feil — «16–23 % … siste måneden» var to separate måltall (23 % observert, 16 % hyppig) slått sammen til et spenn, med en tidsramme som ikke finnes i studien. Sjekklisten fant den. **Gratis-gevinstene** `hund-darlig-ande` og `orebetennelse-hund` gjenbrukte O'Neill-kildene fra batch 2; periodontitt-påstanden er nå konsistent i fire artikler. **Nye kilder:** Dewhirst et al. 2012 (353 taksa erstatter «400+»), WSAVAs vaksineretningslinjer, CMPS-SF. **Verktøy vs prosa igjen:** `hvor-mye-vann-hund` sa flatt 50–60 ml/kg mens kalkulatoren skalerte 80/65/55/50 etter størrelse — kalkulatoren var riktig, prosaen fulgte til 40–60; korpus-sveip dro inn `hund-og-varmen`. Priser tidsstemplet. Live: 711→711, kun de 11 forventede, 0 kollateral, sha256 == HEAD, 11 URLer til GSC.

**Ny speilingsflate oppdaget — meta-description.** Tre sider ga FAIL på rendret verifisering selv om seksjonsfilene var rene: de gamle tallene lå i **Shopify Admins SEO-felt**, som ligger utenfor repoet og derfor er usynlig for både `grep` og fil-sjekker — men er det brukeren ser i Googles utdrag. Formalisert som «flate 3» i `docs/artikkel-sjekkliste.md` (flate 1 = brødtekst, 2 = JSON-LD, 3 = meta-description), med metoden for å oppdage den (skill `<head>` fra body i rendret HTML). **Fire åpne Admin-steg** logget i registeret: hund-spiser-avforing, hvor-mye-vann-hund, hund-slikker-ansikt + hund-om-sommeren (åpen siden 25.07). Går til Friday som eget steg — blokkerte ikke live-push.

**Batch 5 — punkt 4 bolk 2 (`b9122fe`, 14 filer live). Kildesettings-prosjektet for generelle hundetips er dermed FULLFØRT** — alle 24 opprinnelig kartlagte artiklene uten navngitt kilde er nå enten kildesatt mot primærkilde eller myket opp.

**⚠ Retningsfeil — prosjektets alvorligste funn.** `eldre-hund` fremstilte «inaktive hunder har forhøyet risiko» som «aktive seniorhunder har **syv ganger lavere** risiko for demens», og kalte mental aktivisering «forebyggende behandling». Invertert oddsforhold + kausal innramming = siden påsto noe studien ikke sier. Rettet til studiens retning: Dog Aging Project Consortium 2022 (Scientific Reports, n=15 019) — +52 % odds per leveår, 6,47× høyere odds hos inaktive, merket som observert sammenheng. CDS-prevalensen «19–41 %» hadde ingen sporbar kilde → Neilson et al. 2001 (JAVMA): 28 % ved 11–12 år, 68 % ved 15–16. **Lærdom: invertering av oddsforhold er ikke symmetrisk, og en observert sammenheng er ikke en behandlingseffekt.**

**Tabeller er en egen speilingsflate.** `eldre-hund` hadde «opp mot 85 %»-tannpåstanden både i prosa og i sykdomstabellen — prosa-fiksen traff bare den ene. Femte og sjette forekomst av samme tall i korpuset; begge rettet.

**Sherman & Mills 2008 verifisert** (ikke antatt riktig): korrekt gjengitt, men en amerikansk telefonundersøkelse — rekkevidden står nå i teksten. Ni ukildede prosenttall myket opp. Honning-dosen i `kennelhoste-hund`, korpusets eneste hjemme-dose, rammet som hjemmeråd med styrket botulisme-advarsel.

**Verktøy-sveip kjørt før kartlegging** (etter Sondres instruks). Detektoren ga først falsk negativ på `hvor-mye-vann` — den kalkulatoren ligger i en `{% javascript %}`-blokk, ikke en `<script>`-tag. Etter fiks viser korpus-sveipen **kun tre treff totalt**: de to kalkulatorene (begge rettet) + `product-andefanten` (antallsvelger). **Verktøy-mot-prosa-risikoen er kartlagt og lukket.**

**Ny sjekklisteregel:** kontrollmønstre som treffer null på tvers av hele batchen behandles som mistenkt, ikke bestått — krev én positiv verifisering før du stoler på et rent resultat. Regelen kom av at meta-sjekken ga «(mangler)» på alle 14 sider fordi meta-taggene er flerlinjede mens mønsteret krevde én linje. Tredje runde på rad hvor kontrollen tok feil og innholdet var riktig.

Live: 711→711, kun de 14 forventede, 0 kollateral, sha256 == HEAD, 14 URLer til GSC. Meta-description ren på alle 14 — ingen nye Admin-steg.

**Enkeltpunktene lukket (`9e356ff`):** Hill's/Orvis/AKC ut av `hund-liker-ikke-bading` → BOAS-forankring (Packer et al.; VetCompass). Feberterskel i `hund-vil-ikke-spise` kildesatt til referanseintervall-studie av >9 000 hunder (37,7–39,5 °C; 39,2 beholdt som oppmerksomhetsnivå, ikke hard grense). Eskaleringstrappa: ingen navngitt WSAVA/AAHA-konsensus funnet — autoriteten myket, **tersklene urørt** (over-48-timer ×6, valpeunntak ×5 verifisert som egne PASS-krav). Alle fire meta-descriptions bekreftet oppdatert på live; Admin-seksjonen lukket.

### 2026-07-31 — C3c-3 WHWT + whippet (`1b8c2a9`, 2 filer live)

**🔴 Dagens alvorligste funn: en ekte kilde med oppdiktet funn.** WHWT-guiden skrev at Salzmann et al. 2011 «identifiserte en 1,3-Mb-region på CFA 17». Studien konkluderer med det motsatte — **«no chromosomal regions were identified with significant linkage»** — og det subterskel-signalet som fantes lå på **kromosom 7**, ikke 17. **Siteringen var korrekt formatert med journal, år, volum og sidetall og ville bestått enhver formatsjekk.** Dette er farligere enn en oppdiktet sitering: kilden finnes, den er riktig gjengitt bibliografisk, og bare funnet er galt.

**🟢 CAD-benet flyttet til Favrot et al. 2020**, som faktisk måler det guiden påsto: 52 % prevalens i en kohort på 108 valper fulgt i tre år, 60 % debut i første leveår. **Begge studiene har n=108 WHWT — sannsynlig årsak til sammensmeltingen. To studier på samme rase med samme utvalgsstørrelse er en konkret forvekslingsrisiko.**

**🔴 Aldersvindu forskjøvet tredje dag på rad** (Jansen/samojedhund → Beardow/cavalier → Favrot/WHWT). **Aldersgrenser er den hyppigst forskjøvne tallklassen i korpuset og bør sjekkes eksplisitt mot studien hver gang.**

**🟢 NKK-tallet verifisert mot primærkilden.** NKKs egen «Topp 25 registrerte raser 2024» gir «25 Whippet 264» — eksakt som guiden. Samme tabell bekrefter golden 1026 (#1) og border collie 982 (#2), så hele NKK-2024-klyngen henger sammen.

**🔵 Eget funn fra 30.07 strøket.** «Whippet-guiden oppgir kun hannspennet» var falskt — guiden er stratifisert begge steder. Substreng-telling uten å lese setningen. **Andre gang på to dager at kontrollmetoden, ikke innholdet, var feilkilden.**

**🟢 Ordbudsjettering før skriving fungerte — første gang prøvd.** Begge er 2400–2800-guider: WHWT landet 2671 mot planlagt ~2653 (slakk 129), whippet 2527 (slakk 273). Ingen trim-iterasjoner.

**Ventende FAQ↔schema-bolk er nå 20 filer, ikke 21** — WHWTs sju tegnsettingsavvik ble ryddet mens fila uansett var åpen.

### 2026-07-31 — C3c-2 cavalier + bichon-havanais + border-collie (`b5047b1`, 3 filer live)

**🟢 Forslagslisten min var upresis — guiden hadde allerede kilden.** Jeg foreslo å legge til HR-2023-1901-A og datoen i cavalier-guiden; begge sto der fra før. **Lærdom: verifiser hva guiden faktisk mangler før du foreslår tillegg.** Det som virkelig manglet var Høyesteretts eget terskeltall (minst 15 % av hundene) og Mattilsynets grensegang om at forbudet kun gjelder renraset avl — blanding er ikke omfattet, men kan likevel bryte § 25.

**🔴 Bilyd-tallene var riktige i retning, forskjøvet i grensene.** Beardow & Buchanan 1993 (n=394) måler 56 % fra **fire** år og 100 % ved ti; guiden hadde 5 år og «over 90 prosent». Samme klasse som Jansen-vinduene i samojedhund — studien oppgir én grense, guiden gjenga en annen.

**🔴 Sirkulær bekreftelse nesten godtatt for andre gang på to dager.** Søket på NAAFs standpunkt ga **vår egen bichon-side** som treff nr. 2, med sammendraget ordrett fra guiden. Verifisert mot NAAFs egen side i stedet. Regelen bør nå regnes som fast.

**🔴 Ingress-drift for tredje gang på rad.** Border collie: ingressen sa «2. mest populære», faktastripen sa allerede «2. mest registrerte rase 2024 (NKK)». Kilden lå i fila. Golden hadde nøyaktig samme feil samme dag; labrador hadde den i Bolk B.

**🟡 CEA-tallet myket framfor kildesatt — bevisst.** Publiserte tall spriker mellom 7,8 % allelfrekvens og 29,6 % bærerfrekvens. Å velge ett ville reprodusert allel-vs-bærer-feilen fra corgi, cocker og samojedhund. **Når to publiserte tall for samme forhold er av ulik type, er oppmykning riktigere enn å velge — valget ser ut som presisjon og er det ikke.**

**🟢 To klubbkilder verifisert mot egne sider:** NAAF («ingen forskjell mellom hunderasene … derimot ganske stor forskjell fra hund til hund, innenfor samme rase» — den innenfor-rase-variasjonen manglet i guiden) og NBHK (patellakravet gjengitt korrekt).

### 2026-07-31 — C3c åpnet: detektor bygget og kalibrert (`b8d8223`) + C3c-1 (`7591e45`, 2 filer live)

**Nytt verktøy i repoet: `tools/rangeringsdetektor.py`.** C3c er en annen jobb enn C3a/C3b — der fantes siteringer å spot-sjekke, her er det rangeringsspråk og prevalens uten opphav. Fire kalibreringsrunder er reell arbeidstid og skal ikke gjøres om igjen; verktøyet er dokumentert i fila.

**Viktigste prinsipp fra kalibreringen: en detektor som skal finne en feilklasse må kalibreres mot en versjon der feilen fortsatt finnes.** Kjent positiv måtte hentes pre-fiks (`git show 04ad4d2^`) — dagens `engelsk-bulldog` har fått påstanden rettet i Bolk A, så arbeidstreet ville gitt falsk negativ.

**Designvalg som bar mest: to nivåer, ikke ett.** Første versjon hoppet over siterte setninger. Men Bolk A/B viste at de alvorligste feilene satt nettopp der — ekte siteringer festet til rangeringer datagrunnlaget ikke støttet. T1 = uten kilde, T2 = med kilde (verifiser at kilden støtter rangeringen), prev = prevalens uten opphav.

**Omfanget måtte korrigeres for fjerde gang — men denne gangen i bokføringen, ikke detektoren.** `riesenschnauzer` var dobbelttalt. Git-historikken er nå autoritativ.

**Ordtellings-rådet mitt fra 30.07 var for bredt.** Wordcount-taket er æra-scopet: 25 av 29 restguider ligger på 3300–4800 ord og er alle pre-regel, altså uten tak å sprenge. Kun `jamthund` (+381), `whippet` (+280) og `west-highland-white-terrier` (+155) er skrevet under 2400–2800-regelen. **Trim-planlegging gjelder 3 guider, ikke 25.**

**C3c-1 levert samme dag.** Golden gikk fra T1=5 til 0/0/0; griffon fra T1=5 til én benign tilbake-referanse.
- **Golden-ingressen motsa guidens egen faktastripe** — femte forekomst av ingress-drift, men her var kilden allerede i fila («Norges mest registrerte rase 2024 (NKK)»). Feilen var ikke manglende kilde, men at ingressen aldri ble oppdatert.
- **Kildesetting endret konklusjonen, ikke bare fotnoten:** «kortere snittlevetid enn mange andre raser» viste seg overdrevet da McMillan et al. 2024 ga referansegruppen (median 12,7 år for renrasede mot guidens ~12).
- **Griffons selvmotsigelse lå løst i kilden.** NMHKs RAS sier både «ikke hos veterinæren oftere eller sjeldnere enn gjennomsnittshunden» **og** «likevel enkelte problemer de er spesielt utsatt for». Guiden hadde sitert første setning og droppet den andre. **Lærdom: når to påstander i samme guide utelukker hverandre, sjekk om begge stammer fra samme kilde.**
- **Øyeskade-påstanden kildesatt på anatomien, aldri på rasemerkelappen.** RAS' egen formulering («anatomien i hode- og øyeregionen påvirkes av mange gener») traff rammen bedre enn O'Neill alene.

**Kjent blindsone i detektoren:** popularitets- og registreringsrangeringer fanges ikke — domenegatingen krever helse- eller kryss-rase-kontekst. Golden-ingressen ble funnet manuelt. **Ikke utvid detektoren uten ny kalibrering.**

### 2026-07-30 — C3b-5 italiensk-mynde (`afbb344`) — C3a/C3b-runden FULLFØRT

**🔴 To feil i én setning om FEH.** «14 % av populasjonen klinisk rammet og 30 % bærere ifølge UC Davis VGL» → Gandolfi et al. 2013 sier 30 % av **hundene med normale tenner**, og begge tall er studiens, ikke VGLs. Sanity-testen som avslørte det: 14 % affisert gir ~47 % bærere under Hardy-Weinberg, ikke 30 % — tallene kunne ikke dele nevner. **Lærdom: når to tall fra samme studie står side om side, sjekk om de har samme referansegruppe før du leser dem som et par.**

**🔴 «Pedersen et al. (2013)» var en fantom-sitering — ny feilklasse.** Ikke en feil kilde, men én ekte studie splittet i to: funnet står i Gandolfi 2013, der Pedersen er fjerde forfatter. Medforfatteren hadde fått sin egen fiktive publikasjon et annet år. Består enhver formatsjekk, siden navn og årstall ser riktige ut hver for seg.

**🔴 Beinbrudd-tallet hvilte på n≈30 fra én privat klinikkblogg.** «25–45 % i løpet av livet» kom fra Walkerville Vet, som selv oppgir grunnlaget: 7 brudd blant ~30 hunder i egen pasientliste. Samme policyklasse som PetMD i C3b-1. Tallet ut; NMK RAS sin «relativt vanlig» inn. Kilden skjulte ikke svakheten — den sto i klartekst og var ikke lest.

**🔴 To påstander motsa primærkilden direkte.** Bruddmekanismen: guiden skrev «skjørt skjelett», RAS sier «lange tynne bein **med normal beintetthet**». Og «NMK RAS dokumenterer at mange italienere ligger over standardens 5 kg-tak» — søk på hele RAS gir null treff på `vekt`, `kilo`, `5 kg`, `høyde`. **Lærdom: «X dokumenterer at …» er en verifiserbar påstand om et dokument. Åpne det og søk.**

**🟢 Én flagget påstand hadde dekning likevel.** «Risikoen er høyest før 1,5 år» sto i et Walkerville-attribuert avsnitt, men NMK RAS sier det ordrett. Beholdt, kilde flyttet. En påstand i et avsnitt med dårlig kilde er ikke automatisk dårlig.

**🟡 Fargeregelen var AKCs i en FCI-rammet faktastripe**; whippet-målene kollapset et kjønnsstratifisert tall (FCI #162: hanner 47–51, tisper 44–47) og motsa vår egen whippet-guide. **`whippet` oppgir fortsatt bare hannspennet — eget oppfølgingspunkt.**

**Metodenotat — sirkulær bekreftelse nesten godtatt.** Søk på NMKs stiftelsesår ga vår egen side som toppresultat, med sammendrag ordrett fra guiden. **Regel: finnes en påstand bare i vår egen tekst i søkeresultatene, er den ubekreftet — ikke bekreftet.** Verifisert mot klubbens historieside i stedet.

**Ordtelling-lærdom for C3c.** Rettingene la på 174 ord (2794 → 2968) og krevde fem trimrunder for å lande på 2791. **En kildefiks er ikke ordnøytral — kildeforankring koster typisk 100–200 ord. Guider som allerede ligger på 2750+ må planlegge trim inn i selve fiksen.**

**Åpent Admin-steg:** meta sier «skjøre ben» — samme premiss brødteksten nå avviser. Ingen tallpåstand; blokkerte ikke pushen. Tas i neste Admin-runde.

### 2026-07-30 — C3b-4 samojedhund (`f74e411`) + FAQ↔schema-funn som ventende bolk

**🔴 FEH-forekomsten var et utvalgstall lest som rasefrekvens.** «1–2 % av samojeder er affisert» → Pedersen et al. 2017 sin egen rasedekkende beregning er ~3,6/1 000, altså **0,36 %** — guiden lå 3–6× over. Studiens 14 affiserte av 182 (7,8 %) er et utvalgstall fra familier rundt kjente tilfeller. Bærertallet 12 % stemte, men forfatternes forbehold om skjevt utvalg manglet. **Lærdom: i en genetikkstudie er andelen affiserte i utvalget nesten aldri rasefrekvensen — se etter forfatternes egen ekstrapolering.**

**🔴 Jansen 1987: siteringen eksakt, tallene forskjøvet.** Proteinuri 2–3 mnd (ikke 3–4); død av nyresvikt **innen** 15 mnd (ikke «mellom 8–16»). Studien oppgir et *tak*; guiden gjorde det til et *vindu* med en nedre grense studien ikke setter. Rettet i §8 og FAQ+schema.

**🟡 Pedersen-journalen bar dagens navn, ikke publiseringsnavnet** — «Companion Animal Health and Genetics» → *Canine Genetics and Epidemiology* 4:11. En sitering må bære navnet ved publisering. Allergen-rangeringen myket; «IKKE en hypoallergen rase» står uendret. ✅ Zheng 1994 og Catchpole 2013 rene.

## 🔴 VENTENDE BOLK — FAQ ↔ schema-avvik (opprinnelig 21 filer, **nå 19** — WHWT og boxer ryddet 31.07)

Oppdaget da strukturkontrollen slo ut på samojedhund. **21 av 118 filer har avvik mellom synlig FAQ og FAQPage JSON-LD; 17 med reelt innholdsavvik**, 4 kun tegnsetting. HARD-regelbrudd (`CLAUDE.md`, `.claude/rules/hundetips-articles.md`): Google leser noe annet i rikresultatet enn siden viser.

**Besluttet (Sondre): egen bolk ETTER at C3 er ferdig — ikke satt inn nå.** Prioritert: `valp` (8 avvik) og `tannhelse` (7 avvik, helseartikkel) øverst, deretter `hund-liker-ikke-bading` (4), `boxer` (3), `aktivisere-hund-pa-tur` + `sommer` (2 hver), så 11 filer med ett avvik. Full tabell i registeret.

**Metodenotat:** ville ikke blitt oppdaget av kildesettings-sporet — det dukket opp fordi strukturkontrollen kjøres uansett. Argument for å beholde de «trivielle» strukturelle sjekkene selv når fokus er kildeverifisering.

## 🏁 SLUTTSTATUS C3 — 2026-08-05: KILDEVERIFISERINGEN ER FERDIG, 42 AV 42

**C3c-21 levert** (commit `eaef8ef`, 6 filer live): `norsk-elghund-gra`, `dansk-svensk-gardshund`, `finsk-lapphund`, `jamthund`, `shetland-sheepdog` — kjørt som én bulk. **Med disse er hele C3-sporet ferdig: 42 av 42 raseguider kildeverifisert, rettet og live.** Regnskapet kontrollert begge veier: 37 + 5 = 42.

### Hva C3 endte med å være

Sporet startet som en jakt på rangeringsspråk og ukildet prevalens. Det ble noe annet. **Den dominerende funnklassen gjennom hele C3c var regulatoriske påstander — hva en klubb eller myndighet faktisk krever.** Mønsteret traff seks sprinter på rad til slutt, og feilen gikk nesten alltid i begge retninger samtidig: krav som ikke fantes ble oppgitt som bindende, mens klubbens ekte krav manglet.

**Detektoren fant ikke dette.** De fem siste guidene scoret alle 0/0/0, og hadde likevel to fabrikkerte NKK-krav, en retnings-invertering, et regelverk guiden lå bak, og en klubb som eksplisitt sier den ikke stiller krav. **Regel 24 er den mest bekreftede regelen i prosjektet: en lav detektorscore sier ingenting om filens kvalitet når risikoen ligger i regelverk, attribusjon eller aldrende forskning.**

### Den ene selvinnførte feilen

I C3c-20 konkluderte jeg med at sankt bernhardshund ikke har NKK-krav. Det var galt og sto live i noen timer (`025c55a` → rettet i `7088ad2`). Jeg leste oversiktssida, som eksplisitt sier at HD/AD- og DNA-listene ligger i egne dokumenter. **Regel 39: fravær er bare bevis når kilden er uttømmende for det du spør om.** Dette er den eneste selvinnførte faktafeilen i C3, og den eneste som har vært live.

### Regler etablert i C3 (24–39)

**24** detektorscore sier ingenting om kvalitet · **27** kildeforankring koster 3× prosa · **28** forskningsseksjoner eldes · **29** klubbens egen begrunnelse slår vår rekonstruksjon · **30** yrkestittel er en verifiserbar påstand om en levende person · **31** et sitat kan være ordrett riktig og feil tilskrevet · **32** å rette en rangering med en rangering er ingen fiks · **33** «loven forbyr X» er dyreste påstandsklasse · **34** adresser lesernes misforståelse, aldri vår egen tidligere ordlyd · **35** riktig sitert dokument beskytter ikke mot feil gjengitt innhold · **36** å gjøre oss strengere enn klubben er like galt som å gjøre oss slappere · **37** HD- og AD-aldersgrenser kan være ulike innen samme rase · **38** sidebar-widgeten er en fjerde speilingsflate · **39** fravær er bare bevis når kilden er uttømmende.

---

## 🔴 ALLE ÅPNE POSTER ETTER C3

### 1. ✅ Admin-steg bolk A — LUKKET 06.08.2026 (16 sider / 17 feltendringer)

Hele bunken utført av Friday og **live-verifisert 06.08: 17 av 17 felt matcher godkjent tekst ordrett.** `og:`/`twitter:`-variantene spot-sjekket på tre sider — innlimingsartefakten på `norsk-elghund-sort` er borte i alle tre.

Sju tekster ble strammet til under 160 tegn før utsending fordi de godkjente versjonene lå over Googles avkortingsgrense. Full historikk, sideliste og lærdom i `docs/health-claims-register.md`.

**Metodelærdom:** bunken ble bygget fra faktiske live-verdier, ikke fra notatene — det avdekket to statusfeil registeret ikke visste om (`norsk-elghund-sort` ført som utført uten å være det; `hund-om-sommeren` ført som åpen og lukket samtidig). **Å være sendt er ikke det samme som å være utført.** Status føres på live-kontroll, aldri på avsendelsen.

**✅ Hypoallergen-bolken LUKKET 06.08** — 4 sider, live-verifisert på alle tre taggvariantene (12 tagger). Startet som to sider (`coton-de-tulear`, `malteser`); korpussveipen Sondre bestilte utvidet den til fire ved å avdekke `pudel` og `lagotto-romagnolo`. **Sveipen viste det motsatte av mistanken:** ingen av de 10 raseguidene påstår at rasen er hypoallergen — alle tilbakeviser myten. Det var meta-feltene som motsa brødteksten, samme feilklasse som gotcha #20. Løst etter bichon-modellen («Er X hypoallergen? Nei — …»), med `pudel` på «Ikke garantert» fordi guiden er nyansert der. Detaljer i `docs/health-claims-register.md`.

**Gjenstår:** `irsk-setter` (blokkert på NKKs 2024-statistikk, skal endres samtidig med brødteksten) · valgfri brødtekst-harmonisering av hypoallergen-formuleringene mot NAAFs kategoriske linje (korrekt overalt i dag, men inkonsistent i styrke — 4 kategoriske mot 6 avdempede).

<details><summary>Opprinnelig oppføring (beholdt for sporbarhet)</summary>

### 1. Admin-steg — flate 3, kan ikke gjøres fra CLI (17 stk)

Godkjente tekster ligger i `docs/health-claims-register.md`. **Sendes samlet til Friday nå som sweepen er ferdig.**

| Gruppe | Antall | Saker |
|---|---|---|
| A-serien (innholdsfeil i meta) | 7 | `dvergpinscher` · `engelsk-springer-spaniel` · `jack-russell-terrier` · `shiba-inu` · `tibetansk-spaniel` · `mops` · `norsk-elghund-sort` (A7 — **sendt isolert 04.08, men IKKE utført**; live-kontroll 05.08 viser artefakten i begge felt. Ligger først i Friday-bunken) |
| B-serien (formuleringer) | 9 | `riesenschnauzer` · `irsk-setter` · `italiensk-mynde` · `hvor-mye-vann-hund` · `griffon-petit-brabancon` · `border-collie` · `whippet` · `mellomschnauzer` · `boxer` |
| Nytt fra C3c-20 | 1 | `sankt-bernhardshund` — meta bærer «51–80 kg», «8–10 år» og «NSBK + NKK-rammeverk» |

**C3c-21 genererte ingen nye.** Alle fem meta-descriptions ble lest og var rene.

**Presedens (Sondre 04.08):** alvorsklasse avgjør om et admin-steg kan vente, ikke hvilken bolk det tilhører.

</details>

### 1b. ✅ OPPRYDNINGEN FERDIG 06.08.2026 — sluttstatus

Alt som ble åpnet i denne runden er lukket. **Gjennomgående funn på tvers av alle fire bolkene: en flate ble rettet, en annen ble ikke sveipet.**

| Bolk | Omfang | Status |
|---|---|---|
| `article_map` H2-liste-drift | 19 oppføringer | ✅ live, sha256 == HEAD |
| Admin-steg bolk A | 16 sider / 17 felt | ✅ live-verifisert |
| Hypoallergen | 4 sider / 12 tagger | ✅ live-verifisert |
| Statusopprydning i registeret | 6 stale markører | ✅ ryddet |

**De tre utslagene av samme rot:**
1. `article_map` bar tilbaketrukne påstander fra ni rettelseskommiter — deriblant et sikkerhetstall (`5-` mot `7-sekunder-regelen`) og et `beroligende`-claim fjernet for markedsføringsloven §§6-8. `4bd8496` navnga eksplisitt flatene sine («11 occurrences across 4 articles + TOC + JS anchor») og traff `article_map` på ingen av dem.
2. Meta-feltene bar fire påstander brødteksten aktivt avviser (hypoallergen-bolken). To av dem var ikke mistenkt før korpussveipen.
3. `norsk-elghund-sort` ble ført som utført fordi statusen ble satt på **avsendelsen**, ikke på en live-kontroll — og sto slik i to døgn mens feilen var synlig i Google.

**Tre permanente mekanismer etablert:**
- **Gotcha #20** (`docs/gotchas.md`) — `article_map` som usynlig flate i rettelsessveip, med begge kalibreringsfellene dokumentert (semikolon-sanitering = 100 falske positive; «fila har flere H2» er spec-konformt).
- **Trigger E** (`.claude/rules/llms-txt.md`) — rettelsessveip må inkludere `article_map` i samme commit. Med verbatim-port, testet med positiv og negativ kontroll.
- **Port 8** (`docs/artikkel-sjekkliste.md`) — endrer en retting en påstand, hentes sidens live-meta og verifiseres. Gjelder enhver påstand, ikke bare tall. Koblet inn i `CLAUDE.md` Phase 3 og `.claude/rules/hundetips-articles.md`.

Port 8 dekker hullet de to andre ikke kan: meta ligger utenfor repoet, så ingen commit-hook, `grep` eller fil-sjekk fanger den.

**Arbeidsprinsippet som avdekket det meste:** hent gammel verdi fra **live**, ikke fra notatene. Det var det som fant begge statusfeilene og utvidet hypoallergen-bolken fra to til fire sider.

**Gjenstår:** `irsk-setter` (blokkert på NKKs 2024-statistikk) · valgfri brødtekst-harmonisering av hypoallergen-formuleringene mot NAAFs kategoriske linje.

### 2. Ventende korpus-bolker — status 2026-08-05 ettermiddag

**✅ LIVE 05.08.2026 — fire bolker lukket samme dag:** Bolk 5 (NKK-krav, 22 guider), Bolk 1 del A+B (FAQ↔schema, 11 filer), CalmBall-schema, TOC-gap (56 lenker, 48 filer) og semikolon-bolken (3 043 konverteringer, 14 filer). Commits `724c4d0`, `91ba4a0`, `b808c23`, `70b8851`. sha256 live == HEAD på 29 + 48 filer. 28 URLer sendt til GSC. Detaljert funnliste i `docs/health-claims-register.md`.

**Deploy-lærdom (gotcha #18, alvorlig).** Første push av Bolk 5 lastet opp **null filer** og meldte likevel suksess: skallet er zsh, som ikke ordsplitter `$FILES`, så `--only $FILES` ble ett argument som ikke matchet noe. Fanget først av sha256-etterkontroll mot live. **Suksessmeldingen fra Shopify CLI er ikke bevis på at noe ble lastet opp** — sha256 live == HEAD er den eneste gyldige kvitteringen. Bruk array i eksplisitt bash.

**Gotcha #19:** Shopifys page_cache holdt rendret side i over 20 minutter etter bekreftet deploy. Verken cache-buster-param, `_fd=0`, `preview_theme_id` på live-tema eller myshopify-domenet omgår den. Rendret-innhold-sjekk er derfor ikke et porttrinn rett etter push. Cachen roterer per side — 15 av 22 var ferske innen en time.

- **Bolk 5 vokste fra 2 til 22 guider** etter full kryss-sjekk av alle 60 raseguider mot NKKs tre kravdokumenter. Fire retningsinverteringer (`cane-corso`, `rottweiler`, `greyhound`, `australian-shepherd`) der guiden både oppga krav som ikke finnes og utelot dem som gjelder. To selvkomponerte kravlister (`italiensk-mynde`, `weimaraner`). 16 med manglende krav.
- **Bolk 1 var 6 filer, ikke 19** — det gamle tallet slo sammen tre kategorier. 27 tekstavvik rettet; 14 filer avskrevet som ikke-defekter (`<a>`-lenke i synlig svar, prosa identisk). Nytt funn: `product-calmball` hadde 8 synlige FAQ og null schema — bygget.
- **Ordtellings-detektoren i `.claude/rules/raseguide-canonical.md` var ødelagt** og er fikset. `<article>` er nøstet i flere filer; både `re.search` og `findall` bommet. Alle ordtellinger fra før 05.08.2026 er systematisk feil — `jamthund` ble rapportert 2572 i C3c-21, reelt 2657 (2819 etter Bolk 5-tillegget).

| # | Bolk | Omfang | Alvorlighet |
|---|---|---|---|
| 1 | ~~FAQ ↔ schema-avvik~~ | ~~19 filer~~ → **6 reelle, alle rettet 05.08** | ✅ Lukket. Kategori B (5 filer tegnsetting) flyttet til semikolon-bolken |
| 5 | ~~NKK-krav endret~~ | ~~2 guider~~ → **22 guider, alle rettet 05.08** | ✅ Lukket |
| 2 | ~~Semikolon-bolken~~ | **3 043 konvertert i 14 filer — live 05.08** | ✅ Lukket. Reelt tall var 3 102 i brødtekst, ikke 2 835. 4 415 semikolon i CSS/JS/entiteter urørt. 87 beholdt som kilde-intern konvensjon |
| 3 | ~~TOC-gap-bolken~~ | **56 lenker på 48 filer — live 05.08** | ✅ Lukket. Etterspill: tre guider manglet `<h2>` over FAQ, så `#faq` landet på «Anbefalt for X»; og `hvor-mye-vann` hadde off-by-one der 8 av 9 lenker traff feil overskrift. Begge rettet samme dag |
| 4 | **Dobbel BreadcrumbList** | Trolig alle raseguider med både inline schema og `mh-article-schema` | 🟡 Duplikat strukturert data; begge parser rent |
| 5 | **NKK-krav endret siden siste retting** | `pomeranian` mangler patellakrav fra 01.07.2025; `bichon-havanais` utelater trolig NKK-registreringskravet fra 01.04.2016 og har en uverifisert avkomsgrense fra 01.01.2026 | 🔴 Gjeldende regelverk mangler i live guider |
| 6 | **Gonioskopi-motsigelsen** | 4 filer: `engelsk-springer-spaniel` (krav) · `flat-coated-retriever` («standard») · `sibirsk-husky` («liten gruppe … sammen med Shiba Inu») · `shiba-inu` (anbefaling) | 🟡 Guidene rangerer utbredelsen ulikt og siterer hverandre |
| 7 | **Raseguider-hub description-drift** | 21 døde `description`-felt i `templates/page.raseguider.json` | 🟢 Ingen live-effekt — feltet rendres aldri |

**✅ Bolk 8 — `article_map`-ordtellingsdrift LUKKET 05.08.** 82 oppføringer rettet mot registerets terskel på 100 ord; gjenværende drift er 0. 43 193 ord manglet totalt, snitt +526. Alle 121 oppføringer er nå målbare — de fire «umappede» skyldtes handle ≠ template-navn, ikke drift. Historikk: Alle 73 er **positive** avvik — `article_map` undertelder systematisk. Den gamle målingen ga 42 avvik hvorav 11 negative; **alle de negative var måleartefakter** fra den ødelagte `<article>`-regexen (`reise-til-utlandet-med-hund` målte 409 ord, reelt 2468). Verste reelle: `chihuahua` +2081, `hund-sover-mye` +1686, `cane-corso` +1552. 🟡 Degraderer verdien av `/llms.txt` for AI-crawlere. **Merk:** Bolk 5-rettelsene la 32–178 ord på 22 guider — under Trigger B-terskelen på 20 %, så de utløser ikke i seg selv `article_map`-oppdatering, men de inngår i tallene over.

**✅ Bolk 9 — `article_map` H2-liste-drift LUKKET 05.08.** 19 oppføringer synket mot seksjonsfil (commit `ad28542` + `pointer`-tillegg, begge live, sha256 live == HEAD).

**Hovedfunnet var ikke at listene hadde blitt gamle — det var at `article_map` er en usynlig flate i rettelsessveip.** Ni av avvikene stammer fra rettelseskommiter: seksjonsfila ble korrigert, `article_map` ble aldri synket, og `/llms.txt` fortsatte å servere nøyaktig de påstandene rettingen fjernet. Blant dem et sikkerhetstall (`5-` mot faktisk `7-sekunder-regelen`), sykdomsrangeringen C3c-7 snudde tilbake på `chihuahua`, typedelingen C3c-8 slo fast ikke finnes i Norge på `engelsk-setter`, feil produkt-form-factor (`Slikkematte` mot `Slikkeball` — og `slikkematte-hund` er et *annet* produkt), og et `beroligende`-claim fjernet for markedsføringsloven §§6-8. Skarpeste illustrasjon: `4bd8496` navnga eksplisitt flatene sine («11 occurrences across 4 articles + TOC + JS anchor») — `article_map` sto ikke på lista og overlevde i to av dem. Ny **Trigger E** i `.claude/rules/llms-txt.md` + gotcha #20.

**To kalibreringsfeller dokumentert:** (1) 100 H2 med `;` der fila har `,` er *påkrevd* sanitering, ikke drift — verbatim-krav ville gitt 100 falske positive; (2) «fila har flere H2 enn lista» er spec-konformt (4–8 representative) — 10 oppføringer på nøyaktig 8 er ikke defekter. Detektoren ble kalibrert mot tre kjente tilfeller før omfanget ble festet; `berner-sennenhund` falt ut fordi gårsdagens FAQ-H2-fiks allerede hadde lukket den.

**`pointer` ble tatt som nr. 19** utover de 18 godkjente: to tankestrek-vs-kolon-avvik jeg først klassifiserte som kosmetiske. De måtte rettes fordi verifiseringsporten i Trigger E ellers aldri ville lest 0 — **en sjekk som alltid rapporterer avvik blir ignorert.**

### 3. Åpne enkeltsaker (3)

- **Div-strukturavvik i `pointer`:** 2 body-divs mot 12 H2 der canonical krever én per H2. Ingen forbudte Cocker-markører. Ikke rørt.
- **Språk-default i Shopify Admin:** butikkens default locale er fortsatt engelsk. Manuelt steg — flipp default til Norsk (Bokmål) **først**, deretter unpublish English. Rekkefølgen er kritisk.
- **`jamthund` meta-description:** nevner ikke det nye gradskravet fra 01.04.2026. Ikke feil, derfor ikke logget som admin-steg — men kan oppdateres hvis ønskelig.

### 4. Neste fase

C3 er lukket. Naturlige kandidater i prioritert rekkefølge: **bolk 1 (FAQ↔schema, 19 filer — eneste røde av de mekaniske)**, deretter **bolk 5 (NKK-krav endret — også rødt, og samme feilklasse som dominerte C3c)**, så de gule mekaniske bolkene. Rekkefølge ikke fastsatt av Sondre.

---

## FULL STATUS 2026-08-05 — C3c-20 levert, 3,0-gruppen tømt

**C3c-20 `sankt-bernhardshund` fullført** (commit `025c55a`, 2 filer live). 19 funn godkjent samlet av Sondre, alle rettet. **C3 står nå på 37 av 42; fem gjenstår** — hele 0,0-stikkprøvegruppen.

**Detektor T1=1 / T2=0 / prev=0 — regel 24 holder ellevte sprint på rad.**

### Tyngste funn

**Klubbkrav-mønsteret traff for femte sprint på rad, med en ny vri.** Guiden oppga NKK-krav som ikke finnes (rasen står ikke på NKKs kravliste i det hele tatt), utelot NSBKs to faktiske krav, og — det nye — **satte en oppdiktet terskel som var STRENGERE enn klubbens egen**. «HD-grad A eller B» utestengte C- og D-hunder NSBK godkjenner for avl. Pointer, pudel og springer diktet opp krav der ingen fantes; her ble en ekte klubbregel overskrevet med en hardere.

**FCI #62 var en annen rase.** Sto 8 steder som «langhåret variant» — er Steirische Rauhhaarbracke, en østerriksk bracke på 45–53 cm. Og standarden hadde ingen vekt: femte FCI-standard på rad uten vektangivelse.

**Osteosarkom: riktig studie, rase som aldri var med.** Edmunds et al. 2021 gjennomsøkt i fulltekst — null treff på «St Bernard», mens Rottweiler-kontrollen slår ut.

### Nye regler etablert

**36 (C3c-20): å gjøre oss strengere enn klubben er like galt som å gjøre oss slappere.** Begge feilretninger feilinformerer valpekjøperen om hva et lovlig avlsdyr er. Sjekk alltid terskelen mot klubbens ordlyd, ikke bare om et krav finnes.
**37 (C3c-20): aldersgrenser for HD og AD kan være ulike innenfor samme rase.** Sankt bernhardshund har HD fra 18 mnd og AD fra 12. «Samtidig med HD-røntgen» er en påstand som må verifiseres per rase, ikke antas.
**38 (C3c-20): sidebar-widgeten er en fjerde speilingsflate.** Tre av funnene overlevde i «Tips fra King»-sidebaren etter at brødteksten var ren. Speilingslisten er nå: ingress → faktastripe → recap → FAQ+schema → **sidebar-widget** → kildedisclaimer → meta.

### 🔴 Selvinnført feil i C3c-20 — oppdaget og rettet samme dag (`7088ad2`)

I C3c-20 konkluderte jeg med at sankt bernhardshund **ikke** har NKK-registreringskrav. Det var galt, og det sto live i noen timer. Den opprinnelige guiden hadde rett; jeg gjorde en riktig påstand feil.

**Årsak:** jeg sjekket kun oversiktssida for «Raser med krav for registrering». Den enumererer øyelysing og patella inline, men sier eksplisitt at HD/AD- og DNA-listene ligger i egne dokumenter. Jeg trakk konklusjon fra fravær på en side som selv opplyser at listen står et annet sted.

**Fasit** (NKKs HD/AD-dokument, ajourført 05.01.2026): «Sankt bernhardshund fra 01.01.87» (HD) og «Sankt Bernhardshund fra 01.01.06» (AD).

**Hvorfor kontrollen ikke fanget det:** den positive kontrollen slo ut — mops, springer og rottweiler sto på sida. Men de står der for øyelysing/patella, ikke HD/AD. **Positiv kontroll må kalibreres mot samme kravtype som konklusjonen gjelder, ikke bare mot «finnes det rasenavn på sida».**

**Ny regel 39:** *fravær er bare bevis når kilden er uttømmende for det du spør om.* Sjekk alltid om dokumentet selv sier at listen ligger et annet sted. Regelen er skrevet inn i `docs/artikkel-sjekkliste.md` seksjon A med de tre dokumentene som må hentes.

Dette er første selvinnførte faktafeil i C3-sporet, og den eneste som har vært live. Alt annet i C3c-20 står uendret.

### Åpne saker

**17 admin-steg** venter (16 + `sankt-bernhardshund`). Godkjent tekst ligger i registeret.

### Neste økt — BULK, ikke én om gangen

**De fem siste C3-guidene kjøres samlet** etter Sondres beslutning 05.08: `norsk-elghund-gra`, `dansk-svensk-gardshund`, `finsk-lapphund`, `jamthund`, `shetland-sheepdog`. Kartlegg alle fem → rapporter alle fem funnlistene samlet → én godkjenning → skriv/preview/verifiser alle fem → én samlet live-push. **Unntak: viser én av dem seg vesentlig tyngre enn resten, tas den separat.** Ordtak gjelder kun `jamthund` (2419 ord).

---

## FULL STATUS 2026-08-04 kveld — økta i sammendrag

**Levert i denne økta: C3c-17, C3c-18 og C3c-19.** Tre guider kildeverifisert, rettet, verifisert mot preview og live, og deployet med docs og mirror-synk. **C3 sto etter denne økta på 36 av 42.** (Oppdatert 05.08: 37 av 42 etter C3c-20.)

| Sprint | Guide | Commit | Tyngste funn |
|---|---|---|---|
| C3c-17 | `norsk-elghund-sort` (+ `norsk-elghund-gra`) | `738f3b6` | «Eneste kritisk truede norske rase» · oppdretter gjort til NMBU-forsker · §9 fire år bak forskningen (LTV 5–10 % mot Bergs 28,6 %) |
| C3c-18 | `pointer` | `45d433e` | NPKs avlskrav oppdiktet i én ende og utelatt i den andre · fire «rasestandard»-sitater fra rasebeskrivelsen · AMS-genet var menneskets |
| C3c-19 | `pudel` | `b1a8299` | Oppdiktet lovforbud om vibrisser · Combination Poodle aldri et NPK-krav · FCI-standard sitert riktig og gjengitt feil |

**Detektorscore i alle tre: T1=1, T2=0, prev=0.** I to av tre var treffet guidens eget forbehold eller en enkeltstående multiplikator. **Regel 24 har nå holdt ti sprinter på rad: en lav detektorscore sier ingenting om filens kvalitet når risikoen ligger i regelverk, attribusjon eller aldrende forskning.**

### Mønsteret som går igjen

Tre av tre sprinter hadde **feil om hva en klubb eller myndighet faktisk krever** — og i alle tre gikk feilen i begge retninger samtidig: krav som ikke finnes ble oppgitt som bindende, mens de ekte kravene manglet. Pointer krevde tre «ufravikelige» DNA-tester klubben ikke ber om, og utelot 20 jaktprøvestarter og AK-premiering. Pudel gjorde et kommersielt panel til inngangsbillett, og utelot øyelysing — klubbens mest universelle krav. Norsk elghund sort gjorde en klubbanbefaling om HD-indeks til et krav, og snudde retningen på hva indeksen kvalifiserer til.

**Attribusjonsfeil er funnklasse i alle tre:** feil yrkestittel på en navngitt privatperson (Nygaard), feil kildedokument for fire ordrette sitater (pointer), og en lov som ikke sier det den tilskrives (pudel).

**Port 7 er snudd.** FCI 125, 257, 242, 1 og 172 oppgir ingen vekt — fire av dem har overskrifter som lover det. **Fravær er nå default-antakelsen; tilstedeværelse må verifiseres.**

**Ordbudsjettet bommet alle tre gangene** (+742, +659, +827 mot anslag). Regel 27 holder likevel presist: seksjoner som får ny kildeblokk koster 3×, seksjoner uten flytter seg null. Anslagene er for lave, ikke modellen.

### Nye regler etablert i økta

**28–30** (C3c-17): forskningsseksjoner eldes · klubbens egen begrunnelse slår vår rekonstruksjon · yrkestittel er en verifiserbar påstand om en levende person.
**31–32** (C3c-18): et sitat kan være ordrett riktig og feil tilskrevet · å rette en rangering med en annen rangering er ingen fiks.
**33–35** (C3c-19): «loven forbyr X» er den dyreste påstandsklassen · riktig sitert dokument beskytter ikke mot feil gjengitt innhold · adresser lesernes misforståelse, aldri vår egen tidligere ordlyd.

### Åpne saker ved øktas slutt

- **✅ Alle 17 admin-steg utført og live-verifisert 06.08** (16 sider; `norsk-elghund-sort` hadde to felt). Bunken ble sendt samlet til Friday 06.08 og kontrollert mot live etterpå — 17/17 ordrett match. `irsk-setter` og hypoallergen-paret (`coton-de-tulear`, `malteser`) står fortsatt utenfor, se punkt 1. Pointer og pudel trengte ingen nye.
- **Fire ventende korpus-bolker:** FAQ↔schema (19 filer) · semikolon (14 filer) · TOC-gap (nå ~53 filer etter at tre er ryddet) · **ny: `article_map`-ordtellingsdrift**, oppdaget i C3c-17 der `norsk-elghund-gra` lå 1 004 ord feil. Korpuset er ikke sveipet.
- **Div-strukturavvik i `pointer`:** 2 body-divs mot 12 H2 der canonical krever én per H2. Ingen forbudte Cocker-markører. Egen sak, ikke rørt.
- **Gonioskopi-motsigelsen** (4 filer) og **dobbel BreadcrumbList** står uendret.

### Neste økt

**C3c-20 `sankt-bernhardshund`** — siste i 3,0-gruppen. Deretter gjenstår kun stikkprøve-gruppen på fem null-treff-guider: `dansk-svensk-gardshund`, `finsk-lapphund`, `jamthund`, `norsk-elghund-gra` og `shetland-sheepdog`. **Merk at `norsk-elghund-gra` fikk en liten kontrollert vektfiks i C3c-17, men er ikke kildeverifisert** — den står fortsatt som full stikkprøve. Ordtak gjelder kun `jamthund` (2419 ord).

Første steg for sankt-bernhardshund, gitt mønsteret over: slå opp rasen i NKKs «Raser med krav for registrering» **og** i NKKs DNA-dokument, og finn klubbens gjeldende avlskrav med vedtaksdato, før noe annet.

## STATUS PER 2026-07-31 — hvor prosjektet står

**Ferdig 30.07:** C1b, C2b, C3a (6 guider), C3b-0 → C3b-5. **Ferdig 31.07:** C3c åpnet med nytt verktøy, og seks bolker levert — C3c-1 (golden-retriever + griffon), C3c-2 (cavalier + bichon-havanais + border-collie), C3c-3 (WHWT + whippet), C3c-4 (mellomschnauzer), C3c-5 (beagle), C3c-6 (boxer). **Ferdig 03.08:** C3c-7 (chihuahua), C3c-8 (engelsk-setter), C3c-9 (fransk-bulldog), C3c-10 (staffordshire-bull-terrier) og C3c-11 (dvergpinscher). **Ferdig 04.08:** C3c-12 (engelsk-springer-spaniel), C3c-13 (jack-russell-terrier), C3c-14 (shiba-inu), C3c-15 (tibetansk-spaniel), C3c-16 (mops), C3c-17 (norsk-elghund-sort), C3c-18 (pointer) og C3c-19 (pudel). **42 av C3s 42 guider er kildeverifisert og live** — sporet lukket 05.08 med C3c-21-bulken, alle med retry-verifisering, GSC-innsending, commit og docs-synk.

**Utenfor kildesporet i dag:** `b413927` «feat(seo): Product-schema utvidet + Organization konsolidert + dobbel H1 fjernet» — Organization-schema i `layout/theme.liquid` anriket med `@id`, `legalName` (Uleberg Appdrift), organisasjonsnummer 935457017 og `sameAs`. Gjort i egen fane, committet separat fra italiensk-mynde. Dukket opp som drift i arbeidstreet under C3b-5-verifiseringen fordi live lå foran repoet; ikke reversert.

### NESTE ØKT STARTER HER — C3c-21: bulk av de fem siste (0,0-gruppen)

**Regnskapet i C3: 37 av 42 ferdig, 5 gjenstår** (per 05.08, etter sankt-bernhardshund). Git-historikken er autoritativ. Kontrollert begge veier: 36 + 6 = 42.

**De 6 som gjenstår, i godkjent rekkefølge:**

| Gruppe | Guider | Merknad |
|---|---|---|
| 3,0 | ✅ TØMT | `mops`, `norsk-elghund-sort`, `pointer`, `pudel` og `sankt-bernhardshund` er alle ferdige |
| 0,0 — stikkprøve til slutt (5) | `dansk-svensk-gardshund` · `finsk-lapphund` · `jamthund` · `norsk-elghund-gra` · `shetland-sheepdog` | Null detektortreff; tas som kontroll av om detektorens nullpunkt er reelt |

**Ordtak gjelder kun `jamthund`** (2419 ord, +381 slakk). De øvrige fem er pre-regel-guider uten tak.

**Hva de fem siste sprintene sier du bør se etter:**
- **Krav vs. anbefaling er nå funnklassen i fem sprinter på rad** — SBT, dvergpinscher, engelsk-springer-spaniel, jack-russell-terrier, tibetansk-spaniel og mops. Skriv alltid ut kravhierarkiet i nivåer: NKK-registreringskrav → raseklubbens tilleggskrav → vår egen anbefaling.
- **Slå opp rasen i NKKs «Raser med krav for registrering» som fast første steg.** Fire av de siste seks guidene hadde feil her: feil dato, feil utsteder, oppdiktet krav eller manglende krav.
- **Levetid mot RAS er nytt fast sjekkpunkt** — to sprinter på rad lå guidens levetid over raseklubbens eget dokument (shiba 12–15 mot RAS-snitt 9,23; tibetansk spaniel 14–16 mot RAS 12–15).
- **Sirkulær bekreftelse traff to ganger i denne bolken** (shiba-forslaget, mops-sitatet). Når et søk «bekrefter» en påstand, sjekk om treffet er vår egen side før du konkluderer.
- **Port 7: anta at vekt IKKE står i standarden.** FCI 125, 257, 242 og 1 oppgir ingen vekt — og 257, 242 og 1 har alle overskrifter som lover det. Kun FCI 231 oppgir begge deler. **Fire av fem siste standarder manglet vekt. Fravær er nå default-antakelsen; det er tilstedeværelse som må verifiseres.**
- **Sjekk om guidens forskningsseksjon har eldet.** Sier den siterte RAS-en «det pågår forsknings-studie», er det et utløpsstempel (regel 28). `norsk-elghund-sort` lå fire år bak: forekomst underrapportert med faktor tre, klinisk betydning og arvegang presentert som uavklarte etter publisering.
- **Attribusjonsfeil er funnklassen tre sprinter på rad** — feil fornavn (mops/Sjølie), feil yrkestittel (elghund sort/Nygaard), feil kildedokument (pointer/rasestandard vs rasebeskrivelse). Sjekk bylinen OG hvilket dokument sitatet står i (regel 30 og 31).
- **«Klubben krever X» er to spørsmål, ikke ett:** krever klubben det, og finnes testen for rasen? `pointer` krevde DNA-test for chondrodysplasi som «ufravikelig» — klubben krever den ikke, og den validerte testen gjelder norsk elghund grå og karelsk bjørnhund, ikke pointer. `pudel` gjorde et kommersielt DNA-panel til inngangsbilletten til klubbens valpeliste; kun én av panelets fem tester er faktisk krav.
- **Sjekk om klubben har vedtatt nye krav siden guiden sist ble rørt.** NPK strammet inn på generalforsamlingen 12.05.2024, NEKF/AUNES i 2023–24, NPK (pointer) justerer kvartalsvis. **Fire av de siste seks guidene lå bak klubbens gjeldende regelverk.** Sammenlign vedtaksdato mot guidens `last_updated`.
- **Let etter kravet som ikke er en test.** Øyelysing hos `pudel` er NPKs mest universelle krav og manglet helt, fordi guiden tenkte i gentester. Utstillingskrav, aldersgrenser, innavlsgrenser og medlemskapskrav er lette å overse av samme grunn.
- **`article_map`-ordtellingen har drift.** `norsk-elghund-gra` lå 1 004 ord feil. Sjekk oppføringen mot fila når du uansett er inne — og vurder en korpus-sveip som egen mekanisk bolk.

---

## 🔴 SAMLEDE ADMIN-STEG — flate 3, kan ikke gjøres fra CLI

**Status: samlet og ventende. Sendes til Friday først når hele sweepen er ferdig** — ikke fortløpende. Alle tekster under er godkjent av Sondre og klare til innliming i Shopify Admin → Online Store → Pages → `<handle>` → Search engine listing.

### Fra denne bolken (C3c-11 → C3c-16), alle godkjent 03.–04.08

| # | Side | Hvorfor | Godkjent tekst |
|---|---|---|---|
| A1 | `dvergpinscher` | Fremhever «hackney-trav» — påstanden som ble rettet som en standard-FEIL. Også «importerte første» (flertall) mot NPKs «en dvergpinscher fra England» | Dvergpinscher raseguide — median levealder 13,7 år, MPS VI og ARSB-gentest (Raj 2020), og Norsk Pinscherklubbs faktiske avlskrav: patella 0/0 og gyldig øyelysning. |
| A2 | `engelsk-springer-spaniel` | 3 forekomster av «DNA-test-quartet» (rasen har fem offisielle KC-ordninger; det norske kravet er gonioskopi) og «fra 1885 til Fant 1992» (1893-separasjonen strøket som anakronisme) | Engelsk Springer Spaniel raseguide — Norsk Spaniel Klubs gonioskopi-krav, fem offisielle DNA-testordninger, og tallene fra Reisner et al. 2005 om eierrettet aggresjon i rasen. |
| A3 | `jack-russell-terrier` | «PLL- og SCA-gentester» — samme undertelling som ble rettet i brødteksten; LOA mangler, og RG Jacks avlskriterier er ikke nevnt | Alt om Jack Russell Terrier: forskjellen til Parson Russell, NKKs patellakrav og RG Jacks strengere avlskriterier, DNA-testene PLL, SCA og LOA, og hverdagsliv. Ærlig norsk raseguide. |
| A4 | `shiba-inu` | Sier «det norske helsekrav-**forslaget** fra Japansk Urhundklubb» — nettopp rammen som ble rettet | Japansk primitiv urhund med 2500 års arv. Glaukom og gonioskopi forklart — hva som faktisk er avlskrav i Norge, og hva som bare er klubbanbefaling. |
| A5 | `tibetansk-spaniel` | Blander de to kravnivåene («NKK-krav fra 2014, og Norsk Miniatyrhund Klubbs avlsregler») | Tibetansk klosterhund med over 1000 års historikk. NKKs øyelysningskrav fra 2014 forklart — og hvor Norsk Miniatyrhund Klubbs egne avlskrav går lenger. |
| A6 | `mops` | Sier «NKKs BOAS-screening» uten dato, og «Norges mest omdiskuterte rase» — kravdatoene mangler helt | Alt om mops: NKKs tre registreringskrav (patella 2020, BOAS og øyelysning 2023), hva BOAS-graderingen faktisk måler, helseutfordringer og hverdagsliv. Ærlig norsk raseguide. |

### Fra tidligere bolker — fortsatt åpne (godkjent 31.07)

| # | Side | Hvorfor | Skal til |
|---|---|---|---|
| B1 | `riesenschnauzer` | «6× risiko» tilskrevet Bianchi 2020 — er Egenvall et al. 2000 | Egenvall-attribusjon |
| B2 | `irsk-setter` | «NKK #14» | Endres samtidig med brødteksten når NKK-tallet foreligger |
| B3 | `italiensk-mynde` | «skjøre ben» — premisset brødteksten nå avviser (NMK RAS: normal beintetthet) | Omformulering uten «skjøre» |
| B4 | `hvor-mye-vann-hund` | Bindestrek «40-60» der korpuset bruker tankestrek | Kosmetisk |
| B5 | `griffon-petit-brabancon` | «brachy-hensyn» på siden som ER Petit Brabançon-guiden — i strid med prosjektregelen | «kort snute-hensyn» |
| B6 | `border-collie` | «2. mest populære rase 2024» i alle tre meta-variantene | «2. mest registrerte rase 2024» |
| B7 | `whippet` | «raskeste hund per kilo» — rangeringen som ble myket i brødteksten | «en av de raskeste hunderasene i forhold til størrelse» |
| B8 | `mellomschnauzer` | «pulmonisk stenose rasespesifikk hjertedefekt, levetid 13-16 år» — begge avvist i brødteksten | Mellomschnauzer raseguide — den originale schnauzer-stamfar-rasen, NSBK 1946, RBM20-DCM med DNA-test, median levetid 13 år. |
| B9 | `boxer` | «NKK-avlsregler» — reglene er Norsk Boxerklubbs | «… og Norsk Boxerklubbs avlskrav.» |

| A7 | `norsk-elghund-sort` | **SENDT ISOLERT 04.08 — men IKKE UTFØRT.** Live-kontroll 05.08 viser artefakten i begge felt; ligger nå først i den samlede Friday-bunken. Feltnavnet er limt inn i selve feltet: `<title>` = «Page title: …» og alle tre description-taggene = «Meta description: …». Synlig i Google nå. Kontrollert mot mops, tibetansk-spaniel, norsk-elghund-gra og pointer — alle rene, altså isolert til denne siden | Page title: `Norsk Elghund Sort — komplett raseguide \| Min Hund` · Meta: `Norsk Elghund Sort — kritisk truet nasjonalrase og bandhund-spesialist. NKKs gentestkrav fra 2024, HD-indeks og hva forskningen sier om overgangsvirvel.` |

**Sum: 17 åpne admin-steg** (7 nye fra denne bolken + 9 fra tidligere). `staffordshire-bull-terrier` (C3c-10) trengte ingen — feltet var rent.

**Unntak fra samle-regelen (Sondre 04.08):** A7 sendes til Friday **isolert og umiddelbart**, ikke i bunken. Begrunnelse: de øvrige 15 er formuleringer som er feil men troverdige og venter internt uten skade; A7 er et innlimingsartefakt som er synlig i søkeresultatet akkurat nå. **Presedens: alvorsklasse avgjør om et admin-steg kan vente, ikke hvilken bolk det tilhører.**

---

## 🟠 VENTENDE KORPUS-BOLKER — alle logget, ingen påbegynt

Disse er bevisst holdt utenfor C3c-sprintene for ikke å blande sammen kildeverifisering med opprydding. Rekkefølge ikke fastsatt.

| # | Bolk | Omfang | Alvorlighet | Oppdaget |
|---|---|---|---|---|
| 1 | **FAQ ↔ schema-avvik** | 19 filer (opprinnelig 21; WHWT og boxer ryddet underveis) | 🔴 HARD-regelbrudd — Google leser noe annet i rikresultatet enn siden viser. Prioritet: `valp` (8 avvik) og `tannhelse` (7, helseartikkel) | 30.07 |
| 2 | **Semikolon-bolken** | 14 filer, 2 835 semikolon mot 3–20 komma | 🟡 Lesbarhet. Årsak: `article_map`-kommaregelen feilaktig anvendt på brødtekst. `mellomschnauzer` er nå blandet etter delvis rydding i C3c-4 | 31.07 |
| 3 | **TOC-gap-bolken** | 55 manglende ankerlenker; `faq` i 43 filer, `faq-heading` i 4, `tips-king` i 4, `oppsummering` i 3, `historie` i 3 | 🟡 Seksjoner unåbare fra innholdsfortegnelsen. Rent mekanisk. Omfatter `jack-russell-terrier` (anchors 13 mot 12 H2) | 31.07 |
| 4 | **Dobbel BreadcrumbList** | Sannsynligvis alle raseguider med både inline breadcrumb-schema og `mh-article-schema` | 🟡 Duplikat strukturert data; begge parser rent, så ingen automatisk sjekk slår ut | 03.08 (C3c-10) |
| 5 | **NKK-krav endret siden siste retting** | `pomeranian` mangler patellakrav fra 01.07.2025 helt. `bichon-havanais` beskriver klubbens 0/0-krav, men ser ut til å utelate NKK-registreringskravet fra 01.04.2016 — og har en avkomsgrense fra 01.01.2026 som ikke er verifisert | 🔴 Gjeldende regelverk mangler i live guider. Regel: sammenlign ikrafttredelsesdato mot guidens siste fikse-dato | 04.08 (C3c-13) |
| 6 | **Gonioskopi-motsigelsen** | 4 filer: `engelsk-springer-spaniel` (krav), `flat-coated-retriever` («standard»), `sibirsk-husky` («liten gruppe … sammen med Shiba Inu»), `shiba-inu` (anbefaling) | 🟡 Guidene rangerer utbredelsen ulikt og siterer hverandre. Krever faktisk opptelling mot NKKs raseklubb-oversikt før harmonisering i én commit | 04.08 (C3c-14) |
| 7 | **Raseguider-hub description-drift** | 21 døde `description`-felt i `templates/page.raseguider.json` | 🟢 Ingen live-effekt — feltet rendres aldri (`article_card`-grenen har null referanser). Reelt valg: fjern de 21, eller deklarer feltet og fyll ut de 39 manglende | 29.07 |

---

#### C3c-19 pudel FULLFØRT 04.08 (commit `b1a8299`, 2 filer live)

Detektor **T1=1/T2=0/prev=0**. **Regel 24 tiende gang.**

- **🔴 Oppdiktet lovforbud, to steder.** «Vibrissene er beskyttet av norsk dyrevelferdslov — klipping er forbudt», med egen H3 og instruks om å kreve bekreftelse av frisøren før betaling. **Dyrevelferdsloven nevner ikke vibrisser**; § 14 gjelder vold, hjelpeløs tilstand, seksuelle handlinger og levende agn. NKKs utstillingsregler tillater normal trimming. **Reneste fabrikkerte regelverkspåstand i C3c** — konkret lov, konkret handling, konkret instruks.
- **🔴 Combination Poodle-testen var aldri et NPK-krav**, men bar hele valpekjøper-rådet: «standard screening-panel» i ingressen, og FAQ + schema sa «NPK krever dette panelet for valpekull på offisiell valpeliste». Av panelets fem mutasjoner er **kun prcd-PRA et krav**; resten er anbefalinger.
- **🔴 NPKs faktiske krav manglet — §10 bygget fra bunnen.** Vedtatt GF 12.05.2024. Alle størrelser: innavlsgrad maks 6,25 %, én Very Good etter 9 mnd, **øyelysing av alle avlsdyr**. Per størrelse: HD A/B + HD-indeks-alternativ og AD-krav fra 2024 (stor), HD/patella/prcd (mellom), patella/prcd og 18 mnd (dverg/toy). **Øyelysing — klubbens mest universelle krav — var ikke nevnt én eneste gang.** Lagt til: NKKs avkomsgrenser 65/85 fra 01.06.2023.
- **🔴 Guiden siterte FCI #172 gyldig fra 01.08.2024 og gjenga innholdet fra før den.** «Alle FCI-anerkjente solide farger» — men 2024-revisjonen anerkjenner partifarget, mantle, tan-tegnet, trefarget og brindle. Samme klasse som chihuahua (C3c-7).
- **🔴 Toy «under 28 cm»** (3 steder) — standarden sier **over 24** opp til 28, og utelukker eksplisitt dvergvekst.
- **🔴 «Eneste rase med fire størrelser»** — tysk spisshund har fem under FCI #97. Guiden motsa seg selv (ingress «én av få» mot §3 «den eneste»).
- **🟠 Addison-multiplikator uten nevner:** «30 ganger høyere» → Famula et al. 2003, 8,6 % mot under 0,5 %, begge oppgitt. Pedersen-siteringen selv verifisert riktig, men flaskehalsen var feildatert (tidlig 1900-tall → midten av århundret).
- **🟠 Vekt i FCI 172 — femte standard på rad** med «SIZE AND WEIGHT»-overskrift og bare høyder.
- Ordtelling 4181 → 5008 (**+827** mot anslag +500–750). Sjette bom.

**Ny redaksjonell konvensjon (Sondre 04.08):** når en rettet påstand også er en utbredt misforståelse blant lesere, skal misforståelsen adresseres direkte («Mange tror det er forbudt. Det er det ikke») — men **aldri** med metakommentar om vår egen tidligere ordlyd. Korpuset retter stille.

#### C3c-18 pointer FULLFØRT 04.08 (commit `45d433e`, 2 filer live)

Detektor **T1=1/T2=0/prev=0** — ekte treff (aortastenose), men hovedfunnene lå i klubbregler og attribusjon. **Regel 24 niende gang.**

- **🔴 §10 feil i BEGGE retninger.** Guiden oppga «NPK avlskrav» som HD-røntgen, **øyenlysning innen 12 mnd før parring**, og tre DNA-tester merket «**ufravikelig**». NPKs faktiske kriterier: **HD status fri A eller B er eneste helsekrav** — verken øyenlysning eller DNA-test er klubbkrav. Samtidig manglet nesten hele det ekte regelverket: 20 jaktprøvestarter, AK-premiering, viltfinnerevne/jaktlyst over rasesnitt, tomstand under 35 %, Very Good etter 24 mnd, matadorliste, aldersgrenser, medlemskap. **Pointer står heller ikke på NKKs kravliste** — ingen myndighet gjør noen DNA-test ufravikelig. **Samme feilmodus som engelsk springer spaniel (C3c-12), andre fuglehund på rad.** §10 skrevet fra bunnen i to nivåer.
- **🔴 Fire «rasestandard»-sitater kom fra NKKs rasebeskrivelse**, ikke standarden. FCI-standard nr. 1 inneholder ingen av dem. Syv flater rettet. Samme klasse som mops-sitatet (C3c-16).
- **🔴 §8 motsa seg selv:** «Felles for de fire tilstandene er at de er autosomal recessive» — tre avsnitt etter at guiden kalte HD polygen.
- **🔴 AMS: feil navn, feil gen, og en kanin.** «Acral Mutilation and Analgesia» → acral mutilation syndrome. Guiden navnga **SCN9A** (det humane CIP-genet); kanin årsak er lincRNA-mutasjon ~90 kb oppstrøms **GDNF** (Plassais et al. 2016, *PLoS Genet* 12(12):e1006482). «En **kanin** parallell til humant CIP» sto på live — skrivefeil for *canin*.
- **🔴 Chondrodysplasi: guiden krevde en test som trolig ikke finnes for rasen.** ITGA10-testen gjelder norsk elghund grå og karelsk bjørnhund; for engelsk pointer er årsaken ikke karakterisert.
- **🟠 Aortastenose = nabo-rase-forveksling** (regel 10, 2. forekomst). Risikorasene er newfoundland/boxer/golden/rottweiler. «Pointer» i oversikter er gjerne **korthåret vorstehhund**.
- **🟠 Historikken var AKC-fortellingen** og internt motstridende (import 1714, engelske referanser 1650). NKK: spanske, franske OG italienske korthårsfuglehunder + «setting spaniels», skiftet i første halvdel av 1700-tallet, og **William Arkwright** som skaperen av den moderne pointeren — han manglet helt.
- **🟠 Vekt ikke normert i FCI 1** («SIZE AND WEIGHT»-overskrift, bare høyde). **Fjerde standard på rad.**
- Ordtelling 3892 → 4551 (**+659** mot anslag +400–600). Femte bom, minste hittil.

**Metodenotat:** da jeg fjernet «Pointer dominerer høyfjellsjakt-segmentet», erstattet jeg den først med en **ny ukildet rangering** («engelsk setter er den klart mest tallrike»). Fanget i samme økt. Å rette en rangering med en annen rangering er en reell felle.

**Uberørt (Sondre 04.08):** fila har 2 body-divs mot 12 H2-er der canonical krever én per H2. Ingen forbudte Cocker-markører. Identisk i HEAD. Egen sak — refaktorering, ikke kildearbeid.

#### C3c-17 norsk-elghund-sort FULLFØRT 04.08 (commit `738f3b6`, 3 filer live)

Detektor **T1=1/T2=0/prev=0**, og det ene treffet var guidens eget forbehold — **reelt nullpunkt, og likevel bolkens tyngste funnliste. Regel 24 åttende gang.**

- **🔴 «Den eneste kritisk utrydningstruede norske rasen»** — i ingress, §2 og oppsummering. NES **er** kritisk truet (Norsk genressurssenter v/ Nina Svartedal, Nationen 29.01.2025), men seks av sju norske nasjonalraser regnes som truet (NIBIO), og haldenstøveren har 7–21 valper/år mot NES' 230. **Rangeringen var nesten omvendt av virkeligheten.**
- **🔴 En oppdretter var gjort til NMBU-forsker.** Nationens byline: «registrert oppdretter og eier av jaktpremierte hunder». Feil yrkestittel på navngitt privatperson, og et debattinnlegg fikk forskningsvekt.
- **🔴 HD-indeksen sto med snudd retning:** «må ha indeks 200 for å kvalifisere til jaktprøver og utstillings-premiering». RAS sier «anbefales», AUNES gjør det til krav, og jaktpremiering/Very Good er **separate** kriterier. Skrevet ut i tre nivåer.
- **🔴 Helseundersøkelsen feil tilskrevet** «NEKF/AUNES, dekker både Grå og Sort» → Frode Lingaas, NMBU, 19.11.2021, rasespesifikk, n=763.
- **🔴 Levetid 12–13 år ukildet** mot rasens eget dokument: 10,3 år (45 døde hunder). **Tredje sprint på rad med levetid over klubbens eget tall.**
- **🔴 §9 lå fire år bak forskningen.** LTV-forekomst 5–10 % (RAS 2021) presentert som rasens tall; **Berg et al. 2024 (Vet J 303:106056) gir 28,6 %** (195/679), mot 18,5 % samlet over 14 raser. Begge oppgis nå med hver sin referansegruppe. **Berg et al. 2025 (Acta Vet Scand 67:10)**: LTV type 2/3 henger sammen med korsryggsmerte (P=0,012, kun 10 NES). **Berg et al. 2025 (67:25)**: arvbarhet 0,199 for NES, blant de høyeste av ni raser — og genetisk korrelasjon LTV↔HD **0,615**, mens studien ikke finner noen generell sammenheng på tvers av raser. 28,6 % ble verifisert i primærtabellen, ikke bare i klubbens gjengivelse.
- **🟠 Pelsfargen i strid med FCI 268 på fem flater** — «hvite tegninger» som rasekjennetegn og «som regel et lite halsbånd», mens standarden tolererer «a little white» og fører hvite sokker som FEIL.
- **🟠 Kryss-guide-motsigelse:** «Grå over 25 kg» mot vår egen grå-guides 23 kg. **FCI 242 har overskriften «SIZE AND WEIGHT» og oppgir ingen vekt** — tredje forekomst etter FCI 125/257. Begge guider rettet i samme commit.
- Ordtelling 3532 → 4274 (**+742** mot anslag +450–650). §8/§9/§2 fikk nye kildeblokker og står for 588; **de seks seksjonene uten ny kilde flyttet seg null ord.** Meldt før push.

**Sidefunn:** `article_map` hadde 3500 ord for `norsk-elghund-gra` mens fila har 4504 — **1 004 ord drift** fra en Trigger B-synk som aldri ble kjørt. Rettet. **Kan gjelde flere guider; ikke sveipet.**

#### C3c-16 mops FULLFØRT 04.08 (commit `e49dfa2`, 2 filer live)

Alle 7 godkjente punkter levert. Siste av BOAS-trioen med feil framstilling. **Full dokumentasjon i `docs/health-claims-register.md`.** Hovedpunktene:

- **🔴 Alle tre kravdatoene var gale.** Guiden sa tre ganger «siden 2019 … som premiss for valperegistrering». Faktisk: **mops 01.01.2023**, engelsk og fransk bulldog **01.08.2022**. Ordningen fantes fra høsten 2019 — som ordning, ikke krav.
- **🔴 Ett krav var oppdiktet, to ekte var nedgradert.** §9 påsto at «NKK krever HD-screening» — HD er *ikke* blant kravene. Patellastatus (krav siden **01.01.2020**) sto som «tilleggsmål»; øyelysning (krav siden **01.01.2023**) manglet helt. FAQ-svaret hadde begge feilene i én setning, nøyaktig invertert.
- **🔴 Sitatet var tilskrevet feil person — og «bekreftet» av oss selv.** «Sigurd Sjølie» → **Renate Sjølie**, NKKs veterinær og **leder for FCIs BOAS-gruppe**. Et søk på sitatet returnerte vår egen mops-side som kilde og «bekreftet» samtidig navnet, «100 veterinærer», «30 land» og 80 %-tallet. **Sondres beslutning: parafraser uten anførselstegn** — la ikke sitattegn stå på en ordlyd vi aldri har lest i primærkilden.
- **🔴 Statistikken var kollapset og hentet fra feil raser.** «Nesten 1000 testet, ~80 % grad 0/1» → **80 % av 131 engelske bulldoger og 85 % av 336 franske**. Mops-tallet mangler helt — og NKK opplyser selv at graderingskriteriene er «noe ulik for mops og de to bulldograsene».
- **🟡 Superlativene erstattet med en verifiserbar rolle:** Renate Sjølie leder FCIs BOAS-gruppe og representerte NKK med Jane Ladlow ved lansering av BOAS-gradering for 14 nye raser under Crufts 2026.
- **🟡 Tre fakta guiden manglet:** belastningstesten (3 min trav i 6–8 km/t), operative vilkår (min. 18 mnd, maks 24 mnd før paring, kun NKK-kurset veterinær), og — viktigst — at **en BOAS-operert hund automatisk får grad III**. Kirurgi kvalifiserer ikke et avlsdyr, den utelukker det.
- **Fjernet framfor myket:** «over 100 veterinærer» og «30 land» lot seg kun bekrefte sirkulært.

Ordtelling 4185 → 4451 (+266). llms.txt Trigger B kjørt (H2 endret).

#### C3c-15 tibetansk-spaniel FULLFØRT 04.08 (commit `f97e440`, 1 fil live)

Alle 5 godkjente punkter + 2 funn til. **Full dokumentasjon i `docs/health-claims-register.md`.** Hovedpunktene:

- **🔴 NKKs registreringskrav var tilskrevet raseklubben.** Øyelysningskravet er NKKs restriksjon f.o.m. **01.04.2014** — og NMHKs eget RAS har de to nivåene under hver sin overskrift. Seksjonen motsa seg selv internt (H2 sa «NKK-kravet», teksten sa «NMHK innførte»). Motsatt retning av boxer (C3c-6).
- **🔴 Ny defektklasse: å delegere regelen til leseren.** Guiden ba valpekjøperen «sjekke gjeldende NKK-anbefaling for hvor nytt resultatet skal være». Regelen er konkret (senest 12 mnd. før paring, ERG teller ikke, ECVO i DogWeb). **Det ser ansvarlig ut, men flytter arbeidet til den som har minst forutsetning for å gjøre det — i nettopp den seksjonen guiden finnes for.**
- **🔴 §10 bygget om til to nivåer:** NKKs ene krav mot NMHKs fem tilleggskrav (fri for PRA, 20 mnd. for **begge kjønn**, Very Good, ID-merking, etiske retningslinjer). Teksten sier nå rett ut hva NKK-registrering *ikke* garanterer.
- **🔴 Levetid én bånd for høyt i seks flater** — «14–16 år» mot RAS' «12-15 år, men gjerne også eldre». **Andre sprint på rad hvor guidens levetid ligger over klubbens eget dokument** (shiba: 12–15 mot RAS-snitt 9,23). Levetid mot RAS bør bli fast sjekkpunkt.
- **🟡 Premisset var snudd:** guiden kalte populasjonen «relativt smal» som begrunnelse for både bærer-avl og matadoravl-grensen. RAS: innavlsgrad 0,94 % (2015), «stor avlsbase» — og det er *grunnen* til at 2 %-regelen gjelder. **Feil premiss brukt til å begrunne en regel som finnes av motsatt grunn.**
- **🟡 Katarakt manglet helt.** RAS navngir «Katarakt og PRA» som de to arvelige øyesykdommene øyelysningen skal fange; guiden fremstilte kravet som rent PRA3-tiltak.
- **Ikke overkorrigert:** «48 kull i 2015 med ukjent PRA3-status» er ordrett match i RAS, og cherry eye/navlebrokk er nær ordrett gjengitt. **Port 7 slår ikke ut** — FCI 231 normerer faktisk vekt.

Ordtelling 3990 → 4338 (+348) mot estimat +560–620. **Nyanse til regel 27: 3×-multiplikatoren gjelder når kildeblokken kommer i TILLEGG; erstatter den en eksisterende feil blokk, blir netto langt lavere.** Live-verifisering krevde **forsøk 5 av 6**.

#### C3c-14 shiba-inu FULLFØRT 04.08 (commit `56f08a8`, 2 filer live)

Alle 4 godkjente punkter levert. **Full dokumentasjon i `docs/health-claims-register.md`.** Hovedpunktene:

- **🔴 Hele guidens norske moat hvilte på et forslag som ikke ble innført — og datert to år feil.** «JUN 2024-forslaget» er i realiteten **sak 5-2 på årsmøtet 2022**, med tre punkter (patella, øyelysning, gonioskopi), mens HD-indeks var en egen sak 5-3. **Bare HD-indeks ble vedtatt og innført** (JUNs egen årsberetning 2022). JUNs gjeldende retningslinjer har ett helsekrav: HD-røntgen fra 01.07.2009. Moaten er snudd til et presist krav/anbefaling-skille.
- **🔴 Bevisst tilbakeholdt:** jeg påstår ikke at forslaget ble *nedstemt* — protokollen finnes ikke i arkivet, og en søkeoppsummering er ikke et referat. **Regel 20 holdt.**
- **Metodefunn:** første søk ga **vår egen side** som toppresultat (sirkulær bekreftelse). Saksdokumentet lot seg bare finne via **Waybacks CDX-indeks på `junnorge.no/wp-content/uploads/2022*`** — klubbens live nettsted er under omlegging. Det er nå den raskeste veien til klubbdokumenter når et nettsted er i «kommer»-tilstand.
- **🔴 Guiden hadde null norske tall.** RAS 2021: **bare 12 shiba gonioskopert 2009–2020 — 6 frie, 6 med glaukom.** Skrevet eksplisitt at 50/50 ikke er en prevalens. 194 øyelyste 1996–2020 (88,1 % frie), 4 av 182 med akutt glaukom.
- **🔴 Port 7 igjen, i verste variant:** FCI 257 har et avsnitt som **heter «Size and weight» men oppgir ingen vekt**. Høydene var dessuten feil (40/37 → 39,5/36,5 cm).
- **🟡 Pemphigus foliaceus var akita-import** (regel 10, femte forekomst).
- **🟡 Levetid:** «12–15 år» → JUNs egne tall gir snitt **9,23 år** med 24 % over 13 år, og **ni av 54 døde hunder avlivet på grunn av atferd**. Knytter helse til temperament.
- **Egen feil fanget før push:** semikolon i desimaltall («39;5 cm») — komma-regelen gjelder kun `article_map`, aldri brødtekst. Ny fast desimal-kontroll.

Ordtelling 4011 → 4602 (+591) mot estimat +500–560.

#### C3c-13 jack-russell-terrier FULLFØRT 04.08 (commit `d663d53`, 2 filer live)

Alle 6 godkjente punkter + 2 speilingsflater levert. **Full dokumentasjon i `docs/health-claims-register.md`.** Hovedpunktene:

- **🔴 En falsk negativ påstand med transplantert attribusjon — tre lag på én setning.** Guiden skrev at LOA/CAPN1 «IKKE» gjelder Jack Russell, tilskrev det negative funnet til «University of Missouri og Animal Health Trust», og brukte det som teknisk begrunnelse for at russell-rasene er separate populasjoner. **The Kennel Club har hatt LOA som offisiell DNA-ordning for Jack Russell siden mai 2017.** Studien er **Gast et al. 2016, BMC Vet Res 12:225, Hannover** — og den fant ingen CAPN1 i *noen* av rasene, heller ikke Parson Russell. Missouri/AHT er korrekt for **PLL**-testen; attribusjonen var flyttet mellom to naboavsnitt i samme fil.
- **🔴 En feil som gjorde en annen feil konsistent.** Samme avsnitt oppga at RKC-pakken «dekker både PLL og SCA» — den dekker tre tester. Undertellingen matchet nøyaktig den falske LOA-påstanden. **Slike par er vanskeligere å oppdage enn hver feil for seg, fordi teksten er internt konsistent.**
- **🔴 Graderingsskalaen matchet ikke registeret guiden ba leseren slå opp.** Guiden ga 1–4; **NKK graderer 0–3**. Samtidig instruerte den leseren i å sjekke DogWeb og «spørre om grad». Samme klasse som dachshund/Jensen (C3b-3).
- **🔴 Intern logisk motsigelse:** NKK-kravet ble kalt «det enkleste skillet mellom en seriøs og en hobby-oppdretter», mens guiden fire avsnitt senere skrev at alle NKK-registrerte kull oppfyller det per definisjon. **Det faktiske skillet manglet: RG Jacks avlskriterier** (fri for patella — ikke bare kjent status — øyenlyst, 2 × excellent, tispe 20 mnd, maks 2 gjentakelser).
- **Krav-hierarkiet er nå skrevet ut i tre nivåer** — NKK krever, RG Jack krever mer, DNA-testene er vår anbefaling. Fjerde sprint på rad hvor krav/anbefaling var funnklassen.
- **Klubbens egen prioritering manglet:** NTK peker på **ulykker** som største årsak til skade og tidlig død, mens guiden kalte patella rasens «definerende helsekonsern».
- **Ikke overkorrigert:** registreringsrestriksjonen 01.01.2019, kravet om *kjent* status, og SCA-debut 2–12 måneder er alle bekreftet og beholdt.

Ordtelling 3885 → 4571 (+686) mot estimat +850–900 — **under budsjett; regel 27s 3× holdt som øvre grense.**

#### C3c-12 engelsk-springer-spaniel FULLFØRT 04.08 (commit `3d8600e`, 1 fil live)

Alle 14 godkjente punkter levert. **Full dokumentasjon i `docs/health-claims-register.md`.** Hovedpunktene:

- **🔴 Rage syndrome-narrativet var galt i begge retninger samtidig.** Guiden anslo forekomst til «under 1 %» (ukildet), framstilte temporallapps-epilepsi som etablert mekanisme, og hentet farge-sammenhengen fra cocker. Alle tre falt. Det som FAKTISK er dokumentert — **Reisner, Houpt & Shofer 2005, JAVMA 227(10):1594–1603, n=1053: 48,4 % knurring eller verre mot egen eier, 26,3 % bitthistorikk**, risiko forbundet med hannkjønn, kastrert status, show-linje og alder >4 år — sto ikke i guiden i det hele tatt. **Nettoeffekten var at guiden understatet rasens reelle problem og overstatet mekanismen.** Studiens egen konklusjon (velg tispe av jakttype fra erfaren oppdretter) er nå med ordrett.
- **🔴 EEG-påstanden hvilte på tre hunder uten rase.** Dodman 1992 er en kasusserie på n=3 der rasetilhørighet ikke oppgis. **Ny variant av Salzmann-klassen: kilden finnes og er korrekt gjengitt, men den handler ikke om denne rasen.**
- **🔴 Gonioskopi — rasens eneste rasespesifikke avlskrav — manglet helt (0 treff i fila).** NSKs avlsanbefalinger krever gonioskopering før første parring og deretter hvert 3. år, med parringsmatrise og forbud mot å krysse glaukom-linjer. Guiden presenterte i stedet en «DNA-test-quartet» som definisjonen på ansvarlig avl. **Et fravær som detektoren per definisjon ikke kan finne.**
- **🔴 HD-rangeringen snudd av datagrunnlaget.** BVA 2024: springer 15-års median **10** (n=850) mot labrador 9, rottweiler 8, berner sennenhund 9. Guiden sa «lavere HD-risiko enn storraser» på to steder.
- **Klubbkrav-blokken ga fem avvik samtidig** (regel 9): NSK- ikke NKK-medlemskap, manglende kullkrav og dispensasjonsadgang, manglende aktivitets- og premieringskrav, og HD nedgradert fra «skal ha kjent status» til «ikke offisielt avlskrav».
- **Fabrikkert standardsitat i fem flater.** «Vennlig, åpen, glad, aktiv og livlig» tilskrevet NKK; standarden sier «Vennlig, glad og medgjørlig». Femte forekomst lå i **ingressen** — port 1 slo ut på nytt.
- **Standarden angir ingen vekt** (regel 13): «FCI-standarden angir 19–25 kg» → standardens Størrelse er kun «Mankehøyde: Ca 51 cm». Cocker-standarden oppgir derimot vekt — nabo-standarden ga falsk trygghet.
- **Ikke overkorrigert:** «Den eldste av fuglehundrasene» står ordrett i NKK-standarden, hele den norske Fant-historikken bekreftes av NJFF, og otitis-retningen «lavere enn cocker» fikk endelig kilde (O'Neill 2021: springer OR 1,24 ikke-signifikant, cocker OR 1,67) — det var *mekanismen* som var oppfunnet, ikke retningen.
- **Forkastet kilde:** Reisner 1996 (CSF-serotonin) ville vært en sterk springer-moat, men utvalget lot seg ikke bekrefte som springere. Regel 20 holdt.

Ordtelling 4045 → 5486. **Ny regel 27 (3×-multiplikator ved ny kildeblokk).**

#### C3c-11 dvergpinscher FULLFØRT 03.08 (commit `e4e1c49`, 2 filer live)

Alle godkjente punkter levert. **Full dokumentasjon i `docs/health-claims-register.md`.** Hovedpunktene:

- **«Hackney-travet» var oppført som ett av tre definerende rasetrekk — det er en FEIL etter FCI-standard nr. 185**, som lister «Hackney gait» under FAULTS. Standardens egen beskrivelse av korrekt gangart er den motsatte. Sannsynlig AKC-import; Norge følger FCI/NKK. Erstattet i ingressen med rasens dokumenterte levetidsfordel.
- **Ny feilklasse: en utregning kilden eksplisitt forbyr.** Guiden regnet Hardy-Weinberg ut fra allelfrekvensen 0,133 og oppga 23 % bærere / 1,8 % affiserte. Raj et al. 2020 advarer i samme avsnitt: «this is a biased population». Siteringen var korrekt — slutningen var ikke. **Farligere enn en feilsitering, fordi HWE er ekte matematikk og resultatet ser rigorøst ut.**
- **Patella-rangeringen snudd av rasens egen klubb.** NPK: «ikke en utbredt sykdom på rasen». O'Neill et al. 2016 (n=210 824): dvergpinscher er ikke blant de 11 rasene med forhøyet odds. Guiden hadde lånt disposisjonen fra Yorkshire Terrier.
- **Klubbhistorikken feil på to punkter:** Norsk Dvergpinscherklubb ble stiftet 1946 (ikke Norsk Schnauzer Klubb), innlemmet 1978 (ikke 1979).
- **Øyelysning kalt «anbefalt» — det er et krav.** Motsatt retning av SBT-feilen.
- **Klubbkrav-blokken ga fem avvik samtidig** (regel 9): patella 0/0 av smådyrspesialist, tispe 18 mnd / hann 12 mnd, HD ikke i kravene, demodikose-avlsforbud manglet, matadoravl maks 34 avkom manglet.
- **Levealder:** McMillan Table S3 gir **median 13,7 år (KI 13,1–14,2), HR 0,75** — blant de lengstlevende rasene. Erstattet ukildet «12–15 år» på fem flater.

Ordtelling 3326 → 4344.

**To nye faste kontroller (se listen nedenfor og `docs/artikkel-sjekkliste.md`).**

**De 33 fullførte, gruppert etter bolk:**

| Bolk | Guider |
|---|---|
| C3a (6) | `berner-sennenhund` · `vizsla` · `irsk-setter` · `rottweiler` · `riesenschnauzer` · `coton-de-tulear` |
| C3b-0 (1) | `malteser` |
| C3b-1 (2) | `cane-corso` · `kortharet-vorstehhund` |
| C3b-2 → C3b-5 (4) | `newfoundland` · `dachshund` · `samojedhund` · `italiensk-mynde` |
| C3c-1 (2) | `golden-retriever` · `griffon-petit-brabancon` |
| C3c-2 (3) | `cavalier-king-charles-spaniel` · `bichon-havanais` · `border-collie` |
| C3c-3 (2) | `west-highland-white-terrier` · `whippet` |
| C3c-4 → C3c-16 (13) | `mellomschnauzer` · `beagle` · `boxer` · `chihuahua` · `engelsk-setter` · `fransk-bulldog` · `staffordshire-bull-terrier` · `dvergpinscher` · `engelsk-springer-spaniel` · `jack-russell-terrier` · `shiba-inu` · `tibetansk-spaniel` · `mops` |

#### 🟠 ÅPEN SAK — dobbel BreadcrumbList på raseguidene

Oppdaget under C3c-10. **`/pages/staffordshire-bull-terrier` rendrer to `BreadcrumbList`-blokker i JSON-LD:** én inline i seksjonsfila og én fra `snippets/mh-article-schema.liquid`. Begge parser rent, så ingen automatisk sjekk slår ut.

Dette er **ikke** innført av C3c-10 — det er et eksisterende mønster. **Sondre besluttet: logg som egen sak, ikke rør nå.** Skal undersøkes på tvers av korpuset når det er kapasitet: sannsynligvis gjelder det alle raseguider som både har inline breadcrumb-schema og rendrer `mh-article-schema`. Google velger normalt én, men duplikat strukturert data er ikke ønskelig og kan gi uforutsigbart rikresultat.

Første steg når saken tas: `grep -l 'BreadcrumbList' sections/hundetips-*.liquid` mot hvilke filer som også kaller `mh-article-schema`.

#### C3c-10 staffordshire-bull-terrier FULLFØRT 03.08 (commit `19db102`, 2 filer live)

Alle godkjente punkter levert. **Full dokumentasjon i `docs/health-claims-register.md`.** Hovedpunktene:

- **Ny feilklasse: klubbens ANBEFALING framstilt som KRAV, med en mekanisme som ikke finnes.** Guiden skrev fem steder at NTK «krever» gentest «for valpeformidling». Rasegruppen skriver selv at den «på det sterkeste vil **anbefale**», og at den eventuelt må vurdere å **foreslå** et krav. Sanksjonen er tapt annonseplass, ikke stanset kull — og **rasegruppen har ikke lenger noen valpeformidler**. Boxer/BSI-klassen, men grovere: her fantes ikke tjenesten kravet var knyttet til.
- **To helserangeringer snudd.** Pegram et al. 2020 (n=1 304 mot 21 029): patellaluksasjon **OR 0,15** — sterkeste *beskyttelse* i studien, ikke en utfordring. Periodontal sykdom **OR 0,41**. Guiden hadde begge motsatt, og den kausale begrunnelsen («kort snute») var oppdiktet.
- **«Mindre rase i Norge» — SBT er nr. 6 på NKKs topp-10.** 11 545 registrert 2013–2024; populasjonen nesten doblet. Klubben sier selv rasen er størst i antall på utstillinger.
- **«The nanny dog … godt dokumentert i britisk lokalhistorie»** hadde ingen dekning. Eldste kjente forekomst er NYT 1971. Verken KC eller NTK bruker uttrykket.
- **Epilepsi manglet helt** — OR 2,06 er rasens sterkeste dokumenterte disposisjon, og lett å forveksle med L-2-HGA.
- **Vektvirkeligheten:** snitt 18,45 kg for hanner mot standardens tak på 17; **37 % veier 20 kg eller mer**. Klubben knytter leddplager til høy vekt.
- **Levealder: tabellen lest, ikke gjettet.** McMillan Suppl. Table S3 gir median **12,0 år (KI 12,0–12,1)** — en avis oppga 11,33. Author Correction sjekket (gjelder kun Miniature Dachshund). Vedleggsnummereringen er forskjøvet: Table S3 er `MOESM8`.
- **Port 7 fjerde forekomst:** Amstaff «43–48 cm» → 46–48 hann / 43–46 tispe.

Ordtelling 4815 → 7166. **Estimatavvik loggført:** Phase 1-anslaget var +400–600, faktisk +2583 før trim. Sondre godkjente veksten på et anslag som var fem ganger for lavt — **Phase 1-ordestimat for bolker med moat-bytte eller ny primærkilde må regnes per H2, ikke som ett totalanslag.** FAQ og historie trimmet −232 ord; §10 holdt urørt etter instruks.

**Ny verifiseringsregel (nr. 24), se listen nedenfor.**

**De 27 fullførte, gruppert etter bolk:**

| Bolk | Guider |
|---|---|
| C3a (6) | `berner-sennenhund` · `vizsla` · `irsk-setter` · `rottweiler` · `riesenschnauzer` · `coton-de-tulear` |
| C3b-0 (1) | `malteser` |
| C3b-1 (2) | `cane-corso` · `kortharet-vorstehhund` |
| C3b-2 → C3b-5 (4) | `newfoundland` · `dachshund` · `samojedhund` · `italiensk-mynde` |
| C3c-1 (2) | `golden-retriever` · `griffon-petit-brabancon` |
| C3c-2 (3) | `cavalier-king-charles-spaniel` · `bichon-havanais` · `border-collie` |
| C3c-3 (2) | `west-highland-white-terrier` · `whippet` |
| C3c-4 → C3c-10 (7) | `mellomschnauzer` · `beagle` · `boxer` · `chihuahua` · `engelsk-setter` · `fransk-bulldog` · `staffordshire-bull-terrier` |

Kontrollert begge veier: 27 fullførte + 15 gjenstående = 42. (Historikk: «14 ferdig / 28 igjen» var feil fordi `riesenschnauzer` var talt i både C3a og C3b-0.)

#### C3c-9 fransk-bulldog FULLFØRT 03.08 (commit `252846e`, 1 fil live)

Ni godkjente punkter levert. **Full dokumentasjon i `docs/health-claims-register.md`.** Hovedpunktene:

- **Bolkens viktigste funn er at en påstand HOLDT.** Guidens BOAS-graderingsregel ble nesten meldt som oppdiktet — men et «bekreftende» søk hadde **vår egen mops-guide som treff nr. 3**. NKKs egen graderingsside avgjorde: grad II og III er begge «Klinisk påvirket, og skal ikke brukes i avl», første graderingskurs 29.08.2019. Guiden hadde rett; kun presisjonen ordning (2019) vs. krav (01.08.2022) er rettet.
- **Kjønnsstratifisert vekt kollapset:** standarden sier hann 9–14 kg / tispe 8–13 kg med 500 g toleranse; guiden skrev «8–14 kg». Port 7, tredje forekomst etter vizsla og whippet. Mankehøyde manglet helt.
- **Rasestandard-datoen var to revisjoner bak** (1986/2015 → publisert 10.08.2023). Tredje sprint på rad.
- **BSI feillest for tredje gang** — NKUs dommerinstruks, ikke NKKs avlsverktøy, og ikke rangert.
- **Levealder lå over begge publiserte tall:** Teng et al. 2022 gir 4,53 år (livstabell fra fødsel, lavest av alle raser), McMillan et al. 2024 gir median 9,8 år. Begge oppgitt med skillet forklart.
- **Moat: O'Neill et al. 2021** (n=2 781 mot 21 850) — forhøyet odds for 20 av 43 diagnoser, med begge forbeholdene skrevet inn: oddsforhold ≠ risikomultiplikator, og **redusert odds for 11 av de samme 43**.

Ordtelling 4516 → 5442 (+926). **Ingen nytt Admin-steg.**

**Ny verifiseringsregel (nr. 23), se listen nedenfor.**

### 🔴 ÅPENT PUNKT TIL `mops` STÅR FOR TUR — BOAS-datoen

Oppdaget under C3c-9. **`mops` skriver at NKK siden 2019 har hatt obligatorisk BOAS-screening «som premiss for valperegistrering». Mops' registreringskrav kom først 01.01.2023.** Screeningordningen fantes fra høsten 2019, men den var ikke et registreringskrav for mops før 2023.

Til sammenligning: `engelsk-bulldog` har allerede det korrekte skillet (ordning 2019, krav 01.08.2022), og `fransk-bulldog` fikk det inn nå. **Mops er den siste av BOAS-trioen med feil framstilling.** Rasen ligger i 3,0-gruppen i C3c-rekkefølgen. Rettes der — ikke som eget hastetiltak.

#### C3c-8 engelsk-setter FULLFØRT 03.08 (commit `26b357b`, 1 fil live)

Ni godkjente punkter levert, inkludert en godkjent omskriving av guidens bærende kapittel. **Full dokumentasjon i `docs/health-claims-register.md`.** Hovedpunktene:

- **Ny feilklasse: selektivt sitat som snur kildens mening.** Guiden siterte NESKs dommerkompendium på at showsetteren er «uegnet som jakthund» og klippet setningen midt i. Samme setning kritiserer fieldtrial-typen like hardt. Klubben avviser **begge** ytterpunktene. Sitatet består enhver kildesjekk — kilden finnes, ordlyden er ordrett, dokumentet er riktig.
- **Kapittelet bygde på en type-deling kilden sier ikke finnes her:** «Som kjent har vi ikke en slik deling av type her i Skandinavia … Hele Skandinavia står samlet bak målsettingen om at engelsk setteren skal være en dual purpose dog.» Fire flater bar premisset. **Sondre besluttet å snu kapittelet framfor å slette det.**
- «Norsk jakthund-standard 58–64/54–60 cm» finnes ikke; både standarden og kompendiet oppgir 65–68 / 61–65.
- **Glutenintoleranse sto på feil rase** — tilhører irsk setter, og manglet der.
- **NCL/CLN8 lagt til** (Katz et al. 2005): rasens best dokumenterte arvelige sykdom, som guiden ikke nevnte.
- **Døvhet fikk tall** (Marsh et al. 2020, n=447): 3,6 % ensidig / 0,9 % bilateral. Guidens ukildede påstand stemte. 4,6×-tallet for utestede foreldre gjør BAER-rådet begrunnet.
- Rasestandarden oppgir **ingen vekt** — berører den åpne setter-vektsaken.

Ordtelling 3693 → 4267 (+574). **Ingen nytt Admin-steg.**

**Nye verifiseringsregler (nr. 21–22), se listen nedenfor.**

#### C3c-7 chihuahua FULLFØRT 03.08 (commit `501b7fa`, 1 fil live)

Alle fjorten godkjente punkter levert. **Full dokumentasjon i `docs/health-claims-register.md`.** Hovedpunktene:

- **Hjertescreening satt for sent — bolkens YMYL-funn.** Guiden sa «årlig auskultasjon fra 7–8 års alder». Pålsson et al. 2025 (J Vet Cardiol; n=97 friske chihuahuaer via Svenska Chihuahuaklubben): **halvparten affisert ved 6,4 år**, 80 % ved 9–10 år. Rådet flyttet til fem–seks år. Hjertesykdom er samtidig største registrerte dødsårsak (18,8 %) — den lå som siste kulepunkt med formuleringen «sjeldnere så alvorlig».
- **Rasestandarden var utgått på to punkter.** Molera sto som rasetypisk kjennetegn; gjeldende NKK-standard lister **åpen fontanell som diskvalifiserende feil**. Og «mankehøyde 15–23 cm» sto i faktalista, mens standarden sier ordrett «kun vekt vurderes; ikke høyde». **Speilvendt beagle-funnet.**
- **Vekten feil i tre flater — og virkeligheten ligger over taket.** Standarden: 1–3 kg, ideal 1,5–2,5, over 3 kg diskvalifiserende. VetCompass median voksenvekt: **3,4 kg**. Begge tall oppgitt med hver sin referansegruppe.
- **Sykdomsrangeringen snudd:** periodontal sykdom 13,5 % mot patellaluksasjon 4,0 % i samme materiale. Guiden kalte patella «dominerende» og tannhelse «nest største». Samme feilklasse som engelsk-bulldog i Bolk A.
- **Levealder 12–18 år var ukildet i fire flater.** O'Neill: median dødsalder 8,2 år (tisper 10,2, hanner 6,9), med forfatternes eget forbehold om ung og voksende populasjon skrevet inn.
- **To påstander strøket framfor kildesatt** (403 på begge kildekandidater), og **én foreslått kilde forkastet i skrivefasen**: den koreanske trachea-serien mangler nevner og kan ikke bære en overrepresentasjons-påstand.

Ordtelling 3924 → 5525. **Ingen nytt Admin-steg** — Sondre besluttet eksplisitt å skippe meta-fiksen.

**Nye verifiseringsregler (nr. 18–20), se listen nedenfor.**

#### C3c-6 boxer FULLFØRT 31.07 (commit `a4b85b5`, 2 filer live)

Alle elleve godkjente punkter verifisert, pluss de tre FAQ↔schema-avvikene. **Full dokumentasjon i `docs/health-claims-register.md`.** Hovedpunktene:

- **Ny feilklasse: studentarbeid løftet til doktorgrad.** «Vibeke Moen Helgelands PhD-arbeid fra NMBU (2007)» er registrert som `OtherStudentWork` i NVA/Sikt — en fordypningsoppgave med Heiene og Indrebø som veiledere. Institusjonen var også anakronistisk: NMBU oppsto i 2014, arbeidet er fra Norges veterinærhøgskole. **Består enhver formatsjekk — bare dokumenttypen er feil.**
- **BSI feiltolket to ganger:** det er Nordisk Kennel Unions instruks til *utstillingsdommere* om overdrevet eksteriør, ikke avlskrav — og Boxers risikoområder er **pust og hud**, ikke hjerte og bevegelsesapparat.
- «Over 100 000 kr i forskningsmidler» til spondylose-prosjektet lot seg ikke spore; klubbens dokumenterte ordning er kostnadsrefusjon (1 500 / 750 kr).
- Lingaas-påstanden pekte på feil prosjekt: hans dokumenterte boxer-arbeid er **nyresvikt-forskning mot en gentest**, ikke gratis obduksjon.
- Rasestandard: NKK-dato 12.07.2021 → **26.06.2024**; vekt «30–32 kg» → standarden sier **«over 30 kg»** uten øvre grense.
- Levetid 9–12 år → McMillan 11,3 år (n=17 219) *og* O'Neill 10,5 år (n=346), begge med referansegruppe.
- Mastcellesvulst tallfestet: **Shoop et al. 2015**, boxer 1,95 % mot 0,27 % samlet (n=168 636) — høyest av alle raser i studien. Førsteforfatter er Shoop, ikke O'Neill.
- Døvhetstallene for hvit boxer viste seg å være **dalmatiner-tall**; Strain 2004 testet ikke boxer. Forankret i O'Neill 2023 i stedet, som fant ingen helseforskjell mellom hvite og ikke-hvite.

**Nye verifiseringsregler (nr. 15–17), se listen nedenfor.**

#### C3c-5 beagle FULLFØRT 31.07 (commits `3485fac` + `4892d17` + `ea18060`, 2 filer live)

Alle ti godkjente punkter verifisert mot primærkilde. **Full dokumentasjon i `docs/health-claims-register.md`.** Hovedpunktene:

- **Lafora-debuten var forskjøvet fire år, i farlig retning:** «4–5 års alder» → Flegel et al. 2021 (JVIM 35(5):2359–2365, n=28) gir gjennomsnitt **8,3 år, spenn 6,3–13,3**, og ingen hund i serien debuterte før 6 år. En frisk 6-åring kunne blitt lest som forbi risikoalderen, når det er da den begynner.
- **Klubbens tall brukt mot klubbens egen konklusjon:** guiden skrev at 4,2 % AMS-symptomer «underbygger at tilstanden er reell». BeagleRingen skriver selv at diagnose kun stilles ved spinalprøve og at symptomer ikke betyr sykdom. **Samme klasse som Salzmann i C3c-3.**
- **Ingen av FCI-standardene #161/#159/#295 oppgir vekt.** Alle tre lastet ned og lest. Høydene rettet (Foxhound 58–64, Harrier 48–55). Pocket beagle: «under 25 cm» usporbart, og typen forsvant ikke — standarden sier mindre eksemplarer fortsatt fødes.
- Fedme-superlativet → Salt et al. 2019 (JVIM 33(1):89–99), der beagle er én av tolv raser: HR 2,40, rundt to års kortere median levetid. Kohort-forbeholdet skrevet inn så tallene ikke leses mot McMillans 12,5.
- **Tre påstander holdt:** MLS-1970-tallet (Bader 2010, som også ga oss 2–3 % i britiske/australske delpopulasjoner), CHIC-kravet, og NKK/FCI-datoene. Én av dem fjernet jeg først som uverifisert og satte tilbake da den viste seg korrekt.
- Ordtelling 3924 → 4643. Meta-description ren; **ingen nytt Admin-steg**.

**Ny verifiseringsregel (nr. 12), se listen nedenfor:** rasestandardens egen historikk-seksjon er en underbrukt primærkilde.

#### C3c-4 mellomschnauzer FULLFØRT 31.07 (commit `f6baaec`, 2 filer live)

Alle seks godkjente fikser levert, pluss fem NSBK-attribusjonsfeil oppdaget under verifiseringen. **Full dokumentasjon i `docs/health-claims-register.md`.** Hovedpunktene:

- **Moat byttet:** PS var «rasens mest rasespesifikke helseutfordring» på seks flater, men mellomschnauzer står ikke på noen dokumentert PS-disposisjonsliste (Brambilla n=1 779, UC Davis n=80 943, Merck). Dverg- og riesenschnauzer gjør — **disposisjonen var arvet fra nabo-rasene i familien**. Erstattet med RBM20-assosiert DCM (Leach et al. 2022: 19,7 % bærere, 1,5 % homozygote, 92,9 % av homozygote affisert), som også er NSBKs egen anbefaling.
- **Fem NSBK-påstander falt samtidig** da klubbens avlsdokument ble åpnet: ekko-anbefalingen finnes ikke, «NSBK krever HD» forvekslet NKKs krav med NSBKs anbefaling, «årlig øyelysning» er før parring med 12 mnd gyldighet, paringsalderen var feil for begge kjønn, og innavlsgrad-grensen på 6,25 % står ingen steder.
- **Medlemstallet gikk feil vei:** klubben oppgir selv «i underkant av 1000», ikke «over 1000». Det gamle tallet lever videre på NKKs regionside.
- Levetid 13–16 «eksepsjonelt» → median 13,0 år (McMillan Tabell S3, n=1 261). Ballongvalvuloplastikk 70–85 % → Bussadori 2001 + Johnson & Martin 2004.
- Ordtelling 3358 → 4190. **Sondre besluttet at den får stå** — reelt moat-bytte, ikke oppblåsthet, og godt innenfor pre-regel-båndet.

**Ny verifiseringsregel (nr. 9), se listen nedenfor:** klubbattribuerte påstander verifiseres som blokk, ikke enkeltvis.

#### Resten av C3c-rekkefølgen — 9 guider igjen, navngitt

Godkjent rekkefølge: score-orden, med de fem null-treff-guidene til slutt som stikkprøve.

`sankt-bernhardshund` (3,0) → **stikkprøve til slutt:** `dansk-svensk-gardshund` · `finsk-lapphund` · `jamthund` · `norsk-elghund-gra` · `shetland-sheepdog` (0,0).

**Ordtak gjelder kun `jamthund`** (2419 ord, +381 slakk) av de gjenstående. Resten er pre-regel-guider på 3300–4800 ord uten tak. `whippet`, `west-highland-white-terrier`, `mellomschnauzer`, `beagle`, `boxer`, `chihuahua`, `engelsk-setter`, `fransk-bulldog`, `staffordshire-bull-terrier`, `dvergpinscher`, `engelsk-springer-spaniel`, `jack-russell-terrier`, `shiba-inu`, `tibetansk-spaniel`, `mops`, `norsk-elghund-sort`, `pointer` og `pudel` er ferdige. **6,0- og 5,0-gruppene er tømt; `mops` og `norsk-elghund-sort` er tatt av 3,0-gruppen.** **Neste: `sankt-bernhardshund` — siste i 3,0-gruppen. Deretter kun stikkprøve-gruppen igjen.** Merk at `norsk-elghund-gra` i stikkprøve-gruppen fikk en liten kontrollert vektfiks under C3c-17, men er IKKE kildeverifisert — den står fortsatt som stikkprøve.

**Ordbudsjett-erfaring fra C3c-4:** et **moat-bytte** koster 4–8× en vanlig kildefiks (100–200 ord) — mellomschnauzer landet på +832. Skal en guide bytte helse-moat, planlegg ordkostnaden inn i Phase 1 framfor å trimme den bort i Phase 3.

#### Verktøyet

`tools/rangeringsdetektor.py` (commit `b8d8223`). Kalibreringsoppskrift i fila: kjent positiv = `git show 04ad4d2^:sections/hundetips-engelsk-bulldog.liquid` (må gi treff på BOAS-trio-rangeringen), kjent negativ = `jamthund` (0/0/0). Fasit v4: 3/3/0 · 2/3/0 · 0/0/0.

**Kjente begrensninger — loggført til neste kalibreringsrunde, bevisst ikke endret midt i bolk:**
1. **Popularitets- og registreringsrangeringer fanges ikke** (domenegatingen krever helse- eller kryss-rase-kontekst). Golden- og border-collie-ingressene ble funnet manuelt.
2. **Forfatternavn med `ä`/`ö`/`ü` klassifiseres som ukildet** — CITE-mønsterets `[a-zæøåé\-]` mangler dem. «Heikkilä 2011» havnet i T1 i stedet for T2.
3. **Sitering der årstallet står i forrige setning** gir falskt prev-treff («Beardow og Buchanans materiale på 394 hunder»).
4. Mendelske avlsratioer (25/50/25) gir falske prev-treff.

---

## NY VENTENDE BOLK — komma erstattet med semikolon i 14 filer (oppdaget 2026-07-31)

**Besluttet (Sondre 31.07): egen bolk ETTER C3, samme plass som FAQ↔schema-bolken. Ikke satt inn i C3c.**

Median-guiden i korpuset har **10 semikolon** i brødteksten. Disse 14 har **80–240 semikolon mot 3–20 komma**:

`cane-corso` · `coton-de-tulear` · `dansk-svensk-gardshund` · `dvergpinscher` · `dvergschnauzer` · `flat-coated-retriever` · `kortharet-vorstehhund` · `lagotto-romagnolo` · `malteser` · `mellomschnauzer` · `newfoundland` · `riesenschnauzer` · `vizsla` · `yorkshire-terrier`

**2835 semikolon totalt.** Alle 14 opprettet **16.–20. mai 2026** — én sammenhengende produksjonsperiode.

Symptomet, fra `mellomschnauzer`: «en hard; stri dobbeltpels» · «milde tilfeller er symptomfrie; mens alvorlige kan behandles» · «Brambilla og medarbeidere; 2020» · «FCI gruppe 2; seksjon 1».

**Sannsynlig årsak: `article_map`-kommaregelen anvendt på brødtekst.** Den gjelder **kun** Title/H2-felt i `snippets/llms-articles-data.liquid`, der komma er entry-separator og bryter parseren. Den har ingenting med artikkeltekst å gjøre. Samme feil ble gjort av Claude 31.07 i en FAQ-setning (`1;5-årsalder`) og fanget umiddelbart — forvekslingen er lett å gjøre.

**Karakter:** mekanisk og verifiserbart, uavhengig av kildesporet. Ikke et kildeproblem, men en user-visible lesbarhetsdefekt. Kan gjøres som én batch med maskinell erstatning + manuell gjennomlesing, siden noen semikolon er korrekte.

---

## Køen etter C3 (oppdatert 31.07) — TRE ventende korpus-bolker

Alle tre er **mekaniske og uavhengige av kildesporet**. De tas etter at C3 er ferdig, ikke satt inn underveis (Sondre 30.–31.07).

**1. FAQ↔schema-bolken — 19 filer** (opprinnelig 21). To ryddet underveis fordi filene uansett var åpne: WHWT (7 tegnsettingsavvik, C3c-3) og boxer (3 avvik, C3c-6). Prioritert `valp` (8 avvik) og `tannhelse` (7, helseartikkel), deretter `hund-liker-ikke-bading` (4), `aktivisere-hund-pa-tur` + `sommer` (2 hver), så 11 filer med ett avvik. Full tabell i registeret. **HARD-regelbrudd:** Google leser noe annet i rikresultatet enn siden viser.

**2. Semikolon-bolken — 14 filer, 2 835 semikolon.** Median-guiden i korpuset har 10; disse har 80–240 mot 3–20 komma. Alle 14 opprettet 16.–20. mai 2026, én sammenhengende produksjonsperiode. Årsak: `article_map`-kommaregelen feilaktig anvendt på brødtekst — den gjelder **kun** Title/H2-felt i `snippets/llms-articles-data.liquid`. Filer: `cane-corso` · `coton-de-tulear` · `dansk-svensk-gardshund` · `dvergpinscher` · `dvergschnauzer` · `flat-coated-retriever` · `kortharet-vorstehhund` · `lagotto-romagnolo` · `malteser` · `mellomschnauzer` · `newfoundland` · `riesenschnauzer` · `vizsla` · `yorkshire-terrier`. **Merk:** `mellomschnauzer` fikk delvis rydding i C3c-4 (nyskrevet tekst bruker komma), så fila er nå blandet.

**3. TOC-gap-bolken — 55 manglende ankerlenker fordelt på filer (NY, oppdaget 31.07).** Av 107 filer med TOC-JS mangler ankere lenke i innholdsfortegnelsen slik: **`faq` i 43 filer** (var 45; beagle og boxer rettet), `faq-heading` i 4, `tips-king` i 4, `oppsummering` i 3, `historie` i 3. Ankeret og H2-en finnes — bare TOC-lenken mangler, så seksjonen er unåbar fra innholdsfortegnelsen. **Rundt 62 filer har lenken allerede**, så dette er en splittet konvensjon, ikke en universell mangel. Rent mekanisk å fikse. **Metodenotat: funnet ble først meldt som «pre-eksisterende avvik i beagle-fila» — korpus-sveipen viste at det var korpusomfattende. Scop kontrollen til korpuset før du karakteriserer omfanget.**

**Øvrige køpunkter:**

4. **Gordon vs irsk setter vektmotsigelse** — krever FCI-standardene for begge raser, holdt bevisst utenfor C3a.
5. **«Hypoallergen» i meta-descriptions** — minst to forekomster (`coton-de-tulear`, `malteser`), korpuset ikke sveipet.
6. ~~`whippet`-guidens mankehøyde~~ — **strøket 31.07: funnet var falskt.** Guiden oppgir stratifiserte mål begge steder; «kun hannspennet» kom av substreng-telling uten å lese setningen rundt.

## Åpne Admin-steg — flate 3, kun i Shopify Admin (9 steg, full tabell i registeret)

Ingen blokkerer live-push. Samles til én runde.

| # | Side | Skal til |
|---|---|---|
| 1 | `riesenschnauzer` | «6x risiko (Bianchi 2020)» → Egenvall et al. 2000 |
| 2 | `irsk-setter` | «NKK #14» — venter på NKKs registreringsstatistikk |
| 3 | `italiensk-mynde` | «skjøre ben» ut — premisset brødteksten nå avviser |
| 4 | `hvor-mye-vann-hund` | bindestrek → tankestrek (kosmetisk) |
| 5 | `griffon-petit-brabancon` | «brachy-hensyn» → **«kort snute-hensyn»** |
| 6 | `border-collie` | «2. mest populære» → **«2. mest registrerte rase 2024»** |
| 7 | `whippet` | «raskeste hund per kilo» → **«en av de raskeste hunderasene i forhold til størrelse»** |
| 8 | `mellomschnauzer` | «pulmonisk stenose rasespesifikk hjertedefekt, levetid 13-16 år» — **begge nå avvist i brødteksten** → **«… den originale schnauzer-stamfar-rasen, NSBK 1946, RBM20-DCM med DNA-test, median levetid 13 år.»** |
| 9 | `boxer` | «… med NMBU-forskning og **NKK-avlsregler**» — avlsreglene er Norsk Boxerklubbs, ikke NKKs → **«… og Norsk Boxerklubbs avlskrav.»** |

## Verifiseringsregler etablert 30.–31.07 (gjelder alt videre arbeid)

1. **Sirkulær bekreftelse.** Et websøk kan returnere vår egen side som toppresultat med sammendrag ordrett fra guiden. Truffet to ganger på to dager (NMK-stiftelsesår, NAAF-standpunkt). **Finnes påstanden bare i vår egen tekst i søkeresultatene, er den ubekreftet.**
2. **Deler to tall nevner?** Når to tall fra samme studie står side om side, sjekk referansegruppen for hvert. FEH-paret 14 %/30 % delte den ikke.
3. **«X dokumenterer at …» er en verifiserbar påstand om et dokument.** Åpne det og søk. «NMK RAS dokumenterer 5 kg-taket» ga null treff i hele RAS.
4. **En flagget påstand kan ha egen dekning.** «Høyest før 1,5 år» sto i et avsnitt med dårlig kilde, men RAS sier det ordrett.
5. **Aldersgrenser er den hyppigst forskjøvne tallklassen.** Tre dager på rad: Jansen-vinduene (samojedhund), Beardow-tersklene (cavalier), Favrot-vinduet (WHWT). Sjekk aldersgrenser eksplisitt mot studien hver gang.
6. **To studier på samme rase med samme n er en konkret forvekslingsrisiko.** Salzmann 2011 og Favrot 2020 har begge n=108 WHWT.
7. **En ekte kilde kan bære et oppdiktet funn.** Farligere enn en oppdiktet sitering: bibliografien stemmer, formatsjekken passerer, bare resultatet er galt. Salzmann 2011 er korpusets tydeligste eksempel.
8. **Kontrollmetoden er like feilbarlig som innholdet.** To ganger på to dager lå feilen i kontrollen: substreng-telling uten å lese setningen (whippet-målene), og meta-mønster som krevde `name` som første attributt (falsk «ingen meta» på fem sider).
9. **Klubbattribuerte påstander verifiseres som blokk, ikke enkeltvis.** I `mellomschnauzer` sto én NSBK-påstand på fikselista; da klubbens avlsdokument faktisk ble åpnet, falt fem til. Er én påstand tilskrevet en klubb feil, kommer de øvrige i samme fil sannsynligvis fra samme ukontrollerte kilde. Samme mønster som «finner du én gal DOI, sjekk alle de andre i fila».
10. **En rasepåstand kan være arvet fra en nabo-rase.** Mellomschnauzer bar dverg- og riesenschnauzers PS-disposisjon som sin egen. **Ved raser i en familie med størrelses- eller fargevarianter: sjekk om disposisjonen tilhører rasen selv eller slektningen.** Første forekomst av feilklassen i korpuset.
11. **Et autoritativt domene er ikke automatisk primærkilde for en tredjeparts nøkkeltall.** NKKs regionside oppga «over 1000 medlemmer» for NSBK; klubbens egen side sier «i underkant av 1000». Katalog- og oversiktssider speiler ofte foreldet tekst.
12. **Rasestandardens egen historikk-seksjon er en underbrukt primærkilde.** FCI-standardene har en «Brief historical summary» som avgjorde tre påstander i `beagle` alene (pocket beagle-opphavet, at typen ikke forsvant, og Foxhound-nedavlingen). Vi har brukt standardene til mål og klassifisering, men sjelden til historikk. **Sjekk den før historiske påstander mykes eller strykes som ukildede.**
13. **Standarder oppgir ofte høyde, men ikke vekt.** Ingen av FCI #161, #159 eller #295 har vekt i det hele tatt. Vekttall som presenteres ved siden av standardfestede høydemål leses som standardkrav av leseren. **Sjekk hvert mål separat mot standarden, og merk anslag som anslag** — samme feilklasse som whippet-vekten (C3c-3) og fargeregelen i italiensk-mynde.
14. **Et treff i residual-sveipen kan være tekstens eget forbehold — eller en ekte overlever.** I `beagle` antok jeg først at «4–5 år» var vår egen setning om at tallet mangler dekning; kontekstlesing viste at det var en gjenglemt forekomst i §8s oppsummering. **Les alltid setningen rundt treffet før du avfeier det.** Utvidelse av regel 8.
15. **Dokumenttype er en egen påstandsklasse.** `boxer` kalte en fordypningsoppgave et «PhD-arbeid». Forfatter, år og institusjon var riktige hver for seg, så ingen formatsjekk slår ut. **For norske akademiske kilder: `hdl.handle.net`-handelen resolver nå til NVA/Sikt, og NVAs API oppgir `publicationInstance.type` eksplisitt.** Sjekk også at institusjonsnavnet fantes på publiseringstidspunktet — NMBU oppsto først i 2014 (jf. anakronisme-regelen for kennel-anerkjennelse i sprint #63).
16. **Når en studie kommer fra et program vi siterer ofte, er feil-attribusjon mer sannsynlig, ikke mindre.** Mastcellesvulst-studien er Shoop et al. 2015; O'Neill er 8. forfatter. Jeg var i ferd med å tilskrive den O'Neill fordi det er VetCompass-navnet korpuset kjenner. Samme mekanisme som ga «Pedersen et al. 2013» i samojedhund. **Les forfatterlista, ikke programnavnet.**
17. **Et sveipe-mønster bygget på den opprinnelige formuleringen finner ikke parafraser av samme tall.** I `boxer` sto «30–32 kg» igjen ett sted, og King-avsnittet sa «mellom 25 og 32 kg» — sistnevnte matchet ikke mønsteret i det hele tatt. **Manuell gjennomlesing av alle setninger i tallklassen slo den regex-baserte sveipen to sprinter på rad.** Etter en tallfiks: les alle setninger som nevner størrelsen, ikke bare de som matcher det gamle strengmønsteret.
18. **En rasestandard kan være utgått uten at noe i guiden ser galt ut.** `chihuahua` beskrev molera som rasetypisk og oppga mankehøyde i cm. Begge deler stemte med en ELDRE standard (og med AKC), men gjeldende NKK-versjon lister åpen fontanell som diskvalifiserende og sier eksplisitt at høyde ikke vurderes. **Sjekk alltid NKK-datoen på standarden, ikke bare FCI-datoen — og sjekk om standarden i det hele tatt normerer den dimensjonen guiden oppgir**, ikke bare om tallet stemmer.
19. **En kildeuthenting som oppgir feil land, dato eller temperament er mistenkt — ikke kilden.** FCIs egen chihuahua-PDF ble automatisk lest som «opprinnelsesland Belgia»; det var FCI-sekretariatets adresse i Thuin. Et gjettet PMID ga en artikkel om pasientsikkerhet i humanmedisin. **Når et felt ikke passer rasen, last ned dokumentet og les det selv.** De tre sterkeste funnene i bolken lå i dokumentet uthentingen hadde forvansket.
20. **En foreslått kilde kan falle i skrivefasen, og skal da falle.** Trachea-kilden overlevde kartleggingen fordi søketreffet sa «over-represented breeds»; ved gjennomlesing viste studien seg å være en kasusserie uten nevner — fordeling blant affiserte, ikke overrepresentasjon. **Kartleggingen godkjenner en kildekandidat, ikke en konklusjon.** Les hele studien før påstanden skrives, og vær villig til å svekke en påstand du allerede har fått godkjent.
21. **Les setningen ferdig, og les avsnittet etter.** `engelsk-setter` siterte NESK ordrett og korrekt — men stoppet midt i setningen, nøyaktig der meningen snudde, og avsnittet etter opphevet premisset for hele kapittelet. **Et sitat som er ordrett kan likevel være uredelig.** Ved klubb- og standardsitater: hent alltid hele setningen og minst ett avsnitt på hver side før du bruker det.
22. **Når guiden avviker fra allmenn kunnskap, men følger primærkilden, er det kilden som gjelder.** NKKs rasestandard skriver «Edward Lavarack»; historisk korrekt er *Laverack*. Guiden fulgte standarden. **Ikke «rett» bort fra primærkilden** — flagg avviket i registeret i stedet. Motstykket til regel 19: der var uthentingen mistenkt, her er allmennkunnskapen det.
26. **Ordestimatet skal regnes per H2 — og det bommer likevel.** To sprinter på rad bommet totalanslaget grovt: SBT anslag +400–600 mot faktisk +2583, dvergpinscher anslag +370 mot faktisk +1110. Etter SBT innførte jeg per-H2-budsjettering; dvergpinscher bommet fortsatt med faktor tre, og hele avviket lå i **én** seksjon (§9: budsjettert +260, faktisk +606). **Lærdommen er ikke at metoden er feil, men at seksjoner som får en ny kildeblokk — klubbkrav, avlsregler, en studies fulle resultatliste — konsistent koster 2–3× det prosaen alene skulle tilsi.** Legg inn den multiplikatoren for den seksjonen som mottar den nye kilden, og oppgi et bånd framfor ett tall. **Og meld fra om avviket før push, ikke etter** — det er Sondres beslutning om lengden, ikke en detalj å rydde stille.
25. **HTML-tagger skal aldri inn i JSON-LD-tekst.** Under skrivingen av `dvergpinscher` la jeg `<strong>` og `<em>` inn i et FAQ-svar. Fordi svaret speiles i både synlig HTML og FAQPage-schema, ville det både brutt 1:1-sjekken (som stripper tagger fra synlig side, men ikke fra schema) og gitt ugyldig praksis i strukturert data. **Ny fast kontroll i pre-publiseringsrutinen: `HTML-tagger i schema-tekst == 0`.** Beslektet observasjon: HTML-balansesjekken viser `div 31/28` og `section 1/0` på raseguidene — det er et **måleartefakt**, fordi `</article>` også finnes i produktkortene og den ikke-grådige regexen i korpusets audit-kommando kutter tidlig. Identisk i HEAD. Ikke «rett» den.
24. **En lav detektorscore er ikke et kvalitetsstempel.** `staffordshire-bull-terrier` ga T1=2/T2=0/prev=0 — laveste baseline i hele C3c — og viste seg å inneholde bolkens groveste feil: en klubbanbefaling framstilt som krav, to helserangeringer snudd av datagrunnlaget, og en myte presentert som dokumentert lokalhistorie. **Detektoren finner rangeringsspråk og ukildet prevalens. Den finner ikke regulatoriske påstander, mekanismer som ikke finnes, eller historiske påstander uten opphav.** Når en artikkels risiko ligger i juss, klubbregler eller historie framfor i tall, må kartleggingen gjøres manuelt uansett hva detektoren sier. Motstykket gjelder også: etter fiksen ga detektoren T1=3/prev=8, og **alle 11 var falske positive** — de tre rangeringstreffene var guidens egne *anti*-rangeringsforbehold. Høy score etter en fiks kan bety at teksten har fått bedre forbehold, ikke dårligere dekning. Les alltid treffet.
23. **Sirkulær bekreftelse virker begge veier.** I `fransk-bulldog` var jeg i ferd med å underkjenne en KORREKT regulatorisk påstand fordi et søketreff som «bekreftet» den viste seg å ha vår egen mops-guide som tredje treff. Regelen fra italiensk-mynde — «finnes en påstand bare i vår egen tekst i søkeresultatene, er den ubekreftet» — betyr **ubekreftet, ikke motbevist**. Gå til utsteders primærside før du konkluderer i noen av retningene. Her lå svaret på NKKs egen graderingsside, og guiden hadde rett hele veien.
27. **En seksjon som får en helt ny kildeblokk koster 3× prosaen — anta det, ikke regn det ut.** (Fastsatt av Sondre 03.08 etter tredje bom på rad.) SBT: anslag +400–600, faktisk +2583. Dvergpinscher: anslag +370, faktisk +1110. Engelsk springer spaniel: anslag +450–750, faktisk +1441 — og der hadde jeg *allerede* lagt inn 2×-multiplikatoren fra regel 26 og bommet med ytterligere en faktor to. Fordelingen var entydig: de to seksjonene som fikk ny kildeblokk stod for +716 av +1441 (§9 +412 mot estimert 120–200, §10 +304 mot estimert 150–250), mens de fire seksjonene uten ny kilde flyttet seg 0–27 ord til sammen. **Multiplikatoren skal ikke reberegnes per sprint — den meldes som et fast forbehold i Phase 1:** «seksjon X får ny kildeblokk, regn 3× prosa-estimatet.» Årsaken er strukturell, ikke sløv skriving: en ny kilde drar med seg forfatter, år, journal, n, referansegruppe, forbehold om utvalget og hva funnet *ikke* sier — seks–sju setninger som ikke fantes i den ukildede versjonen. Kildeforankring er dyrere enn prosa fordi den må bære sin egen etterprøvbarhet.
28. **En guides forskningsseksjon eldes selv om ingen rører den.** `norsk-elghund-sort` §9 var korrekt mot RAS 2021 og gal mot 2026: forekomsten var underrapportert med faktor tre (5–10 % mot Bergs 28,6 %), klinisk betydning ble presentert som uavklart etter at den var publisert, og arvegangen som ukjent etter at arvbarheten var estimert. **Når en guide siterer et RAS-dokument som sier «det pågår forsknings-studie», er det et utløpsstempel — søk opp om studien har publisert.** Klubbens egne oppdaterte notater (her AUNES 02.10.2025) er den raskeste inngangen, men gå videre til artikkelen: klubbnotatet ga tallet 28,6 %, primærtabellen bekreftet det.
29. **Et klubbnotat kan bære forskerens konklusjon bedre enn vår egen resonnering.** Guiden begrunnet fraværet av LTV-avlsrestriksjoner med effektiv populasjon og et «omvendt føre-var-prinsipp» — plausibelt, velskrevet og **lagt i munnen på AUNES**. Utvalgets egen begrunnelse var kortere og bedre: «før vi har flere svar enn spørsmål». **Når du tilskriver en aktør et resonnement, sjekk om aktøren har formulert det selv — parafraser den, ikke din egen rekonstruksjon.** Beslektet med regel 9 (klubbattribuerte påstander verifiseres som blokk) og med anførselstegn-regelen fra C3c-16.
30. **En yrkestittel er en verifiserbar påstand om en levende person.** «NMBU-forsker Karianne Nygaard» — Nationens byline sier «registrert oppdretter og eier av jaktpremierte hunder». Tittelen var ikke pynt: den ga et debattinnlegg forskningsvekt og flyttet tyngdepunktet i en pågående faglig strid. **Sjekk alltid bylinen/kildens egen presentasjon av en navngitt person før du gjengir rolle eller institusjon.** Samme klasse som feil fornavn i C3c-16 (Sigurd vs Renate Sjølie) — to sprinter på rad med personattribusjonsfeil.
31. **Et sitat kan være ordrett riktig og likevel feil tilskrevet — sjekk hvilket dokument det står i.** `pointer` siterte NKK fire ganger med «i sin rasestandard». Ordlyden stemte perfekt, men den står i NKKs **rasebeskrivelse** — rasepresentasjonen for valpekjøpere — mens rasestandarden er et eksteriør- og bedømmelsesdokument uten slike anbefalinger. NKKs egen side skiller mellom de to. **En rasestandard sier hvordan hunden skal se ut og bevege seg; den sier ikke hvem rasen passer for.** Ser du en «standard» som uttaler seg om egnethet som familiehund, alenetid eller aktivitetsbehov, er det nesten sikkert et annet dokument. Andre sprint på rad med sitat-attribusjonsfeil (mops/Sjølie i C3c-16).
32. **Å rette en rangering med en annen rangering er ingen fiks.** I `pointer` fjernet jeg «Pointer dominerer høyfjellsjakt-segmentet» og skrev i stedet «engelsk setter er den klart mest tallrike av de tre» — like ukildet, men den *føltes* som en oppmyking fordi den var mer beskjeden på rasens vegne. **Oppmyking betyr å fjerne rangeringen, ikke å flytte den til en annen rase.** Fanget i egen gjennomlesing samme økt. Beslektet med C2b-regelen om overkorreksjon, men motsatt retning: der reddet forsiktighet en korrekt påstand, her innførte forsiktighet en ny ukildet.
33. **En påstand om at «loven forbyr X» er den dyreste klassen vi har.** `pudel` hevdet at norsk dyrevelferdslov forbyr å klippe vibrisser, i en egen H3, med instruks om å kreve bekreftelse av hundefrisøren før betaling. Loven nevner ikke vibrisser. **Juridiske påstander har tre egenskaper som gjør dem verre enn andre feil:** de er sjekkbare mot én autoritativ tekst (så det finnes ingen unnskyldning), leseren kan ikke etterprøve dem selv uten juridisk kjennskap, og de får leseren til å konfrontere en tredjepart — her hundefrisøren — på feil grunnlag. **Slå alltid opp lovteksten på Lovdata, aldri en sekundærkilde.** Beslektet med regel 24: detektoren finner ikke juss.
34. **Å sitere riktig dokument beskytter ikke mot å gjengi feil innhold.** `pudel` navnga FCI-standard #172 med korrekt gyldighetsdato (01.08.2024) og beskrev deretter fargeseksjonen slik den så ut før den revisjonen — den nye standarden anerkjenner partifarget, tan-tegnet, trefarget og brindle, mens guiden skrev «alle FCI-anerkjente solide farger». Samme mønster som `chihuahua` (C3c-7). **En korrekt datert kildehenvisning er et signal om nøyaktighet som ikke nødvendigvis er innfridd — åpne dokumentet selv om datoen ser fersk ut.** Motstykket til regel 31: der var ordlyden riktig og dokumentet feil, her er dokumentet riktig og innholdet feil.
35. **Når en rettet påstand også er en utbredt misforståelse, adresser misforståelsen — ikke vår egen ordlyd.** Fastsatt av Sondre 04.08 etter `pudel`. Første utkast skrev «vi har tidligere skrevet at loven forbyr dette — det stemmer ikke». Korpuset retter stille; en metakommentar om egne feil er ikke innhold leseren har bruk for. Riktig form er «Mange tror det er forbudt i Norge. Det er det ikke» — som fanger opp at leseren sannsynligvis har hørt påstanden andre steder også, uten å gjøre vår historikk til tema.

### 2026-07-30 — C3b-3 dachshund (`eece6f1`, 1 fil live)

**🔴 Jensen-anbefalingen var forskjøvet med én og motsa guidens egen skala.** «4 eller flere kalsifiseringer» skulle vært «mer enn fire» (fem eller flere) — og guidens egen IDC-skala definerer nettopp 5+ som IDC 3. Feilen gikk i «for streng» retning: en oppdretter kunne avvist et avlsdyr Jensen ville godkjent. **Lærdom: når en guide oppgir både en gradert skala og en terskel, må terskelen sjekkes mot skalaen.**

**Min mistanke var feil for tredje gang samme dag.** «19–24 %» og «10–12 ganger» viste seg korrekt gjengitt fra DachsLife 2015 (Packer et al., Canine Genet Epidemiol 2016;3:8). C2b-regelen om overkorreksjon har nå reddet en påstand med dekning tre ganger på én dag. Men tallene er studiens *bakgrunnsoppsummering*, mens dens eget måleresultat er 15,7 % — nå merket eksplisitt, og variantfordelingen lagt til.

**Beste tilføyelsen i dag:** Standard Strihår topper Stigens kalsifiseringstall (27,1 %) og ligger nederst på klinisk IVDD hos DachsLife (7,1 %). Guiden advarte allerede om at kalsifisering ikke er klinisk sykdom, men det sto som en abstrakt reservasjon — nå viser et konkret tallpar hvorfor.

Purina fjernet som kilde, cervikal-rangeringen myket, Stigen 1991 fikk full referanse (Acta Vet Scand 32(2):197–203; utvalget var 16,1 % av alle NKK-registrerte dachshunder 1986–88).

**Neste:** samojedhund, deretter italiensk-mynde.

### 2026-07-30 — C3b-2 newfoundland (`67fb821`) + PRE-PUBLISERINGSPORT i produksjonsflyten

**🔴 Ny feilklasse: en gyldig DOI som peker på feil forskning.** `newfoundland` siterte «Stern et al. 2014; J Vet Cardiol; DOI 10.1016/j.jvc.2014.10.004» for SAS-arvegang. DOI-en resolver til en artikkel om pulmonal hypertensjon hos hund — ingen Newfoundland, ingen SAS. Riktig kilde er Hum Genet 133(9):1139–1148, DOI 10.1007/s00439-014-1454-0. **En velformet, resolverbar DOI beviser ingenting om innholdet, og består enhver automatisk lenkesjekk.** Den andre DOI-en i fila (Parker 2017) ble sjekket som følge og er korrekt.

**🔴 Meurs 2013 var en boxer-studie** brukt til å bære en Newfoundland-DCM-påstand (Abadie/Evans-klassen). Erstattet med Merck-forankring. I tillegg: SAS-prevalens-rangeringen strøket, «variabel ekspresjon» → inkomplett penetrans med avlskonsekvensen skrevet ut, PICALM konkretisert, Pyle & Patterson strammet, «rasespesifikk» myket i ingress + H2.

**NY FAST REGEL (Sondre): pre-publiseringsporten er nå et obligatorisk steg i produksjonsflyten**, ikke et dokument man skal huske. Gjelder **alt som skrives**, ikke bare det vi retter — målet er at nytt innhold er riktig fra første publisering. Sju porter (utvidet til **åtte** 06.08.2026 med live-meta-porten) — ingress først, sitering mot primærkilde, DOI åpnet og lest, referansegruppe ved rangering, presis tall-identifikasjon, verktøy mot prosa, stratifiserte tall stratifisert), koblet inn fire steder: sjekklisten selv, `CLAUDE.md` Phase 3, `.claude/rules/hundetips-articles.md`, og **generator-skillen**.

**Hullet lå i generatoren.** `hundetips-article-creator` — skillen som faktisk produserer nye artikler — hadde null referanser til sjekklisten, og dens 18 post-flight-checks er alle strukturelle. Ingen av dem kan fange en feil kilde eller et feilidentifisert tall. Uten denne koblingen ville kildesettings-prosjektet reprodusert seg selv på nytt innhold.

**Neste:** dachshund.

### 2026-07-30 — C3b-1 cane-corso + kortharet-vorstehhund (2 filer live)

**🔴 Glickman-multiplikatoren var oppdiktet i to guider, med to ulike tall.** `cane-corso` sa «tredobler GDV-risiko», `kortharet-vorstehhund` sa «øker med 110 %». Glickman et al. 2000 (JAVMA 217(10):1492–1499) rapporterer at ~20 % av GDV-tilfellene hos storraser kunne **tilskrives** høyt fôringsbrett — en attributabel andel, ikke et multiplikator. Begge hadde konvertert andelen til en multiplikator og landet ulikt. **Lærdom: når to av våre sider oppgir ulike multiplikatorer for samme funn, er begge sannsynligvis utregnet, ikke sitert.** De tre generelle artiklene som siterer samme studie er rene — de oppgir kun retning. Funnet kom fra korpus-sveip på studie-identifikator, regelen som ble formalisert dagen før.

**🔴 `cane-corso` DCM-prevalens 10–15 % hvilte på PetMD** (kommersiell kilde) og finnes ikke i noen fagfellevurdert studie — Merck lister ikke engang rasen blant de DCM-disponerte. Tallet, rangeringen og PetMD strøket. **Ikke overkorrigert:** ekko-screening fra 2 år står, med eksplisitt setning om at ingen rasespesifikk prevalensstudie finnes.

**Prosessendring (Sondre):** etter fjerde ingress-forekomst på rad er **ingress-først nå et fast steg i kartleggingen**, ikke bare en etterkontroll — rekkefølgen er ingress → faktastripe → recap → FAQ/schema → §-avsnitt. Skrevet inn i `docs/artikkel-sjekkliste.md` seksjon A, sammen med fella at `grep | cut` kan kappe treffet på en lang ingress-linje og se rent ut.

**Metodefunn:** retry gjelder også sekundære live-sjekker. En kryss-guide-konsistenssjekk uten retry ga falsk «gammelt innhold» på begge sider rett etter at hovedverifiseringen passerte og sha256 matchet HEAD.

**Neste:** newfoundland.

### 2026-07-30 — C3b-0 (`6d27fb0`, 2 filer live) + C3b kartlagt

**🔴 `malteser` bar den feilen C1b rettet i `yorkshire-terrier`.** Guiden siterte JAAHA-DOI-en for at Yorkshire Terrier har «omtrent 35 ganger forhøyet risiko sammenlignet med hundepopulasjonen generelt» — alle tre defektene C1b fikset, fortsatt live. **To av våre egne sider motsa hverandre om samme tall fra samme studie i seks dager.** C1b-sveipen fant riktig den femte forekomsten i yorkshires ingress, men krysset aldri filgrensen. **Lærdom: korpus-sveipen ved en tallfiks må kjøre på studie-identifikatoren (DOI, forfatternavn), ikke bare på tallet — og på tvers av filer.** Rettet til C1b-fasiten; kryss-guide-konsistens verifisert på live.

**✅ `riesenschnauzer` 6×-tallet hadde full dekning — mistanken min var feil.** Primærkilden er Egenvall et al. 2000 (Veterinary Record 146(18):519–525), en svensk epidemiologisk kartlegging av forsikrede hunder, sitert i Bianchi 2020s bakgrunn. Navngitt i §8 og faktastripen. **C2b-regelen om overkorreksjon har nå spart oss to ganger** — hadde tallet blitt mykt i C3a, ville en påstand med full dekning blitt fjernet. Kildepolicy avklart samtidig: forbudet mot Agria gjelder kommersielle aktører som *autoritet*, ikke fagfellevurdert forskning som *bruker* et forsikringsregister som datakilde — samme kategori som VetCompass.

**C3b kartlagt: 36 guider gjenstår.** Detektoren har fortsatt støy (`Crufts 1936`, `Bernhardspasset 1050`, `Før 1900` teller som siteringer), så fem–seks guider er rangert for høyt; bunnsjiktet på 12 guider uten kvantitative markører er reelt. Rekkefølge etter alvorlighet, ikke rå score: **cane-corso** (DCM-prevalens 10–15 % hviler på PetMD — kommersiell kilde, samme policyklasse som Hill's/Orvis) → **newfoundland** (seks rangeringspåstander, «høyeste rase-prevalens» for SAS) → **dachshund** (10–12× IVDD-multiplikator tilskrevet «større populasjonsstudier», ingen navngitt studie) → **samojedhund** (Jansen/Zheng uverifisert + allergen-rangering) → **italiensk-mynde** (lettest).

**Neste:** cane-corso.

### 2026-07-30 — Bolk C3a FULLFØRT (`d4ae954`, 7 filer live)

Seks raseguider kildeverifisert mot primærkilde: `berner-sennenhund`, `vizsla`, `irsk-setter`, `rottweiler`, `riesenschnauzer`, `coton-de-tulear`. C3-omfanget er 42 guider etter detektor-rekalibrering (tredje bolk på rad der omfanget måtte korrigeres for målefeil — whippet ga falsk null fordi mønsteret manglet STOP-liste for landsnavn og klubbforkortelser).

**🔴 Den navngitte norske kilden i `berner-sennenhund` finnes ikke.** «46 % av norske bernere dør av kreft (NVH 2014)» lot seg ikke finne i noen indeksert database, og sto i fem flater sammen med 6,9 år. Det som gjorde det verre enn et vanlig ukildet tall: guiden *forklarte* avviket mot Dobson 2012 med «ulik metodikk og noe forskjellig populasjon» — en metodologisk begrunnelse for spriket mellom et verifisert tall og et tall som muligens ikke eksisterer. Naboavsnittet ga påstanden falsk troverdighet. Strøket; Dobson 2012 (n=394) er nå bærende, og Ruple &amp; Morley 2016 forankrer HS-rangeringen (225× risiko, 17× dødelighet, livstidsrisiko opptil 25 %).

**🔴 `irsk-setter` rcd1-frekvens var ~4× for høy.** «Over 30 prosent på tidlig 1990-tall» → verifisert 7,8 % bærerfrekvens (34 av 436 klinisk normale, ISCA 1994–97, J Hered 90(1):143). Oppdagelsen co-krediteres Suber (Cornell) og Clements, begge 1993 uavhengig.

**🟡 `rottweiler`: vår egen divisjon presentert som studiefunn.** OR 13,30 (KI 10,55–16,75) erstatter studiens abstraktsammendrag «over 10». «Mer enn 30 ganger lavere risiko enn Rottweiler» var 10 ÷ 0,30 — regnet fra det understatede tallet, og bichon/fransk bulldog ligger på eksakt 0,30, ikke under. Strøket. 40 kg+ OR 45,44 lagt til.

**🟡 `riesenschnauzer`: samme populasjon talt to ganger.** Alle tre siteringer verifisert (Bianchis IFNA-delesjon ER beskyttende — guiden leste den riktig, tittelen er misvisende). Men «opptil 16 % i svenske kohorter» er Bianchis bakgrunnsoppsummering av nettopp Ferm-materialet guiden alt siterer som 7,2 %.

**🟡 `vizsla`: abstraktet avgjorde uten fulltekst.** Zink 2014 beregner odds per alder ved gonadektomi og per kjønn for hemangiosarkom; de fire tallene guiden oppgav kollapset tre strata til ett og står ikke i abstraktet. Stratifisert innramming + eierundersøkelse-forbeholdet inn.

**✅ `coton-de-tulear`: Zeng 2011 helt ren.** YMYL-fiksen var «aldri mer enn 4–6 timer uten mat» — en ukildet hard terskel. Kryssjekk mot `chihuahua` viste måltidsfrekvens-rammen (3–4 daglig, ingen timegrense), så det var ingen tallmotsigelse å harmonisere. Varseltegn + vet-kontakt lagt til; guiden manglet dem.

**To metodefunn.** Cache-rotasjonen var verre enn i Bolk B: berner og rottweiler krevde forsøk 3, riesenschnauzer 6 av 6 — én henting ville gitt falsk FAIL på halve batchen. Og sha256-kontrollen ga falsk DIFF på alle syv filer fordi `shopify theme pull --path` ikke oppretter katalogen selv; «alle feiler» er samme mistenkte-resultat-klasse som «alle består».

**Bekreftet lukket:** root `/llms.txt` serverer nå den kuraterte lista (124 `/pages/`-lenker) — den gamle åpne saken om native UCP-boilerplate på root-varianten gjelder ikke lenger.

**Tre åpne punkter logget i registeret:** riesenschnauzer «6× risiko» (mistenkt Wilbe-haplotype-sammenblanding; meta-description tilskriver den til den beskyttende studien) skal verifiseres **før C3b starter**; irsk-setter NKK #14 holdt tilbake med koblingen at meta-feltet må endres samtidig; coton «hypoallergen» i meta til generell bøtte.

**Neste:** C3b — kartlegg neste gruppe av de resterende 36 C3-guidene, samme prosess.

### 2026-07-30 — Bolk C1b FULLFØRT (`686e5ef`, 2 filer live) — alle YMYL-hull lukket

Begge kildeblokkerte guider er ferdige. **Ingen åpne YMYL-hull igjen i raseguide-sporet.**

**🔴 `yorkshire-terrier` — tre lag feil på samme tall.** Guiden siterte to ulike Tobias-2003-artikler og byttet om på dem: JAAHA-artikkelen er en pedigree-/arvegangsstudie på 82 hunder av én rase, mens rase-risikotallet tilhører Tobias & Rohrbach (JAVMA, 2 400 tilfeller). En pedigree-studie på én rase kan ikke produsere et rase-relativt risikotall. I tillegg feil verdi og feil referansegruppe: «35 ganger enn generell hundepopulasjon» → **36 ganger enn alle andre raser samlet** og **59 ganger enn blandingshunder**. Spriket mot UFAWs 60× var referansegruppe, ikke motsigelse — tredje gang batch 2-fella opptrer. Femte forekomst lå i ingressen, fanget av negativkontrollen.

**🟡 `strihaaret-vorstehhund` — min flagging var feil.** RAS-dokumentet bekrefter Ne=186, innavlsgrad 1,8 % (1947–2013) og HD 92 %/4,2 %/3,8 %. Den beroligende konklusjonen jeg meldte som guidens overtolkning er **raseklubbens egen**, nesten ordrett. Jeg lot en generisk bevaringsgenetisk terskel (Ne<500) overstyre fagvurderingen til dem som forvalter rasen; klubbens mål — innavlsøkning 0,3 % per generasjon — er mer relevant for en levende avlspopulasjon. **Lærdom: en tommelfingerregel er også en referanseramme og kan brukes feil på samme måte som et oddsforhold.**

**Neste:** C3 — de ~30 guidene som har kilder, men der siteringene ikke er spot-sjekket.

### 2026-07-30 — Bolk C2b FULLFØRT (`5bbc283`, 3 filer live)

Ren oppmykning av `pomeranian`, `schaferhund`, `norsk-buhund` — ingen nye kilder hentet. To oppdiktede autoriteter og fire ukildede tall fjernet i pomeranian; historisk presisjon uten kilde myket i schaferhund; tre lag konklusjon på ett års øyeblikksbilde skilt fra det målte tallet i norsk-buhund.

**⚠ Overkorreksjon unngått — ny regel.** Planen var å myke rangeringen «Alopecia X rammer pomeranian høyere enn noen annen rase». Brødteksten attribuerte den til AKC Canine Health Foundation med direkte sitat. Rangeringen ble beholdt; defekten var at FAQ og schema gjentok den *uten* attribusjonen. **Speilbildet av korpusets vanlige feil** — normalt overdriver FAQ, her underforankret den. Sjekk brødteksten for attribusjon før du myker en rangering: å fjerne en påstand som har dekning er også en feil.

**Tredje-forekomst-fella:** «Vestlig veterinærdermatologi» hadde en søskenformulering med annen bøyning som `replace_all` ikke traff. Fanget av negativkontrollen, ikke av planen.

**Admin-steg lukket:** rhodesian-ridgeback meta-description bekreftet byttet til «khoikhoi-hund» i alle tre variantene, live-verifisert over tre hentinger.

**Neste:** skaffe JAVMA-fulltekst (Tobias & Rohrbach 2003) og raseklubbens RAS-dokument før C3. Hvis 35× ikke lar seg bekrefte etter fulltekst, mykes tallet framfor å velge mellom 35× og UFAWs 60×.

### 2026-07-30 — Bolk C2 delvis fullført (`40765d1`, 2 filer live)

**Manuell null-verifisering var avgjørende.** Et rent detektor-resultat sa ingenting om hvilken guide som faktisk hadde mest ukildet helseinnhold: `pomeranian` slo ut med null prosenttall og null årstall, men har 32 helsepåstand-setninger. `irsk-setter` slo ut med 17 «årstall» — alle historiske. Regelen fra i går («ikke stol på et rent resultat uten å sjekke det») holdt.

**🔴 `australian-shepherd` — legemiddelsikkerhet.** 50 % MDR1 er korrekt (WSU VCPL), men åpningsavsnittet sa «omtrent halvparten av alle aussier reagerer ekstremt annerledes», mens guidens egen status-liste rett under korrekt skilte bærere (moderat) fra homozygot affiserte (dramatisk). 50 % omfatter begge. Skillet nå eksplisitt i fem flater. «Nedarves autosomalt recessivt» rettet — den formuleringen var selve kilden til sammenblandingen.

**🔴 `gordon-setter` — kryss-sykdom-sammenligning.** «29 % HA-CA-bærere … høyere enn CLAD-bærerfrekvensen hos irsk setter (12 %)» sammenlignet to ulike sykdommer på tvers av to raser. Fjernet. Geografi rettet: n=82 er Skandinavia **og** USA, ikke Skandinavia alene.

**Ny åpen sak — Gordon vs irsk setter vektmotsigelse.** Gordon-guiden kaller rasen «tyngst av setterne» ved 25,5–29,5 kg og «merkbart kraftigere enn irsk setter»; irsk-setter-guiden oppgir 27–32 kg. Fem speilingsflater. Trolig ulik målebasis (FCI-idealvekt per kjønn vs generelt spenn) — samme klasse som bulldog-motsigelsen i batch 2. Ikke rørt; krever FCI-standardene for begge raser.

**Gjenstår:** C2b-oppmykning (`pomeranian`, `schaferhund`, `norsk-buhund` — trenger ikke kilder, trenger å slutte å påstå presist), samt `yorkshire-terrier` og `strihaaret-vorstehhund` som fortsatt venter på JAVMA-fulltekst og RAS-dokument.

### 2026-07-30 — Bolk C1 FULLFØRT (`e3c8eb9`, 2 filer live) + scoping-korreksjon

**⚠ Registerets «38 raseguider uten navngitt kilde» var feil — reelt tall er 13.** Detektoren bak tallet krevde `et al.` og var blind for enkeltforfatter-siteringer, PMC-IDer og DOI-er. `whippet` sto oppført med null kilder, men har `Mosher 2007` og `Stern 2015`; `yorkshire-terrier` har `Tobias (2003)` + DOI. Desimal-prevalens uten sitering: 8, ikke 17. **Lærdom: detektoren som definerer en bolks omfang må kalibreres mot kjente positive FØR tallet skrives inn i registeret — ellers arves målefeilen som prosjektplan.** Bolk D er dermed langt mindre enn antatt; Bolk C tettere av alvorlige funn.

**🔴 `welsh-corgi-pembroke` — allelfrekvens som bærerfrekvens, seks steder.** 55,49 % er allelfrekvens, ikke bærerandel. Faktisk fordeling (Animals 2024, n=91): 23,08 % frie, 42,86 % bærere, **34,06 % homozygot i risiko**. Feilen skjulte tallet en valpekjøper trenger — at en av tre testede corgier har to kopier sto ikke i guiden i det hele tatt. Samme klasse som prcd-feilen i cocker (Bolk B), men motsatt retning: cocker underdrev, corgi skjulte.

**🔴 `sibirsk-husky` — retningsfeil.** «30,5 % HD-fri» → 30,5 % fikk toppkarakteren «excellent»; «2,2 % alvorlig grad» → 2,2 % var dysplastiske i det hele tatt. Reelt HD-fri ~97,8 %. Avsnittet motsa seg selv i begge ender.

**Holdt tilbake bevisst:** `yorkshire-terrier` (35× lar seg ikke bekrefte; UFAW sier 60× mot blandingshunder — enten er tallet eller referansegruppen feil) og `strihaaret-vorstehhund` (Ne=186 med beroligende konklusjon, ukildet). Krever JAVMA-fulltekst hhv. raseklubbens RAS. **Å bytte ett ubelagt tall mot et annet er ikke en fiks.**

**Verktøystatus:** Shopify CLI-auth virker nå fra Claudes skall — preview- og live-push kjørt uten manuell overtakelse for første gang siden Bolk B.

**Neste:** Bolk C2 (13 reelt ukildede), med manuell verifisering av hver «null».

### 2026-07-30 — Bolk B FULLFØRT (`6d048e2`, 7 filer live)

Seks raseguider (`cocker-spaniel`, `labrador-retriever`, `flat-coated-retriever`, `rhodesian-ridgeback`, `weimaraner`, `dvergschnauzer`) + `llms-articles-data`. **Den justerte linsen fra Bolk A holdt:** tallene var nesten uten unntak korrekt gjengitt, og alle 14 funnene lå ett nivå over sifrene — fem rangeringsfeil, fire årstalls-/metadatafeil, tre slutninger studiene ikke støtter, to interne selvmotsigelser.

**Alvorligste funn — `weimaraner` vaksinasjonsråd.** Guiden ga et konkret medisinsk råd basert på et utvalg som utelukkende besto av syke valper, uten kontrollgruppe. Etter Sondres skjerping ble også «bekreftet autosomalt recessiv arvegang» **strøket framfor myket** — ingen mutasjon er identifisert. Prinsippet er nå etablert på tvers av eldre-hund (batch 5) og denne: *der terskelen eller rådet kan påvirke en beslutning, mykes aldri konklusjonen — den fjernes hvis den ikke holder.*

**To rangeringsfeil av engelsk-bulldog-typen:** `cocker-spaniel` gjorde otitt til vanligste diagnose (periodontitt er nr. 1 med 20,97 % mot 10,09 %), og `labrador-retriever` påsto førsteplass i NKKs statistikk (2024: golden nr. 1, border collie nr. 2, labrador nr. 3). **Feil gen:** EIC er DNM1, ikke DYNC1. **Feil sitering på riktig tall:** Abadie 2009 er en berner-studie; flat-coats 20 % står i Evans 2021.

**Ekstra funn — fabrikkert screeningkrav.** `weimaraner` ba valpekjøpere kreve vWD-DNA-test i fem posisjoner; testen finnes ikke for rasen. Fjernet. Ny regel: en screeninganbefaling er en påstand som må verifiseres som enhver annen.

**Metode-lærdom (to egne feil):** (1) Jeg påsto to ganger at preview ikke kunne curl-verifiseres, med henvisning til sjekkliste D — mens `gotchas.md` gotcha #11 hadde dokumentert cookie-jar-løsningen dagen før. Kryssreferanse lagt inn i `artikkel-sjekkliste.md` D. (2) Cache-rotasjon traff `cocker-spaniel` på live: 2 av 6 hentinger med unik cache-buster ga gammelt innhold. Retry til alle nye strenger treffer er nå påkrevd — én henting er ikke bevis.

**Admin-steg LUKKET samme dag:** `rhodesian-ridgeback` meta-description byttet til «khoikhoi-hund» i alle tre variantene; live-verifisert med cache-buster.

**Neste:** Bolk C (desimal-prevalens uten sitering — `welsh-corgi-pembroke`, `vizsla`, `riesenschnauzer`, `strihaaret-vorstehhund` m.fl.), deretter Bolk D (38 uten navngitt kilde).

### 2026-07-29 — RASEGUIDE-SPORET startet: Bolk A (`04ad4d2`, 2 filer live)

**Kartlegging av 60 raseguider:** 3 med oddsforhold, 17 med desimal-prevalens, 10 med `et al.`-sitering, 18 med journalreferanse — og **38 helt uten navngitt kilde i brødteksten**. Kartleggingen 24.07 sa «0 uten kilde» for raseguidene; målt inne i `<article>` er bildet et helt annet. Raseguidene er ikke i vesentlig bedre forfatning enn de generelle var.

**Detektoren tok feil tre ganger før tallene holdt:** (1) 1 oddsforhold av 60 = nær-null, mistenkt — `<strong>19,2 ganger</strong> så stor` er ikke sammenhengende med tagger; (2) «Velg et al» i fire guider = «Velg et **al**ternativ», løst med årstall-krav; (3) sitat-telling falt 21→10 mellom kjøringer, men det var scope-endring til `<article>`, ikke reelt fall. Kalibrert mot både kjente positive og kjente falske positive før tallene ble brukt.

**🔴 Bolk A-hovedfunn: alle tall stemte, konklusjonen var feil.** Ti av elleve verifiserte tall var eksakt korrekte, inkl. mutasjonskoordinater i lagotto-guiden. `engelsk-bulldog` hadde riktige tall fra riktig studie (BOAS OR 19,20; ≥1 lidelse OR 2,04; hudfoldedermatitt OR 38,12) men påsto at rasen var «høyest av BOAS-trioen» — fransk bulldog har ~31× odds i sin egen studie, og på målt prevalens er engelsk bulldog **lavest** av de tre (19,5 / 20,0 / 26,5 %). Samme mekanisme som bulldog-«motsigelsen» i batch 2, men her ga den en rangering stikk motsatt av datagrunnlaget.

`greyhound`: tallene stemte mot O'Neill 2019 og Martinez 2020, men osteosarkom-studien var datert 2018 i stedet for 2023 (3 steder), og sekundærtilstandene sto i feil rangering uten nedgrodde klør (11,1 %). La også til at populasjonssnittet er 0,037 % og at skotsk hjortehund og leonberger ligger høyere enn greyhound — uten det leser 0,62 % som om greyhound er verst, samme rangeringsfelle som nettopp ble fjernet fra bulldog-guiden.

`lagotto-romagnolo`: ingen endring, best kildesatte guide i bolken.

**Justert metode for Bolk B:** tallene i raseguidene er stort sett riktige. Risikoen sitter i **hva guiden påstår med tallene** — rangeringer, «høyest av», sammenligninger på tvers av studier med ulike referansegrupper. Bolk B (flat-coated-retriever, weimaraner, cocker-spaniel, labrador-retriever, rhodesian-ridgeback, dvergschnauzer) leses med den linsen. Deretter Bolk C (desimal-prevalens uten sitering) og Bolk D (de 38 uten kilde). Foreslått rekkefølge #1–8 i én bolk (valp-de-forste-ukene, hund-smerte-tegn, hund-slikker-ansikt, hund-tisser-inne, klippe-klor-hund, hvor-mye-vann-hund, hund-rister-pa-hodet, hund-spiser-avforing). `orebetennelse-hund` og `hund-darlig-ande` er billige — kildene er allerede hentet i batch 2. **Raseguide-korpuset er eget spor:** 146 Griffon-forekomster i 93 filer (53 i body, 28 filer) er navnekonsistens fra `e298130`, ikke kildeverifisering. Raseguidene bruker prevalenstall og oddsforhold tungt og trenger spot-sjekk av alle siteringer mot primærkilde — batch 2 viste hvorfor.

### 2026-07-29 — Raseguide-hub «description»-drift kartlagt (ingen fiks utført)

**Utløser:** Pre-push-snapshotet i King-batchen viste at `templates/page.raseguider.json` i repo har `description` på 21 kort som live mangler helt.

**ÅRSAK — Shopify stripper udeklarerte block-settings ved opplasting.** `raseguider-grid.liquid`-schemaet deklarerer `description` på blokktypen `featured_article`, men **ikke** på `article_card`. Alle 60 blokkene i malen er `article_card`. Shopify dropper settings som ikke er deklarert i blokkens schema.

**Bevis (naturlig eksperiment):** preview-temaet `#149856485454` fikk fila med alle 21 descriptions i en full push under King-batchen. Pull-back returnerte **0**. Ingen har rørt preview i theme-editoren. Repo 21 → push → pull → 0 på to uavhengige temaer. Strippingen skjer altså i opplastings-/valideringslaget, ikke i theme-editoren. (CLI alene kan ikke skille «strippet ved opplasting» fra «lagret men ikke lest ved pull» — operasjonelt er det uten betydning: fiksen er den samme, deklarer feltet i schemaet og push på nytt.)

**VIKTIGERE FUNN — feltet ville aldri rendret uansett.** `article_card`-grenen (linje 83–135) har **null** referanser til `block.settings.description`. Kun `featured_article`-grenen (linje 58–59) rendrer det, og malen har **0 featured_article-blokker**. `.mh-hub__featured-desc` finnes på live kun som CSS-regel, aldri som HTML-element.

**KORRIGERING av min egen tidligere vurdering:** jeg beskrev dette som at «21 kort mangler beskrivelse på live — det påvirker hvordan hubben leses av både brukere og crawlere». **Det var feil.** De 21 verdiene er død data i repoet og har vært det siden 2026-05-15. Ingen live-regresjon, ingen synlig effekt, ingen SEO-effekt. Verifisert mot rendret live-HTML: 61 `mh-hub__card-title`, 0 kort-beskrivelser, og ingen av prøvestrengene finnes.

**Historikk:** `description` ble lagt til én per sprint fra sprint #10 (Staffordshire, 2026-05-15) t.o.m. sprint #33 (Sankt Bernhardshund, 2026-05-18) — sprint #28/29/30 hoppet over det. Praksisen **opphørte helt fra sprint #34**; de 39 senere kortene har aldri hatt feltet. Det er altså et forlatt mønster, ikke et regressjonstap.

**Omfangs-sjekk:** hundetips-hubben (`hundetips-grid-2`) har **ingen** udeklarerte settings — problemet er isolert til `raseguider-grid`. Eneste udeklarerte felt i hele raseguider-malen er `description` på de 21.

**Ingen fiks utført — kartlegging bestilt, ikke reparasjon.** Reelt valg senere: (a) fjern de 21 døde feltene fra repoet så det speiler live, eller (b) deklarer `description` i `article_card`-schemaet + legg til rendering i kort-grenen + fyll ut de 39 manglende — altså en bevisst designendring av hubben, ikke en «fiks».

**Øvrige to driftfunn — notert, ikke prioritert:** `templates/page.yorkshire-terrier.json` (live har `"settings": {}`, repo utelater nøkkelen — kosmetisk normalisering) og `locales/en.default.schema.json` (JSONC-parse-avvik i Shopifys auto-genererte språkfil). Ingen av dem er fra King-batchen.

### 2026-07-29 — King-boks fakta-batch deployet live (commit `e298130`, 97 filer)

**Utløser:** King-boksen skulle forbedres visuelt, forkortes og faktarettes. Sondre delte i to runder: **fakta først, alene** — visuelt/tekstlengde i egen runde etterpå.

**Kartleggingsfunn:** Ingen delt snippet. Tre helt separate King-komponenter, alle inline: (A) sidebar-boks `mh-article__tips-sidebar` × **122 filer**, (B) body-H2 «Tips fra King» × **73 filer** (median 205 ord), (C) produktside-boks `mh-king-layout` × **10 filer** (inline styles + foto). **205 forekomster i 132 filer.** Visuelt en ren to-deling, ikke tilfeldig drift: mørk grønn gradient på alle generelle hundetips (62), lys krem/grønn tint på alle raseguider (60) — kun `docs/page-patterns.md:85` dokumenterte den mørke.

**BESLUTNING — 5 kg er kanonisk.** Korpuset hadde tre konkurrerende vekter (`4,5 kg` 27 filer, `5,2 kg` 28 filer) pluss fem prosa-varianter. `chihuahua` og `cocker-spaniel` motsa seg selv internt (body vs sidebar). Kun `border-collie` og `golden-retriever` var korrekte fra før.

**BESLUTNING — multiplikator-påstander må reberegnes ved enhver vektendring.** 11 artikler regner «X ganger min vekt» ut fra Kings vekt; 4,5 → 5 gjorde dem feil. Rettet: rhodesian-ridgeback (åtte→sju), riesenschnauzer ×2 (åtte-elleve→sju-ti), weimaraner ×2 (nesten ti→seks-åtte), newfoundland ×2 (tretten-femten→tolv-fjorten), vizsla ×2 (fire-sju→fire-seks), flat-coated ×2 (tretti→seks — feil også før batchen: 25/4,5 = 5,6). Regelen er dokumentert i `docs/products.md`.

**BESLUTNING — Griffon-prefiks kun i sidebar denne runden.** De 74 sidebar-boksene sier nå «Griffon Petit Brabançon» (i tråd med raseguidens egen H1). Body-teksten sier fortsatt «Petit Brabançon» — 238 forekomster, bevisst utsatt til runde 2 sammen med body-H2-varianten. **Midlertidig, ikke permanent, intern inkonsistens — godkjent av Sondre.**

**To funn som kartleggingen bommet på, fanget under gjennomføring:**
1. **`layout/theme.liquid`** — cedille-feil i den nettstedsomfattende Organization-JSON-LD-en, som rendrer på **hver eneste side** og beskriver King til Google/AI-crawlere. Kartleggingen skannet kun `sections/`, `snippets/`, `templates/` — ikke `layout/`. Fanget først da render-verifisering av preview flagget cedille på alle fem testsider. Sannsynligvis den mest synlige enkeltforekomsten i batchen.
2. **`weimaraner.liquid:124`** — en 11. multiplikator. Sveipet krevde 60 tegn foran «ganger», så linjer der uttrykket sto tidlig falt ut. **Lærdom: ikke ankre korpus-sveip på fast lookbehind-bredde.**

**IKKE endret:** 226 g fødselsvekt på forsiden (bekreftet korrekt av Sondre). Body-H2 (73 filer) + visuell redesign + snippet-uttrekk av de 122 CSS-blokkene = egen runde.

**Metodisk gjennombrudd — curl-preview av upublisert tema virker.** Gotcha #11 slo fast at `preview_theme_id` strippes på domene-redirecten og at «curl can't replicate the cookie handshake». Det er nå motbevist: en cookie-jar (`-c` + `-b`) overlever redirecten. Prime sesjonen mot store-roten én gang, deretter rendrer alle påfølgende fetch det upubliserte temaet. **Krever alltid en diskriminator-streng som kun finnes på preview** (her: live `/pages/hvor-mye-vann-hund` → 0 treff på `tips-sidebar-link`, preview → 3) — uten den kan man ikke skille «preview rendrer riktig» fra «jeg falt stille tilbake til live». Dette **tetter hullet i `.claude/rules/template-deletion.md` Step C**, der curl-verifisering hittil stille validerte mot LIVE.

**Deploy-funn — live/repo-drift oppdaget i pre-push-snapshot.** Full pull av live før push viste 196 filer som avvek fra HEAD. 200 av 203 JSON-avvik var kun Shopifys auto-genererte kommentar-header (JSONC). **Tre er reell drift, ikke fra denne batchen:** `templates/page.raseguider.json` (repo har `description` på 21 raseguide-kort som live mangler helt), `templates/page.yorkshire-terrier.json` (tom `settings: {}`), `locales/en.default.schema.json`. **En full `theme push` ville overskrevet live med repo-versjonen.** Pushet derfor med 95 eksplisitte `--only`-flagg. Verifisert etterpå: 95/95 batch-filer identiske med HEAD, **0 filer utenfor batchen endret**. → **ÅPEN OPPGAVE: raseguider-hub-driften må undersøkes separat.**

### 2026-07-28 — Produktkort inn i hvor-mye-mat + hund-kaster-opp (preview-godkjent, live pending)

**Utløser:** GA4 viser at 95,1 % av øktene siste 30 dager avsluttes uten at brukeren ser en produktside. Tre høyest-trafikkerte artikler uten kjøp kartlagt: hund-om-sommeren (248 visn./91 landinger), hund-kaster-opp (100/88), hvor-mye-mat (90/80).

**Kartleggingsfunn:** Ingen av de tre hadde hund-og-reise-problemet (produkt omtalt uten lenke) — alle produkthandles 200. Problemet var dybde og synlighet. Målt på live-HTML: hund-om-sommeren har over-fold produktboks på 4 % og er allerede riktig bygget (0 kjøp der er ikke et lenkeproblem — sannsynligvis produkt-match/intensjon). hund-kaster-opp hadde første produktlenke på 31 % som ren tekstlenke og **null produktbokser i hele fila**. hvor-mye-mat hadde ingenting før 93 %. **Strukturelt funn på tvers:** sidebar-produktbokser er verdiløse på mobil — `.mh-article__sidebar` ligger utenfor media-queryen og stables nederst i DOM, under bunn-CTA og «Les også». «Vi har produktboks på den siden» kan være sant på desktop og usant for 90 % av trafikken.

**BESLUTNING — plassering avviker bevisst fra reise-mønsteret.** Sondre ba først om samme plassering som `productduo` på reise-til-utlandet (15 % ned). Avvist etter begrunnelse på begge sider: (1) **hvor-mye-mat** har en hoppebanner på linje 34 (`scrollIntoView` til `#kalkulator`) — alt mellom 0 og 32 % hoppes fysisk over av de mest engasjerte leserne. Kortet ligger derfor rett etter kalkulatorblokken (~37 % synlig tekst), der leseren nettopp har fått et gramtall og porsjonskontroll er top-of-mind. (2) **hund-kaster-opp** — 15 % lander midt i «gult skum»/«alvorlige årsaker», rett før bloat (23 %) og pankreatitt (27 %). Produktkort med pris og kjøpsknapp i den sekvensen leser som salg inn i en akuttsituasjon og treffer medisinsk-claim-regelen. Kortet ligger i Forebygging (46 %), der aktiviseringsskål-argumentet allerede står i brødteksten.

**Byggevalg:** enkeltkort-variant `.mh-article__productduo--single` (bilde 104 px venstre / 88 px under 420 px, tekst høyre, knapp full bredde 44 px tapphøyde). Ikke tvunget frem et svakt produkt nummer to for å fylle to-kolonne-gridet. CSS-blokk byte-identisk i begge filer (SHA `c23161bf`, 124 linjer), portert fra reise **uten** `.mh-article--v2`-prefiks — v2 er et helt designsystem og skal ikke dras inn for én komponent. Knappen scopet til `.mh-article__productduo` så den ikke overstyrer den hvite knappen i hvor-mye-mats eksisterende sidebar-boks.

**BESLUTNING — knappefarge:** fylt grønn `#2d6a35` med hvit tekst, IKKE reise-sidens hvit-på-hvit. Raseguide-canonical i CLAUDE.md foreskriver grønn knapp på hvite kort; reise-siden er avviket. Godkjent av Sondre — «ikke kopier den feilen».

**Verifisert:** TOC-ankere intakt (13=13, 17=17 — productduo legger til null `<h2>`, jf. gotcha #13), theme check uten feil, aktiviseringsskål 149 kr `InStock`, preview pull-back byte-identisk. Godkjent på mobil og desktop via temaeditor-preview. **Live-push gjenstår — Sondre gir klarsignal separat.**

### 2026-07-28 — HENDELSE + FIKS: PostToolUse-hook auto-pushet til LIVE (gotcha #15)

**Hva skjedde:** `.claude/settings.local.json` hadde siden commit `23d6787` (28. juni, «Infrastructure day») en `PostToolUse`-hook på `Write|Edit` som kjørte `shopify theme push --theme 148333264974 --allow-live` — hele arbeidstreet til live ved hver redigering av `.liquid/.json/.css/.js`. Den fyrte tre ganger under bygging av productduo-kortene. Fordi hooken fyrer per redigering og ikke per ferdig oppgave, lå `hund-kaster-opp` ute med markup uten CSS (ustylet kort) i vinduet. CSS-en kom via python/Bash, som ikke trigger hooken — den asymmetrien er lett å feiltolke.

**Eksponering:** temafil ~20:33 → ~20:37:50 (≈4 min 50 s); besøkende til ~20:39 pga. Fastly page_cache-etterslep (maks ~6 min). Eksakt sekund for første push ikke gjenopprettbart (mtime overskrevet). Ingen serverlogg-tilgang → kan ikke bekreftes om noen faktisk lastet siden.

**Rollback:** `git show HEAD:` → `/tmp/live-sync` → `theme push --live --only`. Verifisert med fersk pull-back fil for fil: begge sha256 identiske med HEAD, 0 diff-linjer. Verifiser alltid mot **temafilen**, ikke rendret HTML — cachen viste komponenten i ~1 min etter at fila var ren (jf. gotcha #9, `?cb=` buster ikke page_cache).

**BESLUTNING — hooken omskopet, ikke fjernet:** `--theme 149856485454 --force`, `--allow-live` strippet. Live-push krever nå eksplisitt manuell kommando; ingen automasjon når live. Backup: `.claude/settings.local.json.bak-20260728`. **Verifisert aktiv i sesjon** via sentinel-test (sentinel fyrte 21:31:23) + empirisk mål-bevis: med arbeidstreet stashet til HEAD ble preview overskrevet (productduo 36→0) mens live forble urørt. Merk: hooken pusher fortsatt **hele treet**, bare til preview — preview speiler arbeidskopien og er ikke et stabilt snapshot.


### 2026-07-28 — Nyhetsbrev-popup redesign LIVE: to varianter, tre steg, første reelle måling

**Utløser:** popupen hadde levert ~5 påmeldinger totalt siden 2026-05-11 og KING10 var innløst **1 gang**. Antatt årsak var trigger-timing; faktisk årsak viste seg å være sammensatt.

**Kartlegging:** popupen er 100 % egenbygget i temaet (`sections/newsletter-popup.liquid` + `assets/newsletter-popup.js`, statisk seksjon fra `layout/theme.liquid:771`, Horizon `dialog.js`). Ingen app, ingen Shopify Forms. Faktisk trigger var **30 s etter første scroll ELLER 50 % scrolldybde** — ikke 20 s som antatt, og armet ikke i det hele tatt uten scroll-event.

**KRITISK FUNN — målingen har aldri eksistert.** Butikken har **ingen GTM-container** (null `GTM-`-treff) og **ingen `gtag()` i hovedsidens scope**. GA4 `G-TR8MTY1BSE`, Google Ads `AW-17878551195` og `GT-NGS3DWB9` kjører alle inne i **Shopifys Web Pixels Manager-sandkasse** via Google & YouTube-kanalappen. Gammel kode gjorde `if (Array.isArray(window.dataLayer)) dataLayer.push(...)` — `window.dataLayer` finnes ikke, vakten feilet, pushen skjedde aldri. **`newsletter_signup` har aldri nådd GA4.** Ingen impression-event fantes uansett, så påmeldingsraten har aldri vært beregnelig. Alle tidligere antakelser om popupens ytelse var udokumenterte.

**Løsning — kanal:** eventene fyrer via `Shopify.analytics.publish` som primærkanal, med dataLayer + gtag + `clarity('set', ...)` som defensive fallbacks (alle i try/catch med eksistenssjekk — fyrer inn i ingenting uten feil hvis pixelen mangler). Ruten var allerede bevist: Custom Pixel «GA4 product_callout_click forw» (id `150765646`, runtimeContext LAX) gjorde samme jobb for callout-sporing. **Utvidet den eksisterende pixelen fremfor å lage ny** — en ny ville lastet `gtag.js` med samme GA4-ID i en andre sandkasse (dobbel konfig, risiko for duplisert sesjonstilskrivning). Verifisert i GA4 DebugView av Friday før live-push: alle seks events lander med korrekte parametere, delt `ga_session_id` holdt over 6 minutter.

**Design:** to varianter valgt server-side på `template.name` (cache-trygt, fullside-cachen er per URL). **A** = kommersielle flater (index/product/collection/search), rabattvinkel, `KING15`, kun nye besøkende. **B** = `/pages/`-artikler, raseguider, blogg, innholdsvinkel, `KINGTIPS15`, ingen ny-besøkende-gate (tilbakevendende leser er den beste kandidaten for et innholdsnyhetsbrev). Tre steg: mikro-ja → e-post → kvittering. Mikro-ja-svaret skrives til `contact[tags]` (`behov-hundehar`/`-hverdag`/`-valp`/`alle-temaer`) → segmenter i Shopify Email. A og B deler underliggende verdier med ulike visningstekster, så segmentene er identiske på tvers. Trigger 12 s fra `DOMContentLoaded` eller 40 % scroll. 30 dagers frekvenstak, permanent suppresjon etter innsending. Liquid-suppresjon på innloggede med tagg `newsletter` + `excluded_paths`. Desktop sentrert modal 420 px, mobil bunn-ark maks 55 dvh, 44 px touch-mål. `?mhpopup=force` omgår all suppresjon for QA (nødvendig — localStorage deles mellom live og preview på samme origin).

**Blokkerende compliance-funn under bygging:** utkastet lovet «kildesjekket mot veterinærfaglig litteratur» på variant B. Korpustelling avslørte at det ikke holder: av 59 generelle hundetips har kun 11 (18 %) navngitt vitenskapelig kilde, 15 kun myndighet/NKK, og **35 ingen navngitt kilde overhodet**. Raseguidene tåler påstanden (35/59 vitenskapelig, 0 uten kilde) — de generelle gjør det ikke, og variant B rendrer på begge. Påstanden fjernet som potensielt villedende etter mfl. § 7. Erstattet med det som faktisk er verifiserbart: vet-disclaimeren finnes i alle 118 artikler.

**Copy-presisjon — tre feil av samme klasse fanget:** (1) «Én e-post i uka» var et kadensløfte butikken ikke holder (12 velkomste-poster totalt) → «Et par e-poster i måneden»; (2) «15 % på første kjøp» stemte ikke med rabattoppsettet (én bruk per kunde, ikke førstegangskjøp) → «15 % velkomstrabatt»; (3) begge feilene lå **også** i den hardkodede samtykketeksten som deles av A og B — en rettelse i schema-feltene alene ville etterlatt motstridende tekst i samme modal. **Lærdom: delt hardkodet copy utenfor schema er en egen feilklasse.** Sveip hele filen, ikke bare feltet som ble meldt.

**Vilkårslinje lagt til** under koden på steg 3 (`discount_terms`, redigerbar): «Gjelder alle produkter. Én bruk per kunde, ingen minstekjøp. Kan kombineres med fraktrabatt. Ingen utløpsdato.» Speiler faktisk Admin-oppsett. Samtykketekst utvidet med lenke til `/policies/privacy-policy`.

**Bevisst utsatt til runde 2:** (a) ikke-modal dialog på mobil så bakgrunnen kan scrolle — native `showModal()` blokkerer bakgrunns-scroll i alle nettlesere, og fokusfelle på ikke-modal dialog må håndskrives (>30 min, a11y-regresjonsrisiko); (b) splitte variant B på raseguide-handles så guidene får den sterkere kildepåstanden de fortjener; (c) kildearbeid på de 35 artiklene uten navngitt kilde.

**Ny-besøkende-gaten feiler ÅPEN — bevisst valg.** Gaten leser `localStorage` + `sessionStorage`, ingen cookies. Blokkert lagring gir `null` overalt → `isNewVisitor()` returnerer `true` → popupen vises. Bivirkning: uten lagring kan heller ikke avvisningen skrives, så de brukerne får popupen på hver sidevisning. Dempet av at samtykkeporten (`userCanBeTracked()`) kjører først og fanger de fleste, og at Safari privat modus har flyktig `localStorage` (én visning per økt). Fail-open er riktig default mens vi trenger volum; revurderes hvis Clarity viser gjentatte visninger.

**Deploy:** popup-filene pushet live `#148333264974` etter preview-verifisering på `#149856485454`; locale-fiks (`free_shipping_over` × 3 språk, «50 USD» → 250 kr/NOK) pushet separat. Snapshots i `~/minhund-rollback/`. Deploy- og rollback-prosedyre skrevet inn i `docs/shopify-rules.md`. To nye gotchas i `docs/gotchas.md`: **#13** preview-temaet er utdatert for alt annet enn pushede filer (kostet en runde da et preview-skjermbilde ble meldt som live-fraktbug — alle tre var rettet på live dagen før); **#14** locale-filer får auto-header ved pull, diff-avvik er ikke feilet push.

---

### 2026-07-28 — MÅLEKONTRAKT: suksesskriterier for nyhetsbrev-popup (satt FØR data)

Satt bevisst før første datapunkt for å hindre etterrasjonalisering.

**Hovedtall: `mh_popup_submit` / `mh_popup_view`**

| Rate | Dom |
|---|---|
| **< 2 %** | Noe er fortsatt strukturelt galt — vi graver på nytt |
| **2–4 %** | Virker, men under det redesignet skulle levere |
| **> 4 %** | Godkjent |
| **> 6 %** | Over e-handelssnittet |

**Baseline:** 5 påmeldinger fra popupen totalt, over ukjent periode, uten nevner. Alt over det er teknisk sett forbedring — derfor er det **raten som teller, ikke antallet**.

**Sekundært — diagnostikk, ikke mål:**
- **Andel `step1_choice = alle`** («Bare send meg alt»). Over 40 % ⇒ mikro-ja-premisset er feil, vurder ettstegs.
- **`dismiss_method`-fordeling.** Mye `close` mot lite `decline` ⇒ folk lukker refleksivt før de leser.
- **Variant A vs B på rate.** **Ingen vinner skal kåres på to uker** — volumet er for lavt til signifikans. Vi ser kun etter om den ene er dramatisk dårligere.

**FRYS: ingen endringer på popupen før 11. august 2026**, uansett hva tallene viser underveis. Vi rører den ikke mens vi måler.

---

### 2026-07-28 — Pelsfjerner pakke-transparens: sjampobørste-avsløring + ærlig re-anker (`f7055de`)
**Utløser:** pakkekortet «1 stk + sjampobørste» (349 kr) ga null kontekst om hva børsten er — vi ba om ~200 kr ekstra for et ukjent produkt. **Kritisk sidefunn under kartlegging:** sjampobørsten var satt ned 299→**249 kr som ny permanent ordinærpris** (Admin, 27.07 17:35). Det gjorde det eksisterende `referansepris`-ankeret (478 = 179+299) utdatert → «Spar 99» var overdrevet mot reelle enkeltpriser i dag (179+249=428). **Sondre re-ankret i Admin:** `referansepris` 478→**428** + pakkepris 379→**349** → ærlig **Spar 79 kr (18,5 %)**. Verifisert live (bundle 349,00 + Spar 79) før bygging.
**Avsløring (Alt. A, CSS-only):** liten blokk vises når pakke-varianten velges — `all_products['hundesjampoborste']` gir thumbnail + tittel + én linje («2-i-1 børste med innebygd sjampodispenser — masserer mens du vasker, alt samlet i én hånd») + «{{ brush.price | money }} alene» (249, **dynamisk, ikke hardkodet** — auto-tracker fremtidige prisendringer, samme filosofi som referansepris-metafeltet) + diskré `brush.url`-lenke (`target=_blank rel=noopener`). **Ingen overstrøket 299** (rabatt inni pakkerabatt = rotete + dobler compliance-flate). Ingen ekstra API-kall (server-side `all_products`, som 10+ hundetips-seksjoner bruker allerede).
**Teknikk:** rent CSS `:has([data-is-bundle]:checked) ~ .pf-bundle-reveal` — **null JS, rører ikke `applyPfVariant()`** (bilde-bytte + utsolgt-logikk urørt). Blokk er søsken ETTER `.pf-variant-cards`, aldri inne i et label-kort. Utsolgt-synergi gratis: utsolgt pakke-radio er `disabled` → kan ikke bli `:checked` → avsløring forblir skjult. Dempet grå sekundærtekst, grønt kun på pris, konkurrerer ikke med Spar-pillen. Verifisert live 375px + desktop (Chrome headless, pakke pre-valgt via `?variant=`): avsløring korrekt ved pakkevalg, skjult ved default (1 stk). Push rett til live per instruks.
**Utestående (Sondre, Admin):** sjampobørstens SEO-meta nevner fortsatt «299 kr». Foreslått ny tekst uten pris (kan aldri gå ut på dato): *«2-i-1 hundebørste med innebygd sjampodispenser. Myke børster masserer mens du vasker, og såpen fordeles jevnt — alt samlet i én hånd. Sendt fra Norge.»* — Sondre fikser i Admin, eget punkt (ikke i denne diffen).
**Variantbilder komplett (28.07):** «1 stk» fikk tildelt hovedbildet `Photoroom_20260413_130951.jpg` i Admin (Friday) — var tom slot. Curl-verifisert: `data-variant-media-id=37151444402254` → riktig fil (media-ID ≠ ProductImage-ID `48492498419790`, bekreftet via thumbnail-URL). Alle tre varianter har nå distinkte variantbilder; `applyPfVariant()`-bildebytte dekker nå også «1 stk» (bytter til hovedbildet, ikke videoen — harde krav #2 fra bildebytte-bygget holder).

### 2026-07-27 (sen kveld) — Pelsfjerner prisstige visuell hierarki-opprydding live (`a0ed251`)
Styling-only follow-up på variant-restruktureringen, ingen logikkendring. (1) Slettet duplikat undertekst-linje på pakkekortet («Pelsfjerner + hundesjampobørste» duplikerte variantnavn-labelen rett over — labelen står). (2) Tre-nivå hierarki: pris uendret (grønn/bold/16px, primær); «per stk» + fraktlinjer nedtonet til 11px dempet grå (#777) — **grønn reservert til pris + Spar-pill**. «Kun 11 kr mer enn én» beholdt, leser nå som fotnote. Push rett til live (hoppet preview per instruks). **Verifisert live på 375px + desktop (Chrome headless):** fraktlinjen brekker ikke til to linjer på 375px, kortene ikke høyere enn før, konverteringsargumentet intakt. Ingen revert nødvendig. De 4 kolleksjons-SEO-descriptions (fra forrige økt) er nå også rettet i Admin av Sondre + curl-verifisert (alle «Gratis frakt over 250 kr», ingen avkorting).

### 2026-07-27 (kveld) — Pelsfjerner variant-restrukturering PDP + frakt-copy-opprydding live (`2d40422` + `2740ac6`)
Admin-prisstige endret: 2 stk 299→269, gammel «3 stk»/399-variant gjenbrukt som **«1 stk + sjampobørste» 379** (ikke slettet). PDP-Liquid oppdatert i takt (commit `2d40422`, 152+/33−, hele STEG 2-logikken + Spar-fiks i én commit):
- **Metafelt-forankret Spar:** `variant.metafields.custom.referansepris` (Variant, **Desimaltall**) styrer sparebeløpet. Bundel = **478** (Pelsfjerner 179 + Sjampobørste 299 = summen av REELLE enkeltpriser, Markedsføringsloven §§6-8). 1/2 stk tomt → faller tilbake på `single_price × antall`. Lar priser rettes i Admin uten kodeendring (jf. pris-gjennomgang 12. aug).
- **Rekkefølge-robust:** bundel-visning (variantnavn som label + undertekst «Pelsfjerner + hundesjampobørste», skjult per-stk) styres av metafelt-tilstedeværelse; utsolgt-visning av `variant.available` — begge IKKE index. Badges + per-stk-divisor beholder index-mapping (antar kanonisk 1→2→pakke).
- **Per-kort fraktlinjer:** 1 stk «+ 79 kr frakt» (179 < 250-terskel), 2 stk «Inkl. gratis frakt — kun 11 kr mer enn én», bundel «Inkl. gratis frakt». Standard fraktcopy; ingen ubetinget «gratis frakt».
- **Utsolgt-infra (variant.available):** kort blir stående (layout kollapser ikke), dimmet, «Utsolgt», radio disabled, BESTE KJØP skjult, ikke valgbar/ATC-bar. Standardvalg forblir 1 stk. Kun logikk-verifisert (bundel-lager 3, ikke satt til 0 — lager slår gjennom live umiddelbart).
- **Variant→bilde-bytte:** utvidet `applyPfVariant()` — varianter med `featured_media` bytter hovedbilde + markerer thumbnail (også mobil); 1 stk (uten bilde) rører ikke galleriet (video ikke tvunget tilbake, ingen restart/auto-scroll).
- **Spar-«99.0»-bug:** Desimaltall-metafelt (478.0) propagerte float → «Spar 99.0 kr». Fikset via **delt** display-kjede `savings | divided_by: 100.0 | round` (alle tre kort, ingen bundel-spesifikk formatering). Live cache-buster-verifisert: «Spar 99 kr» + «Spar 89 kr».
**Frakt-copy-opprydding (samme økt):** 3 produktbeskrivelser med ubetinget «Sendt fra Norge med gratis frakt.» → «Sendt fra Norge. Gratis frakt over 250 kr.» via `update-product` API (pelsfjerner, potevasker, vannflaske-hund-3-i-1). Read-back-diff mot innsendt HTML **byte-identisk** — ingen Shopify-normalisering. Comparison-article (commit `2740ac6`): «gratis levering fra Norge» → «gratis levering over 250 kr» i synlig FAQ + FAQPage JSON-LD (1:1).
**Korpus-sweep 145 URLer @ 200 (produkter+kolleksjoner+sider):** SEO meta-descriptions rene; sitewide trust-linjer «Gratis frakt over 250 kr» korrekte. **Gjenstår som MANUELT Admin-steg** (ingen collection-write i Shopify-MCP): **4 kolleksjons-SEO-descriptions** med ubetinget frakt — populaere-produkter/klaer/seng «Gratis frakt i Norge, 30 dagers åpent kjøp» + pleie «Gratis frakt, 30 dagers åpent kjøp» → alle «Gratis frakt over 250 kr, 30 dagers åpent kjøp».
**Åpne tråder:** (1) 4 kolleksjons-SEO-descriptions manuell Admin-fiks; (2) `referansepris`-metafeltet ble opprettet manuelt i Admin (MCP har ingen variant-metafelt-def-verktøy); (3) pelsfjerner PDP-render ruller på Shopify full-page-cache — lagret data verifisert korrekt via API, ikke tvunget purge; (4) opsjonsnavn «Antall» nå semantisk feil for bundel — navnebytte trygt men ikke gjort denne runden.

### 2026-07-27 — Helsepåstand Bolk 1 verifisert (27 Tier-1) + Fikse-økt 1: evidensbasert heteslag-kjøling live (`0117a77`)
Full kildeverifisering av alle 27 generelle Tier-1 akutt-artikler (3 parallelle verbatim-uttrekk-agenter → manuell klinisk fare-rangering). **Ingen FARLIG-funn** av «utsett livstruende vet-besøk»-typen — akutte tilstander (GDV, forgiftning, urinstopp, heteslag, DKA, glaukom, hoggorm) er gjennomgående korrekt rammet «ikke-vent/umiddelbart». To positive nøkkelfunn: (1) ingen artikkel instruerer eier i å framkalle brekning hjemme (giftig-mat/hund-kaster-opp/livreddende forbyr det + flagger saltvann-fare + navngir apomorfin klinikk-only); (2) ingen menneskemedisin med dose.
**Fikse-økt 1 (A1) deployet — medisinsk oppdatering, ikke omformulering:**
- Det utdaterte «IKKE iskaldt / bruk lunkent 15–20 °C»-kjølerådet → evidensbasert **kaldt-vann-råd** i 5 filer (sommer, hund-og-varmen, hund-drikker-ikke, hund-i-bil, livreddende). Kildeforankret **Royal Veterinary College «cool first, transport second»** (Hall et al. 2016–2018 UK cooling-studie) — «tepid-ikke-kaldt» er avkreftet myte, samme som i humanmedisin. Dette var eneste funnet med reell (om enn moderat) skade-risiko: rådet kunne få en eier til å nøle med å bruke kaldt vann på en tilstand som dreper på 15–30 min.
- Bevart: «ikke pakk inn i våte håndklær» + «kjøl først → ring/kjør vet mens du kjøler»-rekkefølge. Lagt til nyanse frisk ung (kaldtvannsbad) vs eldre/syk (helle over + vifte/trekk). Inkl. 2 myte-forkledde ekstra-fikser (hageslange-bullet + drikke-kontekst); fornuftig drikke-råd (små slurker) intakt.
- Schema speilet 1:1 (sommer L1308+L1340, hund-drikker-ikke L1210, hund-og-varmen L1038; JSON-LD parser OK). Live cache-buster-verifisert (5×200, 0 gjenværende myte-mekanisme); 5 URLer til GSC.
**Gjenstår i Bolk 1:** Fikse-økt 2 = A2 (hund-oeyne øye-observasjon) + A3 (hund-spiser-for-fort GDV-skille) + B1–B4 konsistens (asfalt 7/8 sek, panikk-terskel, matvegring, fôrbytte) — små lav-risiko innstramminger. Full fare-rangering i `docs/health-claims-register.md`.

### 2026-07-25 — Helsepåstand Bolk «varmeklyngen»: 5 varmetall kildeverifisert + konsistensrettet live (`1d39586`)
Sesong-kritisk (juli). Forsonet 4 sprikende varmetall + hånd-test på tvers av 5 artikler mot primærkilder:
- **Brachy tur-terskel (viktigst):** sommer 22–23 °C → 18–20 °C — BOAS-litteratur viser brachy overopphetes fra ~21 °C (2,1× mer utsatt, 3× dødelighet). Den for lempelige verdien var det eneste avviket som faktisk kunne skade en hund.
- **Bil ved 22 °C:** sommer 40 °C/10 min → 35 °C/10 min + 85 °C verste fall (Mattilsynet); hund-og-reise «over 40 °C» aligned til samme innramming.
- **Asfalt:** ~52/62 °C med kildeforbehold «amerikanske målinger viser» (US-studier, ingen norsk primærkilde); hund-blor-fra-poten urørt (Frostburg-sitert).
- **Hånd-test:** samlet til 7 sek (var 5/7/8).
- **Heteslag-startgrense:** bevisst urørt — allerede korrekt spenn-innrammet.
FAQ↔FAQPage-schema byte-identisk (brachy+7-sek i sommer, 35 °C i hund-og-reise). King-sidebar (Petit Brabançon, mesocephalic) urørt. Live cache-buster-verifisert; 5 URLer til GSC. **Åpent manuelt Admin-steg:** hund-om-sommeren meta-description sier fortsatt «5-sekunders» (SEO-felt, ikke tema).

### 2026-07-24 — Helsepåstand-prosjekt Bolk 0: disclaimer-hygiene live (`81c9c61`) + register i docs
Nytt prosjekt: kildeverifisering av helsepåstander i hele artikkelkorpuset (118 artikler). Full kartlegging fullført (6 parallelle lese-agenter) → `docs/health-claims-register.md` (49 Tier-1, 14 Tier-2, 50 Tier-3, 4 Tier-4; mirrors i FAQ/schema). **Bolk 0 (disclaimer-hygiene) deployet:**
- **Selv-audit korrigerte parallell-agent-feil:** «dachshund + 5 raseguider mangler topp-disclaimer» var FALSKT — alle 60 raseguider har både topp og bunn. Kun 3 generelle manglet topp.
- **20 filer normalisert (disclaimer-only):** 3 topp-disclaimer lagt til (hund-og-reise, hundehar-i-bilen, vaske-hundeseng); 4 Tier-1/helse-artikler «kontakt fagperson» → kanonisk vet-frase (hund-sover-mye + hund-vil-ikke-ga-tur beholdt vetnett.no-lenke); 13 raseguider semikolon→komma i avslutningsfrasen (FAQ+schema 1:1 via replace_all).
- **Kanonisk standard fastslått** (ref. hund-i-bil) og skrevet i registeret: invariant «Er du usikker på din hunds helse, kontakt veterinær.» (komma). Atferds-ruting + sterkere vet-varianter bevisst beholdt.
- Live-verifisert cache-buster (alle 20); 20 URLer til GSC. Ingen delte snippets.

Neste: Bolk 1 — Tier 1 generelle akutt-artikler (kildeverifisering av tall/tidsfrister/doser).

### 2026-07-24 — YMYL travel-rule fix på `hund-og-reise` (3. mest AI-siterte side) live (`559a125`)
Tredje side i YMYL-runden (14 AI-siteringer). Alle reisekrav verifisert mot Mattilsynet + kryssjekket mot `reise-til-utlandet` og `hund-i-bil` for konsistens. To reelle lovfeil (begge motsa både Mattilsynet OG våre egne sider) + tre presiseringer; 6 redigeringer i `sections/hundetips-reise.liquid`:
- **Finland FJERNET fra ormekur-krav**: Finland/Malta/Irland er UNNTATT (parasitten finnes ikke). Feilen sto i body + FAQ + FAQPage-schema. FAQ↔schema speilet byte-identisk.
- **Sverige-rabies RETTET**: direkte Norge↔Sverige krever IKKE rabiesvaksine (Mattilsynets Sverige-side); pass + ormekur kreves fortsatt. Sto i FAQ + schema. Speilet byte-identisk.
- **Chip må være FØR rabies** (ikke «eller samtidig som») per Mattilsynet.
- **«1 tonn»-fysikk → NAF-innramming** («titalls ganger egenvekten») — konsistent med hund-i-bil-rettelsen.
- **«over 40 °C på 10 min» → verifiserte Mattilsynet-tall** («over 40 °C, i verste fall opp mot 85 °C»).
- **Korpus-sweep**: begge lovfeilene var isolert til denne ene filen — `reise-til-utlandet` hadde allerede korrekt Finland-unntak + Norge–Sverige-rabiesunntak. Sidene er nå konsistente.
- Uendret: operatør-policy-påstander (ferge/fly/tog/hotell) — hedget, utenfor primærkilde-kravet. Ingen delte snippets.

Preview → live (`#148333264974`) verifisert med cache-buster (0 gamle; FAQ==schema byte-identisk). `/pages/hund-og-reise` sendt til GSC re-indeksering. Commit `559a125`. **Tre mest AI-siterte sider (hund-i-bil, bandtvang-norge, hund-og-reise) er nå kildeverifisert.**

### 2026-07-24 — YMYL legal-accuracy fix på `bandtvang-norge` (2. mest AI-siterte side) live (`4e99ba7`)
Fortsettelse av hund-i-bil-metoden på nest mest siterte side (13 AI-siteringer). Alle straffe-/paragraf-/unntak-påstander verifisert mot Hundeloven (LOV-2003-07-04-74) på Lovdata. 8 inline-redigeringer i `sections/hundetips-bandtvang.liquid` (5 korreksjonspunkter; ingen delte snippets, ingen FAQ/schema berørt):
- **§ 6-sitat UTDATERT → verbatim**: gammelt «quote» («storfe, sau, geit, fjærfe, rein, hest eller vilt…») matchet ikke loven; erstattet med gjeldende «husdyr, tamrein eller viltlevende dyr og deres reir, bo eller hi». Feilsitat av lov på AI-sitert side.
- **§ 11 → § 6 annet ledd**: § 11 er «ro og orden», ikke hjemmel for utvidet båndtvang. Var intern selvmotsigelse (body siterte selv § 6 andre ledd korrekt).
- **Fengsel-trigger FEIL → rettet**: § 28 første ledd = båndtvangsbrudd uten skade gir BØTER; fengsel inntil 6 mnd (andre ledd) kun når hunden angriper/skader folk eller dyr. Rettet factstrip-label + answer + «strengere reaksjoner»-bullet.
- **«3 000–5 000 kr» forelegg-sats FJERNET** (ingen fast forskriftssats — som 2600-saken). Factstrip-kort 2 omformulert til § 10 («Enhver kan ta inn en hund som går løs i båndtvangen» — hjemlet + lite kjent); body mykt til skjønnsmessig forelegg.
- **Jakthund-unntak PRESISERT**: la til datoforbeholdet 20. aug–1. april (utenfor nasjonal båndtvang) per § 9 første ledd f — «under aktiv jakt» uten forbehold var misvisende.
- BEKREFTET uten endring: § 4 (kontroll hele året), § 9 tjenestehund-unntak, § 10, § 14/§ 15 avliving ved angrep på husdyr/tamrein, samt HELE `reise-til-utlandet-med-hund` (bendelorm 24–120 t, Finland/Malta/Irland-unntak, 28-dagersregel, Sverige-rabies-unntak, 21-dagersregel — alt mot Mattilsynet, holder etter 2026-07-03-korreksjonen).

Preview (Development-theme) → live (`#148333264974`) verifisert med cache-buster (0 gamle strenger). `/pages/bandtvang-norge` sendt til GSC re-indeksering (service-account). Commit `4e99ba7`.

### 2026-07-23 (kveld) — YMYL legal-accuracy fix på `hund-i-bil` (mest AI-siterte side) live (`5b12d33`)
Clarity 17.–23. juli: `/pages/hund-i-bil` = mest AI-siterte side (21 siteringer, 100 % Share of Authority på «lov hund i bil uten bur norge» + «dog transport car norway laws»). Våre formuleringer gjengis direkte i AI-svar → feiltall forsterkes. Kildeverifisering mot primærkilder (Lovdata/Mattilsynet/NAF) avdekket to påstander uten hjemmel + småfeil. 8 inline-redigeringer i `sections/hundetips-hund-i-bil.liquid` (ingen delte snippets):
- **«2 600 kr gebyr» FJERNET** — ingen slik sats i forenklet forelegg (1990-492) eller gebyrforskriften (2021-963). Mykt opp til «kan gi forelegg; beløpet fastsettes av politiet». Ordet «gebyr» var også teknisk feil (last er ikke gebyr-overtredelse).
- **«prikker på førerkortet» FJERNET** — prikkbelastningsforskriften (2003-1164) §2 lister ikke last-sikring eller §3-aktsomhet → hund-i-fanget gir forelegg, ikke prikker.
- **Fysikk «over 200 kg / 300 kg»** → NAF-krasjtest-innramming («titalls ganger egenvekten»).
- **Forsikring**: la til hjemmel forsikringsavtaleloven §4-9 (BEKREFTET ordrett: «grovt uaktsomt … kan settes ned eller falle bort»).
- **Presisjon**: «kjøretøyforskriften» → «forskrift om bruk av kjøretøy»; «dyrevelferdsloven» → «dyrevelferdsloven §11 (transport)».
- **Factstrip-kort**: `2 600 kr` → `4 av 6` / «bilseler røk i NAFs frontkollisjonstest i 50 km/t» (hjemlet, står støtt alene for AI-plukk).
- BEKREFTET uten endring: Mattilsynet 85 °C ved 22 °C (ordrett på mattilsynet.no), NAF bur>sele-test, straffeloven §17 nødrett (knuse rute).

FAQ synlig ↔ FAQPage-schema holdt 1:1 (verifisert `True`). Preview (Development-theme) → live (`#148333264974`) verifisert med cache-buster (0 gamle strenger, alle nye med riktig antall). `/pages/hund-i-bil` sendt til GSC re-indeksering (service-account). Commit `5b12d33`.

### 2026-07-23 — Homepage restructure phase 1 + 2 + 3: fjernet 2 seksjoner + reorder (`580e763`) + FAQPage JSON-LD (`38b2a59`) + scroll-animasjoner (`1d70200`)

**Kontekst:** Full strukturell inventory av forsiden (`templates/index.json`, 10 seksjoner) kjørt read-only først — kartla render-rekkefølge, shared-use (hvilke section-filer brukes andre steder), schema, theme-editor-avhengigheter, CSS-scoping og hardkodede handles. Ingen homepage-seksjon emitterte JSON-LD; ingen av de berørte filene var shared (recipes-teaser + UGC-block er homepage-only).

**Phase 1 — fjern 2 + reorder (commit `580e763`, live `#148333264974`):** Forsiden gikk fra 10 → 8 seksjoner. Fjernet fra `order` + section-defs: `home_recipes_teaser` (CalmBall-oppskrifter-teaser) og `1768648793c9c64a49` (UGC «Del bilder av din fornøyde hund»). Byttet `custom_liquid_kingPromo` ↔ `section_j3AAXA` slik at **Møt King** nå står FØR nyhetsbrevet. `divider_F98HWb` beholdt før FAQ (breather mellom de to lyse seksjonene; King→nyhetsbrev er mørkegrønn→hvit = naturlig brudd uten divider). **Reversibelt:** `sections/home-recipes-teaser.liquid` + `blocks/ai_gen_block_a93a906.liquid` ligger fortsatt på disk (kun av-wiret fra index.json). Ny rekkefølge: hero → trust-bar → Judge.me → Hundetips/raseguider → Møt King → nyhetsbrev → divider → FAQ. Live-verifisert: begge fjernede seksjoner borte (0 markører), rekkefølge Møt King → nyhetsbrev → FAQ bekreftet.

**Phase 2 — FAQPage JSON-LD (commit `38b2a59`, live):** Homepage-FAQ (`custom_liquid_XRexTm`) rendret et synlig 5-spørsmåls-accordion uten structured data. La til FAQPage JSON-LD som speiler artikkel-korpus-mønsteret (`sections/hundetips-hund-kaster-opp.liquid`): `<script type="application/ld+json">` med `@type` FAQPage + `mainEntity[Question→acceptedAnswer]`. **Svar byte-identiske (1:1) til synlig accordion** — ingen parafrasering, ingen nye claims. Alle 5 Q dekket (Hvor sender dere fra / leveringstid / Hva koster frakt [«over 250 kr»] / trygt å handle / Hvem tester produktene). Pre-push verifisert: JSON-LD parser valid; count matcher accordion (5); frakt-svar bærer «over 250 kr» uten ubetinget frakt-copy; kun én FAQPage på siden (theme.liquid-FAQPage er guardet til `product.pelsfjerner`, ingen homepage-konflikt). Live-verifisert cache-busted: FAQPage present, parser valid, 5 Q.

**Phase 3 — subtile scroll-animasjoner (commit `1d70200`, live):** **Funn:** det fantes allerede et komplett, LIVE reveal-system — `assets/mh-premium.js` (92 linjer) + `assets/mh-premium.css` §12–13, lastet globalt i `theme.liquid` («Premium Scandinavian»-lag fra tidligere sesjon, ikke synlig fra index.json). Dekket ~70 % av spec-en (IntersectionObserver fires-once + unobserve, hero-cards staggered med LCP-hero ekskludert, Judge.me/tips/King/FAQ reveal, hover-lift, reduced-motion). **Beslutning (Sondre-bekreftet):** UTVID mh-premium, ikke bygg parallell asset (unngår to observere + to hidden-state-konvensjoner). Behold live motion-verdier (80ms stagger, −6px/.3s hover, .6s/24px reveal — Sondre: «mine spec-tall var vilkårlige, dine er live og fungerer»). La kun til de manglende bitene: (1) §2 trust-bar fade-up 4 items staggered (utvidet stagger til å telle `.mh-t4-item`); (2) §6 nyhetsbrev (`section_j3AAXA`) wrapper fade-up — email-signup-internals urørt; (3) §5 count-up på 226g/2019/100% ved enter-view, 1,2s ease-out cubic, final-verdier i HTML (no-JS safe), reduced-motion viser final umiddelbart, stat-bokser bredde-låst før telling (CLS-safe); (4) §8 FAQ opacity-fade lagt til `max-height`-sliden på accordion. **Safety-failsafe (Sondre 3. opsjon — Googlebot kjører JS ved indeksering, worst case må være «ingen animasjon», aldri «ingen innhold»):** head-guard starter en 2500ms-timer som stripper `mh-anim-ready` hvis `mh-premium.js` aldri booter (`window.__mhBooted` uset → blokkert/404/throw) → alt innhold synlig; normalcase setter scriptet `__mhBooted` ved eksekvering → ingen flash. Observer + count-up wrappet i try/catch; `boot()` faller tilbake til `revealAll()` ved feil. **Housekeeping:** fjernet ALLE døde referanser til de phase-1-slettede seksjonene (`home_recipes_teaser` + `1768648793c9c64a49`) fra mh-premium.css (reveal-liste + reduced-motion-tvilling + typografi/eyebrow/knapp/container-grupper) og mh-premium.js `REVEAL_SELECTORS`. **Live-verifisert:** ny minifisert JS/CSS servert (countUp/revealAll/__mhBooted/mh-t4-item/section_j3AAXA/bredde-lås; trust-reveal 5×, nyhetsbrev-reveal 4×, FAQ aria-opacity 2×, 0 døde refs); failsafe funksjonelt bevist headless mot LIVE head-script (blokkert JS → synlig etter 2,5s; booted → beholdt/ingen flash); reduced-motion-path (ingen skjuling, ingen timer, stats final); no-JS (all seksjons-copy + count-up final-verdier i HTML, `<html>` uten hardkodet skjule-klasse); CLS (reveal kun opacity/transform, hero ekskludert). Gjenstår: menneskelig visuell sjekk av bevegelsen på 375/768/1280 (CLI kan ikke se animasjon). Reversibelt via `git revert 1d70200`.

**Åpent punkt (utsatt til senere pass):** foreldreløse `mh-home-recipes__*`-regler i `assets/custom.css` (14 regler) står igjen — eneste konsument (recipes-teaser) er av-wiret, men CSS-cleanup gjøres i en egen runde for å holde denne endringen reversibel.

### 2026-07-22 — GSC page-2 opportunity-sprint: 5 batcher (A/D/C/B + gotcha) live + Andefanten-regel korrigert

**Utløser:** GSC-analyse (service-account, 90d, query×page) av page-2-queries (posisjon 8–20, impr >20) → 300 kandidater, intent-klassifisert (KJØP×3 / INFO / SØPPEL via google-ads-script-negativ-logikk adaptert for organisk). 0 SØPPEL (organisk = alle rader har allerede landingsside). Top-15 sider aggregert (anchor-fragmenter kollapset); 6 KJØP-rader surfacet separat. Rapport-only først, batch-godkjenning per steg (preview → STOP → live).

**Batch A (metas, Admin):** 4 raseguide-meta-rewrites — australian-shepherd (manglet head-term helt), newfoundland / italiensk-mynde / weimaraner (ledet med genetikk-jargong uten click-hook) → head-query front-loaded + reason-to-click, ≤155 tegn. **Rettelse:** min opprinnelige «alle 15 top-sider mangler meta»-funn var FALSK — single-line `curl | grep '<meta name=\"description\"'` bommer på theme-ens multi-line `<meta>`-tags (→ gotcha #14). Alle 15 hadde gode custom metas; kun 4 trengte CTR-omskriving. Nesten forårsaket 15 unødvendige rewrites.

**Batch D (kommersiell, commit `1fd00f2`):** leker-subtittel (collection-catalog) + «rund hundeseng»-answer-block (product-hundeseng) + pelsfjerner «fjerne hundehår fra sofa»-exact-anchor (pelsfjerner-test) + 4 potevasker inbound-links (bader-ute / graver-i-hagen / vil-ikke-ga-tur / i-bil — potevasker hadde kun 8 inbound vs pelsfjerners 60). Admin: seng-title+meta, pelsfjerner-meta, leker-title+meta. **2 frakt-compliance-brudd fanget & fikset:** pelsfjerner-meta «Fri frakt fra Norge» + leker-meta «Gratis frakt i Norge» → «Gratis frakt over 250 kr». **Lukker det åpne punktet fra BESLUTNING 2026-07-20 (linje ~134):** pelsfjerner PDP-meta var tom/non-compliant — nå satt compliant.

**Batch C (interne lenker, commit `8d1cfb3`):** pre-flight viste breed-cluster-grafen allerede tett; kun 7 reelle gap + 2 resiprositets-kompletteringer = 9 crossover-links i 6 «Les også»-blokker (cocker→golden · welsh-corgi/shiba→pomeranian · cavalier/malteser→griffon · griffon→cavalier/bichon/tibetansk · malteser→cavalier). Griffon↔cavalier nå toveis; griffon-blokka hadde NULL breed-links før. Alle mål HTTP 200.

**Batch B (content, commit `2b8050e`):** targeted FAQ i EKSAKT query-frasering, hver speilet 1:1 i FAQPage JSON-LD (verifisert valid + count-match): hund-kaster-opp +3 (hvitt skum / ufordøyd mat / tørrbrekk — alle m/vet-disclaimer) 9→12; bandtvang +1 «Er det båndtvang nå?» (satt først, sesong-snippet) 8→9; hva-kan-hund-spise sukkererter (liste+hurtigoversikt) + 2 FAQ (yoghurt/skinke) 8→10. **Scope-funn:** artiklene var allerede mer komplette enn rapporten antok → holdt lean/high-ROI. llms.txt Trigger B: word_count korrigert (hund-kaster-opp 2550→3050, bandtvang 2300→2750, hva-kan-hund-spise 3650→2550 — map overstated ~1100 ord).

**Andefanten-regel korrigert (Sondre-catch):** memory `feedback_calmball_supervision.md` var INVERTERT (sa «Andefanten = safe alone/alenetid») — motsier `docs/products.md` (revidert 2026-05-28: ALDRI markedsfør Andefanten som safe-alone; begge leker er supervised-only). Fikset i memory + MEMORY.md-indeks + stale cross-referanse i docs/products.md. Canonical beroligende-leker-frasering låst: «myke kosleker som Andefanten». `docs/gotchas.md` #14 lagt til (commit `5e3a858`).

**Verifisering:** alle 9 Admin-felt (4 Batch A-metas + seng-title/meta + pelsfjerner-meta + leker-title/meta) + alle theme-endringer live-verifisert på minhundpet.no. **2 judgment calls holdt** (weak-fit links + King→griffon sitewide — se Åpne tråder). **Round 2 (64 gjenstående page-2-opps) gated på GSC-avlesing ~12.08** (samordnet med v2-avlesingen 14.08).

### 2026-07-21 (kveld) — Checkout-språk til Norsk Bokmål: nb enabled+published via API, default-flip gjenstår i Admin UI

**Mål:** Shopify-hostet checkout skal rendre på **norsk bokmål (nb)**, ikke engelsk. Butikk-innhold er allerede hardkodet norsk (jf. `theme.liquid` lang="nb"-override); dette gjelder KUN Shopify sin egen checkout/locale-config, ingen tema- eller oversettelses-endring.

**Bakgrunn:** Butikkens **primær-locale er engelsk (en)** — derfor returnerer `request.locale.iso_code` "en" (memory `project_default_locale_is_english.md`), og Shopify-checkout arver engelsk.

**Phase 1-funn (API-gap bekreftet):** `ShopLocaleInput` (Admin API 2026-04) eksponerer kun `published` + `marketWebPresenceIds` — **ingen `primary`-felt**. `ShopLocale.primary` er read-only. **Å flippe default/primær-locale er IKKE mulig via Admin GraphQL API** — krever Shopify Admin UI. Verifisert via Shopify Dev MCP mot 2026-04.

**Utført via API:** **nb enabled + published** (mens en forble primær og urørt — å disable aktiv primær-locale sletter ALLE oversettelser permanent). Trygg, ikke-destruktiv operasjon.

**Token-scope-gotcha:** Alle 5 Shopify CLI-session-tokens mangler `read_locales`/`write_locales`-scope (`['*']`-labelen i CLI-store er en CLI-layer-label, ikke ekte Admin-scope). shopLocales-mutasjoner via CLI-OAuth gir ACCESS_DENIED — et eget custom-app-token med eksplisitte locale-scopes kreves for API-locale-arbeid.

**⏳ MANUELT ADMIN-STEG (Sondre, ikke skriptbart):** I Shopify Admin → Settings → Languages: (1) flipp **default language til Norsk (Bokmål)**, deretter (2) fjern/unpublish **English**. Rekkefølge er kritisk — en må ALDRI disables mens den er primær (sletter oversettelser). Etter flip vil checkout rendre norsk. Til da er nb tilgjengelig men en er fortsatt default.

### 2026-07-21 — Fri-frakt-terskel 250 kr LIVE: cart-progress-bar + sitewide copy-sweep (commit `a0d6826`)

**Beslutning:** Innført **fri-frakt-terskel på 250 kr** (betalt frakt **79 kr** under terskel, satt i Shopify Admin). Reverserer den gamle «fri frakt på ALLE ordrer»-regelen (Chihuahua-fix 2026-05-14). Terskel = 250 (ikke 300) fordi vanligste upsell 2× CalmBall ≈ 298 kr må kvalifisere.

**Del A — cart-drawer progress-bar:** ny `snippets/free-shipping-bar.liquid` (`fs_threshold = 25000` øre) + CSS i `assets/custom.css` + én `{% render %}`-linje i `snippets/header-actions.liquid` (drawer). Viser «Du er kr X unna gratis frakt» → «🎉 Du har gratis frakt!» ved 250 kr. Auto-refresh på quantity-endring verifisert empirisk (morphSection av header-seksjonen inkluderer baren). Funksjonstestet på preview (tom kurv skjult / 149 kr = 59 % / 298 kr = full).

**Del B — sitewide copy-sweep:** all ubetinget frakt-copy → «Gratis frakt over 250 kr» på tvers av 88 filer (6 globale: trust-bar/footer/cart-summary[badge slettet]/cart-products/meta-tags/om-oss · 2 template-JSON hero+PDP · 11 PDP-leveringslinjer · 3 llms-flater · 66 artikkel/raseguide trust-linjer) + 6 uncovered (layout topbar, collection-catalog, calmball-PDP-badge, sommer, calmball-oppskrifter, 5 pelsfjerner-test prose incl. FAQ+JSON-LD 1:1). Final audit: 0 ubetingede treff igjen (kun Tier-6 locale-schema-placeholders «over $50 USD» = inaktive). Google Ads-scripts (`create_ad_3.py`, `fix_snippet_header.py`) også oppdatert (kilde — endrer IKKE live-annonser).

**Deploy:** 94 filer pushet live `#148333264974`, pull-verifisert. Regel forankret i CLAUDE.md (Legal/Content Rules) + memory `feedback_fri_frakt_uconditional.md` (reversert). **14 URL-er re-indeksert** (homepage + 11 PDP + pelsfjerner-artikkel[via 301-target hvordan-fjerne-hundehar] + llms-side).

### 2026-07-20 (kveld) — Batch #2 v2-retrofit LIVE: valp-biter-pa-alt + bandtvang-norge + hund-slikker-ansikt

De 3 batch #2-pilotene (satt opp tidligere samme dag) er retrofittet og **live** (commit `2f91312`). Utvider august-avlesings-sampelet fra 6 til **9 piloter**. Kjørt med 3 parallelle subagenter (én per fil, som batch #1) + egen manuell audit (batch #1-lærdom: subagent-avvik må fanges).

- **Additiv vei-A alle 3:** scoped `.mh-article--v2`, factstrip (3 tall/side), answer-first per informasjonell H2, top-disclaimer (canonical grønn), factstrip-mobil. **0 H2 endret** (gotcha #13 — index-baserte anchors), FAQ 1:1 byte-identisk (8/8 alle), veterinær/juridisk-disclaimer intakt.
- **Factstrip-tall verifisert mot eksisterende body** (ingen nye påstander/YMYL): valp 12–16 uker / 6–7 mnd / 18–20 t søvn; bandtvang 1.apr–20.aug (Hundeloven §6) / 3 000–5 000 kr forelegg / 6 mnd maks fengsel (§28); slikker 400+ bakteriearter / barn under 5 år / 7 regler.
- **Product-box kun valp** → `/products/aktiviseringsleke-for-hund` (allerede lenket; framet KUN som mental aktivisering/kanalisering av tygge-trang, **ingen stopp-biting-claim**). bandtvang + slikker: additiv uten product-box (ingen ekte produkt-fit) → nyttig kontrast: isolerer content-løft fra product-box-løft vs batch #1.
- **Konsolideringsfiks:** subagentene endte inkonsistent på top-disclaimer (bandtvang grå vs 2 andre grønne) → satt alle til canonical grønn.
- **Ordtelling:** valp 2707→3047, bandtvang 2333→2683, slikker 2011→2293 (additivt).
- **Admin-meta satt + verifisert av Sondre** (title + description alle 3). Titler: «Valp biter på alt — slik stopper du bitingen», «Båndtvang i Norge — regler, datoer og bøter», «Hund slikker ansikt — er det farlig?».
- **Re-indeksering:** alle 3 URL-er sendt via service-account — ✅.
- **Deferred (valgfritt):** llms word_count for de 3 er <20 % drift (Trigger B ikke utløst) → ikke oppdatert. Kan refreshes ved anledning (valp 2750→3050, bandtvang 2300→2700, slikker 2000→2300; H2-lister uendret).

**Neste:** batch #2 teller nå i den rene 14.08-avlesingen (9 piloter totalt). Se Åpne tråder for GO/NO-GO-kriteriet.

### 2026-07-20 — GSC-avlesing pilot-retrofit: NO-GO korpus (for tidlig/konfundert) + batch #2 satt opp

**Avlesing (28d 22.06–19.07) vs 90d-baseline, 7 sider (6 batch #1-piloter + hund-i-bil):** v2-effekt **ikke isolerbart ennå**. Dominant signal er en bred **impresjons-surge 1,5–5,7× på ALLE sider**, inkl. det ulikt-behandlede hund-i-bil (vei-A additiv) → organisk/sesong + indeksmodning, IKKE v2. Klikk/dag-økning er dermed impresjons-drevet, ikke CTR-drevet. **CTR (metrikken v2 skal flytte) er blandet:** 3 opp (hvor-mye-vann +0,44pp / sover +0,23 / øyne +0,13), 2 ned (hva-kan-spise −0,13 / gress −0,24), 2 flate — og nedgangene korrelerer med de største impresjons-hoppene (fortynning). Posisjon opp 6/7 men samme modnings-confound. **Måle-vindu ~40 % pre-retrofit** (retrofits live 02–03.07). → **NO-GO på full korpus-utrulling**; mega-sider (`hund-kaster-opp`, `hvor-mye-mat`) + 60 raseguider forblir gated. hund-i-bil watch-queries bekreftet bedre posisjon: «hund i bil regler» 22,2→18,3; «hund i bagasjerom uten bur» 12,5→8,2 (men 0 klikk, pos 8–18).

**Batch #2 satt opp (3 Tier-1-piloter, HELD for execution — full standardpakke, samlet gate):** utvider august-sampelet fra 7 til 9 piloter for en robustere GO/NO-GO. Valgt etter GSC-profil (Tier-1-trafikk + page-1-posisjon + CTR-headroom). **Baselines dokumentert (90d / 28d pre-retrofit):**
| Side | 90d impr/kl/CTR/pos | 28d pre impr/kl/CTR/pos |
|---|---|---|
| valp-biter-pa-alt | 5548 / 70 / 1,26 % / 9,6 | 2808 / 36 / 1,28 % / 7,5 |
| bandtvang-norge | 5957 / 37 / 0,62 % / 8,8 | 3527 / 20 / 0,57 % / 8,5 |
| hund-slikker-ansikt | 4007 / 28 / 0,70 % / 8,0 | 2185 / 17 / 0,78 % / 7,4 |

- **Design-note:** 2 av 3 mangler ren produkt-fit (ingen bånd/tyggeleke/face-produkt) → batch #2 blir hovedsakelig **additiv vei-A (factstrip + answer-first + schema)**, product-box kun ved ekte fit. Nyttig kontrast: isolerer content-løft fra product-box-løft vs batch #1 (som hadde productduo).
- **Gotcha #13 gjelder:** valp-biter-pa-alt har index-baserte JS-anchors (#grunner/#plan/#tyggeleker indeksert som egne URL-er) → IKKE legg til/fjern H2 under retrofit.
- **Timing:** må gå live innen ~utgangen juli for å ha ~25 post-retrofit-dager i 14.08-vinduet. Execution ikke startet — venter GO (samlet gate for alle 3, som batch #1).

### 2026-07-20 — Pelsfjerner-cluster P1–P4 KOMPLETT (admin-steg lukket + curl-verifisert)

Lukker de tre utestående admin-stegene fra 2026-07-13-oppføringen. Curl-verifisert live 2026-07-20:
- **P4 301-redirect ✅** — `/pages/beste-pelsfjerner-2026` → **HTTP 301** → `/pages/hvordan-fjerne-hundehar-effektivt-hjemme` (final 200). Comparison-siden satt Hidden i Admin + redirect aktiv; template/section-filer bevisst beholdt på disk (ingen deletion-protokoll).
- **P2b artikkel SEO-title ✅** — live `<title>` = «Slik fjerner du hundehår hjemme — guide | Min Hund». INFO-differensieringen nå komplett (H1 + title + meta byttet bort fra kommersiell «pelsfjerner»-framing).
- **P1 PDP-title ✅** (fra før) = «Pelsfjerner til sofa, klær & bil | Min Hund».
- **Re-indeksering:** `/products/pelsfjerner` + artikkelen sendt på nytt via service-account — begge ✅.

**Eneste gjenstående (valgfritt, ikke-blokkerende):** PDP `/products/pelsfjerner` meta-**description** er fremdeles tom i live-HTML (kun title satt). Google auto-genererer i mellomtiden; kan settes ved anledning med foreslått tekst («Elektrostatisk pelsfjerner som drar hundehår ut av sofa, klær og bilseter — dobbeltsidig, brukes tørr, ingen refill. Kun for tekstil. Fri frakt fra Norge.»).

**Status: cluster P1–P4 lukket.** PDP eier KJØP, artikkelen er ren INFO-hub som trakter til PDP via over-fold product-box, comparison-siden retired via 301. Neste: les av effekt i GSC (PDP-posisjon/CTR + om artikkelen begynner å hente INFO-queries) — tidligst ~4–6 uker.

### 2026-07-13 — Pelsfjerner-cluster P1–P4: cannibalization-drevet konsolidering (theme-side live; 3 admin-steg utestående)

**Utløser:** dedikert cannibalization-analyse av 3-URL pelsfjerner-clusteret (GSC, 365d — første store service-account-lesejobb, alt OK). Funn: PDP `/products/pelsfjerner` vinner **10 av 11 delte queries** (pos 9–16 på money-terms), artikkelen co-rangerer men henter **0 klikk på 12 mnd** (pos 22–70), comparison-siden `/pages/beste-pelsfjerner-2026` er **praktisk talt død** (1 relevant impr/365d, 0/28d, rangerer ikke for «beste pelsfjerner» — ingen etterspørsel). Fjerde URL `pelsfjerner-for-sofa-klaer-og-bil` er avindeksert (handle-migrasjon, ufarlig). Strategi: PDP eier KJØP, artikkelen differensieres til ren INFO og trakter til PDP, comparison-siden retires.

**Theme-side gjennomført + live-verifisert (commit `badb733`, GitHub main):**
- **P2 — artikkel `hvordan-fjerne-hundehar-effektivt-hjemme`:** ny H1 «Slik fjerner du hundehår hjemme — metoder som faktisk funker» (bevisst unntak fra vei-A — H1 endres for å bryte title-overlap med PDP; URL urørt). Full v2-retrofit: factstrip (2×/70–80 %/5 min), 11 answer-first-blokker, **over-fold product-box → PDP** (kommersielt anker «Se pelsfjerner-hansken», produktregel-compliant: elektrostatisk fiber/tørr/kun tekstil), top-disclaimer, scoped `.mh-article--v2` CSS. Method-level «hvilken type bør du velge»-merge (ingen merkenavn — bevart INFO-signal). Egen beste-pelsfjerner-selvlenke fjernet. 3251 ord. FAQ 1:1 (8/8) bevart.
- **P3 — PDP→artikkel:** `mh-product-readmore` link1 → INFO-anker «Les guiden: Slik fjerner du hundehår hjemme»; link3 av-pekt fra beste-pelsfjerner → `pelsskifte-hund` (respekterer horizon-cart-regel — kun content-snippet, ingen beskyttede cart-filer rørt).
- **P4 theme-side:** hub-kort `card_34` fjernet + featured-tittel oppdatert; llms-entry beste-pelsfjerner fjernet (121 entries, 0 malformed); inbound-repoint i `hund-bader-ute`.
- **P1 PDP-title live:** `Pelsfjerner til sofa, klær & bil | Min Hund` (bekreftet i live-HTML).
- **Re-indeksering:** `/products/pelsfjerner` + artikkelen sendt via service-account request_indexing.py — begge ✅ (ingen auth-feil; service-account-migrasjonen holder).

**⚠ UTESTÅENDE admin-steg (verifisert IKKE på plass 2026-07-13):**
1. **P4 301-redirect IKKE lagt inn** — `/pages/beste-pelsfjerner-2026` returnerer fortsatt **HTTP 200** og rendrer comparison-innholdet. Template/section-filene bevisst beholdt på disk (ingen deletion-protokoll). Redirect må legges i Admin → URL Redirects → mål `/pages/hvordan-fjerne-hundehar-effektivt-hjemme`.
2. **P2b artikkel SEO-title fortsatt gammel** — live `<title>` er «Hvordan fjerne hundehår effektivt hjemme — komplett guide». H1 (theme) er ny, men admin-meta-title ikke oppdatert → differensieringen er ufullstendig til den byttes.
3. **P1 PDP meta-description ikke bekreftet satt** — tom i live-HTML; kun title er inne.

**Konklusjon:** P1(title)/P2/P3/P4(theme) komplett & live; **P1(meta-desc) + P2b(title) + P4(301) gjenstår i Admin** før clusteret er fullt lukket. Cluster tjener kun ~6 klikk/12 mnd (alle PDP) — største gevinst er PDP-CTR/posisjon + INFO→PDP-trakting, ikke av-kannibalisering (mild, PDP vinner allerede).

### 2026-07-03 — YMYL-korreksjon live: `reise-til-utlandet-med-hund` bendelorm/28-dagersregelen (offentlig påpekt presisjon)

**Utløser:** offentlig påpekt at artikkelens formulering «bendelormkuren kan ikke gjøres i Norge» var upresis — den gjelder kun **hovedregelen**, ikke 28-dagersregelen. Verifisert mot Mattilsynet (3 sider: hovedregel + 28-dagersregelen + Sverige-side) før endring.

**Fire endringer (commit `3b9d30d`, live verifisert på alle 4):**
1. **§4 Bendelormkuren** — «kan ikke gjøres i Norge» scopet eksplisitt til HOVEDREGEL + direkte henvisning «(unntak: 28-dagersregelen, se neste avsnitt)» + Mattilsynets ordlyd «i landet hunden reiser fra».
2. **§5 28-dagersregelen** — eksplisitt at de **to oppstartsbehandlingene kan gis hos veterinær i Norge** (Norge er del av EU/EØS), med hyttefolk-poenget (slipper vet i utlandet før hver retur). Mattilsynet-belegg: tillatt config «én i Norge og én i et annet EU/EØS-land».
3. **FAQ 4** — flatt «Nei» → «Etter hovedregelen: nei» + eget 28-dagers-unntaksledd; JSON-LD FAQPage-schema oppdatert 1:1.
4. **Fase-tidslinje** — Fase 2-badge merket «(hovedregel)» + figcaption presiserer at 28-dagers-brukere følger eget løp.

**Verifiserte Mattilsynet-fakta:** hovedregel 24–120 t før innreise av vet i avreiselandet; 28-dager: to oppstartsbehandlinger maks 28 dager fra hverandre, vedlikehold minst hver 28. dag, avslutning med siste behandling i Norge. Ingen andre endringer (~+80 ord, under 20 %-terskel → ingen llms.txt Trigger B). **⚠ Re-indeksering feilet på GSC «Insufficient Permission»** (kjent tilbakevendende service-account/OAuth-tilgang) — Google fanger endringen ved neste crawl; manuell re-submit i GSC anbefalt når tilgang er gjenopprettet.

### 2026-07-03 — v2-retrofit BATCH #1 live: `hvor-mye-vann` + `hund-spiser-gress` + `hund-sover-mye` (siste batch før GSC-avlesing)

**Tre Tier-1-piloter i én batch** (commit `4ebe74e`, live verifisert via cache-bust etter en forbigående Shopify 503). Siste retrofit-batch før avlesing ~30–31.07. Parallellisert: 3 subagenter kjørte den mekaniske retrofiten (én per fil), deretter egen verifisering + 2 konsolideringsfikser + samlet preview/push.

Baselines (90d) → avlesing **~2026-07-31**:
| Side | Impr | Clicks | CTR | Pos |
|---|---|---|---|---|
| hvor-mye-vann-hund | 3 896 | 23 | 0,59 % | 7,5 |
| hund-spiser-gress | 3 853 | 30 | 0,78 % | 7,8 |
| hund-sover-mye | 3 121 | 23 | 0,74 % | 7,3 |

- **Felles:** ren additiv vei-A, INGEN ny H2 (alle index-basert JS-anchor, gotcha #13 — h2-antall verifisert uendret: 9/14/14), scoped `.mh-article--v2` leak-test 0, FAQ 1:1 (7/8/8), YMYL null nye påstander (factstrip-tall verifisert mot eksisterende body).
- **Productduo (alle 3 hadde naturlige par):** vann = TurPakken + Vannskål (begge 299 kr — verifisert distinkte produkter/bilder, ikke render-bug); gress = Aktiviseringsleke + Aktiviseringsskål (begge 149); sover = Beroligende hundeseng (799) + Aktiviseringsleke (149). Alle InStock.
- **sover NY søvntabell** (Valp/Voksen/Senior → timer/døgn) med mobil kort-stack — mønster: legg til v2-temptable på sider UTEN eksisterende tabell.
- **2 subagent-avvik fanget + fikset i egen review:** (1) vann hadde redundant TurPakken bunn-CTA → fjernet; (2) gress hadde repurposet bunn-CTA til «aktiviseringsleken Andefanten» (feilmerking — Andefanten er kosedyr-leke, ikke aktiviseringsleke) → fjernet helt. **Lærdom: verifiser subagent-output manuelt — produkt-feilmerking + redundante CTA-er sniker seg inn.**
- **Meta:** A-varianter satt i admin av Sondre (alle tre).
- **llms Trigger B:** wc vann 1650→1000 (kalkulator-side, kort prosa), gress 3100→3000, sover 2700→2150 (korrigerer prior over-estimater; H2-lister uendret). 122 entries, 0 malformed.
- **PAUSE etter batch #1.** Ingen flere retrofits før GSC-avlesing ~30.07 av de nå 6 live pilotene (hva-kan-hund-spise, giftig-mat, hund-oeyne + disse 3). Mega-sidene (hund-kaster-opp, hvor-mye-mat) forblir gated. Sidenote: `hvordan-fjerne-hundehar-effektivt-hjemme` vurdert (742 impr, flat 12mnd, money-queries pos 23–55) → Tier 3, IKKE verdt tidlig retrofit (ranking-problem, ikke CTR); revurderes evt. i dedikert pelsfjerner-cluster-pass.

### 2026-07-03 — v2-retrofit PILOT #3 live: `hund-oeyne` (lettere additiv lift, ingen duo)

**Tredje Tier-1-pilot** (commit `d3b382a`, live verifisert via cache-bust). Baseline **4 719 impr / 64 klikk / 1,36 % CTR / pos 8,1** (90d) → avlesing **~2026-07-31**.

- **Ren additiv vei-A**, scoped `.mh-article--v2` (leak-test 0): 10 answer-first, factstrip (0,6 mm hornhinne / 3× hornhinnesår-risiko Packer et al. / 24–48 t glaukom→blindhet).
- **INGEN ny H2** (gotcha #13 — hund-oeyne bruker index-basert JS-anchor; verifisert 12 h2 = uendret mapping).
- **Triage-farger på EKSISTERENDE symptomtabell** i stedet for ny tabell: la til rad-klasser (`is-safe/is-mod/is-danger/is-critical`) + scoped CSS (desktop bg-tint, mobil venstre-aksent, hastenivå-celle farget). Struktur og eksisterende mobil-stack urørt. Mønster: **når en side allerede har en severity-tabell, fargekod den i stedet for å legge til en v2-temptable.**
- **Productduo bevisst DROPPET:** eneste naturlig relevante produkt for øye-side er sjampobørsten (allerede sidebar-boks + 1 inline tekstlenke). Ingen naturlig produkt nr. 2 for øyne i katalogen → en duo ville tvunget inn urelatert produkt på YMYL-side. **Lærdom: productduo-konsolidering forutsetter ≥2 naturlig relaterte produkter; med bare 1 relevant produkt beholdes eksisterende enkelt-sidebar-boks.**
- Lettere lift enn #1/#2 (siden rangerer bedre, 1,36 % vs 0,39–0,42 %) — CTR-løft ligger primært i meta + answer-first-snippets.
- **Meta:** tittel A «Hundens øyne: symptomer, sykdommer og trygg rens | Min Hund» + beskrivelse — settes i admin.
- **llms Trigger B:** wc 3400→3800 (+answer-first; H2-liste uendret). 122 entries, 0 malformed. Re-index: manuell GSC UI (Indexing API permission-blokkert).

### 2026-07-03 — v2-retrofit PILOT #2 live: `giftig-mat` (additiv vei-A + productduo)

**Andre Tier-1-pilot** (commit `8d1ccc1`, theme `#148333264974`, live verifisert via cache-bust). Neste side i GSC-prioriteringen: worst-CTR-profil (list-formet toksisitet).

- **GSC-baseline (90d, 2026-04-03→07-01):** **4 874 impr / 19 klikk / 0,39 % CTR / snittposisjon 8,3.** Re-avlesing **~2026-07-31**.
- **Ren additiv vei-A:** body/H1/URL/kategori (Helse) urørt. Additivt v2-lag scoped `.mh-article--v2` (leak-test 0): 10 answer-first, factstrip (1 drue / 17–18 t / 0 min), farenivå-tabell 11 rader (4 livsfarlig / 5 farlig / 2 moderat) ved §farligste med mobil kort-stack.
- **⚠ Sidespesifikk gotcha (LÆRDOM):** giftig-mat tildeler TOC-ankre via **JS-indeks** (`querySelectorAll('.mh-article__body h2')` mot en fast 13-element `anchors`-array). En ny H2 inne i `.mh-article__body` ville forskjøvet ALLE påfølgende ankre og brutt TOC. Løsning: **INGEN ny H2** — factstrip (utenfor body), answer-first (`<p>`), tabell (`<figure>`) og productduo (`<div>`) legges additivt uten å øke h2-antallet. Verifisert: 13 h2 = 13 anchors live. **Sjekk alltid om en side bruker index-basert JS-anchor-tildeling før du legger til H2 i en retrofit.**
- **Productduo (CalmBall + Aktiviseringsskål) ved §trygt** — safe-food-pivoten, bevisst borte fra forgiftnings-/nødsituasjon-innholdet. Selvstendig knapp (siden hadde ingen base `.mh-article__product-btn`). **Ingen sidebar-produktboks** lagt til (restraint på YMYL-forgiftningsside — siden hadde null produkt-touchpoints fra før; én tasteful duo er nok). Lager live (gotcha #12): 249/149 kr, InStock.
- **YMYL:** null nye påstander (tabell speiler vettet copy, ASPCA-forankret); disclaimer + FAQ 8:8 urørt.
- **Meta:** tittel A «Giftig mat for hund — komplett liste + hva du gjør | Min Hund» + beskrivelse — settes i admin.
- **llms Trigger B:** article_map wc 2600→1850 (korrigerer prior over-estimat; faktisk body ~1834 ord; H2-liste uendret). 122 entries, 0 malformed.
- **Re-indexing:** Indexing API fortsatt «Insufficient Permission» — manuell «Request indexing» i GSC UI.

### 2026-07-02 — v2-retrofit PILOT #1 live: `hva-kan-hund-spise` (ren additiv vei-A på eksisterende side)

**Første v2-retrofit på en EKSISTERENDE side** (commit `9a297f6`, theme `#148333264974`). Valgt fra GSC-prioritering (90d, alle `/pages/`): Tier 1 = høye impressions + pos 8–25, under-optimalisert. `hva-kan-hund-spise` valgt som de-risket første pilot (worst CTR-gap, kun 22 klikk i risiko, list-formet innhold ideelt for hurtigtabell).

- **GSC-baseline (90d, 2026-04-03→07-01):** **5 220 impr / 22 klikk / 0,42 % CTR / snittposisjon 9,9.** CTR-fix er hovedmålet (0,42 % er i bånn for pos 9,9). Re-avlesing **~2026-07-30** (samme klokke som hund-i-bil + ferie).
- **Ren additiv vei-A** (som hund-i-bil): body/H1/URL/kategori (Ernæring) urørt, ingen eksisterende H2-tekst/-rekkefølge endret. Additivt v2-lag scoped `.mh-article--v2` (leak-test 0):
  - Answer-first-ingress i alle 11 innholds-H2 + ny H2 «Kan hunden spise det? Hurtigoversikt»
  - Factstrip (10–15 % / 15 000 år / 0 druer-rosiner-sjokolade)
  - Checklist «Huskeregler for menneskemat»
  - **Hurtigtabell** 17 rader (6 trygt / 5 med måte / 6 aldri), `data-label` + mobil kort-stack ≤640px + kort-tittel-fix. Datatabell-undermønster (uavhengige rader).
- **YMYL:** null nye matvare-påstander — tabellen speiler eksisterende vettet copy; toksiske punkter ASPCA-forankret (druer=nyre, løk/hvitløk=RBC, xylitol, methylxantiner, makadamia). Disclaimer intakt.
- **Productduo DROPPET her** (bevisst): YMYL-ernæringsside, naturlig produkt-krok (aktiveringsleker) først midt i artikkel, og siden har allerede 4 produkt-touchpoints. Unngår påtvunget kobling. CalmBall + Aktiviseringsskål verifisert `InStock` (gotcha #12) i tilfelle senere toggle.
- **Meta (CTR-fix):** tittel A «Hva kan hund spise? Komplett liste — trygt og farlig | Min Hund» + ny beskrivelse — settes i admin av Sondre.
- **llms Trigger B:** article_map wc 2950→3650 + Hurtigoversikt-H2 (122 entries, 0 malformed).
- **Re-indexing:** Indexing API-submit feilet «Insufficient Permission» (kjent GSC-gap: service account ikke Owner). **Manuell «Request indexing» i GSC UI anbefalt.**

**Merk vs. korpus-gate:** dette er ÉN de-risket Tier-1-pilot, ikke korpus-retrofit. Korpus-bred retrofit (~40 hundetips + 60 raseguider) forblir gated på ~2026-07-30-avlesingen. Denne piloten starter sin egen 4-ukers klokke parallelt for et tidlig datapunkt.

**Oppfølging samme dag — produktvisning konsolidert til productduo-mønsteret (commit `f3fa769`, live verifisert via cache-bust: 249,00/149,00 kr dynamisk, Andefanten sidebar, end-CTA borte).** De 4 v1-touchpoints erstattet: ETT `.mh-article__productduo` (CalmBall + Aktiviseringsskål) plassert etter §fyll (den kommersielle kroken midt i artikkelen, ikke tvunget til toppen på YMYL-ernæringsside); sidebar byttet fra Aktiviseringsskål til **Andefanten** (canonical: sidebar ≠ duo-produkter); gammel CalmBall slutt-CTA fjernet. Hvert produkt = maks ett kort-touchpoint. CalmBall-compliance-sweep: kun mental aktivisering/engasjement, 0 beroligende/alenetid-språk på siden (fikset også «beroligende protein-snack» → «mild» i §godbiter). Duo-knapp fikk scoped grønn-fyll-override (base-knapp er hvit-på-grønn for sidebar). Lager live-verifisert (gotcha #12): 249/149/249 kr, alle InStock. **Nytt standard-punkt lagt i `docs/page-patterns.md` v2-canonical-seksjon:** «produktvisning konsolideres til productduo-mønsteret» som fast retrofit-sjekklistepunkt.

### 2026-07-02 — Ny hundetips-artikkel «Ferie med hund i Norge» live + v2-design blir CANONICAL for nye artikler

**Artikkel live** (`/pages/ferie-med-hund-i-norge`, kategori Aktivitet, commit `0cab3b4`, theme `#148333264974`). Net-new, 2330 ord, 12 answer-first H2 + 8 FAQ 1:1. Admin-side opprettet manuelt (handle + template `page.ferie-med-hund-i-norge` + SEO); template-kobling verifisert live (HTTP 200, artikkel rendrer).

- **Bygget på hund-i-bil v2-standarden:** scoped `.mh-article--v2` (factstrip, temptable som «Sommerens farer»-tabell, checklist «Pakkeliste»). Leak-test: 0 v2-klasser på hund-og-reise live.
- **Hero:** IMG_0273.jpg (King på campingplass), unified hero-canonical (1:1 cover, scale-bleed).
- **Schema:** inline Article med `about` (båndtvang/flått/hoggorm) + `lastReviewed` + FAQPage + BreadcrumbList (bevisst avvik fra `mh-article-schema`-snippet, som mangler `about`).
- **Intern lenking:** 2× hund-i-bil (§4 + §8) + krysslenke hund-og-reise; **back-link FRA hund-i-bil** (§lange-turer, additiv) TIL denne. Begge URL-er re-indeksert.
- **Produktkoblinger:** TurPakken, vannskål, potevasker, ullgenser, aktiviseringsleke/-skål, pelsfjerner (tekstil-only), CalmBall (tilsyn). Hub-kort card_62 + llms-entry (121 entries, 0 malformed).

**⚖️ BESLUTNING — v2-design er ny CANONICAL for ALLE NYE hundetips-artikler fra 2026-07-02.** Factstrip + temptable + checklist, scoped via `.mh-article--v2`, answer-first per H2, inline Article-schema med about-entiteter.

**Produktkort — `.mh-article__productduo` (lagt til 2026-07-02, del av v2-canonical):** ETT produktkort-cluster med inntil 2 produkter side om side, plassert **høyt i artikkelen** (rett etter en tidlig seksjon, over fold — Clarity viser scroll-dropoff, kort under fold konverterer ikke). Dynamiske bilder via `all_products['handle'].featured_image` (aldri hardkodet URL; `product` finnes ikke i page-scope), **`object-fit: contain`** (produktshots skal ikke beskjæres), pris via `| money`. Mobil: kompakt 2-kolonne (85 % mobiltrafikk). **Maks ETT produktkort-cluster per artikkel** — ingen duplikat produkt-CTA-er ellers i brødteksten (tekstlenker OK). Sidebar-produktboks kan beholdes, men skal vise et **ANNET** produkt enn productduo-en (unngår cluster nederst på mobil). Referanse: `sections/hundetips-ferie-med-hund-i-norge.liquid` (productduo: TurPakken + Potevasker; sidebar: vannskål). Lager verifiseres alltid live før produkt-lenking (gotcha #12).

**Tabeller — mobil-stack (lagt til 2026-07-02, del av v2-canonical):** Enhver tabell med **3+ kolonner** (temptable / krav-tabell / sammenligning) MÅ ha mobil-stack ved `≤640px`: `thead` skjules, hver `<tr>` blir et kort, hver `<td>` får `data-label="<kolonnenavn>"` og vises som «label: verdi»-linje via CSS `::before { content: attr(data-label) }` (ingen JS). Fargekoding per rad beholdes som **venstre kant-aksent** på kortet. Desktop uendret. Årsak: 4 kolonner (og 3 kolonner med lange celler) klipper siste kolonne på 390px. **Nytt post-flight-sjekkpunkt: «ingen horisontal klipping på 390px»** — verifiser hver 3+ kolonne-tabell i mobil-preview før push. Retrofittet på alle tre trilogi-artiklene 2026-07-02 (reise 4-kol, ferie + hund-i-bil 3-kol).

**Tabell-tillegg (2026-07-02, senere samme dag):** (1) **Første kolonne = kort-tittel** i alle stackede tabeller — første `<td>` som fet tittel uten label, øvrige labels dempet (grå), verdier primære. (2) **To tabell-undermønstre:** (a) *datatabell* (uavhengige rader) → ren kort-stack; (b) *prosess/tidslinje-innhold* (rader tilhører ordnede faser) → `mh-article__temptable--phased` med **fase-overskrifter mellom kortgruppene** (én `<tbody class="mh-article__phase--N">` per fase + `mh-article__phase-row` med nummer-badge, grønn→oransje→rød). Desktop: multi-kolonne-tabell med fase-seksjonsrader; mobil: fase-overskrift mellom kortene; kort-aksent følger fase-fargen. Ingen tidslinje-strek/ny komponent. Referanse: reise «Krav-tabell». Post-flight-sjekkpunktet gjelder begge undermønstre.

**Retrofit av eksisterende korpus (~40 hundetips + 60 raseguider) besluttes IKKE nå** — avventer GSC-avlesing ~2026-07-30 av hund-i-bil (vei-A-baseline 582 impr / pos 13,5) + ferie-artikkelen, for å måle om v2 faktisk løfter CTR/posisjon før vi investerer i retrofit.

**Sidegevinst — gotcha #12:** potevasker var feilaktig dokumentert som «OUT OF STOCK» i `docs/products.md` (stale). Verifisert live in-stock (179 kr, `schema.org/InStock`). Regel dokumentert: lager verifiseres alltid live, aldri fra docs/products.md. Doc-linje korrigert.

### 2026-07-02 — Hund i bil: vei-A additivt løft live (data-drevet, ikke overhaul) + v2-designeksperiment + gotcha #11

**Kontekst:** Brief ba om «ny artikkel» Hund i bil, men artikkelen fantes allerede live (3 491 ord, kategori Helse, i hub + llms). I stedet for overhaul ble beslutningen tatt på GSC-data.

- **GSC-baseline `/pages/hund-i-bil` (siste 12 mnd, avlest 2026-07-02):** 582 impressions / 5 klikk / 0,86 % CTR / snittposisjon 13,5. Alle topp-queries on-topic (hund i bil regler, sikring av hund i bil, hund i bil bot). → **Vei A valgt** (behold indeksert body/kategori/H1/URL; kun additivt), fordi 582 impr på relevante queries = under-optimalisert, ikke død. Re-avlesing planlagt **~2026-07-30** for å måle løft.
- **Additivt levert (commit `1e2efd2`, live `#148333264974`):**
  - **11 answer-first** lead-setninger (én per substans-H2; H2-tekst/rekkefølge urørt). §Metoder svarer eksplisitt på «hund i bagasjerom uten bur» (posisjon-12,5-query): lovlig hvis forsvarlig sikret (f.eks. bak gitter), men bur tryggest.
  - **+~800 ord fakta**: 2 600 kr gebyr, 85 °C/22 °C (Mattilsynet), +22 °C/time, 80 % første 30 min, bagasjerom +10 °C, burstørrelse-formel (×1,10 / ×2,5 / hodehøyde), heteslag-førstehjelp (lunkent vann, 38–39 °C, dog mode ikke feilsikkert). Wordcount 3 491 → 4 278 (ingen kutt).
  - **v2-designeksperiment, scoped `.mh-article--v2`** (CSS inline, 0 globale lekkasjer — verifisert på hund-og-varmen live): **factstrip** under hero (2 600 kr / 85 °C / 0), **temptable** i §Varme (gradient hvit→rød, tysk bilorg. + Mattilsynet-kilde), **checklist** «Før du kjører» (✓ via CSS, ikke emoji).
  - Vannskål-lenke (in-stock) i pakkeliste; last_updated mai→juli 2026; llms word_count 3500→4300.
  - **Ny meta-tittel/-beskrivelse** satt i admin («Hund i bil — sikring, regler og varme | Min Hund»); **re-indeksert 2× 2026-07-02** (etter push, og på nytt etter meta-endring).
- **Gotcha #11 dokumentert (`docs/gotchas.md`):** curl-preview av et *upublisert* tema via `preview_theme_id` er brutt — myshopify-domenet 301-redirecter til primærdomenet og stripper param, så curl validerer LIVE, ikke preview. Dette avdekket et **hull i `template-deletion.md` Step C** → Step C skrevet om til **browser-basert** verifisering (cookiet preview-sesjon) + evidenskrav i commit + scriptbar theme-pull-kryss-sjekk (commit `c243522`).

### 2026-07-01 — Feriekampanje teardown: sommerferie-banner + feriebeskjed fjernet (revert av `ce99199`, commit `34787fe`)

Sommerferien 19.–28. juni er over; hele feriekampanjen som ble lagt inn i `ce99199` (toppbanner + feriebeskjed på PDP/cart + CSS, alt merket «FJERN ETTER 28. JUNI 2026») er fjernet.

- **Metode:** `git revert --no-commit ce99199` med `.claude/settings.local.json` bevisst ekskludert (lokale hooks/permissions beholdt). ce99199 var HEAD + rent working tree → isolert, trygg revert. Commit `34787fe` (15 filer, 1 ins / 106 del).
- **Fjernet:** `snippets/mh-ferie-notice.liquid` (slettet), `announcement-bar`-blokk i `header-group.json` (order → `header_section`), FERIEKAMPANJE-blokk i `assets/custom.css`, render-kall i cart-drawer (`header-actions.liquid`) + alle 11 custom PDP-seksjoner.
- **Orphan-cleanup:** `--only`-push sletter ikke remote-filer, så `mh-ferie-notice.liquid` lå igjen inert på live. Full theme-push kjørt etter live-vs-lokal diff-verifisering (eneste fil på live men ikke lokalt var nettopp den snippeten, 0 utilsiktede slettinger) → snippet slettet fra live-tema `#148333264974`, re-pull bekreftet borte.
- **KING10 beholdes aktiv.** Koden brukes også som velkomstrabatt i nyhetsbrev-popupen (`sections/newsletter-popup.liquid`, default `KING10`) — uavhengig av ferie. Deaktivering ville gitt død kode i popupen; derfor IKKE rørt.
- **Verifisert på produksjon:** banner + feriebeskjed = 0 forekomster på forside + 2 PDP-er (calmball, pelsfjerner) + cart-drawer. Google re-indeksering forespurt for forside + calmball + pelsfjerner + potevasker (Indexing API, service account).

> **Eldre historikk arkivert:** BESLUTNINGER eldre enn 2026-06-23 og SPRINT-LOG-uker utover de 2 siste ligger i [`docs/archive/project-status-history.md`](archive/project-status-history.md) (split 2026-07-23). Arkivet er IKKE speilet til den offentlige GitHub-mirroren — kun denne aktive fila synces.

---

## SPRINT-LOG — append-only, nyeste øverst

### 2026-07-29 — King-boks fakta-batch (commit `e298130`, 97 filer, live `#148333264974`)
**246 endringer i 94 tema-filer + 2 docs.** Vekt 108 (alle → 5 kg; Cocker/Springer rasevekt «12,5–14,5 kg» bevart via negativ lookbehind — 0 falske positive). Multiplikator 11 (reberegnet). Brachy→mesocephalic 14 i 9 filer (`mops.liquid:218` var ikke i kartleggingen). Cedille 28 (inkl. `layout/theme.liquid` Organization-JSON-LD). Griffon-prefiks 74 (sidebar). Lenke 12 i 6 filer (`Les mer om King →` + manglende `.mh-article__tips-sidebar-link`-CSS — 116/122 → **122/122**). Alder: om-king «snart sju år» → «over sju år» (evergreen).

**Verifisering:** rendret HTML fra preview via cookie-jar-metoden med live-baseline som diskriminator — 5 sider på tvers av begge visuelle varianter + 6 multiplikator-filer, alle PASS. Etter live-push: 95/95 sha256/semantisk match mot HEAD, 0 filer utenfor batchen endret, 5/6 live-sider PASS. `hvor-mye-vann-hund` viste stale `page_cache` (etag urotert over 3 polls) — kildefil på live verifisert korrekt og ucachet render via `preview_theme_id=148333264974` bekreftet lenke=1/cedille=0. Gotcha #10-oppførsel, ikke innholdsfeil.

**Docs:** `docs/products.md` King canonical facts-tabell + avledet-påstand-regel. `docs/gotchas.md` #11 omskrevet (cookie-jar-metoden).

**NESTE RUNDE (avtalt):** body-H2-varianten (73 filer, median 205 ord) + Griffon-prefiks i body (238 forekomster) + visuell redesign + vurdering av snippet-uttrekk for de 122 inline CSS-blokkene.

### Uke 24 — 2026-06-12 (Full nettside-helsesjekk + 2 cleanup-tasks — commit `3db6d6a`)
**Full-site audit (alt grønt):** 122 artikkelsider + 11 produkter + hubs + contact + 129 unike interne lenker = alle HTTP 200, 0 brutte. JSON-LD (Article/FAQPage/BreadcrumbList på artikler+raseguider; Product+BreadcrumbList på produkter) rendrer. JSON-validitet OK (5 «feil» = Shopify stock JSONC; «apps»×11 = app-block-placeholder). Schema-navn ≤25 (våre custom; stock bruker `t:`-nøkler). Breadcrumb-handles synket (4 templateSuffix-avvik = falske positiver). llms split 120/malformed 0/0 komma-pipe. Sitemap 127 sider, ny artikkel inkludert. Ingen fremtidsdatoer.

**Cleanup 1 — danger-list flex-regresjon** (bommet i 2026-05-09-sweepen): `aktivisering-article.liquid` + `bade-hund-article.liquid` hadde `display:flex` på `.mh-article__danger-list li` (fete overskrifter klemt i smal kolonne m/ stygg orddeling). Byttet til hanging-indent + canonical danger-icon.

**Cleanup 2 — genericisert navngitte konkurrent-autoriteter** → generisk veterinær-autoritet i 7 filer: hund-lugger-i-band (H2 «AniCuras tre-fire-fem-skritt-metode» → «Tre-fire-fem-metoden: belønn riktig posisjon» + anchor anicura→tre-fire-fem + llms article_map Trigger-B), cavalier-king-charles-spaniel (Agria, prosa+FAQ+JSON-LD), hund-liker-ikke-bading (Agria), fjerne-hundehaar-article (Evidensia/AniCura + co-located Royal Canin), bade-hund-article (Evidensia/AniCura), hund-spiser-gress (AniCura + co-located FirstVet/EMPET), dansk-svensk-gardshund (AniCura). Beslutning: co-located ikke-listede merker (Royal Canin/FirstVet/EMPET) fjernet for ren merkefri prosa.

**Checkpoint:** 0 merke-residu i 7 filer, flex=0/text-indent=1, band anchors 12=12, FAQ 1:1 (cavalier+fjerne), llms split 120/malformed 0, æøå+en-dash intakt. Live verifisert via cache-buster (edge-cache-lag ga falske ikke-null treff på først pass — fresh render = 0). 9-fil commit `3db6d6a` live `#148333264974` + GitHub main.

**ÅPEN — 8. fil flagget:** `hundetips-aktivisere-hund-pa-tur.liquid:62` har «Agria og andre norske forsikringsselskaper ser dette hvert år» — IKKE i Sondres 7-fil-liste, derfor IKKE rørt. Venter på go for samme genericiserings-fix.

### Uke 24 — 2026-06-09 (Ny Helse-artikkel: hund-blor-fra-poten «Hund som blør fra poten — årsaker og førstehjelp» — commit `6355d5f`)
Ny answer-first hundetips-artikkel (Helse), Phase 0–3 godkjent av Sondre før assembly, Phase 4 deploy etter eksplisitt go. Dekker poteomsorg / blod fra pote — et hull i Helse-clusteret (komplementerer vaske-hundens-poter + klippe-klor-hund + allergi-hos-hund).

**Struktur:** 12 answer-first H2 + 8 FAQ (FAQPage JSON-LD 1:1) + Article-schema (mh-article-schema snippet) + BreadcrumbList (handle registrert i mh-breadcrumb-schema Helse-liste) + sticky TOC (13↔13↔13 anchor/H2/TOC) + Tips fra King sidebar + post-FAQ recap-grid. **2739 ord** (godkjent — moat/FAQ-gulv; ingen trim av mandatert innhold).

**Moat-seksjoner (verbatim, Sondre-levert):** pote-anatomi (tredeputer/midtpute/karpalpute + keratin/fettvev/blodåre-nett), klo-pulpa (nedslitt vs avrevet, sporeklør/dewclaws), varm-asfalt 7-sekunders-test + Frostburg University-studie (40/43/51 °C) + 52 °C-skadeterskel, veisalt/is-syklus om vinteren, førstehjelp 6-stegs (trykk 5–10 min, Kwik Stop/maisstivelse, to-finger-bandasje), von Willebrand + rottegift-faresignal (blødning 3–7 dager etter inntak) → vetnett.no for vakt.

**Recap-grid «Anbefalt for poteomsorg»:** Potevasker (hero — restock imminent; beholdt som hero per Sondre-beslutning), Aktiviseringsleke for hund (ærlig ramme: mental aktivisering for kjedsomhets-slikking), Beroligende hundeseng (mykt liggested mens poten gror — ingen medisinsk claim). CalmBall holdt ute (tilsyn-only-regel). Hvite kort + grønn CTA, canonical recommend-pattern.

**Interne lenker:** §8 → allergi-hos-hund (pododermatitt-overlap); les-også × 5 (allergi / vaske-hundens-poter / klippe-klor-hund / hund-og-varmen / livreddende); inbound back-link lagt til FRA allergi-hos-hund (les-også). Alle mål HTTP 200 verifisert.

**Registreringer (6-fil atomic commit `6355d5f`):** ny seksjon + ny page-template (`page.hund-blor-fra-poten`), hub `card_61` (Helse) i page.hundetips.json, llms article_map Helse-entry (split 120, malformed 0, ingen komma/pipe i felt), breadcrumb-handle, allergi back-link. Hero: `poter.png`. last_updated `'juni 2026'`; datePublished/dateModified = Admin-dato (2026-06-09).

**Post-flight (live `#148333264974` + GitHub main):** hub-kort live (card_61 synlig), allergi back-link live, alle les-også/produkt-mål HTTP 200, llms-sync `/pages/llms-txt` = 1. 18/18 self-audit pass før push.

**Admin-side opprettet + sluttverifisering (2026-06-09 ettermiddag):** Sondre opprettet Shopify Admin-siden (Visible). `/pages/hund-blor-fra-poten` returnerer nå **HTTP 200** og rendrer korrekt: hero `poter.png`, 14 `<h2>` (12 innholds-H2 + FAQ-heading + recap-heading), 8 FAQ-summaries, sticky TOC 13 lenker, recap-grid med alle 3 produktlenker, Tips fra King. **Alle 3 JSON-LD-blokker rendrer nå live** (Article + FAQPage + BreadcrumbList — sistnevnte to keyer på `page` som tidligere 404et).

**Google re-indeksering BLOKKERT (åpen):** Indexing API `submit_url` (URL_UPDATED) feilet 2× med «Insufficient Permission»; `inspect_url` feilet med «You do not own this site». Read+write GSC-auth nede samtidig = OAuth-token-utløp igjen (jf. kjent gotcha: consent screen i «Testing»-modus → kortlevd token; re-auth gjort i morges 11:32a virket, men er utløpt på nytt). Krever Sondre re-auth (og evt. service-account owner-access for Indexing API). Siden er live + i Shopify-sitemap, så organisk Google-discovery skjer uansett; Indexing API akselererer kun. **Re-index på `/pages/hund-blor-fra-poten` gjenstår etter re-auth.**


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
