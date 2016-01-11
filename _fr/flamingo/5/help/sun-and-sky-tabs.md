---
title: Soleil et ciel
---

# ![imagessun.svg](images/sun.svg) {{page.title}}
Le [soleil](#sun) et le [ciel](#sky) sont �troitement li�s entre eux. Le soleil peut modifier la luminosit� du ciel en mode automatique. Si le soleil est activ� et que le ciel est une image HDR, il est important d'�quilibrer leurs intensit�s. 

## Soleil
{: #sun}
Le soleil est une lumi�re parall�le invisible tr�s puissante. Les facteurs simulant des conditions du monde r�el tels que la latitude et la longitude, l'heure de la journ�e et la saison contr�lent la direction et la luminosit�du soleil.

Cette rubrique de l'aide couvre les contr�les de Flamingo pour le soleil. Le contr�le du [soleil de Rhinoceros](http://docs.mcneel.com/rhino/5/help/fr-fr/commands/sun.htm) peut �galement �tre utilis� pour placer le soleil. Flamingo synchronisera les deux contr�les.  

##### O� puis-je trouver les contr�les du soleil de Flamingo ?

Le soleil doit �tre activ� � travers les [pr�r�glages d'�clairage](lighting-tab.html#lighting-presets) ou les [param�tres d'�clairage personnalis�](lighting-tab.html#sun).

* ![images/options.png](images/options.png)Barres d'outils >![images/flamingo-icon.png](images/flamingo-icon.png)Barre d'outils de Flamingo nXt
* ![images/menuicon.png](images/menuicon.png)Menus > Flamingo nXt 5.0 > Montrer le panneau de configuration > Onglet Flamingo nXt > Soleil

**Remarque�:** L'onglet Soleil ne sera visible que si le soleil est activ� dans un pr�r�glage d'�clairage. 

Les angles solaires devront �tre indiqu�s afin de pouvoir calculer la lumi�re du soleil. Vous pouvez indiquer la direction du soleil de deux fa�ons : avec la date, l'heure et le lieu ou directement avec l'angle. Utilisez le positionnement selon la date, l'heure et le lieu si vous essayez de simuler le soleil r�el dans une �tude de l'emplacement du mod�le. Le positionnement par angle direct permet de contr�ler l'angle de la lumi�re sans faire r�f�rence � un soleil r�el. Utilisez cette option pour essayer des effets de lumi�re.

![images/sydneymorning.png](images/sydneymorning.png)  ![images/stockholmmorning.png](images/stockholmmorning.png)
*Sydney, Australie, 21 juin, 09h30 (� gauche). Stockholm, Su�de, 21 Juin, 09h30 (� droite).*

### D�finir l'azimut et l'altitude
{: #set-azimuth-and-altitude}
Utiliser des angles pour d�finir manuellement la direction du soleil. Active les contr�les de l'[azimut](#azimuth) et de l'[altitude](#altitude).

#### Azimut
{: #azimuth}
D�finit la direction du soleil en degr�s angulaires � partir du Nord (0) sur le plan horizontal.  La carte circulaire montre le monde sur une vue en plan. 

#### Altitude
{: #altitude}
D�finit la hauteur du soleil dans le ciel en degr�s angulaires � partir de l'�quateur (0).  La carte en demi-cercle simule une section dans la direction verticale des coordonn�es dans le rep�re g�n�ral. 

### D�finir le lieu sur la terre
{: #set-location-on-earth}
Utilisez l'angle du soleil pour placer le soleil en fonction de la date, de l'heure et du lieu. **Remarque�:** Comme pour tous les calculateurs de soleil, la pr�cision du positionnement du soleil peut varier. Si une pr�cision absolue est n�cessaire, nous vous recommandons de v�rifier la position du soleil. 

#### Date
{: #date}
D�finit la date.

#### Temps
{: #time}
Indique l'heure.

#### Heure d'�t�
{: #daylight-savings-time}
Avance l'heure d'une heure.

#### Latitude/Longitude
{: #latitude-longitude}
Entrez une latitude et une longitude ou choisissez une position sur la carte.
Les nombres seront �galement actualis�s pour afficher la latitude et la longitude de la position s�lectionn�e sur la carte avec la souris.

#### Fuseau horaire
{: #time-zone}
Affiche le fuseau horaire � partir de la latitude et la longitude du lieu indiqu�.

#### Liste des villes
{: #city-list}
Utilisez cette liste pour s�lectionner une ville afin de d�finir le lieu.

#### Carte
{: #map}
Cliquez sur la carte pour s�lectionner un lieu. Faites glisser la carte avec le bouton de gauche pour la d�placer.

### Intensit� du soleil
{: #sun-intensity}
Permet de modifier la luminosit� du composant de lumi�re directe de la lumi�re du jour (le soleil). L'intensit� du soleil est automatiquement calcul�e selon les angles solaires et les conditions du ciel mais elle peut �tre modifi�e pour s'�quilibrer avec les autres lumi�res.

### Reflet du soleil
{: #sun-highlight}
La nettet� du reflet du soleil.

![images/sunhighlight-0.png](images/sunhighlight-0.png)
*Reflet du soleil=0 (gauche) et 1 (droite).*

**Remarque�:** Des d�fauts de reflet solaire peuvent parfois �tre vus sur les rendus ext�rieurs lorsque le param�tre de Reflet du soleil est activ�. Pour att�nuer ou �liminer cet artefact, d�finissez le Reflet du soleil sur une plus petite valeur.
{: #speckle-artifacts}

{% include_relative snippets/snippet-sunchannel.md %}

#### Direction du nord
{: #north}
**Remarque�:** Nord correspond � la direction y positive du rep�re g�n�ral.

## Ciel
{: #sky}
Le ciel est une grande sph�re autour du rendu qui peut �tre utilis�e pour l'�clairage. Le ciel est tr�s diff�rent de l'environnement. Le ciel contr�le l'�clairage. L'environnement contr�le ce qui est r�fl�chi et visible en arri�re-plan. Dans de nombreux cas le ciel et l'environnement devront �tre d�finis diff�remment l'un de l'autre. 

#### O� puis-je trouver les contr�les du ciel de Flamingo ?
Le ciel doit �tre activ� � travers les [pr�r�glages d'�clairage](lighting-tab.html#lighting-presets) ou les [param�tres d'�clairage personnalis�](lighting-tab.html#sky).

 1. ![images/options.png](images/options.png)Barres d'outils >![images/flamingo-icon.png](images/flamingo-icon.png)Barre d'outils de Flamingo nXt
 1. ![images/menuicon.png](images/menuicon.png)Menus > Flamingo nXt 5.0 > Montrer le panneau de configuration > Onglet Flamingo nXt > Ciel

Les sch�mas d'�clairage pr�d�finis pour la lumi�re du jour [Ext�rieure](lighting-tab.html#exterior-daylight) et [Int�rieure](lighting-tab.html#interior-daylight) utilisent le ciel automatique par d�faut. Le sch�ma d'�clairage de [studio](lighting-tab.html#studio-lighting) pr�d�fini utilise un �clairage par image HDR.

Le ciel peut �tre d�fini de cinq fa�on diff�rentes�:

>[D�sactiv�](lighting-tab.html#off)
>[Ciel automatique](#automatic-sky)
>[Image � grande plage dynamique (HDRI)](#high-dynamic-range-image-sky)
>[Couleur](#color-sky)
>[Image](#image-sky)

Les deux meilleurs param�tres pour les types d'�clairage z�nithal sont [Image HDR](#high-dynamic-range-image-sky) et [Ciel automatique](#automatic-sky). Le ciel avec image HDR utilise une image contenant des valeurs d'�clairage enregistr�es sur chaque pixel pour d�finir l'�clairage et les r�flexions. Le ciel automatique utilise une n�bulosit� et une position du soleil dans le monde r�el pour simuler le ciel.  Ces param�tres produiront les rendus les plus dynamiques. 

### Ciel automatique
{: #automatic-sky}
Le ciel automatique utilise les param�tre de l'[onglet Soleil](sun-and-sky-tabs.html) pour d�terminer la gamme de couleurs et l'intensit� de la lumi�re z�nithale. Par exemple, lorsque le soleil est haut dans le ciel, l'�clairage et les couleurs du ciel sont tr�s diff�rents de ceux appliqu�s lorsque le soleil est bas. 

![images/sky-002.png](images/sky-002.png)
*Ciel automatique : soleil haut (gauche) et bas (droite) dans le ciel.*

#### N�bulosit�
{: #sky-cloudiness}
Lorsque la n�bulosit� est d�sactiv�e, le ciel est consid�r� comme d�gag� et des ombres dures sont cr��es. Plus la n�bulosit� est �lev�e, moins il y a de contraste entre la lumi�re et les ombres. Une n�bulosit� plus importante cr�era des ombres plus l�g�res et un effet d'�clairage plus r�gulier. Le param�tre d'opacit� touche de nombreux aspects du calcul de la lumi�re du jour, y compris la quantit� relative de lumi�re directe et indirecte, le mode de calcul de la lumi�re indirecte et la couleur de l'arri�re-plan si le mode ciel automatique a �t� s�lectionn�. La n�bulosit� varie de 0 (d�gag�) � 1 (compl�tement couvert). La gamme de n�bulosit� entre 0.35 et 0.50 est tr�s sensible et dynamique. 

![images/cloudiness0.png](images/cloudiness0.png)
*N�bulosit� 0 (gauche) et 1 (droite).*

#### Intensit� du ciel
{: #sky-intensity}
Permet de modifier la luminosit� du composant de lumi�re indirecte de la lumi�re du jour (le ciel). L'intensit� de la lumi�re z�nithale est automatiquement calcul�e selon les angles solaires et les conditions du ciel mais elle peut �tre modifi�e. **Remarque�:** Ce param�tre n'est important que si la sc�ne poss�de d'autres lumi�res qui doivent �tre compens�es. Si aucune autre lumi�re n'est d�finie, le contr�le de tonalit� compensera l'exposition et l'image rendue ne sera pas plus brillante ni plus terne en fonction de ce param�tre.

{% include_relative snippets/snippet-skychannel.md %}

### Ciel avec image � grande plage dynamique
{: #high-dynamic-range-image-sky}
Une [image � grande plage dynamique (HDR)](https://fr.wikipedia.org/wiki/Imagerie_%C3%A0_grande_gamme_dynamique) est un fichier image sp�cial en 2D. Ces images contiennent une plus grande plage de valeurs au niveau de chaque pixel qu'un fichier image standard, comme .jpg ou .png. Ces donn�es suppl�mentaires peuvent �tre utilis�es pour �clairer les mod�les. Si les valeurs contenues dans l'image HDR sont justes, l'�clairage peut �tre pr�cis. Cet effet peut produire un �clairage tr�s dynamique dans la sc�ne. Le sch�ma d'�clairage de studio pr�d�fini utilise des images HDR pour le ciel. Si vous consid�rez l'�clairage de studio comme une activit� d'int�rieur, imaginez l'image HDR comme un plafond qui �met de la lumi�re � partir des couleurs de l'image.

![images/lighting-001.png](images/lighting-001.png)
*�clairage avec une image HDR.*

Les images HDR contiennent normalement des valeurs de rayonnement exprim�es en watts. Si ce n'est pas le cas, l'intensit� de ces images HDR devra probablement �tre ajust�e pour obtenir des niveaux corrects d'illumination.

En plus du ciel, une autre image HDR peut �tre utilis�e pour chacun des trois arri�re-plans : [Visible](environment-tab.html#advanced-background), [R�fl�chi ](environment-tab.html#advanced-background) et [R�fract� ](environment-tab.html#advanced-background).

#### Image HDR
D�finit le fichier image HDR � utiliser. Cliquer sur l'image pour choisir une autre image. 

![images/hdrimage-001.png](images/hdrimage-001.png)
*Projection cylindrique �quidistante.*

Les images HDR peuvent avoir deux types de projection afin de d'envelopper correctement l'image autour de la sph�re du ciel. La plus connue est la projection cylindrique �quidistante. Ces images sont rectangulaires avec des proportions de 2:1. Les images cylindriques �quidistantes ont une r�solution uniforme sur toute l'image. La deuxi�me projection est la projection sph�rique. Les images HDR sph�riques sont carr�es avec une courbure �lev�e. Les projections sph�riques pr�sentent une r�solution r�duite au niveau de la jonction. 

#### Intensit�
Modifie la luminosit�de la lumi�re �mise par l'image HDR. Ce param�tre n'est important que si la sc�ne poss�de d'autres lumi�res qui doivent �tre compens�es. Si aucune autre lumi�re n'est d�finie, le contr�le de tonalit� compensera l'exposition et l'image rendue ne sera pas plus brillante ni plus terne en fonction de ce param�tre.

![images/hdrlightintensitylow.png](images/hdrlightintensitylow.png)
*Intensit� HDR faible et �lev�e.*

{% include_relative snippets/snippet-rotatehdrimage.md %}Dans l'illustration, l'image a �t� tourn�e afin que le reflet du soleil apparaisse sur l'objet. Indiquer les degr�s de rotation ou d�placez l'indicateur de rotation.
![images/hdrlightrotation2.png](images/hdrlightrotation2.png)
*Image tourn�e de sorte que le soleil apparaisse sur l'objet.*

#### Saturation
La saturation de la couleur de la lumi�re. �tant donn� que la lumi�re d'une image HDR provient de la couleur des pixels de l'image, des effets de couleur ind�sirables peuvent se produire parfois. Choisissez une saturation peu �lev�e si vous ne voulez utiliser que la lumi�re de l'image, sans la couleur.

![images/hdrlightsaturation0.png](images/hdrlightsaturation0.png)
*Saturation faible (gauche) et �lev�e (droite.*

{% include_relative snippets/snippet-mirrorimage.md %}

{% include_relative snippets/snippet-skychannel.md %}

### Couleur
{: #color-sky}
Il est possible d'utiliser une couleur ou un d�grad� de couleurs pour �clairer la sc�ne. Les couleurs du ciel sont multipli�es par la valeur de l'intensit� afin de donner aux couleurs une valeur d'�clairage. 

#### Intensit�
La valeur de l'intensit� est utilis�e pour multiplier les couleurs du ciel afin d'obtenir une valeur d'�clairage.  Les couleurs peuvent aller de 0 � 256 par canal. L'intensit� multipliera ces valeurs.

#### Type de couleur
Il existe trois fa�ons de contr�ler la couleur du ciel. Les contr�les sont similaires � ceux de l'environnement. Voir les contr�les de l'[arri�re-plan avec une couleur](environment-tab.html#environment-color-and-gradient-backgrounds) pour plus d'informations. 

### Image
{: #image-sky}
Il est possible d'utiliser une image pour �clairer la sc�ne. Les couleurs de l'image sont multipli�es par la valeur de l'intensit� afin de donner aux couleurs une valeur d'�clairage.

#### Intensit�
La valeur de l'intensit� est utilis�e pour multiplier les couleurs du ciel afin d'obtenir une valeur d'�clairage.  Les couleurs peuvent aller de 0 � 256 par canal. L'intensit� multipliera ces valeurs.

#### Projection de l'image
Il existe plusieurs fa�ons de contr�ler le placage d'une image sur le ciel. Les contr�les sont similaires � ceux de l'image en arri�re-plan.  Voir les contr�les de l'[arri�re-plan avec une image](environment-tab.html#environment-image) pour plus d'informations.