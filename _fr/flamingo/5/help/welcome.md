---
title: D�marrer avec Flamingo
---


# ![images/flamingotab.svg](images/flamingotab.svg) D�marrer avec Flamingo nXt
Flamingo nXt cr�e des fichiers d'animation et d'image haute qualit� et photor�alistes � partir de mod�les 3-D dans Rhinoceros�. Flamingo nXt 5 est une mise � jour de Flamingo qui se combine avec les fonctions de rendu int�gr�es dans Rhino 5. Cette version est en cours de d�veloppement.

T�l�chargez et installez Flamingo depuis la page de [t�l�chargement de Flamingo nXt 5](http://www.rhino3d.com/download/flamingo/5/beta).

Vous pouvez rejoindre la discussion technique sur le [forum de Flamingo](http://discourse.mcneel.com/c/rendering/flamingo).

## Installation

* Flamingo 5 B�ta ne peut �tre install� que si une version pr�c�dente de Flamingo nXt est d�j� install�e.
* Rhino 5 Version r�vis�e 12 doit �tre install� pour utiliser Flamingo nXt 5.

Apr�s avoir t�l�charg� et lanc� le fichier RHI, lancez Rhino.

Sur le [site web de Flamingo nXt](http://nxt.flamingo3d.com/) vous trouverez des informations sur l'assistance technique, des tutoriels, des exemples et des informations pour commencer � utiliser **Flamingo nXt**.

> [Tutoriels](http://nxt.flamingo3d.com/page/tutorials-and-documentation)
> [Galerie](http://nxt.flamingo3d.com/photo)
> [Assistance technique](http://nxt.flamingo3d.com/forum)

## Le panneau de commande de Flamingo nXt
{: #control-panel}
Cette version de Flamingo pr�sente une interface int�gr�e dans les outils de rendu de Rhino 5. Le panneau de configuration de Flamingo nXt pr�sente diff�rents onglets permettant de configurer le mod�le pour le rendu :

> [Mat�riaux](materials-tab.html)
> [�clairage](lighting-tab.html)
> [Environnement](environment-tab.html)
> [Rendu](render-tab.html)

## Pour acc�der au panneau de commande de Flamingo
* Dans le menu Flamingo nXt 5.0, cliquez sur Montrer le panneau de configuration.

## Bases du rendu
{: #rendering-basics}
Le rendu des mod�les termin�s se fait en quatre �tapes principales :

 1. [D�finir des mat�riaux](material-editor.html)
 1. [D�finir l'�clairage](lighting-tab.html)
 1. [D�finir un environnement](environment-tab.html)
 1. [D�finir les conditions du rendu](render-tab.html)

##### Pour commencer un rendu
* Dans le menu Rendu ou Flamingo nXt, cliquez sur  Rendu.
* Ou, dans la barre d'outils Standard, cliquez sur le bouton Rendu.

### Arr�ter le rendu
Par d�faut, le processus de rendu continuera � am�liorer l'image, passe par passe, jusqu'�ce que vous cliquiez sur le bouton Arr�ter le rendu. Ceci vous permet de g�rer le rapport temps/qualit�. Plus le rendu continue pendant longtemps, plus il se rapproche du r�sultat enti�rement calcul�. Vous pouvez arr�ter un rendu � tout moment.

###  Reprendre le rendu
Le bouton Arr�ter le rendu permet d'interrompre le rendu apr�s la fin de la passe en cours.
Le texte affich� sur le bouton indique ensuite Reprendre le rendu. Si vous arr�tez le rendu avant que les contraintes du nombre de passes ou de temps n'aient �t� atteintes, vous pouvez cliquer sur le bouton Reprendre le rendu pour continuer.

Utilisez les param�tres [Nombre de passes](render-window.html#number-of-passes) ou [Temps](render-window.html#time) dans la [fen�tre de rendu](render-window.html) ou dans les [Propri�t�s du document > Flamingo nXt](documentproperties-flamingo.html) pour d�finir un point d'arr�t automatique.