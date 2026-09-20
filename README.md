# roger-srey

Site personnel de **Roger Srey** : un inventaire et un carnet de notes écrits en
Markdown, publiés sur GitHub Pages.

- Site : https://srroger.github.io/roger-srey/
- Accueil : [`index.md`](./index.md)

Le reste du contenu vit dans les notes `.md` à la racine (`Inventaire.md`,
`Livres.md`, …). La mise en page est dans `_layouts/default.html`, le style dans
`assets/css/style.scss` et les cartes de l'accueil directement dans `index.md`.

## Icônes

Le layout `_layouts/default.html` ne référence qu'un seul nom de fichier :
`<link rel="icon" href="{{ '/favicon.svg' | relative_url }}">`. Les trois SVG
présents à la racine sont interchangeables sans toucher au code :

- `favicon.svg` — **en service** : un R tracé dans la radiographie
  `images/HarmoRayonX.jpeg`, sur une tuile noire (le fichier s'appelait
  `favicon-r.svg` avant sa mise en service).
- `favicon-radio.svg` — variante : trois anches de la radiographie cadrées en
  carré (l'export GIMP d'origine, 885 × 784, reste dans l'historique git,
  commit `a966570`).
- `favicon-sr.svg` — variante : le monogramme SR, les deux lettres taillées dans
  la même radiographie et se chevauchant sur la même tuile noire. Pour la mettre
  en service : `mv favicon-sr.svg favicon.svg`.

Les trois sont carrés et embarquent l'image en base64 : 256 px pour le R
(9,9 Ko) et pour le SR (7,6 Ko), les lettres étant découpées dans le PNG, 192 px
pour la radiographie (26 Ko). Les deux derniers ne contiennent volontairement
**aucun `clipPath`** : un pochoir est ignoré par certains outils
(visionneuses d'images, aperçus d'éditeurs), qui n'affichent alors que la photo,
sans la lettre. Ici la tuile est un simple rectangle vectoriel et la lettre un
PNG à canal alpha : tout s'affiche partout. Le R occupe les trois quarts de la
hauteur de la tuile — assez grand pour se lire d'un coup d'œil, assez détaché des
bords pour ne pas être à l'étroit — sur un fond noir (`#1a1612`) aux coins
arrondis à 15 %. La texture intérieure est volontairement très contrastée
(gamma 1,8), pour que les anches se voient même en tout petit.

Le monogramme SR applique la même recette : la paire occupe 57 % de la hauteur de
la tuile et 78 % de sa largeur, les deux lettres se chevauchant sur 26 % de leur
hauteur. Aucun trait ne sépare le S du R : le S passe **derrière** et reçoit 55 %
de la lumière de la texture, le R devant gardant la sienne. La séparation se fait
donc par la lumière, seule façon de laisser voir le chevauchement sans amputer
une des deux lettres.

## Photos de profil

Trois jeux d'images carrées, au choix, à téléverser telles quelles (ces services
prennent le PNG) :

- `images/avatar-r-1024.png` (et sa copie `-460.png`) — le R du favicon sur fond
  noir, plein cadre. La lettre est dimensionnée à 66 % de la hauteur pour tenir
  dans le **cercle inscrit** : les plates-formes recadrent en rond, et un R plus
  grand verrait ses coins rognés. Le fond n'a pas de coins arrondis, c'est la
  plate-forme qui applique sa propre forme.
- `images/avatar-sr-1024.png` (et sa copie `-460.png`) — le monogramme SR, mêmes
  principes : le fond noir est plein cadre et les deux lettres, ensemble, tiennent
  dans le cercle (leur boîte garde un rayon de 0,48 pour 0,50 disponibles).
- `images/avatar-photo-1024.png` (et sa copie `-460.png`) — la radiographie
  elle-même, cadrage « plein cadre » : les trois anches entières, parce que
  l'export GIMP, plus large que haut, perdrait ses bords dans un recadrage rond.

Un export GIMP en SVG embarque le PNG d'origine tel quel : réduire l'image avant
l'export évite les fichiers de plusieurs centaines de Ko. Les navigateurs
n'affichant les favicons qu'en 16 à 32 px, inutile de viser plus grand. Après un
changement, forcer le rechargement (Ctrl+Maj+R) : le cache des favicons est le
plus tenace de tous.

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

Les gems sont installées dans `vendor/bundle` (dossier ignoré par git). Si
`bundle exec jekyll` répond « command not found: jekyll », c'est que ce chemin
n'est pas configuré : `bundle config set --local path vendor/bundle` (une fois),
ou prefixer la commande par `BUNDLE_PATH=vendor/bundle`.

Pour tester la recherche en local, ajouter l'index Pagefind après le build :

```sh
bundle exec jekyll build
npx pagefind --site _site
```
