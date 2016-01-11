
### Masque
Bloque des portions de l'image en fonction d'une valeur de couleur ou d'un canal alpha enregistr� dans l'image. Il est ainsi possible d'obtenir des textures avec des bords aux formes complexes et cr�er des effets tels que des trous dans une surface. 

Dans cet exemple, une image avec un arri�re-plan canal alpha est plac�e sous forme de d�calcomanie sur une surface rectangulaire. Les masques des mat�riaux fonctionnent de la m�me fa�on.

![images/airplane.png](images/airplane.png)  ![images/masking-004.png](images/masking-004.png)
*Image de d�calcomanie originale. La zone en damier gris repr�sente le canal alpha de l'image.*

Les informations sur le masque peuvent provenir de trois sources dans l'image�:

> [Aucun](#nomask)
> [Canal Alpha](#alphamask)
> [Couleur](#colormask)

#### Aucun
{: #nomask}
Sans masque, l'image assombrit le mat�riau situ� en-dessous. Le masque permet de voir le mat�riau � travers l'image l� o� se trouve le canal alpha ou la couleur du masque. Le mat�riau assign� � une surface plane dans cet exemple poss�de une couleur de base rouge.

![images/masking-002.png](images/masking-002.png)
*Sans masque (gauche), l'image couvre la surface, avec masque (droite), le mat�riau rouge se voit � travers.*

#### Canal Alpha
{: #alphamask}
Utilise le [canal alpha](environment-tab.html#alpha) de l'image, s'il en existe un, pour d�finir la zone masqu�e.

![images/airplane.png](images/airplane.png)  ![images/masking-004.png](images/masking-004.png)
*Original � gauche. La zone en damier gris repr�sente le canal alpha de l'image. � droite se trouve l'image sur une surface d'eau.*

Le canal alpha est une portion de chaque donn�e de pixel qui est r�serv�e aux informations sur la transparence. Les canaux alpha cr�ent et stockent des masque qui vous permettent d'isoler et de prot�ger des parties d'une image pendant que vous appliquez les changements de couleur, les filtres ou d'autres effets sur le reste de l'image. Chaque pixel dans une image est d�crit sous forme de canaux de donn�es qui d�finissent le m�lange de rouge, vert et bleu (RVB). Le canal alpha est une repr�sentation en nuances de gris de 8 bits (256 niveaux) de l'image qui est utilis�e pour masquer la couleur du pixel sous-jacent. La valeur du masque alpha d�termine l'intensit� de la couleur du pixel. Si le canal alpha est � 100�%, les pixels seront compl�tement transparents.  Sinon, les pixels se m�langeront avec la transparence.

#### Couleur
{: #colormask}
Si le canal alpha n'existe pas dans un image, une couleur dans l'image peut �tre d�finie comme masque. Il existe �galement une valeur de sensibilit� afin de rendre le masque plus ou moins sensible � une couleur sp�cifique. Lorsque l'option Couleur est s�lectionn�e, la pipette, le s�lecteur et la sensibilit� sont activ�s. 

#### Pipette
Cliquez pour s�lectionner la couleur dans l'image. Cliquez sur la pipette puis sur l'image pour choisir la couleur. Ce contr�le n'est disponible que lorsque l'option Couleur est s�lectionn�e.

{% include_relative snippets/snippet-material-color-select.md %}

#### Sensibilit�
La valeur indique la taille de la zone qui est �galement masqu�e autour de la couleur. La sensibilit� doit �tre sup�rieure � 0 pour que le masque de couleur ait un effet sur l'objet. Ce contr�le n'est disponible que lorsque l'option Couleur est s�lectionn�e.

#### Flou
Masque partiellement les pixels. La valeur d�termine l'importance du masque partiel autour de la couleur masqu�e. Ce contr�le n'est disponible que lorsque l'option Couleur est s�lectionn�e.

#### Inverser
Inverse le masque. Les  pixels qui auraient d� �tre masqu�s sont maintenant inclus et vice-versa.

![images/masking-007.png](images/masking-007.png)  

#### Transparent
La zone masqu�e de l'objet sous-jacent est transparente, ainsi les autres objets ou l'arri�re-plan se trouvant derri�re l'objet peut �tre vu � travers celui-ci. Normalement, le mat�riau de l'objet se voit dans cette zone.

Un masque transparent permet d'obtenir une ombre plus naturelle et de voir les objets situ�s derri�re. Le mat�riau sous-jacent pourrait aussi simplement �tre transparent mais dans certains cas il est plus int�ressant de rendre la surface derri�re la d�calcomanie transparente et de maintenir les autres zones de la surface opaques.

![images/masking-003.png](images/masking-003.png)    ![images/masking-004.png](images/masking-004.png)

#### Montrer les couleurs masqu�es
Affiche directement les r�sultats du masque lorsque les param�tres sont modifi�s. Utilisez le [s�lecteur de couleur](select-color.html) ![images/colorswatch-001.png](images/colorswatch-001.png) pour changer la couleur d'affichage des pixels masqu�s. La zone masqu�e ne change pas lorsque vous changez la couleur d'affichage ou si vous activez ou d�sactivez la case. Ce n'est qu'un outil de visualisation facilitant la modification du masque.

![images/masking-008.png](images/masking-008.png)