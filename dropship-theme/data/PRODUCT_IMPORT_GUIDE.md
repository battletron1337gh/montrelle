# Montrelle Product Import Guide

## Geïmporteerde Producten van Maison Fierce

### Collectie: FEMME (Dames)

| Product | Prijs | Vergelijkprijs | Maten | Tags |
|---------|-------|----------------|-------|------|
| **Matilda** - Robe longue moulante | €89,00 | €129,00 | XS, S, M, L | robe, soiree, mariage, elegante |
| **Liora** - Ensemble blazer et pantalon | €119,00 | €159,00 | XS, S, M, L | ensemble, blazer, bureau, elegante |
| **Imogen** - Robe longue dos nu | €79,00 | €109,00 | XS, S, M | robe, dos-nu, ete, volants |
| **Saoirse** - Robe courte en dentelle | €69,00 | €99,00 | XS, S, M | robe, dentelle, courte, soiree |
| **Céline** - Robe longue dos nu drapée | €95,00 | €135,00 | XS, S, M | robe, longue, drapee, mariage |

### Collectie: HOMME (Heren)

| Product | Prijs | Vergelijkprijs | Maten | Tags |
|---------|-------|----------------|-------|------|
| **Axel** - Short sport 2 en 1 | €45,00 | €65,00 | S, M, L | short, sport, fitness, training |
| **Kaleb** - Pantalon à carreaux | €59,00 | €79,00 | S, M, L | pantalon, carreaux, casual, quotidien |
| **Kade** - Pantalon cargo | €65,00 | €85,00 | S, M, L | pantalon, cargo, decontracte, exterieur |
| **Noah** - Pantalon jogging à carreaux | €49,00 | €69,00 | S, M, L | pantalon, jogging, carreaux, detente |

---

## Hoe importeer je in Shopify?

### Stap 1: Producten importeren
1. Shopify Admin → **Producten**
2. Klik op **Importeren**
3. Upload `maison-fierce-products.csv`
4. Klik op **Producten importeren**

### Stap 2: Collecties aanmaken
Maak handmatig twee collecties aan:

**Collectie: Femme**
- Condition: `Product tag = femme`
- URL: `/collections/femme`

**Collectie: Homme**
- Condition: `Product tag = homme`
- URL: `/collections/homme`

### Stap 3: Productfoto's uploaden
De CSV bevat placeholder URLs. Je moet:
1. Eigen productfoto's maken/uploaden
2. Of dropshipping supplier foto's gebruiken
3. Foto's toevoegen aan elk product in Shopify

### Stap 4: Voorraad aanpassen
De CSV bevat testvoorraad (5-20 stuks per variant). Pas dit aan naar je eigen voorraad/supplier beschikbaarheid.

---

## Belangrijke Opmerkingen

⚠️ **Dropshipping:** Deze producten zijn gebaseerd op Maison Fierce. Voor eigen verkoop moet je:
- Eigen supplier vinden (Spocket, CJ Dropshipping, etc.)
- Vergelijkbare producten sourcen
- Eigen productfoto's maken

⚠️ **Merknamen:** Productnamen zijn geïnspireerd op maar niet exact gekopieerd van Maison Fierce.

⚠️ **Prijzen:** Prijzen zijn indicatief. Pas aan op basis van je kostprijs + marge.

---

## CSV Kolommen Uitleg

- **Handle**: Unieke product identifier (URL-vriendelijk)
- **Title**: Product naam
- **Body (HTML)**: Product beschrijving met HTML
- **Vendor**: Merk naam (Montrelle)
- **Type**: Product type (Robe, Pantalon, etc.)
- **Tags**: Tags voor filtering (femme, homme, etc.)
- **Variant**: Maten/kleuren opties
- **Price**: Verkoopprijs
- **Compare At Price**: Oude prijs (voor korting weergave)
- **Image Src**: URL naar productfoto (placeholder!)

---

## Volgende Stappen

1. ✅ Importeer de CSV in Shopify
2. ✅ Maak collecties aan
3. ✅ Configureer het Montrelle theme
4. ✅ Voeg eigen productfoto's toe
5. ✅ Koppel supplier (voor dropshipping)
6. ✅ Test bestelling plaatsen
7. ✅ Go live!

---

*Laatst bijgewerkt: 31 maart 2026*
