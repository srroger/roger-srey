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

<!-- 1. Le bouton avec la miniature automatique (Changez juste l'ID après /vi/ et dans data-id) -->
<div class="yt-lazy-container" data-id="_tWh4cYCTv0" style="width: 100%; max-width: 500px; aspect-ratio: 16/9; background: url('https://i.ytimg.com/vi/5Fxw1DqZaYA/hqdefault.jpg') center/cover no-repeat; position: relative; cursor: pointer; display: flex; align-items: center; justify-content: center; background-color: #000; border-radius: 4px;">
  <!-- Icône de lecture (Triangle blanc) -->
  <div style="width: 0; height: 0; border-style: solid; border-width: 15px 0 15px 25px; border-color: transparent transparent transparent #fff; filter: drop-shadow(0px 2px 8px rgba(0,0,0,0.6)); transition: transform 0.2s;"></div>
</div>

<!-- 2. Le script magique qui injecte la vidéo au clic -->
<script>
(function() {
  // On utilise un sélecteur strict pour éviter les conflits si le script est répété
  const containers = document.querySelectorAll('.yt-lazy-container:not(.js-active)');
  containers.forEach(container => {
    container.classList.add('js-active');
    
    // Effet visuel au survol du bouton Play
    const playBtn = container.querySelector('div');
    container.addEventListener('mouseenter', () => playBtn.style.transform = 'scale(1.2)');
    container.addEventListener('mouseleave', () => playBtn.style.transform = 'scale(1)');
    
    container.addEventListener('click', function() {
      const videoId = this.getAttribute('data-id');
      const iframe = document.createElement('iframe');
      
      iframe.setAttribute('src', `https://youtube.com{videoId}?autoplay=1`);
      iframe.setAttribute('frameborder', '0');
      iframe.setAttribute('allow', 'accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share');
      iframe.setAttribute('allowfullscreen', '1');
      
      // Ajuste l'iframe à la taille du conteneur
      iframe.style.width = '100%';
      iframe.style.height = '100%';
      iframe.style.borderRadius = '4px';
      
      this.innerHTML = '';
      this.appendChild(iframe);
    }, { once: true });
  });
})();
</script>

- [Meetup C++ Montpellier][https://www.youtube.com/@CppMediterranee] : Un truc de dev du sud. 
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/LUt0bdExtZs?si=QHU3AjhB1u_zl0pY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

# Outils
- [https://haveibeenpwned.com/](https://haveibeenpwned.com/) : Savoir si une adresse mail a été piraté.
- [https://www.immuniweb.com/websec/](https://www.immuniweb.com/websec/) : Outil pour checker la sécu d'un site.
- [https://whatcms.org/](https://whatcms.org/) : Savoir le CMS qui a été utilisé pour un site web.
- [https://builtwith.com/](https://builtwith.com/) : Encore un truc pour connaitre les technos d'un site.
