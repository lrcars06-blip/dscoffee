# DS Coffee-n-Cake

Site vitrine du coffee shop **DS Coffee-n-Cake**, 15 rue Thiers, 51000 Châlons-en-Champagne.

Site statique en un seul fichier (`index.html`) : HTML, CSS et JavaScript intégrés, sans build ni dépendance.

## Structure

```
index.html    page unique (styles + scripts inclus)
favicon.svg   icône d'onglet
robots.txt    indexation autorisée
.nojekyll     désactive Jekyll sur GitHub Pages
.gitignore
README.md
```

## Lancer en local

Ouvrir `index.html` dans un navigateur, ou :

```bash
npx serve .
```

## Déployer

- **GitHub Pages** : Settings → Pages → Source « Deploy from a branch » → `main` / `/ (root)`.
- **Vercel** : New Project → importer le dépôt → Framework « Other » → Deploy (aucune commande de build).
- **Netlify** : Add new site → importer le dépôt → Build command vide, Publish directory `.`.

## À configurer avant la mise en ligne

Tout se règle dans l'objet `CONFIG`, en haut du dernier `<script>` de `index.html` :

| Clé | Rôle | État |
|---|---|---|
| `HOURS` | Horaires d'ouverture (minutes depuis minuit, `null` = fermé, `0` = dimanche) | **Provisoires, à valider** |
| `BEHOLD_FEED_ID` | Flux Instagram @dscoffeencake via [behold.so](https://behold.so) | Vide → tuiles illustrées |
| `IG_COUNT` | Nombre de posts Instagram affichés | 8 |

À vérifier aussi dans le HTML :
- les associations « Parfait avec un… » sous chaque cake ;
- les liens « Mentions légales » et « Confidentialité » du pied de page (pages à créer, obligatoires en France) ;
- la balise `og:url` et un `sitemap.xml` à ajouter une fois le nom de domaine connu.

## Crédits

Typographies Google Fonts : Anton, Yellowtail, DM Sans (licence OFL).
Illustrations : SVG générés dans le code.
