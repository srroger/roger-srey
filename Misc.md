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
<!--<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/_tWh4cYCTv0?si=N1azsAcK5yFhOYJW" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe> -->

<!-- Le bouton inspiré d'itch.io avec texte centré -->
<button type="button" 
        class="embed_preload youtube_preload" 
        data-video-id="_tWh4cYCTv0" 
        data-video-si="N1azsAcK5yFhOYJW"
        style="width: 500px; height: 281px; 
               background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), url(https://i.ytimg.com/vi/5Fxw1DqZaYA/hqdefault.jpg) 50% 50% no-repeat; 
               background-size: cover; 
               border: none; 
               cursor: pointer;
               display: inline-flex;
               align-items: center;
               justify-content: center;
               color: white;
               font-family: sans-serif;
               font-size: 16px;
               font-weight: bold;
               text-shadow: 1px 1px 3px rgba(0,0,0,0.8);">
  Cliquer pour charger la vidéo YouTube
</button>

<!-- Le script qui injecte exactement iframe -->
<script>
(function() {
  document.querySelectorAll('.youtube_preload').forEach(function(bouton) {
    bouton.addEventListener('click', function() {
      const id = this.getAttribute('data-video-id');
      const si = this.getAttribute('data-video-si');
      const iframe = document.createElement('iframe');
      
      // Reconstruction stricte de votre URL avec vos arguments
      iframe.src = "https://www.youtube-nocookie.com/embed/" + id + "?si=" + si + "&autoplay=1";
      iframe.width = "560";
      iframe.height = "315";
      iframe.title = "YouTube video player";
      iframe.frameBorder = "0";
      iframe.allow = "accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share";
      iframe.setAttribute("referrerpolicy", "strict-origin-when-cross-origin");
      iframe.setAttribute("allowfullscreen", "1");
      
      this.parentNode.replaceChild(iframe, this);
    });
  });
})();
</script>

- [Meetup C++ Montpellier](https://www.youtube.com/@CppMediterranee) : Un truc de dev du sud. 
<!--<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/LUt0bdExtZs?si=QHU3AjhB1u_zl0pY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe> -->

<!-- Le bouton inspiré d'itch.io avec texte centré -->
<button type="button" 
        class="embed_preload youtube_preload" 
        data-video-id="LUt0bdExtZs" 
        data-video-si="QHU3AjhB1u_zl0pY"
        style="width: 500px; height: 281px; 
               background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), url(https://srroger.github.io/roger-srey/images/lazy.png) 50% 50% no-repeat; 
               background-size: cover; 
               border: none; 
               cursor: pointer;
               display: inline-flex;
               align-items: center;
               justify-content: center;
               color: white;
               font-family: sans-serif;
               font-size: 16px;
               font-weight: bold;
               text-shadow: 1px 1px 3px rgba(0,0,0,0.8);">
  Cliquer pour charger la vidéo YouTube
</button>

# Outils
- [https://haveibeenpwned.com/](https://haveibeenpwned.com/) : Savoir si une adresse mail a été piraté.
- [https://www.immuniweb.com/websec/](https://www.immuniweb.com/websec/) : Outil pour checker la sécu d'un site.
- [https://whatcms.org/](https://whatcms.org/) : Savoir le CMS qui a été utilisé pour un site web.
- [https://builtwith.com/](https://builtwith.com/) : Encore un truc pour connaitre les technos d'un site.
