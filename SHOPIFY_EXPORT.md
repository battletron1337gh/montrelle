# 🚀 Shopify Export Checklist

## Stap 1: Theme Upload

```bash
# Zip het thema
cd dropship-store/shopify-theme
zip -r ../../noir-blanc-theme.zip .

# Of download de hele folder
```

**Shopify Admin:**
1. Online Store → Themes
2. "Add theme" → Upload zip file
3. Selecteer `noir-blanc-theme.zip`

## Stap 2: Producten Importeren

**Shopify Admin:**
1. Products → Import
2. Upload `shopify-theme/data/products.csv`
3. Check "Overwrite products with matching handles"
4. Review import

## Stap 3: Collecties Maken

| Collectie | Condition | Beschrijving |
|-----------|-----------|--------------|
| Femme | Product tag = femme | Mode pour femmes |
| Homme | Product tag = homme | Mode pour hommes |
| Unisexe | Product tag = unisexe | Pour tout le monde |
| Nouveautés | Created date > 30 days | Dernières arrivées |
| Promotions | Compare at price > 0 | Soldes & promos |

## Stap 4: Thema Configureren

**Theme Settings:**
- Logo uploaden
- Kleuren checken
- Lettertypes instellen
- Social links toevoegen
- Menu's aanmaken

**Homepage:**
- Hero sectie: Banner afbeelding + tekst
- Featured collections: Femme + Homme
- Newsletter: Text aanpassen
- Footer: Menu's linken

## Stap 5: Panda/Alibaba Koppeling

1. DSers app installeren
2. Panda als leverancier toevoegen
3. Producten linken aan Panda catalogus
4. Prijzen & voorraad sync instellen

## Stap 6: Payment & Shipping

**Settings → Payments:**
- Shopify Payments (creditcard)
- PayPal activeren
- iDEAL (voor NL testen)

**Settings → Shipping:**
- France: €0 (vanaf €50)
- France: €4.90 (< €50)
- EU: €9.90
- Express: €14.90

## Stap 7: Legal Pages

Maak aan:
- /pages/mentions-legales
- /pages/politique-de-confidentialite
- /pages/conditions-generales
- /pages/livraison-retours

## Stap 8: Pre-Launch Check

- [ ] Alle producten hebben foto's
- [ ] Prijzen zijn correct
- [ ] Verzendkosten getest
- [ ] Betaalmethodes werken
- [ ] Email templates goed
- [ ] Mobile responsive check
- [ ] Speed test (PageSpeed)

## Export Files

| Bestand | Locatie | Doel |
|---------|---------|------|
| Theme ZIP | `dropship-store/shopify-theme/` | Upload naar Shopify |
| Products CSV | `shopify-theme/data/products.csv` | Product import |
| Brand Guide | `docs/BRAND_IDENTITY.md` | Referentie |
| Logo Brief | `docs/LOGO_BRIEF.md` | Voor designer |

---

Klaar voor export! 🎉
