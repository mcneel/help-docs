---
title: Bibliotheken-Panel
---

# ![images/libraries.svg](images/libraries.svg){: .inline} {{page.title}}
Mit dem Befehl Bibliotheken kann das Bibliotheken-Panel geöffnet werden, um Material-, Textur- und Umgebungsbibliotheken zu verwalten.

Renderinhalt kann in Dateien gespeichert werden, die dann externe Bibliotheken erzeugen und zwischen Modellen verwendet werden können. Inhalt kann auch in andere Rhino-Sitzungen oder einen Ordner gezogen werden.

Farbräder können auf die gleiche Art und Weise per Drag&Drop abgelegt werden.

Im Bibliotheken-Panel werden die Ordner mit den angelegten Bibliotheken angezeigt. Sie können damit Inhalt per Drag&Drop in das Modell ziehen oder Dokumenteninhalt an einem Ort außerhalb des Modells speichern.

Materialien sind Dateien auf Ihrer Festplatte.  Bibliotheksordner sind normale Windows-Ordner.  Sie können diese Ordner kopieren, einfügen und verschieben, wie Sie es mit jedem anderen Windows-Ordner tun würden.

In der Adresszeile im oberen Bereich des Bibliothekenreiters können Sie den Ort eines Ordners auf Ihrem Computer eingeben.

Um wieder schnell zurück zum Standardordner zu gelangen, verwenden Sie die Schaltfläche mit dem Schraubenschlüssel im oberen rechten Bereich. ![images/library_default.png](images/library_default.png){: .inline}

#### Organisation der Bibliotheken
{: organizing_libraries}
Bibliotheken sind einfache Dateien, die Sie kopieren, einfügen und in Ihren Ordnern verschieben können. Verwenden Sie den Windows Explorer, um die Ordner und Dokumente zu bearbeiten. In den [Bibliothekseinstellungen](#settings) ![images/library_default.png](images/library_default.png){: .inline} können Sie festlegen, welche Ordner standardmäßig angezeigt werden.

## Materialbibliothek
{: #material}
Materialien sind Dateien auf Ihrer Festplatte.  Wenn ein Material einem Modell zugewiesen wurde, wird es im Modell gespeichert.  Änderungen am zugewiesenen Material haben keinen Einfluss auf das Originalmaterial auf der Festplatte.

Materialien können einem Modell per Drag&Drop zugewiesen werden. Für die Zuweisung eines Materials gibt es mehrere Möglichkeiten:

#### Zuweisung nach Ebene
Ziehen Sie dazu ein Material direkt auf den Ebenennamen im Ebenenpanel. Diese Methode ist empfehlenswert, da so allen Objekten auf der Ebene das entsprechende Material zugewiesen wird. Wenn das Material später geändert werden soll, kann einfach ein neues Material auf der Ebene abgelegt werden.

#### Zuweisung nach Objekt
Ziehen Sie dazu ein Material direkt auf ein Objekt in einem beliebigen Ansichtsfenster. Dadurch wird die Zuweisung *nach Ebene* überschrieben und das Material *nach Objekt* zugewiesen.

#### Zuweisung nach Block
Ziehen Sie dazu ein Material auf einen Block. Dadurch wird allen Objekten des Blocks mit der Definition *Nach übergeordnet* dieses Material zugewiesen.  Alle Objekte im Block mit einer Materialquelle *Nach übergeordnet* übernehmen das Material des Blocks.

## Pflanzenbibliothek
{: #plant}
Im Standard-Bibliotheksordner gibt es einen Pflanzenordner.  Von hier aus können Sie Pflanzen ins Modell einfügen.  Wenn eine Pflanze im Modell platziert wird, wird sie im Modell gespeichert. Änderungen an einer zugewiesenen Pflanze hat keinen Einfluss auf die Originalpflanze auf der Festplatte. Pflanzen können per Drag&Drop in ein Ansichtsfenster im Modell platziert werden. Weitere Informationen finden Sie im Hilfethema zu [Pflanzen](plants.html).

## Umgebungsbibliothek
{: #environment}
Umgebungen können in der Bibliothek gespeichert werden.  Dadurch können Umgebungseinstellungen von einem Modell in ein anderes kopiert werden.  Weitere Infos finden Sie im Hilfethema zu [Umgebungen](environment-tab.html).

## Bibliothekseinstellungen
{: #settings}
In den ![images/options.png](images/options.png){: .inline} Bibliotheksoptionen können die Standardeinstellungen der Bibliothek im Menü ![images/library_default.png](images/library_default.png){: .inline} eingestellt werden.

##### Wo befindet sich dieser Befehl?
Es gibt drei Möglichkeiten zum Öffnen der Bibliotheksoptionen.

 1. Bibliotheken-Reiter > ![images/library_default.png](images/library_default.png){: .inline} im oberen rechten Bereich des Bibliotheken-Panels > Einstellungen...
 1. Rhino-Menü > Werkzeuge > Optionen > Bibliotheken
 1. Menü > Panels > Bibliotheken.


### Renderinhalt anzeigen
Mit dieser Option können Sie den Standardordner des Renderinhalts anzeigen oder ausblenden.

#### Standardmäßige Bibliotheksstandorte verwenden (Eigene Dokumente)
Die [Inhaltsbibliotheken](libraries.html) befinden sich standardmäßig in einem Unterordner des Ordners *Eigene Dokumente*.

#### Benutzerdefiniert
Zur Einstellung eines benutzerdefinierten Orts für die [Bibliotheken](libraries.html).  Dadurch wird der Standardordner der [Inhaltsbibliotheken](libraries.html) für diesen Computer geändert.

##### Schaltfläche Durchsuchen
Öffnet einen Dateibrowser, um die Datei anzugeben.

#### Den Ordner "Dokumente" anzeigen
Im [Bibliotheken-Panel](libraries.html) wird der angegebene Dokumentenordner im Menü angezeigt.

#### Benutzerdefinierte Ordner anzeigen
Zur Anzeige benutzerdefinierter Ordner im Menü des [Bibliotheken-Panels](libraries.html).