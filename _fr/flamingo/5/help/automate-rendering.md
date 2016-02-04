---
title: Rendu automatisé
---

# {{page.title}}


## Rendu par lots
{: #batch-rendering}
Les travaux par lots vous permettent d'envoyer plusieurs travaux pour calculer automatiquement le rendu. Un travail par lot peut définir une vue, une résolution et un nombre de passes. Les rendus par lot peuvent être lancés seuls ou envoyés à la [ferme de rendu](render-farm.html). Ouvrez la liste de lots et ajoutez les travaux dans cette liste. La liste des travaux par lots sera enregistrée dans le modèle.

##### Où puis-je trouver cette commande ?

 * Menus > Flamingo nXt 5.0 > Plus d'outils > Rendu par lot

### Boîte de dialogue du rendu par lots
{: #batch-render}
Commencez par ajouter un travail, puis modifiez les propriétés pour définir des travaux par lots.

#### Ajouter
Chaque travail par lots est basé sur une vue enregistrée dans le modèle. Cliquez sur l'élément Ajouter pour sélectionner dans une liste de vues dans le modèle.  Tous les autres éléments du menu sont activés lorsqu'un travail est ajouté et sélectionné.

#### Supprimer
Sélectionnez un travail par lots existant.  Puis utilisez Supprimer pour retirer le travail de la liste.

#### Propriétés
Sélectionnez un travail par lots existant, puis utilisez Propriétés pour définir les [propriétés de rendu par lots](#batch-render-properties).  Les propriétés comprennent le nom du fichier, la résolution et le nombre de passes pour chaque travail.

#### Vers le haut
Déplacer le nom de la vue vers le haut dans la liste.

#### Vers le bas
Déplacer le nom de la vue vers le bas dans la liste.

#### Liste du lot
{: #batch-list}
Affiche des informations sur la liste des vues à rendre. Double cliquez sur un travail existant, pour modifier les [propriétés de rendu par lots](#batch-render-properties).

#### Statut du rendu
Affiche les informations concernant les passes, les lignes de balayage et le temps écoulé du traitement par lots.

####  Arrêter le rendu
Arrête le traitement par lots.

#### Rendre le lot localement
{: #render-batch-locally}
Utilise uniquement l'ordinateur actuel pour calculer le rendu des travaux par lot. Les images rendues seront placées dans le dossier indiqué dans les [propriétés du travail par lots](#batch-render-properties).

####  Envoyer le lot vers la ferme
Envoie le travail de rendu par lots vers la [ferme de rendu](render-farm.html). Les travaux seront rendus par tous les clients disponibles de la ferme. Les images rendues seront placées dans le dossier partagé de la ferme.

### Propriétés du rendu par lot
{: #batch-render-properties}

#### Fenêtre à rendre
Affiche la vue qui sera rendue lors de ce travail. Voir [Onglet Rendu, Fenêtre à rendre](render-tab.html#viewtorender).

#### Nom du fichier
Cliquez sur le bouton Enregistrer ![images/saveimageas.png](images/saveimageas.png) et indiquez le nom que vous voulez donner au fichier de l'image rendue.

#### Canal Alpha
Enregistre l’image avec le canal alpha.  Voir la section [Utiliser un arrière-plan avec canal alpha](environment-tab.html#alpha) pour plus d'informations. 

#### Utiliser les paramètres du document
{: #rendering-resolution}
Les paramètres de résolution du document actif sont utilisés par défaut pour le rendu. Si une autre résolution est nécessaire, désactivez cette case et indiquez la résolution. Voir la rubrique [Onglet Rendu, Résolution](render-tab.html#resolution) pour plus d'informations.

#### Passes de contraintes de rendu
{: #rendering-constraints}
Définir le nombre de passes nécessaires pour terminer le travail de rendu. Voir la rubrique [Passes](documentproperties-flamingo.html#number-of-passes) pour plus d'informations.

<!-- TODO: Flamingo nXt 5 runs from the RDK.  The need to Flamingo Automate render is not clear.  What is needed to run animations with nxt right now?
The number of passes and the ability to send a render to the farm are required still.  So the dialog should be smaller.
Alpha channel This needs to be investigated. The rest of this section is commented out.-->

<!-- Commented out until automated render can be determined

## Animations
{: #animation}
Deux options sont disponibles pour créer des animations dans Rhino.  Les animations peuvent être configurées en utilisant la [barre d'outils Animation de Rhino](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#commands/animation.htm) ou en utilisant le module d'animation [Bongo](http://bongo.rhino3d.com/).

##### Pour envoyer un travail d'animation vers la ferme de rendu
1. Lancez la commande [FlamingoNXtRenduAutomatique](automate-rendering.html#flamingonxtautomaterender).
1. Dans la boîte de dialogue Configurer le rendu automatique, sélectionnez **Rendu vers la ferme**.
&#160;
Indiquez le nom d'un travail et cliquez sur le bouton Accepter.
&#160;
Définissez un type d'animation dans la barre d'outils Configuration de l'animation de Rhino. Sélectionnez rendu entier comme méthode de capture.
&#160;
Enregistrez l'animation à partir de la barre d'outils Animation. Les travaux de rendu seront envoyés vers la ferme de rendu.
&#160;
Lorsque les travaux sont terminés, lancez à nouveau la commande FlamingoNXtRenduAutomatique et sélectionnez tous les travaux de la boîte de dialogue.
&#160;
Cliquez sur le bouton Copier les fichiers sélectionnés vers le dossier de destination indiqué et sélectionnez un dossier où copier toutes les images rendues.


## Commande FlamingoNXtRenduAutomatique
{: #flamingonxtautomaterender}


## Configurer la commande de rendu automatique

### Activé
La commande **Rendu** par défaut utilise maintenant automatiquement la **ferme de rendu**.

### Utiliser la fenêtre de rendu par défaut
La commande **Rendu** effectuera le rendu directement au lieu de l'envoyer vers la ferme.

### Nombre de passes de rendu
Indique le nombre de passes de rendu.

### Rendu vers la ferme
La commande **Rendu** enverra directement le rendu vers la ferme.

### Nom du travail
Définit le [nom du travail](automate-rendering.html#job-name) dans la **ferme de rendu**.

## Contraintes de rendu

### Nombre de passes de rendu
Définit le [nombres de passes](documentproperties-flamingo.html#number-of-passes).

### Enregistrer le canal alpha
Enregistre l'arrière-plan avec [canal alpha](render-window.html#save-with-alpha-channel).
-->