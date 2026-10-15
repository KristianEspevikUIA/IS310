# Stack 5 · Bachelorgruppe · UiA

Nettsted for **Stack 5**, prosjektgruppen vår i **IS-310 Prosjektgjennomføring** ved Universitetet i Agder.
Siden er gruppas ansikt utad mot bedrifter og virksomheter som kan bli oppdragsgiver for
bacheloroppgaven vår våren 2027. Den bygger videre på oppgave 1 (presentasjon av gruppen) med en
profilering rettet mot potensielle oppdragsgivere.

**Publisert side:** https://kristianespevikuia.github.io/IS310/

## Gruppen

- Endi Muriqi
- Taavi-Topias Henell
- Brage Kristoffersen
- Nicolai A.M. Stephansen
- Kristian Espevik

## Innhold

Siden er én side med ankere til hver seksjon:

| Seksjon        | Anker          | Innhold                                                                  |
| -------------- | -------------- | ------------------------------------------------------------------------ |
| Toppen         | `#start`       | Promovideoen, hvem vi er, hva vi søker og nøkkeltall                     |
| Om oss         | `#om-oss`      | Gruppen overordnet og hva som kjennetegner oss                           |
| Teamet         | `#teamet`      | Presentasjon av hvert medlem, med lenke til LinkedIn                     |
| Kompetanse     | `#kompetanse`  | Samlet kompetanse og et eksempel fra tidligere prosjekter                |
| Prosjektønsker | `#prosjekt`    | Interesser, eksempler på oppdrag, ønsket oppdragsgiver og ambisjonsnivå  |
| Samarbeid      | `#samarbeid`   | Hva oppdragsgiver får, hva vi trenger, og spørsmål og svar               |
| Arbeidsform    | `#arbeidsform` | Slik jobber vi, verktøy og tidsplan                                      |
| Kontakt        | `#kontakt`     | Kontaktperson og e-post                                                  |

## Navn og logo

Gruppen heter **Stack 5**. Logoen er fem lag i en stack – ett for hver av oss. Den ligger som
`assets/img/favicon.svg` (fanen i nettleseren) og som innebygd SVG i toppmenyen i
[`index.html`](index.html), så endrer du logoen, må begge oppdateres.

## Promovideo

Promovideoen (1 min 47 s) er det første man ser på siden. Den ligger i repoet og spilles av direkte
fra GitHub Pages:

- `assets/video/promo.mp4` – selve videoen (1080p, 25 bilder/s, ca. 59 MB)
- `assets/img/promo-poster.jpg` – forsidebildet som vises før avspilling (16:9)

Skal videoen byttes ut, erstatter du de to filene med samme filnavn. Husk at GitHub ikke tar imot
filer over 100 MB, så en eksport rett fra redigeringsprogrammet må komprimeres først – for eksempel
til H.264 i 1080p med rundt 4–5 Mbit/s, og med «web optimized»/«fast start» slått på så videoen kan
starte før hele fila er lastet ned. Endrer lengden seg, oppdaterer du også «1:47» i
[`index.html`](index.html).

## Legg inn LinkedIn-profilen din

1. Åpne [`index.html`](index.html) og finn kortet ditt i seksjonen `id="teamet"`.
2. Lim inn hele adressen til profilen i `href=""` på LinkedIn-lenken, for eksempel
   `href="https://www.linkedin.com/in/fornavn-etternavn/"`.
3. Ferdig – knappen vises automatisk. Lenker med tom `href` skjules, så siden viser aldri døde
   lenker.

GitHub- og videolenken fungerer på samme måte. Har du motforestillinger mot LinkedIn, lim inn
adressen til en annen kanal og bytt teksten på knappen.

## Portrettbilder

Portrettene ligger i `assets/img/` som `fornavn.jpg` (`endi.jpg`, `taavi.jpg`, `brage.jpg`,
`nicolai.jpg` og `kristian.jpg`). Vil du bytte bilde, erstatter du fila med et nytt bilde med samme
filnavn. Et kvadratisk, profesjonelt portrett på rundt 400 × 400 px blir finest.

## Gruppebilde i toppen

Gruppebildet (`assets/img/gruppebilde.jpg`) er bakgrunn i toppseksjonen: teglveggen toner inn bak
video og tekst, og nederst står vi fem. Skal bildet byttes, bør det nye ha omtrent samme utsnitt –
gruppen midtstilt og god plass over hodene. Hvor stort bildet er og hvor mye av det som vises,
styres av variablene `--photo-w`, `--photo-hide` og `--photo-window` på `.hero` i
[`assets/css/styles.css`](assets/css/styles.css).

## Filer

```
index.html              hele nettsiden (én side, med ankere til hver seksjon)
assets/css/styles.css   design, farger, mørk modus og responsivt oppsett
assets/js/main.js       mobilmeny, avspillingsknapp, aktiv menylenke og fade-inn ved scroll
assets/img/             favicon, delingsbilde, portrettbilder, gruppebilde og forsidebilde til videoen
assets/video/           promovideoen
.github/workflows/      publiserer automatisk til GitHub Pages ved push til main
```

`assets/img/og-image.png` er bildet som vises når lenken deles på LinkedIn, i Teams eller i e-post.

## Kjøre lokalt

Åpne `index.html` direkte i nettleseren, eller start en enkel lokal server:

```bash
python -m http.server 8000
```

Siden ligger da på http://localhost:8000

## Publisering

Hver push til `main` bygger og publiserer siden automatisk via GitHub Actions
(`.github/workflows/pages.yml`).
