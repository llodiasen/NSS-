# Instructions de déploiement

## Déploiement sur GitHub

1. Créer un nouveau dépôt sur GitHub (https://github.com/new)
2. Nommer le dépôt (ex: `nss-website`)
3. Ne pas initialiser avec README, .gitignore ou licence
4. Exécuter les commandes suivantes :

```bash
git remote add origin https://github.com/VOTRE-USERNAME/nss-website.git
git branch -M main
git push -u origin main
```

## Déploiement sur Vercel

### Option 1 : Via l'interface Vercel

1. Aller sur https://vercel.com
2. Se connecter avec GitHub
3. Cliquer sur "New Project"
4. Importer le dépôt GitHub créé précédemment
5. Configuration :
   - **Framework Preset**: Other
   - **Root Directory**: `NSS APP`
   - **Build Command**: (laisser vide)
   - **Output Directory**: (laisser vide)
6. Cliquer sur "Deploy"

### Option 2 : Via Vercel CLI

```bash
npm i -g vercel
vercel login
vercel
```

Suivre les instructions et spécifier :
- Root Directory: `NSS APP`
- Framework: Other

## Configuration Vercel (si nécessaire)

Si vous avez besoin de configurer le routage, le fichier `vercel.json` est déjà créé à la racine du projet.

## Notes importantes

- Les images sont chargées depuis `wasafrica.org` et `html.themewant.com`
- Les assets locaux sont dans le dossier `assets/`
- Le site est statique, aucun build n'est nécessaire

