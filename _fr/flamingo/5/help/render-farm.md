---
title: Rendu avec la ferme
---

# {{page.title}}
La ferme de rendu de Flamingo nXt utilise la puissance de plusieurs ordinateurs pour rendre des images simples, des lots de plusieurs images ou des animations en fonction de la vue. Ni Rhino ni Flamingo nXt ne sont n�cessaires sur les ordinateurs utilis�s uniquement comme clients de la ferme de rendu.

#### Organisation typique d'un r�seau avec une ferme de rendu
{: #render-farm}

![images/renderfarm-002.png](images/renderfarm-002.png){: style="margin-top:25px;"}

>![images/01.png](images/01.png)Un ordinateur avec Rhino et Flamingo nXt.
>![images/02.png](images/02.png)Serveur de r�seau ou dossier partag�.
>![images/03.png](images/03.png)Deux clients de la ferme de rendu. (La ferme de rendu de nXt est livr�e avec deux copies gratuites du logiciel client.)
>![images/04.png](images/04.png)Clients de la ferme de rendu achet�s en suppl�ment.

La ferme de rendu est gratuite jusqu'� deux ordinateurs clients. Pour ajouter d'autres ordinateurs clients, achetez une licence de la Ferme de rendu nXt sur [https://www2.mcneel.com/commerce/accurender/buy-farm.asp](https://www2.mcneel.com/commerce/accurender/buy-farm.asp).

#### Dossier partag� de la ferme
{: farm-folder}
La cl� d'une ferme de rendu fonctionnelle est un dossier partag� auquel l'ordinateur principal et tous les ordinateur clients peuvent acc�der. Ce dossier est normalement un dossier r�seau partag�. Il peut se trouver sur l'ordinateur principal ou sur un r�seau. Le dossier ne doit pas forc�ment avoir le m�me nom sur chaque client mais chaque client doit pouvoir lire, �crire et supprimer dans ce dossier. Le dossier partag� devrait disposer d'au moins 20 Go de m�moire libre.

#### La ferme de rendu nXt inclut deux applications�:

##### Le client de la ferme de rendu (nXtFarmer64.exe)
Un petit programme qui est lanc� sur chaque client de Rendu du r�seau et qui attend les travaux � r�aliser. Normalement, les fermes de Rendu travaillent en silence sans afficher les rendus sur un moniteur pendant leurs calculs. Gr�ce � cette m�thode, vous pouvez utiliser la puissance de plusieurs ordinateurs pour ex�cuter des t�ches longues pour lesquelles vous n'avez pas besoin d'intervenir au cours du rendu.

##### Le moniteur de la ferme (nXtFarmMonitor64.exe)
Une application qui vous montre le statut de vos travaux de rendu et qui offre quelques outils de contr�le simple.
La ferme de rendu nXt vous permet de travailler avec des gestionnaires de rendu externes. Les proc�dures suivantes s'appliquent � la ferme de rendu incluse avec Flamingo nXt. Si vous pr�voyez utiliser un logiciel de ferme de rendu externe, certaines proc�dures seront diff�rentes.

#### Mode de fonctionnement de la ferme
{: #the-farm-process}
 1. Pour lancer un rendu avec la ferme de Flamingo nXt, au lieu d'utiliser la commande Rendu, utilisez la ferme de rendu *(menu Flamingo nXt 5.0 > Ferme de rendu)*. Un travail de rendu sera envoy� dans le [dossier de destination de la ferme](options-flamingo.html#farm-output-folder). Tous les mat�riaux et toutes les informations sur les ressources seront automatiquement envoy�s avec le travail.
 2. Les travaux de rendu sont divis�s en plusieurs t�ches diff�rentes. Les clients de la ferme de rendu v�rifient continuellement le dossier de destination de la ferme pour voir s'il y a de nouvelles t�ches � r�aliser. Chaque client choisira une t�che et commencera le rendu. Le moniteur de la ferme *(Flamingo nXt 5.0 > Ferme de rendu > Moniteur de la ferme)* assure un suivi de l'avanc�e du travail.
 3. Chaque client de la ferme d�pose les r�sultats dans le dossier de la ferme sous <<nom du travail>>\\R�sultat.
 3. Au fur et � mesure que les clients finissent le travail, ils choisissent de nouveaux travaux suivant leur ordre d'arriv�e dans la ferme.
 4. Le r�sultat sera au [format image nXt (.nXtImage)](image-editor.html). Les images dans ce format peuvent �tre modifi�es avec l'[�diteur d'images nXt](image-editor.html). Les r�sultats peuvent �galement �tre enregistr�s dans des fichiers TGA, PNG, TIF et JPG � partir de l'[�diteur d'images nXt](image-editor.html). 

## Installation et configuration de la ferme
{: #install}
Le client de rendu de la ferme et le moniteur sont install�s avec Flamingo sur l'ordinateur principal o� se trouve Rhino. Le client de la ferme doit �tre install� sur les autres ordinateurs clients o� Rhino et Flamingo nXt ne sont pas install�s. 

##### Installer la ferme de rendu
Installez le client de la ferme sur les ordinateurs o� Rhino et Flamingo nXt ne sont pas install�s:

 1. T�l�chargez le [logiciel de la ferme de rendu](http://www.rhino3d.com/download/The-Farm/1.0/release).
 1. Lancez le programme d'installation sur chaque ordinateur client. 
 1. Dans le menu D�marrer, ex�cutez la ferme de rendu sur chaque machine.
 1. La ferme de rendu appara�tra sous forme d'ic�ne dans la barre de syst�me.

##### Pour configurer la ferme de rendu
{: #configure-the-render-farm}
1.  [Cliquez avec le bouton de droite](mouse-button-right.html) sur l'ic�ne et s�lectionnez R�tablir.
1. Dans la fen�tre nXt Farmer, dans le menu Options, cliquez sur le Path et s�lectionnez le chemin du dossier de la ferme de rendu.

Sur l'ordinateur avec Rhino et Flamingo nXt, d�finissez le dossier du Zoo dans Rhino. Dans le menu Outils, cliquez sur Options, d�finissez l'emplacement commun de la ferme � partir du [dossier de destination de la ferme](options-flamingo.html#farm-output-folder).

La ferme de rendu est maintenant configur�.

## Utiliser la ferme de rendu
{: #using-the-render-farm-from-flamingo-nxt}
� l'heure actuelle, la ferme peut �tre utilis�e de trois fa�ons pour traiter les rendus sur plusieurs ordinateurs : travail de rendu simple, travail par lot et animation.

##### Pour v�rifier que les stations clients r�pondent
Apr�s avoir lanc� le client de la ferme de rendu sur tous les ordinateurs clients�:

 1. Sur un des ordinateurs client, dans le menu D�marrer de Windows, cliquez sur [Moniteur de la ferme](#render-farm-monitor).
 1. Les ordinateurs clients devraient appara�tre dans la liste sup�rieure.
 1. Chaque client de la ferme de rendu devrait appara�tre dans la liste des ordinateurs. Leur statut devrait indiquer Actif. 

En cas de probl�me avec cette section, consultez les rubriques [Installation](#install) et [Configuration](#configure-the-render-farm).


##### Pour envoyer un travail de rendu vers la ferme de rendu
1. Dans Rhino, configurez votre rendu et votre vue comme pour un rendu normal.
1. Dans le menu Flamingo nXt, cliquez sur Lancer la ferme de rendu. 
1. La bo�te de dialogue [Travail de rendu](#farm-job) s'ouvre.
1. V�rifiez les options et cliquez sur Accepter. 


##### Contr�ler la ferme
Apr�s avoir envoy� un travail vers la ferme de rendu, utilisez le [moniteur de la ferme](#render-farm-monitor).

 1. Sur l'ordinateur principal, dans le menu D�marrer de Windows, cliquez sur [Moniteur de la ferme](#render-farm-monitor).
 1. Les derniers travaux envoy�s devraient appara�tre dans la liste. Ceci peut prendre quelques minutes pour les travaux de grande taille. 
 1. Le statut du travail deviendra actif. 
 1. Les ordinateurs devraient ensuite choisir des t�ches avec la m�me date. 
 1. La valeur du pourcentage achev� augmente au fur et � mesure que les t�ches sont termin�es. 
 1. Recherchez les t�ches dont le statut est Termin� lorsque le travail est fini. 


## Options de travail de la ferme
{: #farm-job}

#### Nom
{: #job-name}
La date et l'heure sont automatiquement ajout�es au nom que vous avez choisi. Un sous-dossier est cr�� pour le travail dans le dossier partag� de la ferme de rendu. Un dossier de destination est �galement cr�� dans le nouveau dossier du travail.
� la fin de chaque travail, le r�sultat est plac� dans le dossier de destination du travail.

#### Lancer le travail
Un travail peut �tre d�marr� juste apr�s avoir �t� envoy�, plus tard ou manuellement en utilisant le moniteur de la ferme. 

#### Maintenant
Lancer le travail maintenant.

#### Plus tard (Manuellement)
Le travail est lanc� plus tard en utilisant le [moniteur de la ferme](#render-farm-monitor) de rendu).

#### Apr�s
Lancer le travail � une date et une heure pr�cise.

#### Passes de contraintes de rendu
{: #rendering-constraints}
D�finir le nombre de passes n�cessaires pour terminer le travail de rendu. Voir la rubrique [Passes](documentproperties-flamingo.html#number-of-passes) pour plus d'informations.


## Moniteur de la ferme de rendu
{: #render-farm-monitor}
Le Moniteur de la ferme de rendu est un programme autonome qui indique le statut des stations de travail et des travaux pr�sents dans la ferme. Les travaux peuvent �tre interrompus et red�marr�s � partir du moniteur ; il est �galement possible d'emp�cher une station de travail de participer � la ferme de rendu.

Pour acc�der au moniteur de la ferme � partir de Rhino, ouvrez le menu Flamingo nXt 5.0 > Ferme de rendu > Moniteur de la ferme. 

Pour acc�der au moniteur de la ferme � partir de Windows, dans le menu D�marrer, cliquez sur **Tous les programmes > nXt Render Farm > Farm Monitor**.

#### Options
Cliquez avec le bouton droit sur un ordinateur ou un travail pour acc�der aux options.

#### Actualiser
Actualiser la liste des travaux.

#### Interrompre l'ordinateur
Emp�cher la station de travail de participer � la ferme de rendu.

#### Continuer l'ordinateur
R�-autoriser la station de travail � participer � la ferme de rendu.

#### Interrompre le travail
Interrompt le travail indiqu�.

#### Continuer le travail
Reprend le travail indiqu�.

#### Supprimer le travail
Supprimer de la liste le travail indiqu� .

## Licence de la ferme de rendu
{: #licensing-the-render-farm-}
La version gratuite de la ferme de rendu permet � deux ordinateurs en r�seau (n�uds) de travailler simultan�ment sur des travaux. Si vous voulez avoir plus de n�uds de r�seau travaillant en m�me temps, vous pouvez acheter une licence illimit�e sur [https://www2.mcneel.com/commerce/accurender/buy-farm.asp](https://www2.mcneel.com/commerce/accurender/buy-farm.asp).

Lorsque vous avez achet� une licence et avez re�u une cl� de produit, suivez la proc�dure suivante pour activer la licence de votre ferme.

##### Pour autoriser le n�ud
1. Attendez la fin de tous les travaux actifs de la ferme avant de commencer l'activation de la licence.
1. Enregistrez votre cl� de produit dans un fichier de texte sur le r�seau afin de pouvoir la copier et la coller facilement sur chaque n�ud.
1. Si le n�ud est actuellement actif, dans la barre d'�tat syst�me de Windows, [cliquez avec le bouton droit](mouse-button-right.html) sur l'ic�ne�de la Ferme de rendu puis cliquez sur **Fermer**.
1. Cliquez sur le bouton **D�marrer de Windows** puis sur **Tous les programmes**.
Dans le dossier nXt Render Farm, cliquez sur **Authorize Farm**.
1. Collez ou tapez votre Cl� de produit dans la case correspondante et cliquez sur OK**.

##### Pour commencer le n�ud
1. Cliquez sur le bouton **D�marrer de Windows** puis sur **Tous les programmes**.
Dans le dossier nXt Render Farm, cliquez sur **Render Farmer**.
1. [Cliquez avec le bouton de droite](mouse-button-right.html) sur l'ic�ne de la barre de t�che et, dans le menu contextuel, cliquez sur **Restore**.
1. Dans le menu Aide, cliquez sur **� propos**.
Si le num�ro de version indique une version d��valuation, l'activation de la licence ne s'est pas faite correctement.
1. Minimiser la fen�tre Render Farmer dans la barre de t�ches.