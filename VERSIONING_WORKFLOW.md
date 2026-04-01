# 🔄 Version Control & Shopify GitHub Workflow

## 1️⃣ GitHub Versioning (Tags)

### Een nieuwe versie taggen

```bash
# Ga naar je project
cd /home/battletron/.openclaw/workspace/dropship-store

# Check huidige status
git status

# Voeg wijzigingen toe
git add .
git commit -m "Beschrijving van de wijzigingen"

# Maak een versie tag (Semantic Versioning)
git tag -a v1.0.0 -m "Release v1.0.0 - Initial theme launch"

# Push alles naar GitHub
git push origin main
git push origin v1.0.0
```

### Semantic Versioning (SemVer)

| Versie | Format | Betekenis | Voorbeeld |
|--------|--------|-----------|-----------|
| Major | vX.0.0 | Grote wijzigingen, breaking changes | v2.0.0 |
| Minor | vx.Y.0 | Nieuwe features, backwards compatible | v1.1.0 |
| Patch | vx.y.Z | Bugfixes, kleine aanpassingen | v1.0.1 |

### Alle versies bekijken

```bash
# Toon alle tags
git tag -l

# Toon met details
git tag -l -n1

# Toon chronologisch
git log --tags --simplify-by-decoration --pretty="format:%ai %d" | head -20
```

### Terug naar een vorige versie

```bash
# Checkout specifieke versie
git checkout v1.0.0

# Of maak een nieuwe branch vanaf een versie
git checkout -b hotfix v1.0.0
```

---

## 2️⃣ Shopify GitHub Integratie

### Optie A: Shopify GitHub App (Aanbevolen)

#### Stap 1: GitHub App Installeren

1. Ga naar **Shopify Admin** → **Online Store** → **Themes**
2. Klik **"Add theme"** → **"Connect from GitHub"**
3. Je wordt doorgestuurd naar GitHub
4. Selecteer je repository: `battletron1337gh/montrelle`
5. Geef toestemming voor toegang

#### Stap 2: Branch Koppelen

1. Terug in Shopify → selecteer **main** branch
2. Kies **welke folder** het thema bevat:
   - Voor jou: `dropship-theme/` of `shopify-theme/`
3. Klik **"Connect"**

#### Stap 3: Auto-Deploy Inschakelen

In Shopify Theme Editor:
1. Ga naar het gekoppelde thema
2. Klik **"Customize"** → **Theme settings** (linksboven)
3. Scroll naar **GitHub integration**
4. ✅ **"Automatically deploy on push"**

### Optie B: Shopify CLI (Meer controle)

#### Installatie

```bash
# Installeer Shopify CLI
npm install -g @shopify/cli @shopify/theme

# Login met je Shopify account
shopify auth login --store JOUWSTORE.myshopify.com
```

#### Commands

```bash
# Push thema naar Shopify (ontwikkel-thema)
shopify theme push --theme-editor-sync

# Pull wijzigingen van Shopify
shopify theme pull

# Serve lokaal met live reload
shopify theme dev --store JOUWSTORE.myshopify.com

# Deploy naar live thema
shopify theme push --live
```

---

## 3️⃣ Complete Workflow (Dagelijkse werkwijze)

### Scenario 1: Lokale wijziging → Shopify

```bash
# 1. Werk lokaal in VS Code

# 2. Test wijzigingen
shopify theme dev --store montrelle.myshopify.com

# 3. Commit wijzigingen
cd /home/battletron/.openclaw/workspace/dropship-store
git add .
git commit -m "fix: adjust hero banner spacing on mobile"

# 4. Tag als het een release is
git tag -a v1.2.1 -m "Release v1.2.1 - Mobile fixes"

# 5. Push naar GitHub
git push origin main
git push origin v1.2.1

# 6. Shopify deployed automatisch (als GitHub App geïnstalleerd)
```

### Scenario 2: Shopify wijziging → Lokale code

```bash
# 1. Haal wijzigingen op van Shopify
shopify theme pull

# 2. Commit de wijzigingen
git add .
git commit -m "sync: update theme settings from Shopify admin"
git push origin main
```

### Scenario 3: Producten Updaten

