
### Masque
Bloque des portions de l'image en fonction d'une valeur de couleur ou d'un canal alpha enregistré dans l'image. Il est ainsi possible d'obtenir des textures avec des bords aux formes complexes et créer des effets tels que des trous dans une surface. 

Dans cet exemple, une image avec un arrière-plan canal alpha est placée sous forme de décalcomanie sur une surface rectangulaire. Les masques des matériaux fonctionnent de la même façon.

![images/airplane.png](images/airplane.png)  ![images/masking-004.png](images/masking-004.png)
*Image de décalcomanie originale. La zone en damier gris représente le canal alpha de l'image.*

Les informations sur le masque peuvent provenir de trois sources dans l'image :

> [Aucun](#nomask)
> [Canal Alpha](#alphamask)
> [Couleur](#colormask)

#### Aucun
{: #nomask}
Sans masque, l'image assombrit le matériau situé en-dessous. Le masque permet de voir le matériau à travers l'image là où se trouve le canal alpha ou la couleur du masque. Le matériau assigné à une surface plane dans cet exemple possède une couleur de base rouge.

![images/masking-002.png](images/masking-002.png)
*Sans masque (gauche), l'image couvre la surface, avec masque (droite), le matériau rouge se voit à travers.*

#### Canal Alpha
{: #alphamask}
Utilise le [canal alpha](environment-tab.html#alpha) de l'image, s'il en existe un, pour définir la zone masquée.

![images/airplane.png](images/airplane.png)  ![images/masking-004.png](images/masking-004.png)
*Original à gauche. La zone en damier gris représente le canal alpha de l'image. À droite se trouve l'image sur une surface d'eau.*

Le canal alpha est une portion de chaque donnée de pixel qui est réservée aux informations sur la transparence. Les canaux alpha créent et stockent des masques qui vous permettent d'isoler et de protéger des parties d'une image pendant que vous appliquez les changements de couleur, les filtres ou d'autres effets sur le reste de l'image. Chaque pixel dans une image est décrit sous forme de canaux de données qui définissent le mélange de rouge, vert et bleu (RVB). Le canal alpha est une représentation en nuances de gris de 8 bits (256 niveaux) de l'image qui est utilisée pour masquer la couleur du pixel sous-jacent. La valeur du masque alpha détermine l'intensité de la couleur du pixel. Si le canal alpha est à 100 %, les pixels seront complètement transparents.  Sinon, les pixels se mélangeront avec la transparence.

#### Couleur
{: #colormask}
Si le canal alpha n'existe pas dans une image, une couleur dans l'image peut être définie comme masque. Il existe également une valeur de sensibilité afin de rendre le masque plus ou moins sensible à une couleur spécifique. Lorsque l'option Couleur est sélectionnée, la pipette, le sélecteur et la sensibilité sont activés. 

#### Pipette
Cliquez pour sélectionner la couleur dans l'image. Cliquez sur la pipette puis sur l'image pour choisir la couleur. Ce contrôle n'est disponible que lorsque l'option Couleur est sélectionnée.

{% include_relative snippets/snippet-material-color-select.md %}

#### Sensibilité
La valeur indique la taille de la zone qui est également masquée autour de la couleur. La sensibilité doit être supérieure à 0 pour que le masque de couleur ait un effet sur l'objet. Ce contrôle n'est disponible que lorsque l'option Couleur est sélectionnée.

#### Flou
Masque partiellement les pixels. La valeur détermine l'importance du masque partiel autour de la couleur masquée. Ce contrôle n'est disponible que lorsque l'option Couleur est sélectionnée.

#### Inverser
Inverse le masque. Les  pixels qui auraient dû être masqués sont maintenant inclus et vice-versa.

![images/masking-007.png](images/masking-007.png)  

#### Transparent
La zone masquée de l'objet sous-jacent est transparente, ainsi les autres objets ou l'arrière-plan se trouvant derrière l'objet peut être vu à travers celui-ci. Normalement, le matériau de l'objet se voit dans cette zone.

Un masque transparent permet d'obtenir une ombre plus naturelle et de voir les objets situés derrière. Le matériau sous-jacent pourrait aussi simplement être transparent mais dans certains cas il est plus intéressant de rendre la surface derrière la décalcomanie transparente et de maintenir les autres zones de la surface opaques.

![images/masking-003.png](images/masking-003.png)    ![images/masking-004.png](images/masking-004.png)

#### Montrer les couleurs masquées
Affiche directement les résultats du masque lorsque les paramètres sont modifiés. Utilisez le [sélecteur de couleur](select-color.html) ![images/colorswatch-001.png](images/colorswatch-001.png) pour changer la couleur d'affichage des pixels masqués. La zone masquée ne change pas lorsque vous changez la couleur d'affichage ou si vous activez ou désactivez la case. Ce n'est qu'un outil de visualisation facilitant la modification du masque.

![images/masking-008.png](images/masking-008.png)