# GitHub Repository Aanmaken (Stap-voor-Stap)

## Stap 1: GitHub Repo Aanmaken

1. Ga naar **github.com**
2. Log in (of maak account)
3. Klik op **"+"** (rechtsboven) → **"New repository"**
4. Vul in:
   - **Repository name:** `montrelle`
   - **Description:** `Montrelle.fr - Shopify fashion theme`
   - **Public** of **Private** (jouw keuze)
   - ❌ **NIET** "Initialize with README" aanvinken (hebben we al!)
5. Klik **"Create repository"**

## Stap 2: Code Pushen

Na het aanmaken toont GitHub instructies. Kopieer dit:

```bash
# Ga naar je project folder
cd /home/battletron/.openclaw/workspace/dropship-store

# Voeg GitHub toe als remote
git remote add origin https://github.com/JOUW_USERNAME/montrelle.git

# Push de code
git branch -M main
git push -u origin main
```

## Stap 3: Verificatie

Je krijgt een popup om in te loggen:
- **Username:** Je GitHub gebruikersnaam
- **Password:** Geen wachtwoord! Gebruik een **Personal Access Token**

### Personal Access Token Maken:
1. GitHub → Settings (rechtsboven)
2. Scroll naar beneden → **Developer settings**
3. **Personal access tokens** → **Tokens (classic)**
4. **Generate new token**
5. Vul in:
   - Note: "Montrelle Repo"
   - Expiration: 90 days
   - ✅ **repo** (alle rechten)
6. **Generate token**
7. **Kopieer de token** (je ziet hem maar 1x!)
8. Gebruik deze token als "wachtwoord" in de popup

## Stap 4: Check op GitHub

Refresh github.com/JOUW_USERNAME/montrelle

Je ziet nu:
- Alle bestanden
- 3 commits
- Complete folder structuur

## 🎉 Klaar!

Je code staat nu veilig in de cloud. Vanaf elke computer:

```bash
git clone https://github.com/JOUW_USERNAME/montrelle.git
```

---

## Alternatief: GitHub Desktop (Makkelijker)

Als je een GUI wilt:
1. Download **GitHub Desktop** (desktop.github.com)
2. Log in met je GitHub account
3. "Add existing repository" → selecteer `dropship-store` folder
4. Klik "Publish repository"
5. Klaar!

---

*Makkelijker kan niet! 🚀*
