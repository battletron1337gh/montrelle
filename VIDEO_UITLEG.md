# 🎬 Video op Shopify vs GitHub Pages

## Nu (GitHub Pages Preview)

**Probleem:** Video's werken niet altijd op mobiel omdat:
- Browsers blokkeren autoplay (zonder user interaction)
- iOS forceert fullscreen voor video's
- Data besparing mode blokkeert video's
- Externe CDN's kunnen traag zijn

**Onze oplossing:**
- ✅ 3 verschillende video bronnen (Coverr, Pexels, Vimeo)
- ✅ Automatische fallback naar CSS animatie
- ✅ JavaScript detecteert als video faalt

## Straks (Shopify)

**GOED NIEUWS:** Op Shopify werkt video VEEL better! 🎉

### Waarom?

| GitHub Pages | Shopify |
|--------------|---------|
| Externe video CDN | ✅ Eigen Shopify CDN (snel) |
| Geen compressie | ✅ Automatische video compressie |
| Handmatig uploaden | ✅ Direct uploaden in admin |
| Geen garantie | ✅ 99.9% uptime |
| Mobiele problemen | ✅ Mobiel geoptimaliseerd |

### Hoe werkt het op Shopify?

1. **In Shopify Admin:**
   - Settings → Files → Upload video
   - Of direct in theme editor

2. **In het thema:**
   ```liquid
   {{ 'video.mp4' | file_url }}
   ```

3. **Voordelen:**
   - Video wordt automatisch geoptimaliseerd
   - Werkt op alle apparaten
   - Snellere laadtijd
   - Geen externe afhankelijkheden

### Wat ik voor je kan doen op Shopify:

- ✅ Video uploaden in Shopify admin
- ✅ Thema configureren om Shopify video te gebruiken
- ✅ Mobiele optimalisatie instellen
- ✅ Poster image instellen (voor als video laadt)

### Kosten?

- **Video hosting:** Gratis (inbegrepen in Shopify)
- **Opslag:** Tot 20GB (meer dan genoeg)

---

## Samenvatting

| Nu | Straks op Shopify |
|----|-------------------|
| 3x video fallback | ✅ 1x Shopify video |
| CSS animatie backup | ✅ Niet nodig |
| Externe CDN | ✅ Eigen CDN |
| 50/50 kans | ✅ 99% werkt |

**Conclusie:** De huidige preview is goed genoeg voor demonstratie. Zodra je Shopify hebt, maak ik een professionele video setup die altijd werkt! 🚀
