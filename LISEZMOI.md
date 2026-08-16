# Ma Boussole — PWA

App mobile (Progressive Web App) reprenant ton Mandala Chart : grille interactive, suivi hebdomadaire, journal des actions, tableau de bord. Fonctionne hors-ligne une fois installée, données stockées uniquement sur ton téléphone (aucun serveur, aucun compte).

## Fichiers

```
index.html    → l'application (tout est dans ce seul fichier)
manifest.json → métadonnées d'installation (nom, icône, couleurs)
sw.js         → service worker (cache hors-ligne)
icons/        → icônes de l'app
```

## Déployer en 5 minutes (GitHub Pages — gratuit)

1. Crée un dépôt GitHub (ex. `ma-boussole`), public.
2. Dépose ces 4 éléments (`index.html`, `manifest.json`, `sw.js`, `icons/`) à la racine du dépôt.
3. Dans **Settings → Pages**, choisis la branche `main` et le dossier `/ (root)`, puis **Save**.
4. Après ~1 minute, ton app est en ligne à une adresse du type :
   `https://<ton-pseudo>.github.io/ma-boussole/`

## Alternative encore plus rapide : Netlify Drop

1. Va sur **app.netlify.com/drop**
2. Glisse-dépose le dossier complet (`index.html` + `manifest.json` + `sw.js` + `icons/`)
3. Netlify te donne une URL en quelques secondes — aucun compte requis pour tester.

## Installer sur Android

1. Ouvre l'URL déployée dans **Chrome** sur ton téléphone.
2. Menu (⋮) → **Ajouter à l'écran d'accueil** (ou une bannière d'installation apparaît automatiquement).
3. L'icône "Ma Boussole" apparaît comme une vraie app, plein écran, sans barre d'adresse.

## Important à savoir

- **Données locales uniquement** : tout est stocké dans le navigateur de ton téléphone (`localStorage`). Si tu changes de téléphone ou vides le cache du navigateur, les données sont perdues — pense à exporter/noter tes chiffres clés de temps en temps si tu veux un historique durable.
- **Un seul appareil à la fois** : pas de synchronisation entre téléphone et ordinateur pour l'instant (évolution possible plus tard avec une vraie base de données si tu veux passer à la V2).
- **Aperçu dans ce chat** : si tu ouvres `index.html` directement ici, l'app s'affiche mais la sauvegarde peut ne pas persister (bac à sable du navigateur intégré) — pour un usage réel, suis les étapes de déploiement ci-dessus.

## Prochaines évolutions possibles (V2)

- Synchronisation multi-appareils (nécessite un petit backend — je peux t'aider avec Claude Code)
- Export CSV/JSON du journal
- Rappels/notifications push pour le suivi quotidien
- Import direct des données depuis ton classeur Excel
