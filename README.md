# roger-srey

Site personnel de **Roger Srey** : un inventaire et un carnet de notes écrits en
Markdown, publiés sur GitHub Pages.

- Site : https://srroger.github.io/roger-srey/
- Accueil : [`index.md`](./index.md)

Le reste du contenu vit dans les notes `.md` à la racine (`Inventaire.md`,
`Livres.md`, …). La mise en page est dans `_layouts/default.html`, le style dans
`assets/css/style.scss` et les cartes de l'accueil directement dans `index.md`.

## Recherche

La recherche est assurée par [Pagefind](https://pagefind.app/) : l'index est
généré au moment du build par GitHub Actions (`.github/workflows/pages.yml`).
Le workflow doit être sélectionné comme source de publication dans
**Settings → Pages → Build and deployment → Source : GitHub Actions**.

## Build local

```sh
bundle install
bundle exec jekyll serve
```

Pour tester la recherche en local, ajouter l'index Pagefind après le build :

```sh
bundle exec jekyll build
npx pagefind --site _site
```
