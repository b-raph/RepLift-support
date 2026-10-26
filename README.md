# Site de RepLift

Les trois pages publiques exigées par l'App Store, en HTML simple, sans
dépendance ni outil de construction. Français puis anglais sur chaque page.

| Page | Sert à |
|---|---|
| `index.html` | Accueil, présentation courte |
| `assistance.html` | **URL d'assistance** — obligatoire dans App Store Connect |
| `confidentialite.html` | **URL de politique de confidentialité** — obligatoire |

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

Elles doivent s'ouvrir sans connexion : le relecteur d'Apple n'a pas de compte
GitHub.
