---
title: Démarrer avec Flamingo
---


# ![images/flamingotab.svg](images/flamingotab.svg) Démarrer avec Flamingo nXt
Flamingo nXt crée des fichiers d'animation et d'image haute qualité et photoréalistes à partir de modèles 3-D dans Rhinoceros®. Flamingo nXt 5 est une mise à jour de Flamingo qui se combine avec les fonctions de rendu intégrées dans Rhino 5. Cette version est en cours de développement.

Téléchargez et installez Flamingo depuis la page de [téléchargement de Flamingo nXt 5](http://www.rhino3d.com/download/flamingo/5/beta).

Vous pouvez rejoindre la discussion technique sur le [forum de Flamingo](http://discourse.mcneel.com/c/rendering/flamingo).

## Installation

* Flamingo 5 Bêta ne peut être installé que si une version précédente de Flamingo nXt est déjà installée.
* Rhino 5 Version révisée 12 doit être installé pour utiliser Flamingo nXt 5.

Après avoir téléchargé et lancé le fichier RHI, lancez Rhino.

Sur le [site web de Flamingo nXt](http://nxt.flamingo3d.com/) vous trouverez des informations sur l'assistance technique, des tutoriels, des exemples et des informations pour commencer à utiliser **Flamingo nXt**.

> [Tutoriels](http://nxt.flamingo3d.com/page/tutorials-and-documentation)
> [Galerie](http://nxt.flamingo3d.com/photo)
> [Assistance technique](http://nxt.flamingo3d.com/forum)

## Le panneau de commande de Flamingo nXt
{: #control-panel}
Cette version de Flamingo présente une interface intégrée dans les outils de rendu de Rhino 5. Le panneau de configuration de Flamingo nXt présente différents onglets permettant de configurer le modèle pour le rendu :

> [Matériaux](materials-tab.html)
> [Éclairage](lighting-tab.html)
> [Environnement](environment-tab.html)
> [Rendu](render-tab.html)

## Pour accéder au panneau de commande de Flamingo
* Dans le menu Flamingo nXt 5.0, cliquez sur Montrer le panneau de configuration.

## Bases du rendu
{: #rendering-basics}
Le rendu des modèles terminés se fait en quatre étapes principales :

 1. [Définir des matériaux](material-editor.html)
 1. [Définir l'éclairage](lighting-tab.html)
 1. [Définir un environnement](environment-tab.html)
 1. [Définir les conditions du rendu](render-tab.html)

##### Pour commencer un rendu
* Dans le menu Rendu ou Flamingo nXt, cliquez sur  Rendu.
* Ou, dans la barre d'outils Standard, cliquez sur le bouton Rendu.

### Arrêter le rendu
Par défaut, le processus de rendu continuera à améliorer l'image, passe par passe, jusqu'à ce que vous cliquiez sur le bouton Arrêter le rendu. Ceci vous permet de gérer le rapport temps/qualité. Plus le rendu continue pendant longtemps, plus il se rapproche du résultat entièrement calculé. Vous pouvez arrêter un rendu à tout moment.

###  Reprendre le rendu
Le bouton Arrêter le rendu permet d'interrompre le rendu après la fin de la passe en cours.
Le texte affiché sur le bouton indique ensuite Reprendre le rendu. Si vous arrêtez le rendu avant que les contraintes du nombre de passes ou de temps n'aient été atteintes, vous pouvez cliquer sur le bouton Reprendre le rendu pour continuer.

Utilisez les paramètres [Nombre de passes](render-window.html#number-of-passes) ou [Temps](render-window.html#time) dans la [fenêtre de rendu](render-window.html) ou dans les [Propriétés du document > Flamingo nXt](documentproperties-flamingo.html) pour définir un point d'arrêt automatique.