```bash
# 1. Update CSV bestand
# Bewerk: dropship-store/dropship-theme/data/maison-fierce-products.csv

# 2. Commit
git add dropship-theme/data/maison-fierce-products.csv
git commit -m "data: update product inventory - 15 new items"
git push origin main

# 3. Importeer in Shopify Admin:
# Products → Import → Upload CSV
```

---

## 4️⃣ Branch Strategie (Voor meerdere developers)

```
main           ●────●────●────●────●
              /         \         \
develop      ●────●────●────●────●
            /      \           \
feature    ●────●  ●────●      ●
                           \
hotfix                      ●────●
```

### Branches

| Branch | Doel | Regel |
|--------|------|-------|
| `main` | Productie code | Alleen geteste code |
| `develop` | Integratie | Features samenvoegen |
| `feature/*` | Nieuwe features | Vanaf develop |
| `hotfix/*` | Snelle fixes | Vanaf main |

### Workflow met branches

```bash
# Nieuwe feature starten
git checkout -b feature/new-homepage-section develop

# Werk aan feature...
git add .
git commit -m "feat: add testimonial carousel section"

# Merge naar develop
git checkout develop
git merge feature/new-homepage-section

# Test, dan merge naar main
git checkout main
git merge develop

# Tag de release
git tag -a v1.3.0 -m "Release v1.3.0 - New homepage sections"
git push origin main --tags
```

---

## 5️⃣ Releases & Changelog

### Changelog Bijhouden

Maak een `CHANGELOG.md` bestand:

```markdown
# Changelog

## [1.2.1] - 2025-04-01
### Fixed
- Hero banner spacing on mobile devices
- Footer links not clickable on iOS

## [1.2.0] - 2025-03-28
### Added
- New collection grid layout
- Quick view modal for products
- Size guide popup

### Changed
- Updated font to Montserrat
- Improved image lazy loading

## [1.1.0] - 2025-03-25
### Added
- Newsletter signup section
- Instagram feed integration

## [1.0.0] - 2025-03-20
### Added
- Initial theme release
- Homepage with hero banner
- Product pages
- Cart and checkout flow
```

### GitHub Releases Maken

1. Ga naar GitHub repo → **Releases** → **"Create a new release"**
2. Kies een **tag** (bv. `v1.2.0`)
3. Vul in:
   - **Release title:** `Version 1.2.0 - New Features`
   - **Description:** Kopieer relevante changelog items
4. Klik **"Publish release"**

---

## 6️⃣ Automatisering (GitHub Actions)

### Auto-Deploy bij Push

Maak `.github/workflows/deploy-theme.yml`:

```yaml
name: Deploy to Shopify

on:
  push:
    branches: [ main ]
    paths:
      - 'dropship-theme/**'

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      
      - name: Setup Node
        uses: actions/setup-node@v3
        with:
          node-version: '18'
      
      - name: Install Shopify CLI
        run: npm install -g @shopify/cli
      
      - name: Deploy Theme
        env:
          SHOPIFY_FLAG_STORE: ${{ secrets.SHOPIFY_STORE }}
          SHOPIFY_CLI_THEME_TOKEN: ${{ secrets.SHOPIFY_THEME_TOKEN }}
        run: |
          cd dropship-theme
          shopify theme push --theme ${{ secrets.SHOPIFY_THEME_ID }}
```

### Secrets Configureren

In GitHub repo → **Settings** → **Secrets and variables** → **Actions**:

| Secret | Waarde |
|--------|--------|
| `SHOPIFY_STORE` | jouwstore.myshopify.com |
| `SHOPIFY_THEME_TOKEN` | Theme access token |
| `SHOPIFY_THEME_ID` | Theme ID nummer |

---

## 7️⃣ Samenvatting Commands

| Taak | Command |
|------|---------|
| Check status | `git status` |
| Voeg toe | `git add .` |
| Commit | `git commit -m "message"` |
| Push | `git push origin main` |
| Maak tag | `git tag -a v1.0.0 -m "Release"` |
| Push tags | `git push origin --tags` |
| Bekijk tags | `git tag -l` |
| Lokale dev | `shopify theme dev` |
| Deploy | `shopify theme push` |
| Pull van Shopify | `shopify theme pull` |

---

🎉 **Je kunt nu professioneel version control gebruiken met Shopify!**
