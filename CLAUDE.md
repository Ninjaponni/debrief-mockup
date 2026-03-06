# Debrief Mockup

Interaktiv scrollytelling-presentasjon som Superponni sender til kunder som en "kvittering" på briefen deres. Kunden scroller gjennom en visuell reise der en kjepphest (ponni) beveger seg fra venstre til høyre over et landskap, mens innholdet fra debrifen presenteres stasjon for stasjon.

## Hva dette er

En single-page HTML-fil (`index.html`) som fungerer som et rammeverk/template. Innholdet fylles inn per kunde basert på output fra debrief-skillen. Akkurat nå er den fylt med Sit Trening-data som testcase.

## Teknisk

- Én HTML-fil med inline CSS og JS, ingen bundler
- Fonter: Eighties Comeback (headings), Inter (body) - ligger i `fonts/`
- Logo: `logo.svg` (Superponni hvit logo)
- Backup av tidligere versjon: `index-backup.html`
- Åpnes direkte i nettleser: `file:///Users/tormartin/debrief-mockup/index.html`

## Brand

Superponni kreativt byrå, Trondheim.

- Tawny Port: `#651a5a`
- Salmon: `#fe8c68`
- Blue Romance: `#dcfae0`
- Hint of Green: `#f4fff6`
- Blue Chalk: `#f7ecff`

## De 9 stasjonene

1. **Stallen** - Intro med kundenavn og prosjekttittel
2. **Oppdraget** - Forståelse av oppgaven med nøkkeltall (count-up animasjon)
3. **Leveransen** - Hva som skal leveres (tilpasses pitch vs vanlig oppdrag)
4. **Innsikt** - Research-funn med kildelenker
5. **Gapet** - GAP-analyse: "I dag" vs "Målet" med barrierer (tooltip ved hover)
6. **Kjernen** - Problemdefinisjonen (dramatisk reveal, det viktigste øyeblikket)
7. **Muligheter** - Strategiske retninger, accordion (én åpen om gangen), med "Denne liker jeg"-favorisering
8. **Spørsmål** - Spørsmål til kunden med textarea-input
9. **Neste steg** - CTA for å sende tilbake favoritter og svar

## Scrollytelling-mekanikk

- Ponni beveger seg fra 5% til 90% av skjermbredden basert på scroll-progress
- Landskap (SVG) i bunn er fixed og panner med ponnien
- Landskapet har z-index foran innholdet (innhold forsvinner bak landskapet)
- Ponni følger terrenget i SVG-en (Y-posisjon interpoleres fra terrainPoints)
- Hver stasjon har scroll-triggered animasjoner (reveal, reveal-left, reveal-scale)

## Atmosfære

- Mørk plum-bakgrunn med subtil grain-overlay
- Stjernehimmel med twinkling-animasjon
- Stjerneskudd hvert 6-14 sekund
- Partikler som svever oppover i brandfargene
- Måne øverst til høyre med pulserende glow
- Generelt: lekent og levende, ikke korporat

## Designprinsipper

- Teksten er king. Aldri ofre lesbarhet for visuelle effekter
- Lekent og alive, ikke korporat
- `text-wrap: balance` på headings for å unngå enslige ord
- Ikke bruk emdash, bruk komma eller punktum
- Animasjoner skal føles "digg" og flytende, ikke hakkete
- Subtile effekter, ikke koko bananas

## Hva som er placeholder

- Ponnien er en emoji (skal erstattes med custom illustrasjon)
- Landskapet er enkel SVG (Tor Martin designer dette selv)
- Innholdet er Sit Trening-spesifikt (skal bli et generisk template)

## Neste steg

- Finere animasjoner mellom seksjoner
- Custom ponni-illustrasjon
- Custom landskap-design
- Template-system som fylles fra debrief-skill output
- Evt. koble "Send dine tanker" til faktisk backend
