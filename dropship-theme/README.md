# 📦 Noir & Blanc - Shopify Theme

Complete Shopify 2.0 theme voor Noir & Blanc fashion dropshipping store.
Gebaseerd op JulesValmont.fr maar moderner en geoptimaliseerd.

## 🚀 Quick Start

### 1. Theme Upload
```bash
# Zip de shopify-theme folder
cd shopify-theme && zip -r ../noir-blanc-theme.zip .

# Upload in Shopify Admin:
# Online Store → Themes → Upload theme
```

### 2. Producten Importeren
```bash
# Ga naar Shopify Admin:
# Products → Import → Upload products.csv
```

### 3. Collecties Maken
- **Femme** - Alle vrouwenproducten
- **Homme** - Alle mannenproducten  
- **Nouveautés** - Nieuwste producten
- **Promotions** - Producten met korting

## 📁 Theme Structuur

```
shopify-theme/
├── assets/           # CSS, JS, fonts
├── config/           # Theme settings schema
├── layout/
│   └── theme.liquid  # Hoofd layout
├── locales/
│   └── fr.json       # Franse vertalingen
├── sections/         # Herbruikbare secties
│   ├── announcement-bar.liquid
│   ├── header.liquid
│   ├── hero.liquid
│   ├── featured-collection.liquid
│   └── footer.liquid
├── snippets/         # Kleine code stukjes
└── templates/        # Pagina templates
    ├── index.liquid      # Homepage
    ├── product.liquid    # Product pagina
    └── collection.liquid # Collectie pagina
```

## ✨ Features

### Design
- [x] Donker/Licht modus toggle
- [x] Moderne typografie (Playfair Display + Inter)
- [x] Premium kleur palette
- [x] Smooth animaties
- [x] Mobile-first responsive

### UX
- [x] Quick view op producten
- [x] Wishlist functie (UI)
- [x] Sticky header
- [x] Cart drawer
- [x] Free shipping progress bar

### Marketing
- [x] Newsletter signup
- [x] Social media icons
- [x] Trust badges
- [x] UGC-ready (Instagram feed placeholder)

## 🎨 Customization

### Kleuren aanpassen
In **Theme Settings → Colors**:
- Primary: #0a0a0a (zwart)
- Accent: #b8a88a (oud goud)
- Background: #ffffff / #faf9f6

### Lettertypes
In **Theme Settings → Typography**:
- Headings: Playfair Display
- Body: Inter

### Homepage
Customize via **Theme Editor**:
1. Hero sectie - Grote banner
2. Featured Collection - Product grid
3. Newsletter - Email signup
4. Footer - Links & social

## 📊 Producten

### Van JulesValmont.fr overgenomen:
1. Doudoune Femme Slim Fit
2. Top Sans Manches Femme
3. Bottes d'Hiver Femme
4. Ensemble Lounge Femme
5. Grand Sac Cabas Femme
6. Chaussures Homme Élégantes
7. Pull Sans Manches Homme
8. Sweat à Capuche Unisexe
9. Veste d'Hiver Homme
10. Blouson Bomber Homme

### Product Setup
```
Titel: [Franse naam]
Beschrijving: HTML met bullet points
Prijs: Zie products.csv
Afbeeldingen: Nog toevoegen
Tags: femme|homme|unisexe + seizoen
```

## 🔧 Apps Aanbevolen

1. **Loox** - Foto reviews
2. **Klaviyo** - Email marketing
3. **Tidio** - Live chat
4. **ReConvert** - Upsells
5. **DSers** - Panda/Alibaba dropship

## 🌍 Domein Setup

1. Koop **noir-blanc.fr** (of .com)
2. Configureer in Shopify: Settings → Domains
3. Stel als primary domain in
4. Configureer SSL (automatisch)

## 📱 Social Media Handles

- Instagram: @noir.et.blanc.officiel
- Facebook: /noiretblanc
- TikTok: @noiretblanc
- Pinterest: /noiretblanc

## 📝 TODO voor Launch

- [ ] Echte productfoto's toevoegen
- [ ] Product beschrijvingen verfijnen
- [ ] Prijzen checken & aanpassen
- [ ] Verzendkosten instellen (Panda)
- [ ] Betaalmethodes configureren
- [ ] Legal pages aanmaken (CGV, etc.)
- [ ] Reviews app installeren
- [ ] Email templates aanpassen
- [ ] Favicon maken
- [ ] Logo uploaden

## 🐛 Troubleshooting

### Theme upload error?
- Check of alle bestanden aanwezig zijn
- Zorg dat `layout/theme.liquid` bestaat
- Probeer via Shopify Theme CLI

### Producten niet zichtbaar?
- Check of collecties zijn aangemaakt
- Verifieer product status (active)
- Check inventory levels

### Vertalingen werken niet?
- Zorg dat browser taal op FR staat
- Check locales/fr.json syntax

---

**Gemaakt:** 28 maart 2026  
**Versie:** 1.0  
**Markt:** Frankrijk 🇫🇷
