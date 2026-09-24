# IS-310 Bachelorgruppe · UiA

Nettsted for prosjektgruppen vår i **IS-310 Prosjektgjennomføring** ved Universitetet i Agder.
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
| Toppen         | `#start`       | Hvem vi er, hva vi søker og nøkkeltall                                   |
| Om oss         | `#om-oss`      | Gruppen overordnet og hva som kjennetegner oss                           |
| Teamet         | `#teamet`      | Presentasjon av hvert medlem, med lenke til LinkedIn                     |
| Kompetanse     | `#kompetanse`  | Samlet kompetanse og et eksempel fra tidligere prosjekter                |
| Prosjektønsker | `#prosjekt`    | Interesser, eksempler på oppdrag, ønsket oppdragsgiver og ambisjonsnivå  |
| Samarbeid      | `#samarbeid`   | Hva oppdragsgiver får, hva vi trenger, og spørsmål og svar               |
| Arbeidsform    | `#arbeidsform` | Slik jobber vi, verktøy og tidsplan                                      |
| Kontakt        | `#kontakt`     | Kontaktperson og e-post                                                  |

## Legg inn LinkedIn-profilen din

1. Åpne [`index.html`](index.html) og finn kortet ditt i seksjonen `id="teamet"`.
2. Lim inn hele adressen til profilen i `href=""` på LinkedIn-lenken, for eksempel
   `href="https://www.linkedin.com/in/fornavn-etternavn/"`.
3. Ferdig – knappen vises automatisk. Lenker med tom `href` skjules, så siden viser aldri døde
   lenker.

GitHub- og videolenken fungerer på samme måte. Har du motforestillinger mot LinkedIn, lim inn
adressen til en annen kanal og bytt teksten på knappen.

## Bilde (valgfritt)

Legg bildet i `assets/img/` og bytt `<span class="avatar" aria-hidden="true">XX</span>` i kortet ditt med
`<img class="avatar" src="assets/img/fornavn.jpg" alt="Portrett av Fornavn Etternavn">`.
Et kvadratisk, profesjonelt portrett (minst 200 × 200 px) blir finest.

## Filer

```
index.html              hele nettsiden (én side, med ankere til hver seksjon)
assets/css/styles.css   design, farger, mørk modus og responsivt oppsett
assets/js/main.js       mobilmeny, aktiv menylenke og fade-inn ved scroll
assets/img/             favicon, delingsbilde (og eventuelle portrettbilder)
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
