---
layout: archive
title: "MHD"
permalink: /MHD/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Les équations de base de la MHD
======
* Il est possible de les établir à partir d'équations bi-fluides, elles mêmes obtenues à partir d'équations de Boltzmann (voir article de revue de J.P. Friedberg). Une autre façon (plus intuitive) est de les établir directement à partir de règles de conservation d'un fluide conducteur (voir ci-dessous).
* Equation de base pour la conservation d'une quantité physique scalaire $F$ dont la densité par unité de volume est $f$: elle s'écrit, $\frac {\partial f} {\partial t} + \nabla . (f \vec V) = s$. En effet, elle exprime que dans un petit volume fixe, $f$ varie dans le temps (premier terme) à cause des entrées/sorties du fait du flot de vitesse par la surface enfermant ce volume (second terme), et aussi à cause de création/disparition en volume exprimée par le terme $s$ qui est un taux de création en volume. Ceci se démontre facilement en utilisant le théorème de Gauss-Ostrogradsky (dit aussi de la divergence).

* Equation de conservation de la masse, dite aussi équation de continuité. Celle ci est obtenue en appliquant la règle ci-dessus avec $f = \rho$ et en considérant $s = 0$ (pas de création ni de disparition de masse par exemple par réaction chimique).
  * $\frac {\partial \rho} {\partial t} + \nabla . (\rho \vec V) = 0$
  
* Equation de conservation de la quantité de mouvement. Celle ci est la plus importante pour la dynamique (équivalent de la seconde loi de Newton qui exprime que la densité de quantité de mouvement varie du fait d'un flux convectif associé, et de création/disparition du fait des densité de forces).
  * $\f
 
