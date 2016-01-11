---
title: Propri�t�s des objets
---


#  ![images/properties.svg](images/properties.svg) {{page.title}}
Les propri�t�s Flamingo nXt des objets jouent uniquement sur l'apparence des objets lors du rendu dans Flamingo nXt.

### ![images/materialtab.png](images/materialtab.png) Source du mat�riau
{: #material-source}
Un mat�riau peut �tre assign� � des calques, des blocs et des objets. Pour plus d'informations sur l'assignation de mat�riaux, consultez la rubrique [Assignation des mat�riaux](material_assignment.html). Si le mat�riau est d�fini par objet, les propri�t�s du mat�riau sont �galement affich�es dans cette bo�te de dialogue. Pour plus d'informations sur l'�dition d'un mat�riau, consultez [Propri�t�s des mat�riaux](material-type-simple.html).

### ![images/apply-cylindrical-mapping.png](images/apply-cylindrical-mapping.png) Placage de texture
{: #texture-mapping}
Le placage contr�le comment le mat�riau est positionn� (plaqu�) sur un objet pr�cis. La m�thode utilis�e pour assigner un mat�riau, que ce soit par calque ou par objet, ne joue pas sur le placage. Pour les mat�riaux ne pr�sentant pas de motif perceptible, le placage n'est normalement pas n�cessaire. Utilisez le placage lorsque le mat�riau est directionnel ou lorsqu'il pr�sente un motif �vident.  M�me dans ces cas, le placage par d�faut peut servir. Le placage est li� � l'objet et il le suit s'il est d�plac�, tourn� ou si son �chelle est chang�e. Pour plus d'informations sur les types de placage, consultez la section [Placage de texture](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#properties/texturemapping.htm).

![images/mapping-cube.png](images/mapping-cube.png) ![images/mapping-planar.png](images/mapping-planar.png)
*Deux directions de placage diff�rentes*

### ![images/decalproperties.png](images/decalproperties.png) D�calcomanies
{: #decals}
Les d�calcomanies sont des placages d'image sans mosa�que appliqu�s directement sur les objets au lieu d'utiliser un mat�riau. Utilisez les d�calcomanies pour modifier une partie d�termin�e de la couleur, de la r�flectivit� ou du reliefs d'un objet. Voir la section [D�calcomanies de Rhino](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#properties/decal.htm) pour plus d'informations sur la cr�ation et le positionnement des d�calcomanies. 

![images/freshmilk.png](images/freshmilk.png) ![images/decal-planar-001.png](images/decal-planar-001.png)
![images/cylindricaldecal-002.png](images/cylindricaldecal-002.png) ![images/uvmapdecal-00.png](images/uvmapdecal-00.png)
*Quatre exemples diff�rents de d�calcomanies*

### ![images/apply-edge-softening.png](images/apply-edge-softening.png)Maillages personnalis�s
{: #custom-meshes}
Plusieurs modificateurs de maillage peuvent �tre utilis�s dans Rhino afin de donner plus de d�tails aux mod�les rendus. Utilisez ces modificateurs pour arrondir les bords, ajouter des lignes de fermetures entre des surfaces et cr�er des c�bles � partir de courbes. 

Pour plus d'informations, consultez les sections suivantes�:

>[Adoucissement des bords](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#commands/applyedgesoftening.htm)
>[Gaine](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#commands/applycurvepiping.htm)
>[Ligne de fermeture](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#commands/applyshutlining.htm)
>[D�placement](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#commands/applydisplacement.htm)

### ![images/object-flamingo.PNG](images/object-flamingo.PNG) Propri�t�s de Flamingo
{: #flamingo-properties}

#### Canal Alpha
{: #alpha-channel}
Rend l'objet invisible. Les ombres projet�es par l'objet et re�ues par celui-ci sont rendues. L'image peut ensuite �tre superpos�e sur une autre et les ombres appara�tront dans l'image composite.

![images/building.png](images/building.png)
Dans l'exemple ci-dessus, quelques surfaces planes simples correspondant � l'image ont �t� cr��es afin de recevoir les ombres projet�es sur le b�timent par les arbres. La propri�t� de canal Alpha a �t� attribu�e aux plans afin qu'ils soient invisibles lors du rendu tout en affichant les ombres. Cette image partiellement transparente a ensuite �t� d�pos�e sur l'image.

#### Caustiques
{: #caustics}
Les rayons de lumi�re r�fl�chis ou r�fract�s par un objet courb� ou la projection de ces rayons sur une autre surface. Les caustiques s'utilisent dans des situations tr�s sp�cifiques. Elle ne sont rendues qu'avec le moteur [Path Tracer](render-tab.html#path-tracer) ou [Hybride](render-tab.html#hybrid) Les calculs des caustiques demandent un grand nombre de passes pour donner un r�sultat. Voir l'article de Wikipedia : Caustique (optique)](https://fr.wikipedia.org/wiki/Caustique) pour plus d'informations. 

![images/kaustik.png](images/kaustik.png)
*Les caustiques produites par un verre d'eau.*

![images/caustics-001.png](images/caustics-001.png)
*Sans caustique (gauche) et avec caustiques (droite).*

#### Fin
{: #thin}
Un objet renfermant un espace et transparent est normalement trait� comme un solide pour la r�fraction transparente. La propri�t� Fin permet de traiter chaque surface comme un objet � deux faces pour la r�fraction. C'est le param�tre � utiliser si des surfaces simples comme du verre sont utilis�es pour les mod�les d'architecture. 

![images/thin.png](images/thin.png) ![images/thinoff.png](images/thinoff.png)
*Mod�le de base de Rhino (gauche), normal (milieu) et fin (droite).*

#### Entr�e de lumi�re
{: #daylight-portal}
Une entr�e de lumi�re naturelle est une ouverture laissant entrer l'[�clairage du soleil et du ciel](lighting-tab.html#interior-daylight) dans un rendu int�rieur. Une entr�e de lumi�re envoie la lumi�re du soleil, du ciel et du sol dans un espace int�rieur de fa�on naturelle. Les entr�es de lumi�re n'ont un effet que lorsque le [soleil](sun-and-sky-tabs.html#sun) est activ�. Lorsque le sch�ma d'�clairage [Lumi�re du jour int�rieure](lighting-tab.html#interior-daylight)est utilis�, toutes les surfaces transparentes agissent automatiquement comme des entr�es de lumi�re. En revanche, si vous voulez apporter la lumi�re ext�rieure du soleil et du ciel dans une sc�ne avec un sch�ma d'�clairage Studio ou Ext�rieur, vous devez marquer manuellement les fen�tres comme des entr�es de lumi�re.

![images/daylightportal-001.png](images/daylightportal-001.png)
*Avec entr�e de lumi�re (gauche), sans entr�e de lumi�re (droite).*