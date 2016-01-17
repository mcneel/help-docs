---
title: Materialzuweisung
---

# ![images/paint.svg](images/paint.svg) {{page.title}}
Objekte in der Szene haben eine Materialquelle. Von dort beziehen sie ihr Rendermaterial.  Materialien können auf verschiedene Arten zugewiesen werden. Die verwendete Methode hat einen großen Einfluss darauf, wie einfach das Modell geändert und gepflegt werden kann.

Materialien können auf drei verschiedene Arten zugewiesen werden. Die drei Methoden stellen eine Hierarchie dar, so dass eine Zuweisung weiter unten auf der Liste eine Zuweisung weiter oben überschreibt. Folgende Methoden sind verfügbar:

 1. [Nach Ebene](#bylayer) - Allen Objekten einer bestimmten Ebene wird das entsprechende Material zugewiesen, wenn sie nicht in einem Block gebunden sind oder ihnen ein spezifisches Material auf Objektebene zugewiesen wurde.
 2. [Nach übergeordnet](#byparent) - Dies wird für Objekte in Blöcken verwendet.  Objekte mit diesem Zuweisungstyp leiten ihr Material aus der entsprechenden Blockdefinition ab.
 3. [Nach Objekt](#byobject) - Materialien können einem Objekt direkt zugewiesen werden, wobei alle anderen Materialzuweisungen überschrieben werden.

Die empfohlene Methode ist die Zuweisung nach Ebene. Dadurch ist es sehr einfach, das Material für alle Objekte einer Ebene auf einmal zu ändern. Verwenden Sie die Zuweisung nach Objekt nur dann, wenn Sie nur einige wenige Objekte haben, die nicht auf separaten Ebenen liegen sollen.

Die Zuweisungsmethode bei importierten Dateien kann je nach Typ variieren. Viele importierte Dateien verfügen über eine Materialzuweisung nach Objekt.  Es kann viel Arbeit bedeuten, den Zuweisungstyp eines Modells auf *Nach Ebene* zu ändern, aber es kann sich lohnen, wenn größere Änderungen am Rendermaterial geplant sind.

Wenn ein Material zugewiesen wurde, wird es im aktuellen Modell gespeichert.  Eine Änderung an diesem Material hat dementsprechend keine Auswirkungen auf andere Modelle.

## Materialzuweisung nach Ebene
{: #bylayer}
Die Materialzuordnung nach Ebene ordnet allen Objekten dieser Ebene ein bestimmtes Material zu. Dies ist die Standardmethode zur Materialzuweisung. Das Material einer Ebene können Sie im Dialogfeld [Ebenen](http://docs.mcneel.com/rhino/5/help/de-de/commands/layer.htm) ändern.
Hinweis: Beim Löschen eines Materials aus dem [Materialeditor](material-editor.html) wird der Zuweisungstyp für alle Objekte, denen das Material zugewiesen war, auf *Nach Ebene* zurückgesetzt.

##### Drag & Drop eines Materials auf eine Ebene
{: #drag-dropmaterialtolayer}
1. Öffnen Sie in Rhino das Dialogfeld [Ebenen](http://docs.mcneel.com/rhino/5/help/de-de/commands/layer.htm).
1. Ziehen Sie ein Material aus der [Liste der Materialien](material-editor.html#material_list) im Materialien- oder Bibliotheken-Reiter auf eine Ebene im [Ebenenpanel](http://docs.mcneel.com/rhino/5/help/de-de/commands/layer.htm).

##### Zuweisung eines Materials zu einer Ebene
1. Öffnen Sie in Rhino das Dialogfeld [Ebenen](http://docs.mcneel.com/rhino/5/help/de-de/commands/layer.htm).
1. Wählen Sie einen oder mehrere Ebenennamen aus und klicken Sie auf die Spalte Material.
1. Wählen Sie im Dialogfenster *Ebenenmaterial* ein Material aus der Dropdownliste aus.

##### Entfernen eines Materials von einer Ebene
{: #detachmaterialfromlayer}
1. Öffnen Sie in Rhino das Dialogfeld [Ebenen](http://docs.mcneel.com/rhino/5/help/de-de/commands/layer.htm).
1. Wählen Sie einen oder mehrere Ebenennamen aus und klicken Sie auf die Spalte Material.
1. Wählen Sie im Ebenenmaterial-Dialog das Standardmaterial aus der Dropdownliste aus.

## Materialzuweisung nach übergeordnetem Element
{: #byparent}
Die Materialzuweisung nach übergeordnetem Element ist eine selten verwendete, aber für spezielle Fälle sehr hilfreiche Methode. Objekte einer Blockinstanz behalten normalerweise ihren Zuweisungstyp nach Ebene bzw. Objekt.  Wenn ihnen das Material basierend auf dem übergeordneten Element zugewiesen wird, erhalten sie das Material von ihrem Block.  So können Objekte einer Blockinstanz das Material des übergeordneten Blocks übernehmen.

Bei der Modellierung eines Autos beispielsweise befinden sich die Reifen auf der Reifen-Ebene und die Räder auf der Räder-Ebene. Das Rendering der Karosserie ist jedoch möglicherweise für einzelne Blockinstanzen unterschiedlich.  Dies kann durch Einstellung des Zuweisungstyps *Nach übergeordnet* für die Karosserie erreicht werden.  Anschließend kann einer Blockinstanz ein Material zugewiesen werden, das dann nur von der Karosserie übernommen wird.

##### Zuweisung eines Materials über die Objekteigenschaften
1. Wählen Sie Objekte aus.
1. Öffnen Sie die **Objekteigenschaften** ![images/properties.png](images/properties.png).
1. Wählen Sie in den [Objekteigenschaften](properties-object.html) auf der Seite **Material** ![images/materialtab.png](images/materialtab.png) im Dropdownmenü *Material zuordnen nach* die Option *Nach übergeordnet* aus.

## Materialzuweisung nach Objekt
{: #byobject}
Die Materialien der Materialbibliotheken können einer Ebene oder einem Objekt zugewiesen werden. Rendermaterialien werden einzelnen Objekten zugewiesen und von Rhinos integriertem Renderer verwendet.
Weitere Infos finden Sie im Hilfethema zum [Materialeditor](material-editor.html).

Die empfohlene Methode ist die Zuweisung nach Ebene. Ordnen Sie Materialien nach Objekt zu, wenn Sie nur einige wenige Objekte haben, die nicht auf separaten Ebenen liegen sollen.

##### Zuweisung eines Materials über die Objekteigenschaften
1. Wählen Sie Objekte aus.
1. Öffnen Sie die **Objekteigenschaften** ![images/properties.png](images/properties.png).
1. Wählen Sie in den [Objekteigenschaften](properties-object.html) auf der Seite **Material** ![images/materialtab.png](images/materialtab.png) im Dropdownmenü *Material zuordnen nach* die Option *Nach übergeordnet* aus und klicken Sie anschließend auf das gewünschte Material.

##### Drag & Drop eines Materials auf ein Objekt
{: #drag-dropmaterialtoobject}

 * Ziehen Sie ein Material aus der [Liste der Materialien](material-editor.html#material_list) im Materialien- oder Bibliotheken-Reiter auf ein Objekt. Das Objekt wird hervorgehoben, wenn sich das Material an der richtigen Stelle befindet.

##### Zuweisung eines Materials zu ausgewählten Objekten
1. Wählen Sie Objekte aus.
1. Klicken Sie mit der rechten Maustaste auf ein Material aus der [Liste der Materialien](material-editor.html#material_list) im Materialien- oder Bibliotheken-Reiter.
1. Wählen Sie im Kontextmenü den Eintrag *Der Auswahl zuordnen*.

##### Objekte mit Materialzuweisung auswählen
{: #select-objects-with-material-assignment}
1. Klicken Sie mit der rechten Maustaste auf ein Material aus der [Liste der Materialien](material-editor.html#material_list) im Materialien- oder Bibliotheken-Reiter.
1. Wählen Sie im Kontextmenü den Eintrag *Objekt(e) auswählen*.

##### Entfernen einer Materialzuweisung nach Objekt
{: #removematerialfromobject}
1. Wählen Sie Objekte aus.
1. Öffnen Sie die **Objekteigenschaften**.
1. Wählen Sie in den [Objekteigenschaften](properties-object.html) auf der Seite **Material** im Dropdownmenü *Material zuordnen nach* die Option *Nach Ebene* aus.