---
title: Canaux
---

# ![images/render.svg](images/render.svg) {{page.title}}
{: #channel}
Flamingo nXt 5 poss�de une fonction tr�s utile qui permet de d�finir des lumi�res sur un des huit canaux disponibles. Chaque source de lumi�re du dessin, y compris le soleil et le ciel peuvent avoir un canal. Au moment du rendu, la lumi�re de chaque canal est plac�e sur son propre calque. Une fois le rendu termin�, l'intensit� des canaux peut �tre ajust�e.  Les modifications sont appliqu�es en temps r�el sans avoir besoin de calculer � nouveau le rendu.  

Les canaux sont tr�s utiles pour�:

 * Essayer d'�quilibrer un environnement HDR et la lumi�re du soleil.  Tous les environnements HDR ne sont pas calibr�s.  Il est donc utile de pouvoir d�finir le ciel HDR sur un canal et le soleil sur un autre.  L'intensit� relative de la lumi�re du soleil par rapport � celle du ciel peut alors �tre ajust�e apr�s le rendu.
 * D�finir des rendus de studio qui utilisent des configurations avec des lumi�res principales, d'appoint et de contre-jour. D�finissez chaque lumi�re sur un canal diff�rent, puis ajustez leur intensit� en temps r�el dans le rendu.
* Utiliser diff�rents ensembles de lumi�res dans un rendu ext�rieur ou int�rieur.  Chaque ensemble de lumi�res peut �tre d�fini sur un canal et poss�der son propre variateur afin de contr�ler son intensit�.
 * Calculer un rendu avec toutes les lumi�res activ�es puis d�sactiver certaines lumi�res. Il n'est pas n�cessaire de calculer plusieurs fois le rendu d'un int�rieur afin de cr�er une prise de vue de nuit et une autre de jours.

Lorsque l'image est rendue, il est possible de modifier chaque canal dans la fen�tre de rendu ou d'enregistrer l'image dans un fichier .nXtImage pour la modifier plus tard.

Utilisez les canaux pour ajuster l'intensit� des lumi�res les unes en fonction des autres, pas pour �claircir toute l'image.  Si vous voulez �claircir toute l'image, utilisez les contr�les de la section Ajuster l'image.

<video id="channelsvideo" src="images/flamingo-lights-onoff.mp4" poster="images/flamingo-lights-onoff.jpg" controls preload></video>
*Cliquez pour voir la vid�o.*

Les conditions suivantes doivent �tre r�unies pour produire et manipuler une image multi-canaux :

 1. Toutes les lumi�res participantes doivent �tre activ�es.
 2. Chaque source de lumi�re doit poss�der un canal. Par d�faut, le soleil et ciel sont li�s au canal 0 alors que les lumi�res artificielles sont d�finies sur le canal 1.
 3. Imm�diatement apr�s le rendu, utilisez les contr�les des canaux dans la fen�tre de rendu.
 3. Le seul format d'enregistrement qui conserve ces informations sur les canaux est le format .nXtImage. L'�clairage peut �tre modifi� dans l'image et celle-ci peut ensuite �tre enregistr�e au format bitmap.

## D�finition des canaux 
{: setting}
Afin de d�finir un rendu avec plusieurs canaux, la premi�re �tape consiste � placer chaque lumi�re sur un canal. Le num�ro du canal est normalement d�fini dans les propri�t�s de chaque lumi�re.  Pour plus d'informations sur d�finir des lumi�res sp�cifiques sur un canal, consultez�:

>[Canal du soleil](sun-and-sky-tabs.html#sun-channel)
>[Canal du ciel](sun-and-sky-tabs.html#sky-channel)
>[Canal de lumi�re artificielle](lights-tab.html#channel)
>[Incandescence de mat�riau](documentproperties-flamingo.html#channel)

Un canal peut poss�der une ou plusieurs lumi�res. Le r�glage du canal est un multiplicateur. L'intensit� relative des lumi�res d'un m�me canal 

## R�glages des canaux 
{: adjusting}
Les canaux d'�clairage peuvent �tre ajust�s imm�diatement apr�s le rendu, ou dans l'�diteur d'images de Flamingo si le rendu est enregistr� dans un fichier nXtImage. Les canaux peuvent �tre ajust�s alors que Flamingo continue le rendu, mais nous recommandons d'arr�ter le rendu avant de r�aliser des ajustements importants. 

#### O� puis-je trouver les contr�les d'�clairage de Flamingo ?
Les contr�les des canaux se trouvent dans l'onglet Flamingo nXt de la [fen�tre de rendu](render-window.html), dans la section Canaux. 

Huit contr�les sont disponibles (de 0 � 7). Seuls les canaux poss�dant des lumi�res sont activ�s. 

![images/channel-slider.png](images/channel-slider.png)
Chaque canal dispose d'un glisseur et d'un compteur. Le compteur repr�sente la valeur maximale du glisseur. Si le glisseur est � droite, toute la valeur du compteur est utilis�e pour multiplier les quantit�s d'�clairage sur ce canal. De m�me, si le glisseur est � 50�%, l'�clairage de ce canal sera multipli� par la moiti� de la valeur du compteur. Lorsque le glisseur est enti�rement � gauche, l'�clairage de ce canal est d�sactiv�. 

La valeur du compteur peut �tre tr�s importante. Le soleil et le ciel sont souvent beaucoup plus lumineux que les lumi�res artificielles, la valeur du compteur des lumi�res artificielles peut alors avoir besoin d'�tre augment�e � 20 ou 50 pour voir une diff�rence. 

Apr�s avoir ajust� les canaux, enregistrez l'image dans un fichier JPG ou PNG afin de conserver le rendu final. 