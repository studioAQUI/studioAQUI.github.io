# studio.AQUI

Site internet de l'agence d'architecture studio.AQUI

## Créer un nouveau projet

La liste des projets se trouve dans le répertoire `_projets`.
Pour créer un nouvelle fiche projet :
1. Créer un fichier `21.15_MON_PROJET.md` (bien penser à l'extension en `.md` sinon ça ne marchera pas).
2. Ajouter les métadonnées suivantes :

```yml
---
layout: project
name: 19.01_ALESIA
title: ALESIA
permalink: projets/alesia
description: Construction d’un village SOSVE
ville: Besse-sur-Issole (83)
adresse: Chemin des pitchounes, 83656 Besse-sur-Issole
maitre_d_oeuvre: Barbara Constantin Architecte en collaboration avec studio. AQUI
programme: 9 maisons individuelles groupées, 3 appartements & 1 bâtiment administratif
cout: 4,5 M€ H.T.
surface: 3 025 m2
etat: Livré en Juin 2020
---
```

**IMPORTANT** La valeur de la clé `name` doit impérativement porter le même nom que la fiche projet. Si le nom fichier de votre fiche projet est `19.01_ALESIA.md` alors on doit avoir `name: 19.01_ALESIA`.


https://user-images.githubusercontent.com/2269165/140411536-cbc5e509-c86d-4401-b898-28e1dcb773ff.mov

3. Importer un dossier photo dans `assets/images` **portant le même nom** que la fiche projet. Le fonctionnement de Github fait qu'il n'est pas possible de créer un dossier vide, vous devez donc impérativement importer un dossier contenant une ou plusieurs images avant de pouvoir ajouter le reste des images.


https://user-images.githubusercontent.com/2269165/140412882-bd010d18-e91f-4f99-adf9-d688f86d410b.mov

## Modifier la home

Les images qui s'affichent sur la home sont décrites dans le fichier `_data/home.json`. Chaque photo est représentée par un "objet" de la forme suivante :

```json
{
  "src": "/assets/images/19.01_ALESIA/ALS_Plan.jpg",  // chemin d'accès au fichier image
  "width": "100%", // largeur relative en % pour ajuster la taille
  "linkTo": "/projets/alesia" // permalink du projet
}
```

Les objets sont séparés par des virgules dans un tableau `[{}, {}, ..., {}]`. Après modification de ce fichier, il est utile de valider le format en copiant collant le code sur https://jsonformatter.curiousconcept.com/. L'affichage des images sur la home se fait de gauche à droite et de haut en bas :

```
1 2
3 4
5 6
7 8
...
```

