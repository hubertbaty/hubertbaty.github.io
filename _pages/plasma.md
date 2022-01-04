---
layout: archive
title: "Plasma"
permalink: /plasma/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}


![](/images/pla2.jpg)


C'est quoi un plasma ?
======
* Un plasma est un milieu contenant des ions (chargés positivement car issus d'atomes ayant perdu un ou plusieurs électrons), des
électrons libres, et des atomes neutres. Les ions peuvent être multi-chargés. C'est un milieu globalement neutre (charge totale nulle).
Le schéma ci-dessus illustre le cas d'un plasma mono-chargé (un ion est constitué d'un seul proton). Chaque type de particule est animé
d'une vitesse moyenne d'agitation thermique qui dépend la sa température et de sa masse (comme pour un gaz).
* Un plasma (considéré comme le quatrième état de la matière) peut être obtenu en portant un gaz donné à une température supérieure à une valeur critique qui
dépend de la composition. Ainsi, ceci permet d'ioniser le gaz par 'arrachement' des électrons. La température critique est de l'ordre de quelques
électrons-volts en moyenne (en terme d'énergie thermique $k_BT$, $k_B$ étant la constante de Boltzmann), ou encore de façon équivalente de plusieurs dizaines
de milliers de degrés Kelvin pour $T$. Cependant, certains plasmas peuvent exister à des températures beaucoup plus basses (quelques centaines de degrés) à cause de densités extrêmement faibles de certains milieux astrophysiques (voir schéma plus bas).
* L'ionisation est plus ou moins forte selon que le nombre restant d'atomes (ou molécules) neutres est plus ou moins grand. En pratique, on parle
de degré d'ionisation $\alpha$ plus ou moins proche de l'unité. Celui ci est défini de la façon suivante,
$\alpha = \frac{n_e}{n_e+n_n}$ avec $n_e$ la densité électronique et $n_n$ la densité de neutres. Un plasma complètement ionisé correspond ainsi à
$\alpha = 1$.
* L'ionisation peut-être aussi obtenue par décharge électrique dans un gaz, ou encore par rayonnement (cas des régions de formation d'étoiles).



![](/images/Plasma-scaling.png)

(Figure tirée de Wikipédia)
 
 
Exemples de plasmas
======
* En astrophysique de nombreux objets astronomiques comme les étoiles (l'intérieur comme leur couronne), les disques d'accrétion, les nébuleuses, et le milieu interstellaire sont composés
de plasma. On peut aussi ajouter les milieux entourant l'atmosphère de la Terre comme l'ionosphère ou de façon plus lointaine la magnetosphère. On parle alors de plasmas naturels, par opposé aux plasmas de laboratoires (comme par exemple ceux créés dans le but de réaliser la fusion
thermonucléaire). Sur la figure ci-dessus, chacun peut constater la diversité impressionnante de conditions, en termes de température et de densité, régnant au sein de différents plasmas.



Modèles de description des plasmas
======
* Il existe un grand nombre de modèles physiques permettant de décrire la dynamique des plasmas. Le lecteur pourra trouver ci-dessous un résumé très succint. Le modèle MHD sera évidemment plus amplement développé (voir l'onglet correspondant). 

* Les modèles PIC (abréviation pour 'Particle In Cell')
  * Ils sont basés sur l'intégration numérique de l'équation du mouvement (seconde loi de Newton de la dynamique) pour chaque particule chargée (de charge $q$ et masse $m$), soumise à la force électique $q \vec E$ et la force magnétique $q (\vec V \times \vec B)$. Ainsi, un très grand nombre de particules (représentant les ions et électrons) sont implémentés avec un pas de temps $\delta t$ par une technique numérique adaptée dans les champs électrique et magnétiques $\vec E$ et $\vec B$ respectivement. La méthode numérique doit ainsi satisfaire des propriétés particulières de conservation (comme celle de l'énergie), comme par exemple dans les schémas de type Boris.
  * Une fois les particules implémentées, il faut déduire les champs $\vec E$ et $\vec B$ correspondant à la 'nouvelle' distribution des particules dans l'espace des phases (c'est à dire l'espace physique et l'espace des vitesses). Pour ce faire, il faut intégrer par rapport à l'espace les équations de Maxwell correspondantes dans l'approximation du vide, que sont l'équation de Maxwell-Gauss (pour $\vec E$) et l'équation de Maxwell-Ampère ($\vec B$). Ceci est alors réalisé sur un domaine découpé en cellules, et nécéssite un lissage pour éviter les gradients trop irréalistes de distribution des particules.
  * Les limitations de la méthode sont multiples. Tout d'abord le nombre maximum de particules est évidemment très inférieur à la réalité, et on parle alors de super-particules. Le rapport de maase entre les ions et les électrons limite fortement le temps de calcul au travers des conditions de stabilité des schémas numériques, conduisant ainsi à l'emploi d'un rapport de masse moins grand.
  * Malgré les limitations, ces modèles permettent une approche complémentaires des modèles cinétiques et fluides (voir ci-dessous).
* Les modèles dits cinétiques
* Les modèles dits fluides
 
 
