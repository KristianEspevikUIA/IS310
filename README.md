# IS-310 Prosjektgruppe · UiA høst 2026

Nettsted for prosjektgruppen vår i **IS-310 Prosjektgjennomføring** ved Universitetet i Agder.
Siden svarer på oppgave 1: presentasjon av hver student, og våre tanker om gruppen, prosjekttype,
bedrift og ambisjonsnivå.

**Publisert side:** https://kristianespevikuia.github.io/IS310/

## Gruppen

- Endi Muriqi
- Taavi-Topias Henell
- Brage Kristoffersen
- Nicolai Stephansen
- Kristian Espevik

## Filer

```
index.html              hele nettsiden (én side, med ankere til hver seksjon)
assets/css/styles.css   design, farger og responsivt oppsett
assets/js/main.js       mobilmeny, aktiv menylenke og fade-inn ved scroll
assets/img/             favicon og eventuelle portrettbilder
.github/workflows/      publiserer automatisk til GitHub Pages ved push til main
```

## Slik fyller du inn din egen presentasjon

Alt som skal fylles inn ligger i [`index.html`](index.html) under seksjonen `id="medlemmer"`.
Finn kortet med navnet ditt og bytt ut:

1. `<p class="member-role">` – rollen din i gruppen (f.eks. «Utvikler», «Prosjektleder»).
2. `<p class="member-bio">` – to–tre setninger om deg selv.
3. `<ul class="tags">` – to til fire interesser eller ferdigheter.
4. **Bilde (valgfritt):** legg bildet i `assets/img/` og bytt
   `<span class="avatar" aria-hidden="true">XX</span>` med
   `<img class="avatar" src="assets/img/fornavn.jpg" alt="Portrett av Fornavn Etternavn">`.
5. **Videopresentasjon (valgfritt):** fjern `hidden` fra `<a class="member-link">` og lim inn lenken.

Teksten om gruppen, prosjektet og ambisjonsnivået ligger i seksjonene `om-gruppen`, `prosjekt` og
`veikart` – juster gjerne ordlyden så den stemmer med det vi blir enige om.

Husk også å bytte kontakt-e-posten nederst i `index.html` til gruppas felles adresse.

## Kjøre lokalt

Åpne `index.html` direkte i nettleseren, eller start en enkel lokal server:

```bash
python -m http.server 8000
```

Siden ligger da på http://localhost:8000

## Publisering

Hver push til `main` bygger og publiserer siden automatisk via GitHub Actions
(`.github/workflows/pages.yml`). Første kjøring slår også på GitHub Pages for repoet.
