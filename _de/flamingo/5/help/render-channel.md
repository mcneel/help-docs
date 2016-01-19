---
title: Kanäle
---

# ![images/render.svg](images/render.svg) {{page.title}}
{: #channel}
Ein sehr nützliches Feature von Flamingo nXt 5 ist die Möglichkeit zur Organisation der Lichter in acht Kanälen. Jede Lichtquelle in der Zeichnung einschließlich Sonne und Himmel kann einem Kanal zugeordnet werden. Beim Rendern wird das Licht eines Kanals auf eine eigene Ebene gesetzt.  So kann die Intensität eines Kanals nach Abschluss des Renderings angepasst werden.  Die Änderung wird in Echtzeit und ohne erneutes Rendering vorgenommen.  

Kanäle sind besonders für die folgenden Fälle nützlich:

* Ausbalancierung einer HDRI-Umgebung und des Sonnenlichts.  Nicht alle HDRI-Umgebungen sind kalibriert.  Es ist sinnvoll, den HDRI-Himmel auf einen anderen Kanal zu setzen als die Sonne.  Dann kann die relative Intensität des Himmelslichts gegenüber der Sonne nach dem Rendering angepasst werden.
* Studio-Renderings mit einer Dreipunktbeleuchtung. Setzen Sie jedes Licht auf einen anderen Kanal und passen Sie ihre Intensität nach dem Rendering in Echtzeit an.
* Bei der Verwendung mehrerer Reihen von Lichtern in einem Innen- oder Außenrendering.  Jede Lichtreihe kann auf einen anderen Kanal gesetzt werden und hat so einen eigenen Dimmer zur Einstellung der Intensität.
* Rendering mit allen Lichtern und anschließendem Ein- und Ausschalten bestimmter Lichter. So müssen für eine Nacht- und eine Tagesansicht keine zwei verschiedenen Bilder gerendert werden.

Nach dem Rendern des Bilds kann jeder Kanal vor dem Speichern im Renderfenster einzeln skaliert werden. Eine andere Möglichkeit ist das Speichern des Bilds als nXtImage-Datei zur späteren Bearbeitung.

Verwenden Sie dabei die Kanäle zur Anpassung der Intensität der Lichtquellen untereinander und nicht, um das ganze Bild aufzuhellen.  Wenn Sie das ganze Bild auf einmal heller einstellen möchten, verwenden Sie dazu die Option *Bild anpassen*.

<video id="channelsvideo" src="images/flamingo-lights-onoff.mp4" poster="images/flamingo-lights-onoff.jpg" controls preload></video>
*Zum Abspielen des Videos klicken*

Die folgenden Bedingungen sind nötig, um ein Mehrkanalbild zu erzeugen und zu ändern:

 1. Alle beteiligten Lichter müssen aktiviert sein.
 2. Jeder Lichtquelle muss ein Kanal zugeordnet sein. Sonne und Himmel sind standardmäßig auf Kanal 0 gesetzt, künstliche Lichter auf Kanal 1.
 3. Verwenden Sie nach dem Rendern die Kanalsteuerung im Renderfenster.
 3. Das nXtImage-Format ist das einzige, das diese Kanalinformation speichert. Die Beleuchtung kann angepasst und das Bild anschließend in einem Bitmap-Format gespeichert werden.

## Einstellung der Kanäle
{: setting}
Der erste Schritt zur Einstellung eines Mehrkanal-Renderings ist die Zuordnung der Lichter zu einem Kanal. Die Kanalnummer wird normalerweise in den Lichteigenschaften eingestellt.  Weitere Informationen zur Einstellung des Kanals für spezifische Lichter:

>[Sonnenkanal](sun-and-sky-tabs.html#sun-channel)
>[Himmelskanal](sun-and-sky-tabs.html#sky-channel)
>[Kanal für künstliche Beleuchtung](lights-tab.html#channel)
>[Material-Leuchtkanal](documentproperties-flamingo.html#channel)

Einem Lichtkanal kann eine beliebige Anzahl Lichter zugeordnet werden.  Die Kanalanpassung ist ein Multiplikator. Lichter auf demselben Kanal behalten bei einer Anpassung des Kanals ihre relative Intensität zueinander bei.

## Anpassung der Kanäle
{: adjusting}
Die Beleuchtungskanäle können direkt nach dem Rendering oder im Flamingo-Bildeditor angepasst werden, wenn das Rendering als nXtImage-Datei gespeichert wurde.  Kanäle können bereits während des Rendervorgangs angepasst werden, es wird aber empfohlen, das Rendering anzuhalten, bevor Sie größere Anpassungen durchführen.

#### Wo befindet sich die Flamingo-Beleuchtungssteuerung?
Die Kanalsteuerung befindet sich im Flamingo-nXt-Reiter im [Renderfenster](render-window.html) unter *Kanäle*.

Die acht Kanäle tragen die Nummern 0-7. Es sind nur diejenigen Kanäle aktiv, denen Lichter zugeordnet sind.

![images/channel-slider.png](images/channel-slider.png)
Jeder Kanal verfügt über einen Schieberegler und einen Zahlenwert.  Mit dem Zahlenfeld kann der maximale Wert für den Schieberegler eingestellt werden. Wenn sich der Schieberegler ganz rechts befindet, wird der im Zahlenfeld eingestellte Wert verwendet, um die Beleuchtungsintensität dieses Kanals zu multiplizieren.  Dementsprechend wird die Beleuchtung eines Kanals bei einer Mittelstellung des Schiebereglers um den halben Betrag des angegebenen Werts multipliziert.  Wenn sich der Schieberegler ganz links befindet, werden alle Lichter auf dem entsprechenden Kanal deaktiviert.

Der eingestellte Zahlenwert kann äußerst wichtig sein.  Da Sonne und Himmel um ein Vielfaches heller sein können als künstliche Lichter, kann für letztere eine Erhöhung auf einen Wert von 20 oder 50 nötig sein, damit ein Unterschied sichtbar wird.

Speichern Sie nach dem Anpassen der Kanäle das Bild als JPG- oder PNG-Datei ab.