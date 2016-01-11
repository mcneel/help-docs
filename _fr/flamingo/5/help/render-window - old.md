---
---

<!-- TODO: This is a combination of the old information here and the Rhino render Windows.  These two still need to be combined. -->

# Rectangle Rendu
La fen�tre de rendu offre des options pour r�gler l'exposition et ajouter des effets par post-traitement. Le cadre principal de la fen�tre de rendu fait partie du cadre de rendu de Rhino.  Pour plus d'informations sur les menus et ic�nes de la fen�tre de rendu, consultez la [rubrique sur la fen�tre de rendu de Rhino](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#information/renderwindowpostprocess.htm)

### Menus d�roulants
Pour plus d'informations sur les menus et ic�nes de la fen�tre de rendu, consultez la [rubrique sur la fen�tre de rendu de Rhino](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#information/renderwindowpostprocess.htm)


### Barres d'outils


### Enregistrer avec le canal alpha de l'arri�re-plan
{: #save-with-alpha-channel}
Enregistre une image 32 bits au format PNG, TIF ou BMP avec l'arri�re-plan du canal alpha. Les versions canal alpha des formats de fichier sont utilis�es pour la composition haute qualit�. Les arri�re-plans appara�tront en noir lorsque le rendu sera enregistr�avec le canal alpha.

### Exporter vers un fichier natif de Flamingo nXt (.nXtImage)
{: #export-to-nxtimage}
Enregistre les informations de couleur et de luminance non comprim�es. Enregistre tous les canaux de rendu, y compris le canal [alpha](environment-tab.html#alpha). Les fichiers nXt Image peuvent �tre ouverts dans l'[�diteur d'images](image-editor.html). Vous pouvez alors ajuster l'[exposition](#adjust-image) et appliquer des [effets](#effects) avant d'enregistrer l'image dans un autre format.
Le format .nXtImage est le format d'image natif des moteurs de rendu nXt. Ce format est recommand� pour l'enregistrement de vos rendus car il conserve la plupart des informations sur votre rendu. Les images enregistr�es dans ce format peuvent �tre manipul�es dans l'[�diteur d'images nXt](image-editor.html) et des effets sp�ciaux peuvent �tre ajout�s. Cet �diteur permet d'enregistrer dans de nombreux formats standards, y compris tous les formats pris en charge dans nXt. Il est �galement possible d'enregistrer au format [Piranesi EPix file (.epx)](http://www.piranesi.co.uk/).

### Exporter vers un fichier HDR
{: #export-to-hdr}
Enregistre les informations de couleur et de luminance non comprim�es. Le format .hdr enregistre les donn�es de luminance directement dans un format � grande plage dynamique. Les arri�re-plans sans luminance, comme les photographies normales, appara�tront en noir s'ils sont enregistr�s dans un de ces formats.

### Exporter vers un fichier EXR
{: #export-to-exr}
Format de fichier image � grande plage dynamique cr�� par la soci�t� Industrial Light and Magic (ILM) et distribu� sous forme de licence libre. Ce format de fichier g�re les nombres flottants en 16 bits par canal avec un bit pour le signe, cinq bits pour l'exposant et dix bits pour la mantisse. Ceci permet d'avoir une plage dynamique de plus de trente niveaux d'exposition. Voir : [Article de Wikipedia : OpenEXR](http://fr.wikipedia.org/wiki/OpenEXR).
Le format EXR enregistre les donn�es de luminance directement dans un format � grande plage dynamique. Les arri�re-plans sans luminance, comme les photographies normales, appara�tront en noir s'ils sont enregistr�s dans un de ces formats.

## Quitter
Ferme la fen�tre de rendu.

##  [Fen�tre de rendu, Onglet Flamingo](render-window.html#help)

## Avancement
{: #progress}

### Action

### Passe

### Ligne de balayage

### Temps total �coul�

### Rayons / seconde

### Pixels / seconde

## Contraintes de rendu
{: #number-of-passes}
{: #time}
{: #render-constraints}
{% include_relative snippets/snippet-renderconstraints.md %}
## Ajuster l'image
{: #adjust-image}
Les param�tres qui contr�lent l'affichage � l'�cran contr�lent aussi tous les fichiers image cr�� � partir de cet affichage. Plusieurs fichiers image avec des param�tres d'exposition diff�rents peuvent �tre enregistr�s � partir d'une seul rendu. Les param�tres d'exposition d�finis pour une image rendue seront appliqu�s � la suivante.
Ce proc�d� est appel� *adaptation des tons.* L'adaptation des tons est le proc�d� de conversion des donn�es de luminance utilis�es par nXt en pixels rouges, verts et bleus (RVB) qui peuvent �tre affich�s ou imprim�s.

### Luminosit�
{: #brightness}
Ajuste la luminosit� g�n�rale de l'image. Par exemple, si une surface blanche est rendue en gris, augmentez la luminosit� jusqu'� ce que la surface apparaisse blanche. Ou, si une sc�ne ext�rieure semble surexpos�e, diminuez la luminosit� jusqu'� ce que les r�sultats soient plus corrects.
![images/brightnessdefault.png](images/brightnessdefault.png)
*Luminosit� par d�faut (gauche) et augment�e.*
{% include_relative snippets/snippet-brightness.md %}
### Densit�
{: #burn}
Ajuste le point blanc de l'image. Il s'agit de la couleur blanche la plus claire de l'image. La densit� peuvent apporter un effet de sc�ne, de la vie et de la nettet� au rendu en ajoutant plus de zones de blanc afin de contraster avec les zones sombres.
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
Affiche la distribution de la lumi�re et des zones sombres de l'image.
Voir : [Article de Wikipedia : Histogramme](https://fr.wikipedia.org/wiki/Histogramme). Internet contient de nombreux articles sur l'utilisation des histogrammes pour �valuer l'exposition en photographie num�rique. Les principes sont les m�mes pour le rendu.
![images/histogram.png](images/histogram.png)
*Histogramme.*

#### Options de l'histogramme

>Cliquez avec le bouton de droite sur l'image de l'histogramme pour voir les options

#### Ajuster

#### M�diane

#### Moyenne

#### Afficher le diagramme tri�

#### Afficher l'�chelle

#### Couleur du diagramme

#### Afficher les valeurs de luminance

### Verrouiller l'exposition
{: #lock-exposure}
Si les param�tres d'exposition sont verrouill�s, lorsque vous changez l'�clairage, l'exposition n'est pas modifi�e en fonction.

## Informations
{: #information}

### R�solution
Affiche la [r�solution de rendu](render-tab.html#resolution).

### Faces
Affiche le nombre de faces de maillage utilis�es pour rendre le mod�le.

### Faces apparentes
Lorsque le mod�le contient des blocs, Flamingo nXt peut utiliser la d�finition de bloc pour rendre les instances sans mailler chaque instance s�par�ment. L'affichage des faces apparentes montre combien de faces temporaires suppl�mentaires�sont g�n�r�es.

## Informations sur le pixel
Point dans la fen�tre
Point sur l'image
Coordonn�e Y dans l'image
Couleur du pixel
Luminance
Distance

## Informations sur l'�clairage

###  [Pr�r�glages](lighting-tab.html)

###  [Soleil](sun-and-sky-tabs.html#sun)

###  [Ciel](sun-and-sky-tabs.html#sky)

###  [Lumi�res](lights-tab.html)

###  [Indirecte](lighting-advanced-tab.html#indirect)

###  [Lumi�re ambiante Activ�e/D�sactiv�e](lighting-advanced-tab.html#ambient)

## Canaux
{: #channels}
Affiche le statut des canaux d'�clairage.

## Effets
{: #post-process-effects}
{: #effects}
Les effets de post-traitement sont appliqu�s apr�s le rendu de l'image. Ils peuvent �tre activ�s et d�sactiv�s et l'ordre de la liste peut �tre modifi�. Chaque effet a ses propres param�tres.

## Options des effets
Ces options sont �galement disponibles dans un menu contextuel.

>Cliquez avec le bouton de droite sur un effet pour afficher le menu contextuel.

![images/toggleeffect.png](images/toggleeffect.png)Activer/d�sactiver l'effet s�lectionn�.
![images/moveup.png](images/moveup.png)D�placer l'effet s�lectionn� vers le haut dans la liste.
![images/movedown.png](images/movedown.png)D�placer l'effet s�lectionn� vers le bas dans la liste.
![images/effectproperties.png](images/effectproperties.png)Propri�t�s de l'effet s�lectionn�.
![images/savelistorderasdefault.png](images/savelistorderasdefault.png)Enregistre comme valeur par d�faut l'ordre actuel des effets ainsi que les propri�t�s.
![images/savecurrenteffectslist.png](images/savecurrenteffectslist.png)Enregistre et donne un nom � la liste d'effets actuelle.
![images/importnamedeffectslist.png](images/importnamedeffectslist.png)Importer une liste nomm�e d'effets.

## Profondeur de champ
{: #postprocessingdof}
L'effet de profondeur de champ estompe l'image en fonction de la distance � partir de la cam�ra.
![images/postprocessing-dof.png](images/postprocessing-dof.png)

## Propri�t�s de la profondeur de champ
{: #depth-of-field-properties}

### Propri�t�s visuelles
{: #dofvisualproperties}

#### Intensit� du flou
{: #dofblurringstrength}
D�termine la quantit� de flou dans l'image. Il s'agit d'une valeur arbitraire et des valeurs tr�s diff�rentes donneront des r�sultats int�ressants dans diff�rentes images.

#### Flou maximum
{: #dofmaxblurring}
D�termine le rayon maximum de flou utilis�. �tant donn� que les zones tr�s floues peuvent rendre l'application de cet effet assez lente, cette option permet de limiter l'effet.

### Zone d'effet
{: #dofareaofeffect}

#### Distance focale
{: #dofocaldistance}
Indique la distance � partir de la cam�ra sur laquelle l'image est nette.

#### S�lectionner
Cliquer dans l'image pour d�finir la distance focale.

#### Arri�re-plan flou
{: #dofblurbackground}
D�termine si l'arri�re-plan est �galement flou. L'arri�re-plan re�oit le flou maximal.

## Brouillard
{: #postprocessingfog}
L'effet de brouillard ajoute � l'image une coloration en fonction de la profondeur. Cet effet peut �tre utilis� pour ajouter un brouillard �pais ou un effet subtil de profondeur.
![images/postprocessing-nofog.png](images/postprocessing-nofog.png)
*Aucun effet n'est appliqu�.*

### Brouillard comme arri�re-plan d�grad�
Le brouillard peut �tre utilis� pour cr�er un arri�re-plan d�grad�.
Dans ce cas, les param�tres de cr�ation de l'arri�re-plan sont les suivants :
Intensit� = 1 Bruit = .1 Couleur du brouillard = Noire Distance finale = environ 110 Distance de d�part = environ 90 Arri�re-plan avec brouillard = Activ� Tremblement = 80
![images/postprocessing-fogasgradient.png](images/postprocessing-fogasgradient.png)
*Brouillard comme arri�re-plan d�grad�.*

## Propri�t�s de brouillard
{: #fogsettings}

### Propri�t�s visuelles
{: #fogvisualproperties}
D�termine l'apparence de l'effet de brouillard.

#### Intensit�
{: #fogstrength}
D�termine la quantit� maximum de brouillard. Si l'intensit� est �gale � 0, l'effet est d�sactiv� ; si elle est �gale � 1, l'effet est � son maximum. Des valeurs sup�rieures � 1 peuvent �tre utilis�es mais ceci n'a de sens que si le Bruit est activ�**.

#### Bruit
{: #fognoise}
Ajoute un effet al�atoire � l'intensit� du brouillard**.

#### Couleur
{: #fogcolor}
Indique la couleur du brouillard.

>Cliquez sur la palette de couleurs pour s�lectionner une couleur dans la bo�te de dialogue [S�lectionner une couleur](select-color.html).
>Cliquez sur le bouton S�lectionner pour s�lectionner la couleur dans l'image rendue.

### Zone d'effet
D�termine la zone concern�e par le brouillard.

#### Distance de d�part
{: #fogstartdistance}
Indique la distance entre la cam�ra et le point o� le brouillard commence � appara�tre.

>Cliquez sur le bouton S�lectionner pour indiquer la profondeur dans l'image rendue.

#### Distance finale
{: #fogenddistance}
Indique la distance entre la cam�ra et le niveau maximal de brouillard.

>Cliquez sur le bouton S�lectionner pour indiquer la profondeur dans l'image rendue.

### Limites (gauche, droite, haut, bas)
{: #fogbounds}
Indique la zone de l'image affect�e par le brouillard. Cette option peut �tre utilis�e pour repr�senter de l�gers nuages bas.
Cliquez sur le bouton S�lectionner une zone pour indiquer la zone d'application dans l'image rendue.

### Brouillard

#### Arri�re-plan avec brouillard
D�termine si le brouillard est aussi appliqu� � l'image en arri�re-plan. Au niveau de l'arri�re-plan, l'intensit� du brouillard sera � son maximum.

#### Tremblement
{: #fogfeathering}
D�termine le nombre de pixels en dehors de la zone d'application o� le brouillard dispara�tra petit � petit.

### Aper�u
Permet de voir l'effet sur l'image lorsque vous changez les valeurs.

## �clat
{: #postprocessingglare}
L'�clat et l'incandescence sont tr�s similaires. L'incandescence utilise une couleur s�lectionn�e alors que l'�clat pousse la couleur vers le blanc. Avec l'�clat, les zones extr�mement claires de l'image semblent briller. Pour ce faire, la zone entourant la zone claire est �claircie. Cet effet tr�s subtile est utilis� normalement pour les sc�nes de nuit car il rend les lumi�res encore plus r�alistes.
![images/postprocessing-noglare.png](images/postprocessing-noglare.png)
*�clat d�sactiv� (gauche) et activ� (droite).*

## Propri�t�s de l'�clat
{: #glaresettings}

### Limite du point blanc
{: #glarewhitepointbound}
D�termine o� commence l'�clat dans la gamme de tons. La valeur est repr�sent�e sur l'histogramme et peut aussi �tre r�gl�e directement sur celui-ci. Les pixels plus clairs que la limite du point blanc (en termes de luminance ou en valeur sur l'�chelle des gris) brilleront.

### Taille de l'�clat
{: #glaresize}
Le rayon de l'�clat autour du pixel clair.

### Gain
{: #glaregain}
Multiplicateur de la luminosit� de l'�clat. La valeur par d�faut est �gale � 1 et elle devrait donner des effets normaux. Utilisez des valeurs sup�rieures pour un �clat extr�mement clair.

### Utiliser les informations photom�triques
{: #glareusephotometric}
En mode photom�trique, la quantit� d'�clat est contr�l�e en d�terminant dans quelle mesure le pixel est "plus blanc que blanc". Sinon, l'effet utilise les pixels les plus blancs de l'image.

### Histogramme
{: #glarehistogram}
Affiche la distribution des zones sombres et claires.

#### Options de l'histogramme

>Cliquez avec le bouton de droite sur l'image de l'histogramme pour voir les options

#### Ajuster

#### M�diane

#### Moyenne

#### Afficher le diagramme tri�

### Aper�u
Permet de voir l'effet sur l'image lorsque vous changez les valeurs.

## Incandescence
{: #postprocessingglow}
L'effet incandescent produit une zone claire autour de couleurs sp�cifiques. Il peut �tre utilis� pour faire briller les lumi�res color�es et les n�ons par exemple. Vous pouvez s�lectionner jusqu'� 10 couleurs sur lesquelles appliquer cet effet.
Dans l'illustration ci-contre, l'effet est appliqu� sur une des couleurs rouges du rubis et le gain est d�fini de sorte que la couleur se rapproche du blanc.
![images/postprocessing-glowassparkle.png](images/postprocessing-glowassparkle.png)
*L'incandescence pour faire scintiller un objet.*
![images/postprocessing-glowon.png](images/postprocessing-glowon.png)
*Incandescence d�sactiv�e (gauche) et activ�e (droite).*

## Propri�t�s de l'incandescence
{: #glowsettings}

### Activ�
Active l'incandescence sur la couleur correspondante.

### Couleur
{: #glowcolor}
Indique la couleur de l'incandescence.

>Cliquez sur la palette de couleurs pour s�lectionner une couleur dans la bo�te de dialogue [S�lectionner une couleur](select-color.html).
>Cliquez sur le bouton S�lectionner pour s�lectionner la couleur dans l'image rendue.

### Sensibilit�
{: #glowsensitivity}
Contr�le la variation permise sur la couleur s�lectionn�e lors du calcul de l'incandescence sur des pixels proches de cette couleur.

### Taille de l'incandescence
{: #glowsize}
Le rayon de l'incandescence autour du pixel clair.

### Gain
{: #glowgain}
Multiplicateur de la luminosit� de l'incandescence. La valeur par d�faut est �gale � 1 et elle devrait donner des effets normaux. Utilisez des valeurs sup�rieures pour une incandescence extr�mement claire.

### Aper�u
Permet de voir l'effet sur l'image lorsque vous changez les valeurs.

## Fils et texte
{: #postprocessingwireframe}
Reproduit les courbes, les textes, les cotes, les courbes isoparam�triques, les bords de maillage et les objets ponctuels dans l'image rendue.
![images/posteffectwires-001.png](images/posteffectwires-001.png)
*Avec (gauche) et sans Fils et texte (droite).*

## Propri�t�s de l'option Fils et texte

### Courbes
Affiche les courbes.

### Cotes et texte
Affiche toutes les cotes et tous les objets de texte.

### Courbes isoparam�triques
Affiche les courbes isoparam�triques des surfaces.

### Bords de maillage
Affiche les bords des maillages.

### Points
Affiche les objets ponctuels.

### Aper�u
Permet de voir l'effet sur l'image lorsque vous changez les valeurs.