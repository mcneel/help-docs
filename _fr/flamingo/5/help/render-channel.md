---
title: Canaux
---

# ![images/render.svg](images/render.svg) {{page.title}}
{: #channel}
Flamingo nXt 5 possède une fonction très utile qui permet de définir des lumières sur un des huit canaux disponibles. Chaque source de lumière du dessin, y compris le soleil et le ciel peuvent avoir un canal. Au moment du rendu, la lumière de chaque canal est placée sur son propre calque. Une fois le rendu terminé, l'intensité des canaux peut être ajustée.  Les modifications sont appliquées en temps réel sans avoir besoin de calculer à nouveau le rendu.  

Les canaux sont très utiles pour :

 * Essayer d'équilibrer un environnement HDR et la lumière du soleil.  Tous les environnements HDR ne sont pas calibrés.  Il est donc utile de pouvoir définir le ciel HDR sur un canal et le soleil sur un autre.  L'intensité relative de la lumière du soleil par rapport à celle du ciel peut alors être ajustée après le rendu.
 * Définir des rendus de studio qui utilisent des configurations avec des lumières principales, d'appoint et de contre-jour. Définissez chaque lumière sur un canal différent, puis ajustez leur intensité en temps réel dans le rendu.
* Utiliser différents ensembles de lumières dans un rendu extérieur ou intérieur.  Chaque ensemble de lumières peut être défini sur un canal et posséder son propre variateur afin de contrôler son intensité.
 * Calculer un rendu avec toutes les lumières activées puis désactiver certaines lumières. Il n'est pas nécessaire de calculer plusieurs fois le rendu d'un intérieur afin de créer une prise de vue de nuit et une autre de jour.

Lorsque l'image est rendue, il est possible de modifier chaque canal dans la fenêtre de rendu ou d'enregistrer l'image dans un fichier .nXtImage pour la modifier plus tard.

Utilisez les canaux pour ajuster l'intensité des lumières les unes en fonction des autres, pas pour éclaircir toute l'image.  Si vous voulez éclaircir toute l'image, utilisez les contrôles de la section Ajuster l'image.

<video id="channelsvideo" src="images/flamingo-lights-onoff.mp4" poster="images/flamingo-lights-onoff.jpg" controls preload></video>
*Cliquez pour voir la vidéo.*

Les conditions suivantes doivent être réunies pour produire et manipuler une image multi-canaux :

 1. Toutes les lumières participantes doivent être activées.
 2. Chaque source de lumière doit posséder un canal. Par défaut, le soleil et ciel sont liés au canal 0 alors que les lumières artificielles sont définies sur le canal 1.
 3. Immédiatement après le rendu, utilisez les contrôles des canaux dans la fenêtre de rendu.
 3. Le seul format d'enregistrement qui conserve ces informations sur les canaux est le format .nXtImage. L'éclairage peut être modifié dans l'image et celle-ci peut ensuite être enregistrée au format bitmap.

## Définition des canaux 
{: setting}
Afin de définir un rendu avec plusieurs canaux, la première étape consiste à placer chaque lumière sur un canal. Le numéro du canal est normalement défini dans les propriétés de chaque lumière.  Pour plus d'informations sur comment définir des lumières spécifiques sur un canal, consultez :

>[Canal du soleil](sun-and-sky-tabs.html#sun-channel)
>[Canal du ciel](sun-and-sky-tabs.html#sky-channel)
>[Canal de lumière artificielle](lights-tab.html#channel)
>[Incandescence de matériau](documentproperties-flamingo.html#channel)

Un canal peut posséder une ou plusieurs lumières. Le réglage du canal est un multiplicateur. Les lumières se trouvant sur un même canal conserveront leurs intensités relatives les unes aux autres lorsqu'elles seront ajustées. 

## Réglages des canaux 
{: adjusting}
Les canaux d'éclairage peuvent être ajustés immédiatement après le rendu, ou dans l'éditeur d'images de Flamingo si le rendu est enregistré dans un fichier nXtImage. Les canaux peuvent être ajustés alors que Flamingo continue le rendu, mais nous recommandons d'arrêter le rendu avant de réaliser des ajustements importants. 

#### Où puis-je trouver les contrôles d'éclairage de Flamingo ?
Les contrôles des canaux se trouvent dans l'onglet Flamingo nXt de la [fenêtre de rendu](render-window.html), dans la section Canaux. 

Huit contrôles sont disponibles (de 0 à 7). Seuls les canaux possédant des lumières sont activés. 

![images/channel-slider.png](images/channel-slider.png)
Chaque canal dispose d'un glisseur et d'un compteur. Le compteur représente la valeur maximale du glisseur. Si le glisseur est à droite, toute la valeur du compteur est utilisée pour multiplier les quantités d'éclairage sur ce canal. De même, si le glisseur est à 50 %, l'éclairage de ce canal sera multiplié par la moitié de la valeur du compteur. Lorsque le glisseur est entièrement à gauche, l'éclairage de ce canal est désactivé. 

La valeur du compteur peut être très importante. Le soleil et le ciel sont souvent beaucoup plus lumineux que les lumières artificielles, la valeur du compteur des lumières artificielles peut alors avoir besoin d'être augmentée à 20 ou 50 pour voir une différence. 

Après avoir ajusté les canaux, enregistrez l'image dans un fichier JPG ou PNG afin de conserver le rendu final. 