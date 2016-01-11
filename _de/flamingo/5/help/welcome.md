---
title: Erste Schritte mit Flamingo
---


# ![images/flamingotab.svg](images/flamingotab.svg) Erste Schritte mit Flamingo nXt®
Flamingo nXt erzeugt erstklassige und fotorealistische Bild- und Animationsdateien aus 3D-Modellen in Rhinoceros®. Flamingo nXt 5 ist ein Update für Flamingo, das mit den eingebauten Renderfunktionen von Rhino 5 zusammenarbeitet. Die aktuelle Version ist eine Work-in-Progress-Version.

Sie können Flamingo nXt [hier](http://www.rhino3d.com/download/flamingo/5/beta) herunterladen.

An technischen Diskussionen können Sie im [Flamingo-Discourse-Forum](http://discourse.mcneel.com/c/rendering/flamingo) teilnehmen.

## Installation

* Flamingo 5 Beta benötigt die Installation einer früheren Version von Flamingo nXt.
* Rhino 5 Service Release 12 wird für Flamingo nXt 5 ebenfalls benötigt.

Laden Sie das RHI-Installationsprogramm herunter, führen Sie es aus und starten Sie Rhino.

Technischen Support, Tutorials, Beispiele und Informationen über **Flamingo nXt** finden Sie auf der [Flamingo-nXt-Website](http://nxt.flamingo3d.com/).

> [Tutorials](http://nxt.flamingo3d.com/page/tutorials-and-documentation)
> [Galerie](http://nxt.flamingo3d.com/photo)
> [Technischer Support](http://nxt.flamingo3d.com/forum)

## Das Flamingo-nXt-Bedienfenster
{: #control-panel}
Die Benutzeroberfläche dieser Version von Flamingo ist in die Renderwerkzeuge von Rhino 5 integriert. Im Flamingo-nXt-Bedienfenster können Sie in verschiedenen Reitern das Modell für das Rendering konfigurieren:

> [Materialien](materials-tab.html)
> [Beleuchtung](lighting-tab.html)
> [Umgebung](environment-tab.html)
> [Rendern](render-tab.html)

## Zugriff auf das Flamingo-Bedienfenster
* Klicken Sie im Flamingo-nXt-Menü auf **Bedienfenster anzeigen**.

## Rendergrundlagen
{: #rendering-basics}
Das Rendering eines Modells umfasst vier wesentliche Schritte:

 1. [Einrichtung der Materialien](material-editor.html)
 1. [Einrichtung der Beleuchtung](lighting-tab.html)
 1. [Einrichtung einer Umgebung](environment-tab.html)
 1. [Festlegung der Renderbedingungen](render-tab.html)

##### Ein Rendering starten
* Klicken Sie im Menü **Rendern** oder **Flamingo nXt** auf **Rendern**.
* Oder klicken Sie in der Werkzeugleiste **Standard** auf die Schaltfläche **Rendern**.

### Rendering anhalten
Standardmäßig führt der Renderprozess einen Durchgang nach dem anderen durch und verfeinert das Bild dadurch so lange, bis Sie auf die Schaltfläche **Rendering stoppen** klicken. So können Sie einfach zwischen Zeit und Qualität abwägen. Je länger Sie das Rendering laufen lassen, desto mehr nähert es sich seinem vollständig konvergierten Ergebnis an. Sie können ein Rendering jederzeit stoppen.

###  Rendering fortführen
Wenn Sie auf die Schaltfläche **Rendering stoppen** klicken, wird der Renderprozess nach dem aktuellen Durchgang beendet.
Die Schaltfläche wechselt dann auf **Rendering fortführen**. Wenn Sie das Rendering anhalten, bevor die in den Renderbeschränkungen festgelegte maximale Anzahl Durchgänge bzw. Zeitdauer erreicht wurde, können Sie durch Klick auf die Schaltfläche **Rendering fortführen** den Renderprozess fortsetzen.

Verwenden Sie die Einstellung [Anzahl Durchgänge](render-window.html#number-of-passes) oder [Zeit](render-window.html#time) im [Renderfenster](render-window.html) oder unter [Dokumenteigenschaften > Flamingo nXt](documentproperties-flamingo.html), um das Rendering automatisch nach Erfüllung der entsprechenden Vorgabe anhalten zu lassen.