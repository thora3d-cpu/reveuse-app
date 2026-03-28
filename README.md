# Pour ma rêveuse 💜 — Guide de déploiement

## Structure du projet
```
rêveuse-app/
├── index.html       ← L'application complète
├── manifest.json    ← Config PWA (icône, nom, couleurs)
├── sw.js            ← Service worker (mode hors-ligne)
├── icons/           ← Dossier icônes (à créer)
│   ├── icon-192.png
│   └── icon-512.png
└── README.md
```

## Étape 1 — Héberger sur GitHub Pages (gratuit)

1. Créer un compte sur github.com
2. Nouveau repository : "reveuse-app" (public)
3. Upload les 3 fichiers (index.html, manifest.json, sw.js)
4. Settings → Pages → Source: "main" → Save
5. URL : https://TON_PSEUDO.github.io/reveuse-app

## Étape 2 — Créer les icônes

Va sur https://favicon.io/favicon-generator/
- Texte : 💜 ou R
- Background : #534AB7
- Télécharge et extrais icon-192.png et icon-512.png dans /icons/

## Étape 3 — Firebase (synchro temps réel)

1. Va sur https://console.firebase.google.com
2. "Créer un projet" → nom : "reveuse-app" → Continue
3. Dans le projet : "Firestore Database" → Créer → Mode test → OK
4. Paramètres (⚙) → "Vos applications" → </> (Web) → Enregistrer
5. Copie les valeurs : apiKey, projectId, appId
6. Dans l'app : bouton ⚙ en haut à droite → colle les valeurs → Sauvegarder

## Étape 4 — Installer sur les téléphones

**Android (Chrome) :**
- Ouvrir l'URL dans Chrome
- Menu (⋮) → "Ajouter à l'écran d'accueil"

**iPhone (Safari) :**
- Ouvrir l'URL dans Safari (pas Chrome!)
- Partager (□↑) → "Sur l'écran d'accueil"

## Utilisation

- **Mode Dylan** : créer rappels, tâches, flashcards, mots doux
- **Mode Elle** : voir et cocher ce qui est fait
- Les flashcards s'ouvrent en appuyant sur la carte
- La synchro est instantanée si Firebase est configuré

## Prochaines étapes possibles

- [ ] Notifications WhatsApp (CallMeBot API)
- [ ] Interface dyslexie-friendly côté elle (grande police, icônes)
- [ ] Catégories (admin, santé, perso...)
- [ ] Mode flashcard avec score de mémorisation
