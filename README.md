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
`<link rel="icon" href="{{ '/favicon.svg' | relative_url }}">`. Les quatre SVG
présents à la racine sont interchangeables sans toucher au code : il suffit de
renommer celui qu'on veut mettre en service.

- `favicon.svg` — **en service** : le monogramme SR, les deux lettres taillées
  dans la radiographie `images/HarmoRayonX.jpeg` et se chevauchant sur une tuile
  noire. Aucun trait ne sépare le S du R : le S passe **derrière** et ne reçoit
  que 55 % de la lumière de la texture, le R devant gardant la sienne (le fichier
  s'appelait `favicon-sr.svg` avant sa mise en service).
- `favicon-srLine.svg` — variante : le même monogramme, mais le S passe **devant**
  et un liseré noir de 3,5 px (une fois réduit à 256) l'isole du R ; la fonte est
  la Condensed Bold, ce qui autorise des lettres plus grandes. Pour la mettre en
  service : `mv favicon.svg favicon-sr.svg && mv favicon-srLine.svg favicon.svg`.
- `favicon-r.svg` — variante : un R tracé dans la même radiographie, sur la même
  tuile (le fichier était en service avant le monogramme).
- `favicon-radio.svg` — variante : trois anches de la radiographie cadrées en
  carré (l'export GIMP d'origine, 885 × 784, reste dans l'historique git,
  commit `a966570`).

Les quatre sont carrés et embarquent l'image en base64 : 256 px pour le SR
(7,5 Ko), le SR au liseré (9,7 Ko) et le R (9,6 Ko), les lettres étant découpées
dans le PNG, 192 px pour la radiographie (26 Ko). Les trois derniers ne
contiennent volontairement **aucun `clipPath`** : un pochoir est ignoré par
certains outils (visionneuses d'images, aperçus d'éditeurs), qui n'affichent
alors que la photo, sans la lettre. Ici la tuile est un simple rectangle
vectoriel et la lettre un PNG à canal alpha : tout s'affiche partout. Le R occupe
les trois quarts de la hauteur de la tuile — assez grand pour se lire d'un coup
d'œil, assez détaché des bords pour ne pas être à l'étroit — sur un fond noir
(`#1a1612`) aux coins arrondis à 15 %. La texture intérieure est volontairement
très contrastée (gamma 1,8), pour que les anches se voient même en tout petit.

Le monogramme SR applique la même recette : la paire occupe 57 % de la hauteur de
la tuile et 78 % de sa largeur, les deux lettres se chevauchant sur 26 % de leur
hauteur. Aucun trait ne sépare le S du R : le S passe **derrière** et reçoit 55 %
de la lumière de la texture, le R devant gardant la sienne. La séparation se fait
donc par la lumière, seule façon de laisser voir le chevauchement sans amputer
une des deux lettres.

Le SR au liseré change de parti pris : le S passe **devant**, et c'est cette fois
un trait qui le détache du R. Ce liseré est l'écart entre la lettre et la même
lettre épaissie d'un contour de 14 px (sur les 1024 px de travail, soit ~3,5 px
une fois réduit à 256) : peint en noir, il disparaît sur la tuile et ne se voit
que là où il recouvre le R. La fonte passe en Condensed Bold, plus étroite, ce
qui autorise 66 % de la hauteur de la tuile sans déborder en largeur.

## Photos de profil

Quatre jeux d'images carrées, au choix, à téléverser telles quelles (ces services
prennent le PNG) :

- `images/avatar-r-1024.png` (et sa copie `-460.png`) — le R de `favicon-r.svg`,
  sur fond noir, plein cadre. La lettre est dimensionnée à 66 % de la hauteur
  pour tenir dans le **cercle inscrit** : les plates-formes recadrent en rond, et
  un R plus grand verrait ses coins rognés. Le fond n'a pas de coins arrondis,
  c'est la plate-forme qui applique sa propre forme.
- `images/avatar-sr-1024.png` (et sa copie `-460.png`) — le monogramme SR, mêmes
  principes : le fond noir est plein cadre et les deux lettres, ensemble, tiennent
  dans le cercle (leur boîte garde un rayon de 0,48 pour 0,50 disponibles).
- `images/avatar-srLine-1024.png` (et sa copie `-460.png`) — le monogramme au
  liseré, mêmes principes encore : les lettres sont à 61 % de la hauteur, la
  boîte gardant elle aussi un rayon de 0,48. Le liseré, noir sur noir, ne se voit
  pas dans le cercle : seul compte le chevauchement des deux lettres.
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
