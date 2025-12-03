# Instructions pour déployer sur GitHub et Vercel

## 📋 Prérequis
- Compte GitHub
- Compte Vercel (peut être créé avec GitHub)

## 🚀 Étape 1 : Créer le dépôt GitHub

1. Allez sur https://github.com/new
2. Nommez votre dépôt (ex: `nss-website` ou `nous-sommes-la-solution`)
3. **Ne cochez PAS** les cases pour README, .gitignore ou licence (déjà créés)
4. Cliquez sur "Create repository"

## 🔗 Étape 2 : Connecter le dépôt local à GitHub

Exécutez ces commandes dans le terminal (depuis le dossier `NSS APP` parent) :

```bash
git remote add origin https://github.com/VOTRE-USERNAME/nom-du-depot.git
git branch -M main
git push -u origin main
```

Remplacez :
- `VOTRE-USERNAME` par votre nom d'utilisateur GitHub
- `nom-du-depot` par le nom que vous avez choisi

## 🌐 Étape 3 : Déployer sur Vercel

### Option A : Via l'interface web (Recommandé)

1. Allez sur https://vercel.com
2. Cliquez sur "Sign Up" et connectez-vous avec votre compte GitHub
3. Cliquez sur "Add New..." puis "Project"
4. Sélectionnez votre dépôt GitHub créé à l'étape 1
5. **Configuration importante** :
   - **Framework Preset**: `Other`
   - **Root Directory**: `NSS APP` (cliquez sur "Edit" et tapez `NSS APP`)
   - **Build Command**: (laissez vide)
   - **Output Directory**: (laissez vide)
6. Cliquez sur "Deploy"

### Option B : Via Vercel CLI

```bash
npm install -g vercel
vercel login
vercel
```

Suivez les instructions et spécifiez :
- Root Directory: `NSS APP`
- Framework: `Other`

## ✅ Vérification

Une fois déployé, Vercel vous donnera une URL (ex: `https://votre-projet.vercel.app`).

Votre site sera accessible en ligne !

## 🔄 Mises à jour futures

Pour mettre à jour le site après des modifications :

```bash
git add .
git commit -m "Description des modifications"
git push
```

Vercel déploiera automatiquement les nouvelles versions.

## 📝 Notes importantes

- Les images externes sont chargées depuis `wasafrica.org` et `html.themewant.com`
- Les assets locaux sont dans le dossier `assets/`
- Le site est 100% statique, aucun build n'est nécessaire
- Le fichier `vercel.json` est déjà configuré à la racine

