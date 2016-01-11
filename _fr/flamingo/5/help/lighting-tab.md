---
title: Pr�r�glages d'�clairage
---

# ![images/flamingotab.svg](images/flamingotab.svg) {{page.title}}
L'�clairage est la partie la plus importante et la plus souvent n�glig�e lors de la cr�ation d'images. Ce n'est pas uniquement une fa�on d'�clairer le mod�le. L'�clairage d�finit l'ambiance et il s'agit d'un composant cl� dans la d�finition de la sc�ne.

![images/christophersotogutierrez.png](images/christophersotogutierrez.png)
*Image de Christopher Soto Guti�rrez.*

#### O� puis-je trouver les contr�les d'�clairage de Flamingo ?

* ![images/menuicon.png](images/menuicon.png)Menus > Flamingo nXt 5.0 > Montrer le panneau de configuration.
* Cliquez avec le bouton de droite et cochez Flamingo nXt.


Essayez de respecter les instructions suivantes lorsque vous d�finissez l'�clairage de votre mod�le :

* Commencez avec un pr�r�glage d'�clairage.
* �tant donn� que Flamingo nXt simule l'�clairage du monde r�el, donnez des informations pr�cises si possible. 
* �vitez d'utiliser des niveaux d'intensit� irr�alistes pour les sources de lumi�re.
* D�finissez correctement les unit�s dans le mod�le. L'�clairage ne sera pas correct si les unit�s ne sont pas. Par exemple, si votre mod�le est en millim�tres, d�finissez les unit�s du mod�le en millim�tres.
* R�glez la luminosit� globale du rendu en utilisant le contr�le [Luminosit�](render-window.html#brightness) dans la fen�tre d'affichage du rendu. N'essayez pas d'ajuster la luminosit� globale de la sc�ne en changeant l'intensit� de toutes les sources de lumi�re�; le r�glage d'[exposition automatique](render-window.html#brightness) annulerait cette augmentation. 

Pour am�liorer les techniques d'�clairage, soyez attentifs � la lumi�re et � son influence sur les surfaces. Les mat�riaux peuvent masquer certains effets d'ombres et de r�flexions, certains experts du rendu appliquent donc l'�clairage � leurs mod�les avant d'appliquer les mat�riaux. Essayez de voir la lumi�re objectivement, comme un appareil photo.

## Pr�r�glages d'�clairage
{: #lighting-presets}
Une bonne option pour commencer � d�finir un �clairage est d'utiliser les pr�r�glages qui correspondent � des situations d'�clairage du monde r�el. Flamingo nXt poss�de des r�glages de l'�clairage qui peuvent vous aider � d�marrer avec l'�clairage de votre mod�le. De nombreuses autres options d'�clairage sont disponibles, mais les pr�r�glages sont souvent suffisants pour la plupart des rendus. Choisissez le sch�ma de pr�r�glages qui se rapproche le plus � votre sc�ne.

L'�clairage de Flamingo nXt utilise quatre modes pr�d�finis :

> [�clairage de studio](lighting-tab.html#studio-lighting)
> [Lumi�re du jour ext�rieure](lighting-tab.html#exterior-daylight)
> [Lumi�re du jour int�rieure](lighting-tab.html#interior-daylight)
> [�clairage artificiel](lighting-tab.html#artificial-lighting)

### �clairage de studio
{: #studio-lighting}
Ce sch�ma imite l'�clairage d'un studio de photographie. Il est tr�s adapt� au rendu d'objets isol�s de petite taille ou de taille moyenne.  Utilisez-le �galement pour une sc�ne bien �clair�e par un environnement HDR.

![images/studiolighting-001.png](images/studiolighting-001.png){: .float-img-left} Un fichier image � grande plage dynamique (HDR) fournit l'�clairage principal. La lumi�re de l'image HDR imite les niveaux d'�clairage int�rieur du studio. Les param�tres HDR sont d�finis dans l'[onglet Ciel](sun-and-sky-tabs.html#sky). Vous pouvez �galement ajouter des lumi�res artificielles � votre sc�ne en utilisant l'onglet Lumi�res. L'arri�re-plan visible dans le pr�r�glage Studio est noir.

L'�clairage Studio est optimis� pour le rendu de petits articles tels que des bijoux ou des produits industriels qui sont pr�sent�s sur des supports ou des tables. Dans ce sch�ma, le soleil est d�sactiv� et un ciel d�fini avec une image HDR apporte une base de r�flexion pour les objets brillants.

Pour un plus grand contr�le, utilisez les sources de lumi�re pour �clairer la sc�ne. Lors de la mise en place des lumi�res d'un studio, il est important d'avoir un �clairage sc�nique. Cet �clairage est obtenu en produisant de grands contrastes. En d'autres termes, les zones sombres sont aussi importantes que les zones claires. L'�clairage sc�nique demande un certain nombre de sources de lumi�re plac�es de fa�on � cr�er des zones tr�s sombres et des zones tr�s claires.

Les techniques d'�clairage pour la photographie sont g�n�ralement les m�mes que l'�clairage pour le rendu. Si vous voulez en apprendre plus sur ce th�me, vous devriez donc commencer par un livre sur l'�clairage en photographie. Pour plus d'informations sur les param�tres d'un �clairage de studio, consultez la section : [Bases de l'�clairage de studio](../guides/studio-lighting-basics.html).

### Lumi�re du jour ext�rieure
{: #exterior-daylight .clear-img}
Ce sch�ma simule la lumi�re du jour pour des rendus ext�rieurs utilisant le soleil et le ciel naturels.

![images/exteriorlighting-001.png](images/exteriorlighting-001.png){: .float-img-right} D�finissez les param�tres dans les onglets [Soleil](sun-and-sky-tabs.html#sun) et [Ciel](sun-and-sky-tabs.html#sky). D�finissez les [angles du soleil](sun-and-sky-tabs.html#set-azimuth-and-altitude) directement ou utilisez la [position g�ographique](sun-and-sky-tabs.html#set-location-on-earth), la date et l'heure. L'arri�re-plan visible par d�faut correspond au ciel simul�.

L'�clairage de l'ext�rieur d'un b�timent est le mod�le d'�clairage le plus simple. La plupart des sc�nes ext�rieures n'auront besoin de rien d'autre que le [soleil](sun-and-sky-tabs.html#sun)  par d�faut.

Lorsque le [soleil](sun-and-sky-tabs.html#sun) est activ�, la sc�ne doit �tre d�finie comme [int�rieure](#interior) ou [ext�rieure](#exterior) . En effet, la contribution de la lumi�re du ciel, de la lumi�re r�fl�chie par le sol et de la lumi�re r�fl�chie par les autres surface est tr�s diff�rente dans les sc�nes int�rieures et ext�rieures. L'utilisation des bons param�tres [Int�rieur/Ext�rieur](#indirect) donne un �clairage tr�s efficace et r�aliste.

Parfois il est facile de d�terminer si une sc�ne est un int�rieur ou un ext�rieur. Si le point de vue est en dehors d'un b�timent, il s'agit d'une sc�ne ext�rieure. Si le point de vue se trouve � l'int�rieur d'une pi�ce, il s'agit d'un int�rieur. Mais certains types de sc�nes ne sont pas aussi �vidents. Prenez par exemple les cours, les belv�d�res, les vues d�compos�es et les sections. Si une cour est beaucoup plus large que haute, elle laisse alors p�n�trer une grande quantit� de lumi�re du ciel, essayez de l'�clairer comme une sc�ne ext�rieure. Si elle est plus haute que large, essayez d'�clairer la sc�ne comme un int�rieur. Dans ce cas, un des trucs est d'ajouter des entr�es de lumi�re du jour au-dessus de la cour pour aider � diriger la lumi�re du ciel dans la sc�ne.

Les lumi�res peuvent �galement simuler l'�clairage d'un paysage. Utilisez des projecteurs pour mettre en valeur des caract�ristiques architecturales et les arbres. Cet effet est tr�s utile pour les sc�nes de nuit ou tr�s sombres. Pendant la journ�e, le soleil sera normalement plus puissant que tout autre �clairage artificiel dans une sc�ne ext�rieure, comme dans le monde r�el.

Les vues �clat�es, les sections et les dessins techniques mentionn�s ci-dessus sont �galement assez compliqu�s. La d�cision d�pend des r�sultats d�sir�s. Pour une sc�ne ext�rieure avec le rendu le plus rapide, utilisez la m�thode de rendu ext�rieur. Si cette m�thode ne donne pas une image assez int�ressante, essayez d'utiliser un rendu int�rieur. L'int�rieur peut �tre plus int�ressant mais la d�finition de l'�clairage prend plus de temps.

### Lumi�re du jour int�rieure
{: #interior-daylight .clear-img}
Ce sch�ma simule un int�rieur �clair� par la lumi�re naturelle.

![images/interiordaylightnoportals.png](images/interiordaylightnoportals.png){: .float-img-left} Il est divis� en deux composants : la lumi�re directe du soleil  transmise par le [soleil](sun-and-sky-tabs.html#sun) et la lumi�re indirecte du soleil transmise par le [ciel](sun-and-sky-tabs.html#sky), le sol et les autres objets ext�rieurs.

Les param�tres du [soleil](sun-and-sky-tabs.html#sun) et du [ciel](sun-and-sky-tabs.html#sky) sont similaires aux pr�r�glages d'un �clairage [ext�rieur](lighting-tab.html#exterior-daylight).
La lumi�re directe du soleil implique un calcul direct et il vous suffit d'indiquer l'heure, la date et le lieu afin d'assurer la pr�cision des r�sultats.

Remarques sur les rendus int�rieurs�:
{: .clear-img}

* Dans la mesure du possible, essayez d'utiliser des valeurs pr�cises pour vos [lumi�res](lights-tab.html), pour les [param�tres du ciel](sun-and-sky-tabs.html#sky) ainsi que les vitres des fen�tres.
* �tant donn� que le soleil et le ciel sont plus brillants que les autres lumi�res, vous ne verrez peut-�tre pas beaucoup de diff�rence lors de l'ajout d'un �clairage artificiel si le soleil est activ�. C'est normal. �vitez d'augmenter artificiellement la puissance de vos sources de lumi�re.
* Vous pouvez baisser l'intensit� du [soleil](sun-and-sky-tabs.html#sun-intensity) ou du [ciel](sun-and-sky-tabs.html#sky-intensity). Ces param�tres simulent un ciel d�gag�, la r�duction de leur intensit� permettra de simuler des conditions plus sombres, comme s'il y avait des nuages.
* Un rendu [multi-canaux](lights-tab.html#channel) peut vous aider � obtenir l'image que vous voulez, tout en conservant des donn�es pr�cises.

### �clairage artificiel
{: #artificial-lighting}
![images/artificiallight-001.png](images/artificiallight-001.png){: style="float: right; padding-left: 25px;"} Ce sch�ma offre une simulation d'un int�rieur architectural �clair� par des lampes la nuit. Utilisez l'[onglet des lumi�res](lights-tab.html) ou les [commandes de lumi�re de Rhino](lights-tab.html#rhino-light-commands) pour ins�rer et g�rer des objets lumineux dans votre mod�le.

L'�clairage indirect, c'est-�-dire la lumi�re qui est r�fl�chie par les surfaces, est activ� lorsqu'un des deux pr�r�glages int�rieurs est s�lectionn� et d�sactiv� pour l'�clairage studio et ext�rieur. Ce type d'�clairage est un composant important d'une simulation d'�clairage int�rieur. Pour les ext�rieurs et les mod�les de studio, les effets de l'�clairage indirect sont plus subtils, c'est pourquoi il est d�sactiv� par d�faut.

### �clairage personnalis�
{: #custom  style="clear:both;"}
Cet onglet permet de m�langer tous les param�tres d'�clairage.  Par exemple, si la sc�ne est une lumi�re du jour ext�rieure dans laquelle un environnement HDR a �t� ajout�, utilisez l'onglet Personnalis� pour d�sactiver ou activer des parties du mod�le d'�clairage.  Si les valeurs d'un sch�ma par d�faut sont modifi�es, le sch�ma devient un sch�ma personnalis�.

####  [Soleil](sun-and-sky-tabs.html#sun)
{: #sun}
Vous pouvez activer et d�sactiver l'onglet du soleil dans le menu contextuel. L'onglet [Soleil](sun-and-sky-tabs.html#sun) permet de modifier les param�tres de la position du soleil. 

![images/lightsunon.png](images/lightsunon.png)
*Soleil activ� et d�sactiv�.*
Le soleil est une source de lumi�re directionnelle tr�s brillante situ�e infiniment loin du mod�le. Les contr�les du soleil d�finissent sa direction en utilisant des coordonn�es sph�riques. Pour plus d'informations, consultez la rubrique sur l'[onglet Soleil](sun-and-sky-tabs.html#sun).

####  [Ciel](sun-and-sky-tabs.html#sky)
{: #sky}
D�finissez le canal du ciel sur une des quatre options�:

> Auto
> HDRI
> Couleur
> Image

Pour plus d'informations, consultez la rubrique sur l'[onglet Ciel](sun-and-sky-tabs.html#sky).
Le ciel est une source de lumi�re h�misph�rique situ�e infiniment loin du mod�le.

#### D�sactiv�
{: #off}
D�sactive le ciel.
![images/chromenosky.png](images/chromenosky.png)

#### Auto
{: #auto}
Offre un mod�le analytique bas� sur les conditions du ciel dans le monde r�el. Les param�tres de l'onglet [Soleil](sun-and-sky-tabs.html) contr�lent l'apparence et les qualit�s de lumi�re du ciel.
![images/chromeautosky.png](images/chromeautosky.png)

#### Image HDR
{: #hdri}
Une image HDR apporte une base pour les r�flexions des objets brillants.
![images/chromehdrbackground.png](images/chromehdrbackground.png)

#### Couleur
{: #color}
Le ciel sera compos� d'une couleur unie ou d'un d�grad� de deux ou trois couleurs et il utilisera des contr�les similaires � ceux de la section [Environnement : Arri�re-plan d'une couleur ou d�grad�s](environment-tab.html#color-and-gradient-backgrounds).
![images/colorsky.png](images/colorsky.png)

#### Image
{: #image}
Le ciel est constitu� d'une image avec une projection plane, cylindrique ou sph�rique, comme dans [Environnement : Image](environment-tab.html#image).
![images/chromeimagesky.png](images/chromeimagesky.png)


### Luminosit� de studio
{: #studio-brightness}
La luminosit� du [soleil](sun-and-sky-tabs.html) et du ciel sont r�duites, afin d'imiter les niveaux d'�clairage int�rieur d'un studio de photographie.
![images/studiobrightnessoffandon.png](images/studiobrightnessoffandon.png)
*Luminosit� de studio d�sactiv�e (gauche) et activ�e (droite).*

### Lumi�res
{: #lights}
Active ou d�sactive l'�clairage artificiel.

![images/lightsonandoff.png](images/lightsonandoff.png)
*Lumi�res activ�es (gauche) et d�sactiv�es (droite).*

### Indirect
{: #indirect}
D�finit l'�clairage qui se r�fl�chit � partir des surfaces. Par d�faut, cette option est activ�e pour l'�clairage int�rieur et d�sactiv�e pour l'ext�rieur et l'�clairage de studio. Il est possible d'activer l'�clairage indirect pour les rendus d' ext�rieurs.

#### M�thode
D�finit la m�thode de calcul de l'�clairage indirect.

#### D�sactiv�
L'�clairage indirect est d�sactiv�.

#### Int�rieur
{: #interior}
Optimise l'�clairage indirect pour les sc�nes int�rieures.

#### Ext�rieur
{: #exterior}
Optimise l'�clairage indirect pour les sc�nes ext�rieures.

L'�clairage indirect r�fl�chi � partir des autres surfaces peut apporter de la subtilit� du r�alisme � vous rendues ext�rieures. En particulier, les parties inf�rieures d'objets suspendus, tels que les avanc�es de toit ou les balcons, sont rendues avec plus de pr�cision avec un �clairage indirect.

#### Rebonds
{: #bounces}
D�finit le nombre de r�flexions entra�n�es par un �clairage indirect.

### Lumi�re ambiante
{: #ambient}
La lumi�re ambiante est une lumi�re constante ajout�e au rendu. Ces param�tres contr�lent l'intensit� de la lumi�re ambiante sous forme de pourcentage de la lumi�re ambiante totale calcul�e dans la sc�ne.

En g�n�ral, si la lumi�re ambiante est r�duite, les images pr�sentent un contraste plus important. Une lumi�re ambiante trop importante peut entra�ner une image plate et fade et une lumi�re ambiante trop faible peut donner un contraste trop important.

#### Aucune
Aucune lumi�re ambiante.

#### Ext�rieur
Optimise la lumi�re ambiante pour les sc�nes ext�rieures.

#### Int�rieur
Optimise la lumi�re ambiante pour les sc�nes int�rieures.

#### Studio
Optimise la lumi�re ambiante pour les sc�nes de studio.

## Enregistrer un �clairage personnalis�

### Enregistrer le sch�ma d'�clairage
{: #save-lighting-scheme}
![images/saveschemeicon.png](images/saveschemeicon.png) Enregistre le sch�ma d'�clairage actuel.

### Ouvrir un sch�ma d'�clairage
{: #open-lighting-scheme}
![images/importfromfile.png](images/importfromfile.png) Ouvre un sch�ma d'�clairage enregistr�.