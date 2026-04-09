# outils-immobilier

Site satellite GitHub Pages — ressource indépendante sur les outils numériques pour l'immobilier.

## Structure

```
outils-immobilier/
├── index.html                          # Page d'accueil (racine)
├── css/
│   └── style.css                       # CSS partagé
└── pages/
    ├── decoration-architecture.html    # Outils déco & archi (liens Ynspir)
    ├── recherche-financement.html      # Estimation, crédit, marché
    └── a-propos.html                   # Page À propos
```

## Déploiement GitHub Pages

### 1. Créer le repository

```bash
# Créer un nouveau repo sur github.com nommé : outils-immobilier
# (ou le nom de ton choix)
```

### 2. Pousser les fichiers

```bash
git init
git add .
git commit -m "Initial commit — site outils immobilier"
git branch -M main
git remote add origin https://github.com/USERNAME/outils-immobilier.git
git push -u origin main
```

### 3. Activer GitHub Pages

1. Aller dans **Settings** du repo
2. Section **Pages** dans le menu gauche
3. Source : **Deploy from a branch**
4. Branch : `main` / `/ (root)`
5. Sauvegarder

Le site sera disponible à :
`https://USERNAME.github.io/outils-immobilier/`

⚠️ Remplacer `USERNAME` par ton nom d'utilisateur GitHub dans tous les fichiers HTML (balises canonical, og:url, Schema.org).

### 4. Remplacer USERNAME

```bash
# macOS / Linux
find . -name "*.html" -exec sed -i '' 's/USERNAME/TON_USERNAME_GITHUB/g' {} +

# Windows (PowerShell)
Get-ChildItem -Recurse -Filter "*.html" | ForEach-Object {
  (Get-Content $_.FullName) -replace 'USERNAME', 'TON_USERNAME_GITHUB' | Set-Content $_.FullName
}
```

## Liens Ynspir intégrés

| Page | Ancre | URL cible |
|------|-------|-----------|
| `index.html` | architecte d'intérieur en ligne | https://ynspir.com/architecte-interieur-en-ligne/ |
| `index.html` | décoration IA gratuite | https://ynspir.com/decoration-ia-gratuite/ |
| `decoration-architecture.html` | architecte d'intérieur en ligne (×2) | https://ynspir.com/architecte-interieur-en-ligne/ |
| `decoration-architecture.html` | décoration IA gratuite (×2) | https://ynspir.com/decoration-ia-gratuite/ |

## Pour ajouter les liens Montclair (demain)

1. Créer `pages/outils-transaction.html` (ou le nom approprié)
2. Intégrer les liens Montclair avec les ancres pertinentes
3. Ajouter le lien dans la nav de toutes les pages
4. `git add . && git commit -m "Ajout page Montclair" && git push`

## SEO checklist

- [x] Balises `<title>` et `<meta description>` uniques par page
- [x] `<link rel="canonical">` sur chaque page
- [x] Schema.org JSON-LD (WebSite sur index, Article sur sous-pages)
- [x] Open Graph sur la page d'accueil
- [x] Liens internes cohérents entre toutes les pages
- [x] Ancres de liens vers Ynspir descriptives et contextuelles
- [ ] Remplacer USERNAME par le vrai nom d'utilisateur GitHub
- [ ] Soumettre le sitemap dans Google Search Console après indexation
