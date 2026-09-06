---
title: Roger Srey
description: Misc
author: Roger Srey
date: 06-09-26
lastmod: 06-09-26
---
[< Home](./)

Plein de choses en vrac avec plus ou moins d'intérêt.

# Cartes
- [Radio garden](https://radio.garden/) : Se balader en montgolfière à travers les radios du monde.
- [Open infrastructure map](https://openinframap.org/) : Les lignes d'énergies du monde.
- [Carto Tchoo](https://carto.tchoo.net/) : Tchou tchou

# Gens
- [SebSauvage](https://sebsauvage.net/) : Un geek. 
- [Shar](https://www.sharyap.com/) : Une artiste / geek (son site web est stiley). 
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/_tWh4cYCTv0?si=N1azsAcK5yFhOYJW" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<!-- Le bouton inspiré d'itch.io -->
<button type="button" 
        class="embed_preload youtube_preload" 
        data-video-id="_tWh4cYCTv0" 
        style="width: 500px; height: 281px; background: url(https://ytimg.com) 50% 50% no-repeat; background-size: cover; border: none; cursor: pointer;">
</button>

<!-- Le script qui donne vie au bouton -->
<script>
(function() {
  // 1. Le script cherche tous les boutons de la page
  const boutons = document.querySelectorAll('.youtube_preload');
  
  boutons.forEach(function(bouton) {
    // 2. Il écoute si on clique dessus
    bouton.addEventListener('click', function() {
      // 3. Il récupère l'identifiant de la vidéo
      const id = this.getAttribute('data-video-id');
      
      // 4. Il fabrique la VRAIE iframe YouTube avec la bonne syntaxe
      const iframe = document.createElement('iframe');
      iframe.setAttribute('src', 'https://youtube.com' + id + '?autoplay=1');
      iframe.setAttribute('width', '500');
      iframe.setAttribute('height', '281');
      iframe.setAttribute('frameborder', '0');
      iframe.setAttribute('allow', 'autoplay; encrypted-media; picture-in-picture');
      iframe.setAttribute('allowfullscreen', '1');
      
      // 5. Il remplace le bouton par l'iframe
      this.parentNode.replaceChild(iframe, this);
    });
  });
})();
</script>

- [Meetup C++ Montpellier](https://www.youtube.com/@CppMediterranee) : Un truc de dev du sud. 
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/LUt0bdExtZs?si=QHU3AjhB1u_zl0pY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

# Outils
- [https://haveibeenpwned.com/](https://haveibeenpwned.com/) : Savoir si une adresse mail a été piraté.
- [https://www.immuniweb.com/websec/](https://www.immuniweb.com/websec/) : Outil pour checker la sécu d'un site.
- [https://whatcms.org/](https://whatcms.org/) : Savoir le CMS qui a été utilisé pour un site web.
- [https://builtwith.com/](https://builtwith.com/) : Encore un truc pour connaitre les technos d'un site.
