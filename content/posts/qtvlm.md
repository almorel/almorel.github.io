---
title: "qtVlm - Harmonics"
description: "Les harmonics sur qtVlm"
date: 2024-10-13T15:39:16+02:00
tags: ["qtvlm"]
draft: false
#tldr: "intro"
---

## Harmonics, kesako ? quelques ressources

Quelques notes concernant les marées et la prédiction.

### Spectre de la marée

> Tout comme une note musicale est composée d'un fondamental et de plusieurs
> harmoniques, (Signal sinusoïdal caractérisé par une période, une amplitude et
> une phase. C'est en quelque sorte une "note pure". ) l'onde de marée peut être
> décomposée en une série d'harmoniques. Ces harmoniques ayant des périodes
> incommensurables entre elles, la marée est un signal non périodique. Elle ne se
> répète jamais à l'identique.
> -- <cite>https://www.futura-sciences.com/planete/dossiers/oceanographie-phenomene-marees-415/page/4/</cite>

### La prédiction des marées

> La marée océanique d’origine astronomique correspond aux variations de la
> surface de l’océan liées aux actions gravitationnelles de la lune et du soleil
> sur les liquides terrestres.  La prédiction de la marée utilise la décomposition
> harmonique. Connaissant l'amplitude et la phase des composantes de marée les
> plus importantes, il est alors possible de reconstruire le signal de marée très
> précisément et à n'importe quel instant, passé ou futur.
> -- <cite>https://refmar.shom.fr/sites/default/files/fiches_data/Fiche_Prediction_maree_mai_2024.pdf</cite>


## Le fichier harmonics

Télécharger le fichier:
- [ Harmonics_V10](http://opencpn.shoreline.fr/__OpenCPN_OA/3_Essentiel/E_61_Les_marees/Harmonics_V10/Harmonics_V10.zip)

Une fois décompressé, 2 fichiers sont attendus:
- HARMONIC
- HARMONIC.idx

Placer les 2 fichiers dans un répertoire, puis paramétrer dans la
configuration de qtVlm.

![Paramétrage des harmonics](/qtvlm_harmonic.png)

Dans le menu Configuration:
1. Sélectionner Gribs et Harmonics
2. Harmonics et stations météos
3. Ajouter le répertoire contenant les 2 fichiers précédemment décompressés
4. Vérifier que le chemin est pris en compte

Vérifier que le paramétrage fonctionne.

![Visualisation des harmonics](/qtvlm_harmonic_verif.png)

## Alternatives 

- [Fichier grib des courants sur weather4d.com](http://grib.weather4d.com/MyOcean/)

