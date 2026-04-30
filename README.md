# Huisverkoop Liveblog

Een persoonlijke liveblog in NOS-stijl voor het bijhouden van de verkoop van je huis. Statisch (geen server), gratis te hosten op GitHub Pages.

## Wat zit erin

- **`index.html`** — De openbare pagina die je met vrienden deelt. Alleen-lezen. Ververst zichzelf elke 30 seconden.
- **`admin.html`** — Jouw redactiekamer. Hier schrijf je posts. Niet aan vrienden geven.
- **`posts.json`** — De data. Wordt gelezen door `index.html`.

## Snel opzetten (5 minuten)

### 1. Maak een GitHub repo

1. Ga naar [github.com/new](https://github.com/new).
2. Repository name: bv. `huisverkoop-liveblog`.
3. Public (gratis GitHub Pages werkt op publieke repos).
4. Maak aan en upload deze drie bestanden (`index.html`, `admin.html`, `posts.json`).

### 2. Zet GitHub Pages aan

1. Repo → **Settings** → **Pages**.
2. Source: `Deploy from a branch`.
3. Branch: `main` / `/ (root)` → Save.
4. Wacht ~1 minuut. Je site staat op `https://JOUWGEBRUIKER.github.io/huisverkoop-liveblog/`.

Die URL deel je met je vrienden.

### 3. Posts toevoegen — kies één van de twee:

#### Optie A — Eenvoudig: download en commit zelf

1. Open `admin.html` rechtstreeks vanaf je computer (dubbelklik) of via de GitHub Pages URL.
2. Schrijf je post → **Toevoegen aan tijdlijn**.
3. Klik **Download posts.json** → vervang het bestand in je repo → commit.
4. Pagina is binnen ~1 min bijgewerkt.

#### Optie B — Gladjes: één klik publiceren via GitHub API

Eenmalige setup:

1. Maak een fine-grained Personal Access Token: [github.com/settings/personal-access-tokens/new](https://github.com/settings/personal-access-tokens/new)
   - Repository access → **Only select repositories** → kies je liveblog-repo.
   - Permissions → Repository permissions → **Contents: Read and write**.
2. In `admin.html`: open ⚙ GitHub-instellingen, vul gebruikersnaam, repo, branch (`main`) en token in. Test verbinding.
3. Daarna: schrijf post → **Publiceer naar GitHub**. Klaar.

De token wordt **alleen in jouw browser** opgeslagen (localStorage). Niet ergens online. Werkt ook prima vanaf je telefoon — handig na een bezichtiging.

## Tips bij gebruik

- **Markdown in posts**: `**vet**`, `*cursief*`, `[tekst](https://...)`, lege regel = nieuwe alinea.
- **Foto's**: vul een afbeelding-URL in. Makkelijkste optie: upload de foto in een GitHub Issue in dezelfde repo (sleep de foto in het tekstveld), kopieer de gegenereerde URL, plak in het `Afbeelding URL` veld. Werkt blijvend en gratis.
- **Bewerken/verwijderen**: in `admin.html` zie je alle posts en kun je ze aanpassen of weggooien.
- **Labels**: `Breaking`, `Bod`, `Verkocht` worden rood; `Mijlpaal` wordt groen.

## Aandachtspunten / wat je moet weten

- **De pagina is publiek.** Een gratis GitHub Pages site is voor iedereen toegankelijk die de URL heeft. De URL is "geheim" maar niet versleuteld. Zet er dus geen dingen op die je écht niet op straat wilt (exacte vraagprijs, biedingen onder NDA, persoonsgegevens van bieders).
- **Adres en herkenbare foto's**: bedenk of je je voordeur, huisnummer en straatnaam herkenbaar in beeld wilt. Niemand weet wie achter de blog zit, maar je huis is wél te herkennen.
- **`admin.html` staat ook online** als je 'm in de repo zet. Dat is niet erg: zonder token kan niemand publiceren. Wil je 'm helemaal weghouden? Hou hem alleen lokaal op je computer (niet uploaden naar GitHub) en open via dubbelklik. Optie B (GitHub API) werkt dan nog steeds.
- **NOS-stijl, niet NOS-logo**: ik gebruik bewust geen echt NOS-logo of -merknaam in de pagina (auteursrecht). Stijl is geïnspireerd, niet identiek.
- **GitHub Pages cache**: na publiceren kan het 30s tot 2 min duren voor de update zichtbaar is. Vrienden met de pagina open zien het automatisch zodra het deploy klaar is.

## Eventuele uitbreidingen

Niks van dit alles is nodig, maar mocht je willen:

- **Eigen domeinnaam** (bv. `huisverkoop.jouwnaam.nl`) → GitHub Pages → Settings → Custom domain.
- **Reacties van vrienden** → koppel een service als [giscus](https://giscus.app) (gratis, gebruikt GitHub Discussions). Vergt wat extra config.
- **Pushmeldingen** → niet eenvoudig op een statische site; laat staan.

Veel succes met de verkoop! 🏡
