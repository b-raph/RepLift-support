# Site de RepLift

Les trois pages publiques exigées par l'App Store **et par Google Play**, en
HTML simple, sans dépendance ni outil de construction. Français puis anglais
sur chaque page, et une seule version des pages pour les deux plateformes : ce
qui ne vaut que d'un côté porte une étiquette.

| Page | Sert à |
|---|---|
| `index.html` | Accueil, présentation courte |
| `assistance.html` | **URL d'assistance** — obligatoire dans App Store Connect, et attendue dans la fiche Play |
| `confidentialite.html` | **URL de politique de confidentialité** — obligatoire des deux côtés |

## Adresse de contact

`rbm.entreprises@gmail.com`, dans `assistance.html` et `confidentialite.html`.
Pour en changer :

```bash
grep -rl rbm.entreprises@gmail.com . | xargs sed -i '' 's/rbm.entreprises@gmail.com/nouvelle@adresse.fr/g'
```

## Mise en ligne

Dépôt **public**, puis Settings → Pages → Source : `main`, dossier `/`.
Les URL deviennent :

- `https://<compte>.github.io/<depot>/assistance.html`
- `https://<compte>.github.io/<depot>/confidentialite.html`

Elles doivent s'ouvrir sans connexion : ni le relecteur d'Apple ni celui de
Google n'a de compte GitHub.

## Cohérence avec la fiche Play

Le formulaire **Sécurité des données** de Google Play doit dire la même chose
que `confidentialite.html` : aucune donnée collectée, aucune donnée partagée.
Une divergence entre les deux est un motif de rejet.
