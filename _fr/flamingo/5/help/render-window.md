---
title: Rectangle Rendu
---

# ![images/render.svg](images/render.svg) {{page.title}}
La fen�tre de rendu offre des options pour r�gler l'exposition et ajouter des effets par post-traitement. Le cadre principal de la fen�tre de rendu fait partie du cadre de rendu de Rhino.  Pour plus d'informations sur les menus et ic�nes de la fen�tre de rendu, consultez la [rubrique sur la fen�tre de rendu de Rhino](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#information/renderwindowpostprocess.htm).  Cette rubrique couvre les options suppl�mentaires apport�es sp�cifiquement par Flamingo.

## G�rer un rendu en cours
Lorsque le rendu est lanc�, la [fen�tre de rendu](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#information/renderwindowpostprocess.htm) s'ouvre et le calcul du rendu d�bute.  Le syst�me de Flamingo utilise plusieurs passes qui actualisent l'image rendue par �tapes. Flamingo recherche tout d'abord les modifications sur son mod�le interne puis lance un processus d'initialisation. Ce processus peut prendre quelques secondes voire plusieurs minutes. Le mod�le est import�, les images des mat�riaux sont copi�es � partir du disque dur et la m�moire tampon de l'image rendue est cr��e. Il est possible de g�rer le rendu � plusieurs moments�:

>[Rendu multi-passes](#multi-pass)
>[Arr�ter un rendu](#stop-render)
>[Ajuster une image](#adjusting)
>[Enregistrer une image](#saving)

### Rendu multi-passes
{: #multi-pass}
Flamingo nXt est un tout nouveau moteur de rendu. Le rendu avec un perfectionnement en plusieurs passes permet des effets de rendu plus avanc�s sans interface compliqu�e. Les premi�res passes de rendu produiront des d�fauts inattendus.  Par exemple, vous verrez que les ombres sont tr�s pr�cises et lin�aires au d�but. Les ombres seront de plus en plus douces � chaque passe et se m�langeront petit � petit. De nombreux autres effets s'am�lioreront � chaque passe de rendu.  Utilisez l'[onglet Flamingo](#flamingo-tab) pour suivre le processus de rendu. 

De cette fa�on, le rendu de nXt n'est jamais vraiment termin�; c'est � vous de d�cider du moment o� il est assez bien pour l'arr�ter. Vous pouvez laisser les images qui semblent correctes continuer � s'am�liorer. Mais, si vous voulez r�aliser une modification ou enregistrer une image, vous pouvez �galement arr�ter un rendu � tout moment.

![images/passes-wide-1.gif](images/passes-wide-1.gif)

Parmi les effets qui s'am�liorent � chaque passe :

>�clairage (comme l'illumination globale si elle est activ�e)
>Ombres floues
>R�flexions (floues)
>R�fraction
>Anticr�nelage
>Profondeur de champ

### Arr�ter un rendu
{: #stop-render}
Diff�rentes options permettent d'arr�ter le rendu :

![images/close-x.png](images/close-x.png) Cliquer sur le bouton X en haut � droite de la fen�tre de rendu pour arr�ter imm�diatement le rendu et fermer la fen�tre de rendu. C'est la meilleure option pour revenir rapidement au mod�le afin de r�aliser des modifications.

![images/stop.png](images/stop.png) Cliquer sur le bouton Arr�ter le lancer de rayons pour arr�ter le rendu � la fin de la passe en cours. C'est la meilleure option pour enregistrer une image.

![images/stop.png](images/stop.png) Double cliquer sur le bouton Arr�ter le lancer de rayons pour arr�ter le rendu imm�diatement et laisser la fen�tre de rendu ouverte.

### Ajuster un rendu
{: #adjusting}
Apr�s avoir arr�t� une image, utilisez les contr�les de l'[onglet Flamingo](#flamingo-tab) pour ajuster rapidement l'image et l'�clairage. Cet ensemble d'outils est tr�s important pour la production d'images de haute qualit�. 

Contr�les permettant d'ajuster les images�:

>[Ajuster l'image](#adjust-image)
>[Canaux](#channels)
>[Effets post�rieurs](#post-process-effects)


### Enregistrer des images
{: #saving}
Plusieurs options sont disponibles pour enregistrer une image en fonction de son utilisation post�rieure. La plupart des images pourront �tre enregistr�es au format JPG ou PNG. Mais il existe d'autres options.

#### ![images/saveimageas.png](images/saveimageas.png) Enregistrer l'image
Apr�s avoir ajust� l'image, le proc�d� normal consiste � enregistrer le fichier au format JPG ou PNG.  

Une image JPG est un format de fichier tr�s performant et assez petit. Ce format convient tr�s bien aux images publi�es sur Internet ou envoy�es par mail. Mais cette performance a un prix, en effet certaines couleurs sont supprim�es de l'image. 

PNG est un format comprim� qui contient 100�% des informations de couleur et de canal Alpha. Ce format convient tr�s bien aux images de haute qualit�.

#### Enregistrer avec le canal alpha de l'arri�re-plan
{: #save-with-alpha-channel}
Enregistre une image 32 bits au format PNG, TIF ou BMP avec l'arri�re-plan du canal alpha. Utilisez les versions canal alpha des formats de fichier pour la composition haute qualit�. Les arri�re-plans appara�tront en noir lorsque le rendu sera enregistr�avec le canal alpha.  Une case dans l'[onglet Flamingo](#flamingo-tab) et la [bo�te de dialogue Enregistrer](#saving) permet d'enregistrer le canal alpha. Le format de fichier PNG permet de capturer les informations sur le canal alpha.

#### Exporter vers un fichier natif de Flamingo nXt (.nXtImage)
{: #export-to-nxtimage}
Enregistre les informations de couleur et de luminance non comprim�es. Enregistre tous les canaux de rendu, y compris le canal [alpha](environment-tab.html#alpha). Les fichiers nXt Image peuvent �tre ouverts dans l'[�diteur d'images](image-editor.html). Vous pouvez alors ajuster l'[exposition](#adjust-image) et appliquer des [effets](#effects) avant d'enregistrer l'image dans un autre format.

Le format .nXtImage est le format d'image natif des moteurs de rendu nXt. Ce format est recommand� pour l'enregistrement de vos rendus car il conserve la plupart des informations sur votre rendu. Les images enregistr�es dans ce format peuvent �tre manipul�es dans l'[�diteur d'images nXt](image-editor.html) et des effets sp�ciaux peuvent �tre ajout�s. Cet �diteur permet d'enregistrer dans  nombreux formats standards, y compris tous les formats pris en charge dans nXt. Il est �galement possible d'enregistrer au format [Piranesi EPix file (.epx)](http://www.piranesi.co.uk/).

#### Exporter vers un fichier HDR
{: #export-to-hdr}
Enregistre les informations de couleur et de luminance non comprim�es. Le format .hdr enregistre les donn�es de luminance directement dans un format � grande plage dynamique. Les arri�re-plans sans luminance, comme les photographies normales, apparaissent en noir s'ils sont enregistr�s dans un de ces formats.

#### Exporter vers un fichier EXR
{: #export-to-exr}
Format de fichier image � grande plage dynamique cr�� par la soci�t� Industrial Light and Magic (ILM) et distribu� sous forme de licence libre. Ce format de fichier g�re les nombres flottants en 16 bits par canal avec un bit pour le signe, cinq bits pour l'exposant et dix bits pour la mantisse. Ceci permet d'avoir une plage dynamique de plus de trente niveaux d'exposition. Voir l'article de Wikipedia : OpenEXR](http://fr.wikipedia.org/wiki/OpenEXR).
Le format EXR enregistre les donn�es de luminance directement dans un format � grande plage dynamique. Les arri�re-plans sans luminance, comme les photographies normales, apparaissent en noir s'ils sont enregistr�s dans un de ces formats.

#### ![images/close-x.png](images/close-x.png) Quitter
Ferme la fen�tre de rendu.

#### Menus d�roulants
Pour plus d'informations sur les menus et ic�nes de la fen�tre de rendu, consultez la [rubrique sur la fen�tre de rendu de Rhino](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#information/renderwindowpostprocess.htm).

## Onglet de Flamingo
{: #flamingo-tab}
L'onglet Flamingo de la fen�tre de rendu apporte de nombreuses options sp�cifiques au moteur de rendu de Flamingo. La compr�hension de ces options est indispensable pour bien g�rer les rendus de Flamingo.

#### Enregistrer avec le canal alpha
Enregistre des images 32 bits au format PNG, TIF ou BMP avec l'arri�re-plan du canal alpha. Les versions canal alpha des formats de fichier sont utilis�es pour la composition haute qualit�. Les arri�re-plans appara�tront en noir lorsque le rendu sera enregistr�avec le canal alpha.  Utilisez cette case et la case de la [bo�te de dialogue Enregistrer](#saving) pour enregistrer le canal alpha. Le format de fichier PNG permet de capturer les informations sur le canal alpha.

## Avancement
{: #progress}
Utilisez les informations sur l'avancement pour v�rifier le statut d'un rendu de Flamingo. 

#### Action
Affiche le statut actuel du calcul de rendu. 

Messages de statut�:

* Rendu d�marr� - Une fois qu'un rendu est lanc�, Flamingo r�alise quelques t�ches telles que la conversion du mod�le et la configuration de la m�moire n�cessaire au rendu. 
* Action r�alis�e - Lorsque le bouton Arr�ter est utilis� et que le moteur de rendu a termin� la passe en cours, l'action est r�alis�e. 
* Passe termin�e - Ce message est affich� � chaque fois qu'une passe est termin�e. 
* Reprendre le rendu - S'il est possible de reprendre le rendu, ce message est affich�. 
* Actualisation - Le moteur de rendu est au milieu d'une passe, en cours d'actualisation du rendu. 

#### Passe
Passe actuellement en cours de rendu. Flamingo est un moteur de rendu fonctionnant avec plusieurs passes. Chaque passe am�liore les effets d'�clairage et de rendu complexes.

#### Ligne de balayage
Une passe avance le long d'une bande de pixels horizontaux.  Chaque ligne de pixels est une ligne de balayage. Cette information indique la ligne de balayage envoy�e par le moteur de rendu.

#### Temps total �coul�
Temps �coul� depuis le d�but du rendu.  Le temps de pr�paration pour le rendu n'est pas compris dans cette valeur.

#### Rayons / seconde
Nombre de rayons calcul�s dans la sc�ne par seconde.

#### Pixels / seconde
Nombre de pixels calcul�s dans l'image par seconde.

## Ajuster l'image
{: #adjust-image}
Cette option est une des plus importantes de Flamingo. Tout comme sur un appareil-photo, vous pouvez ajuster l'exposition de l'image. Cette option est id�ale pour rendre des rendus plus clairs, plus fonc�s, ajouter du contraste ou augmenter la saturation de couleur. Ce r�glage est appel� l'[adaptation des tons](https://en.wikipedia.org/wiki/Tone_mapping). Flamingo travaille dans l'espace de luminance, une gamme beaucoup plus importante de couleurs et d'intensit�s que celle pouvant �tre affich�e sur un �cran ou une imprimante. L'adaptation des tons est le proc�d� de conversion des donn�es de luminance en pixels rouges, verts et bleus (RVB) qui peuvent �tre affich�s sur un �cran ou imprim�s. Les param�tres contr�lent �galement comment les images sont enregistr�es.

![images/tonefinals-nocorrection.png](images/tonefinals-nocorrection.png)  ![images/tonefinals-correction.png](images/tonefinals-correction.png)
*L'image de gauche est celle produite par d�faut. L'image corrig�e apr�s avoir appliqu� une luminosit� de 0.20, une densit� de 0.16 et une saturation de 1.20.*
Utilisez ce proc�d� pour ajuster rapidement la luminosit� d'une image ainsi que sa couleur g�n�rale sans relancer le rendu.

### Luminosit�
{: #brightness}
Ajuste la luminosit� g�n�rale de l'image. Par exemple, si une surface blanche est rendue en gris, augmentez la luminosit� jusqu'� ce que la surface apparaisse blanche. Ou, si une sc�ne ext�rieure semble surexpos�e, diminuez la luminosit� jusqu'� ce que les r�sultats soient plus corrects.

![images/brightnessdefault.png](images/brightnessdefault.png)
*Luminosit� par d�faut (gauche) et augment�e.*

{% include_relative snippets/snippet-brightness.md %}

### Densit�
{: #burn}
Ajuste le point blanc de l'image. Il s'agit de la couleur blanche la plus claire de l'image. Un peu de densit� peut apporter un effet de sc�ne, de la vie et de la nettet� au rendu en ajoutant plus de zones de blanc afin de contraster avec les zones sombres.
Voir l'article de Wikipedia : Point blanc](https://fr.wikipedia.org/wiki/Point_blanc).

![images/burn-001.png](images/burn-001.png)
*Densit� par d�faut (gauche) et augment�e.*

### Saturation
{: #saturation}
La saturation contr�le la quantit� de couleurs d'une image. Une saturation nulle donnera une image en �chelle de gris. Les valeurs sup�rieures � 1 peuvent donner des couleurs plus  extr�mes.

![images/saturationdefault.png](images/saturationdefault.png)
*Saturation par d�faut (gauche) et multipli�e par 3 (droite).*

### Histogramme
{: #histogram}
Affiche la distribution de la lumi�re et des zones sombres de l'image apr�s l'application des ajustements sur l'image. Le bord gauche du diagramme repr�sente les couleurs sombres jusqu'au noir.  Le bord droit du diagramme montre la quantit� de couleurs claires jusqu'au blanc. Cette repr�sentation est tr�s utile pour d�terminer les parties importantes de l'image. Il peut �tre int�ressant d'ajuster l'image jusqu'� obtenir toute la gamme de valeurs dans l'image.  Par exemple, si l'histogramme s'arr�te avant d'atteindre l'extr�mit� droite du diagramme, ajoutez de la luminosit� ou de la densit� afin de faire tendre vers le blanc les portions les plus claires du rendu. Voir : [Article de Wikipedia : Histogramme](https://fr.wikipedia.org/wiki/Histogramme). Internet contient de nombreux articles sur l'utilisation des histogrammes pour �valuer l'exposition en photographie num�rique. Les principes sont les m�mes pour le rendu.

![images/histogram.png](images/histogram.png)
*Exemple� d'histogramme montrant la distribution de couleurs dans une image. Le diagramme gris montre quelques zones sombres (c�t� gauche) et une grande gamme de couleurs claires (c�t� droite). Ce diagramme montre �galement qu'il existe quelques pixels enti�rement blancs �tant donn� le diagramme est coup� sur le bord droit (les couleurs claires jusqu'au blanc sont repr�sent�es sur l'extr�mit� droite). 

#### Options de l'histogramme
Cliquez avec le bouton de droite sur l'image de l'histogramme pour voir les options suivantes.  Ces options changement la fa�on dont l'histogramme affiche les informations. Elles ne changement pas les valeurs de l'histogramme. 

* **Ajuster** - Cette option ajuste les verticales les plus �lev�es du graphique. 
* **M�diane** - Cette option ajuste la valeur m�diane sur la verticale. Elle permet de voir les d�tails au niveau des bords du diagramme. 
* **Moyenne** - Cette option ajuste la valeur moyenne sur la verticale.
* **Afficher le diagramme tri�** - Cette option trie toutes les valeurs en fonction de leur quantit� dans l'image. 
* **Afficher l'�chelle** - Affiche les valeurs correspondantes le long de la partie inf�rieure du diagramme. 
* **Couleur du diagramme...** - D�finit la couleur du diagramme.

### Verrouiller l'exposition
{: #lock-exposure}
Si les param�tres d'exposition sont verrouill�s, lorsque vous changez l'�clairage, l'exposition n'est pas modifi�e en fonction.

## Contraintes de rendu
{: #number-of-passes}
{: #time}
{: #render-constraints}
{% include_relative snippets/snippet-renderconstraints.md %}

## Informations
{: #information}

#### R�solution
Affiche la [r�solution de rendu](render-tab.html#resolution) actuelle. 

#### Faces
Affiche le nombre de faces de maillage utilis�es pour rendre le mod�le.  Cette valeur permet de comparer plusieurs [param�tres de maillage de rendu](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#documentproperties/mesh.htm) dans Rhino.

#### Faces apparentes
Lorsque le mod�le contient des blocs, Flamingo nXt peut utiliser la d�finition de bloc pour rendre les instances sans mailler chaque instance s�par�ment. L'affichage des faces apparentes montre combien de faces temporaires seraient g�n�r�es en plus si les occurrences de bloc n'existaient pas.

#### Informations sur l'�clairage
Informations sur la configuration actuelle de l'�clairage du rendu.  Liste des informations donn�es sur l'�clairage�:

>[Pr�r�glages](lighting-tab.html)
>[Soleil](sun-and-sky-tabs.html#sun)
>[Ciel](sun-and-sky-tabs.html#sky)
>[Lumi�res](lights-tab.html)
>[Indirecte](lighting-tab.html#indirect)
>[Lumi�re ambiante Activ�e/D�sactiv�e](lighting-tab.html#ambient)

## Canaux
{: #channels}
Utilisez ces contr�les pour changer les canaux de lumi�res en temps r�el. Assignez des lumi�res � un des huit canaux disponibles. Apr�s le rendu, ajustez l'�clairage dans l'image rendue. Cette fonction permet de travailler sur l'�quilibrage de plusieurs sources de lumi�re dans un rendu. Pour plus d'informations, voir la  rubrique [Canaux de rendu](render-channel.html#adjustng-channels).

## Effets post�rieurs
{: #post-process-effects}
Applique des effets de traitement post�rieur apr�s avoir calcul� le rendu de l'image. Les effets peuvent �tre activ�s et d�sactiv�s et l'ordre de la liste peut �tre modifi�. Chaque effet a ses propres param�tres. Effets disponibles :

>Brouillard
>Incandescence
>�clat
>Profondeur de champ
>Points
>Courbes
>Courbes isoparam�triques
>Annotations

Pour plus d'informations sur les filtres voir la rubrique [post-traitement des images](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#information/renderwindowpostprocess.htm).