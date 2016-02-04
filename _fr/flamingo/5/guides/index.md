---
layout: fullwidth-page
title: Table de matières du guide
---

<!-- TODO: Liens pour la mise à jour : "First Rendering Tutorial" and everything below "Rendering Basics" -->

# Démarrer avec Flamingo nXt 5Â®

## Premiers tutoriels
* [Premier tutoriel de rendu]({{site.baseurl}}/{{page.language}}/flamingo/5/guides/getting-started-tutorial.html)
* [Astuces d'éclairage studio]({{site.baseurl}}/{{page.language}}/flamingo/5/guides/studio-lighting-basics.html)

## Accéder au panneau de configuration
  * Dans le menu **Flamingo nXt 5**, cliquez sur **Panneau de configuration**.

## Panneau de configuration
Le panneau de configuration de Flamingo nXt présente différents onglets permettant de configurer le modèle pour le rendu :

 *  [Matériaux]({{site.baseurl}}/{{page.language}}/flamingo/5/help/libraries.html#material)
 *  [Éclairage]({{site.baseurl}}/{{page.language}}/flamingo/5/help/lighting-tab.html)
 *  [Environnement]({{site.baseurl}}/{{page.language}}/flamingo/5/help/environment-tab.html)
 *  [Rendu]({{site.baseurl}}/{{page.language}}/flamingo/5/help/render-tab.html)

## Bases du rendu

Le rendu des modèles terminés se fait en quatre étapes principales :

 *  Définir les matériaux
 *  Définir l'éclairage
 *  Définir l'environnement
 *  Définir les conditions du rendu

#### Pour commencer un rendu

 * Dans le menu **Rendu**, cliquez sur **Rendu**.
           - Ou -
 * Dans la barre d'outils **Standard**, cliquez sur le bouton **Rendu**.

### Arrêter le rendu


Par défaut, le processus de rendu continuera à améliorer l'image, passe par passe, jusqu'à ce que vous cliquiez sur le  bouton **Arrêter le rendu** ![images/stop.png](images/stop.png) . Ceci vous permet de gérer le rapport temps/qualité. Plus vous laisserez le rendu continuer pendant longtemps, plus il se rapprochera du rendu entièrement calculé.  Vous pouvez arrêter un rendu à tout moment.


Utilisez le paramètre [Nombre de passes](..\render\render-window.html#number-of-passes) ou [Temps](..\render\render-window.html#time) dans la [fenêtre de rendu](..\render\render-window.html) ou dans les [Propriétés du document de Flamingo nXt](..\render\documentproperties-flamingo.html) pour définir un point d'arrêt automatique.

&#160;