# Dépendances du site.
#
# On n'utilise plus le paquet `github-pages` (builder "legacy" de GitHub Pages) :
# le site est désormais construit par GitHub Actions, ce qui permet d'y brancher
# Pagefind pour la recherche. Voir .github/workflows/pages.yml.

source "https://rubygems.org"

gem "jekyll", "~> 4.4"

# Plugins activés dans la section `plugins:` de _config.yml.
group :jekyll_plugins do
  gem "jekyll-default-layout" # applique _layouts/default.html aux pages sans layout explicite
  gem "jekyll-relative-links" # réécrit les liens Markdown relatifs (ex. ./Inventaire) vers la bonne URL
end

# Nécessaire uniquement pour `bundle exec jekyll serve` en local (retiré de Ruby >= 3.0).
gem "webrick", "~> 1.9"
