---
title: Materialeditor-Panel
---

# ![images/paint.svg](images/paint.svg) {{page.title}}
Materialien enthalten die Spezifikationen für Farbe, Reflexionsvermögen, Transparenz, Texturen und Bump-Maps eines Flächen-Finish. Alle Materialien verfügen über Grundeinstellungen. Das Standardmaterial ist weiß und matt, ohne Reflexionsvermögen oder Transparenz. Die besten Resultate erzielen Sie mit Flamingo-spezifischen Materialien.

Materialien können Ebenen, Objekten und Blöcken zugewiesen werden. Diese Zuweisungen können durch Drag&Drop auf Objekte oder verschiedene Steuerelemente definiert werden. Weitere Informationen finden Sie im Hilfethema zur [Materialzuweisung](material_assignment.html).

Nach der Zuweisung werden Materialien im Modell gespeichert. Mit den korrekt eingestellten [Rendering-Optionen](http://docs.mcneel.com/rhino/5/help/de-de/index.htm#options/rendering.htm) können das Material, die Texturen und alle Render-Unterstützungsdateien im Rhino-Modell gespeichert werden.

Materialien, Umgebungen und Texturen werden im Modell gespeichert, der Renderinhalt kann aber auch in Dateien gespeichert werden, die von mehreren Modellen gemeinsam genutzt werden. Der Inhalt kann zwischen Rhino-Sitzungen und in einen Ordner gezogen werden. Farbräder können auf die gleiche Art und Weise per Drag&Drop abgelegt werden. Das [Bibliotheken-Panel](libraries.html) zeigt den standardmäßigen Inhaltsordner an. Verwenden Sie dies, um Inhalt in das Modell zu ziehen und abzulegen oder um Modellinhalt in eine externe Datei zu ziehen und abzulegen.

![images/material_editor_panel.svg](images/material_editor_panel.svg){:  #panel_map .float-img-right}

##### Wo befindet sich dieser Befehl?
Auf den Materialreiter können Sie auf mehrere Arten zugreifen.

* ![images/materialtab.png](images/materialtab.png) Materialreiter
* ![images/icon-render.png](images/icon-render.png) Werkzeugleiste Rendern > ![images/materialtab.png](images/materialtab.png) Materialeditor
* Menü > Rendern > Materialeditor
* Durch Eingabe des Befehls Materialeditor in der Befehlszeile

Das Materialeditor-Panel ist in mehrere Abschnitte unterteilt.  Je nach Materialtyp werden andere erweiterte Optionen angezeigt.

Farben und Texturen können per Drag&Drop aus dem Farbenrad in ein anderes Farbenrad oder eine sonstigen Steuerung im Materialeditor, der [Texturenpalette](texturepalette.html) oder dem [Umgebungseditor](environmenteditor.html) gezogen werden.

##### Material-Panel

 1. [Einstellungsleiste](#Einstellungen)
 1. [Liste der Materialien](#material_list)
 1. [Fensterteiler](#divider)
 1. [Materialeigenschaften](#properties)
 1. [Name](#name)
 1. [Materialeigenschaften-Panels](#panels)

## [Einstellungsleiste](#panel_map) ![images/callout_1.svg](images/callout_1.svg)
{: #settings .clear-img}
In dieser Leiste können Sie durch die Liste der Materialien navigieren.

#### ![images/met_leftarrow.png](images/met-leftarrow.png) Pfeil zurück
Zum Zurückblättern durch das aktuelle Material oder die bereits vorher ausgewählten Materialien.  Materialien mit Texturen haben beispielsweise mehrere Ebenen.  Mit diesem Pfeil können Sie von den Texturdetails zum übergeordneten Material zurückkehren.

####  ![images/met_rightarrow.png](images/met-rightarrow.png) Pfeil vorwärts
Zum Vorwärtsblättern durch das aktuelle Material oder die bereits vorher ausgewählten Materialien.  Materialien mit Texturen haben beispielsweise mehrere Ebenen.  Mit diesem Pfeil können Sie vom übergeordneten Material zur zuletzt verwendeten Textur zurückkehren.


#### ![images/material_editor.png](images/material_editor.png)![images/texture-2dchecker.png](images/texture-2dchecker.png) Aktuell ausgewählter Materialname
Zeigt den Namen und die Ebene des aktuellen Materials an.  Wenn beispielsweise eine Textur oder eine prozedurale Materialebene vorhanden ist, wird ein ">" angezeigt. Hier können Sie nachsehen, in welchem Bereich eines Materials sich der Editor befindet.

#### ![images/library_default.png](images/library_default.png) Werkzeugmenü
Zeigt das [Werkzeugmenü](#tools-menu) an.  Dies ist ein umfassendes Menü mit Befehlen, Einstellungsmöglichkeiten und Werkzeugen für Materialien.


## [Liste der Materialien](#panel_map) ![images/callout_2.svg](images/callout_2.svg)
{: #material_list}
Die Liste aller im Modell verwendeten Materialien. Funktionen dieser Liste:

* Sie können durch die Liste scrollen und sich so alle Materialien im Modell ansehen.
* Sie können ein Material dieser Liste per Drag&Drop auf eine Ebene im [Ebenenpanel](http://docs.mcneel.com/rhino/5/help/de-de/index.htm#commands/layer.htm) oder direkt auf ein Objekt ziehen, um es zuzuweisen. Weitere Informationen finden Sie im Hilfethema zur [Materialzuweisung](material_assignment.html).
* Durch Klick auf die Plus-Schaltfläche ![images/add_material.png](images/add_material.png) am Ende der Liste kann ein neues Material hinzugefügt werden.


* Klicken Sie auf ein Material, um es auszuwählen. Nach Auswahl einer Umgebung werden ihre Materialeigenschaften in den Panels unten angezeigt. Weitere Informationen finden Sie im Hilfethema [Rendermaterialeigenschaften](#properties).
* Durch Klick mit der rechten Maustaste auf ein Material wird das Kontextmenü des Materials angezeigt.
* Durch Klick mit der rechten Maustaste in den leeren Bereich der Liste wird das Kontextmenü für ein neues Material angezeigt.

###  ![images/add_material.png](images/add_material.png) Hinzufügen eines neuen Materials
{: #add_material}
Scrollen Sie ans untere Ende der Liste der Materialien und klicken Sie auf die Plus-Schaltfläche.

Dadurch wird die [Bibliothek](libraries.html) der Renderumgebungen angezeigt.
Die Materialien in der Bibliothek verhalten sich wie Vorlagen, um Materialien im Modell zu erzeugen.

### Kontextmenü des Materials
{: material_context}
Dieses Menü wird durch Klick mit der rechten Maustaste auf ein Material geöffnet.  Weitere Infos zu den zahlreichen Optionen in diesem Menü finden Sie im Hilfethema zum [Werkzeugmenü](#tools_menu).

### Kontextmenü für ein neues Material
{: new_material_context}
Dieses Menü kann durch einen Rechtsklick in den leeren Bereich der Materialliste geöffnet werden.

#### ![images/toolbarlus.png](images/toolbarplus.png) Neues Material anlegen
Erzeugt ein neues grundlegendes mattes weißes Material.


#### ![images/paste.png](images/paste.png) Einfügen
Zur Einfügen eines Materials aus der Zwischenablage.

#### ![images/pasteasinstance.png](images/pasteasinstance.png) Als Instanz einfügen
Erzeugt ein neues Material aus dem Inhalt der Zwischenablage, das mit dem Originalmaterial verknüpft ist.

#### ![images/grid.png](images/grid.png) Raster
Zeigt die Vorschau als Raster von Miniaturansichten an.

#### ![images/list.png](images/list.png) Liste
Zeigt die Vorschau als Liste von Miniaturansichten an.

#### ![images/tree.png](images/tree.png) Baum
Zeigt die Vorschau als verzweigtes Baumverzeichnis an.

#### ![images/horizontal.png](images/horizontal.png) Horizontales Layout
Zeigt die Vorschau auf der linken Seite der Steuerungen an.

#### ![images/showpreview.png](images/showpreview.png) Vorschaufenster anzeigen
Zeigt die Vorschaueigenschaften für die zur Zeit ausgewählte Miniaturansicht an. Definiert Vorschau-Geometrie, Größe, Hintergrund, Drehverhalten.

#### ![images/floatthumbnail.png](images/floatthumbnail.png) Schweben
Lässt das Vorschaubild in einem Fenster, dessen Größe angepasst werden kann, schweben.

#### Miniaturansichten

##### ![images/small.png](images/small.png) Klein
Miniaturansichten werden sehr klein angezeigt.

##### ![images/medium.png](images/medium.png) Mittel
Miniaturansichten werden in mittlerer Größe angezeigt.

##### ![images/large.png](images/large.png) Groß
Miniaturansichten werden groß angezeigt.

##### ![images/showlabels.png](images/showlabels.png) Labels anzeigen
Zeigt im Rastermodus Labels mit den Namen der Miniaturansichten an.
Im Listenmodus werden immer Labels angezeigt.

##### ![images/showunits.png](images/showunits.png) Einheiten anzeigen
Zeigt die Größe in Modelleinheiten an.

##### ![images/autoupdatethumbnail.png](images/autoupdatethumbnail.png) Vorschau mit autom. Aktualisierung
Alle Vorschauansichten werden bei Änderungen der Einstellungen aktualisiert.

##### ![images/updateallpreviews.png](images/updateallpreviews.png) Alle Vorschauansichten aktualisieren
Zur manuellen Aktualisierung der Vorschauen, wenn die Option Vorschau mit autom. Aktualisierung deaktiviert ist.

## [Fensterteiler](#panel_map) ![images/callout_3.svg](images/callout_3.svg)
{: #divider}
Durch Ziehen an diesem Element kann die Länge der Materialliste angepasst werden. Wenn die Materialliste verlängert wird, wird dementsprechend der Abschnitt der Materialeigenschaften verkürzt.

## [Materialeigenschaften](#panel_map) ![images/callout_4.svg](images/callout_4.svg)
{: #properties}

#### [Name des Materials](#panel_map) ![images/callout_5.svg](images/callout_5.svg)
{: #name}
Der Name des Materials. Der Name des Materials wird beim Export des Materials in eine Bibliothek als Dateiname verwendet. Hinweis: Materialien werden im Rhino-Modell gespeichert. Verschiedene Materialien in unterschiedlichen Modellen können daher denselben Namen haben.

#### [Materialpanels](material-editor.html#panel_map) ![images/callout_6.svg](images/callout_6.svg)
{: #panels}
Im Abschnitt der Materialeigenschaften gibt es mehrere Panels mit Einstellungsmöglichkeiten. Durch Klick auf die Titelleiste eines Panels kann dieses zu- bzw. aufgeklappt werden.

Je nach Art des Materials und der aktuell eingestellten Materialebene werden andere Panels angezeigt. Weitere Informationen zu den einzelnen Materialpanels finden Sie im Hilfethema [Flamingo-Materialien](material-type-simple.html).

## Werkzeugmenü ![images/library_default.png](images/library_default.png)
{: #tools-menu}
<!-- This comes from the page http://docs.mcneel.com/rhino/5/help/en-us/popup_moreinformation/materialthumbnail_contextmenu.htm -->
Diese Einstellungen erscheinen auch auf Kontextmenüs (Klick mit der rechten Maustaste) für Miniaturansichten und Miniaturansichtshintergründe.

#### ![images/assigntoobjects.png](images/assigntoobjects.png) Der Auswahl zuordnen
Ordnet den ausgewählten Objekten das aktuelle Material zu.

##### Objekten ein Material zuweisen
 1. Klicken Sie auf *Der Auswahl zuordnen*.
 1. Wählen Sie im Rhino-Ansichtsfenster die Zielobjekte aus.

##### Objekte vorauswählen
 1. Wählen Sie im Rhino-Ansichtsfenster die Zielobjekte aus.
 1. Klicken Sie auf *Der Auswahl zuordnen*.
Die Zielobjekte können ausgewählt werden, bevor oder nachdem Sie auf Der Auswahl zuordnen klicken.

##### Drag & Drop von Materialien auf Objekte
 * Ziehen Sie das Material aus den Miniaturansichten oder aus der Liste auf die Zielobjekte.
Drag & Drop funktioniert jeweils nur für ein Objekt gleichzeitig.

#### ![images/assigntolayers.png](images/assigntolayers.png) Den Ebenen zuordnen
Ordnet das aktuelle Material den Ebenen zu.

##### Zuweisung eines Materials zu einer Ebene
 1. Klicken Sie auf *Den Ebenen zuordnen*.
 1. Wählen Sie im Dialogfenster *Ebenen auswählen* die entsprechenden Ebenen aus.

##### Materialien aus dem Ebenen-Panel zuordnen
 1. Wählen Sie im [Ebenen](http://docs.mcneel.com/rhino/5/help/de-de/index.htm#commands/layer.htm)-Panel eine oder mehrere Ebenen und klicken Sie auf die Spalte  [Material](http://docs.mcneel.com/rhino/5/help/de-de/commands/layer.htm#Material).
 1. Wählen Sie im Dialogfenster *Ebenenmaterial* das zuzuweisende Material aus.


##### Drag & Drop eines Materials auf eine Ebene
 * Ziehen Sie das Material aus der Miniaturansicht oder Liste auf die Zielebene.
Drag & Drop funktioniert nur für jeweils eine Ebene.

#### ![images/materials_selectobjects.png](images/materials_selectobjects.png) Objekte auswählen
Objekte im Modell für die Materialzuordnung auswählen.

#### ![images/toolbarplus.png](images/toolbarplus.png) Neues Material anlegen
Dadurch wird die [Bibliothek](libraries.html) der Renderumgebungen angezeigt.
Die Materialien in der Bibliothek verhalten sich wie Vorlagen, um Materialien im Modell zu erzeugen.

#### ![images/import.png](images/import.png) Material aus Datei importieren
Importiert Materialien aus einer gespeicherten .rmtl Rhino-Datei.

#### ![images/savetofile.png](images/savetofile.png) In Datei speichern
Speichert ein Material in eine .rmtl Rhino-Datei.

#### ![images/changetype.png](images/changetype.png) Typ ändern
Wechselt den Materialtyp.

#### ![images/changetype.png](images/changetype.png) Typ ändern (ähnliche Einstellungen kopieren)
Wechselt den Materialtyp.
Das Standardverhalten hängt vom aktuellen Status der [Renderoptionen](http://docs.mcneel.com/rhino/5/help/de-de/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm) >  [Ähnliche Einstellungen kopieren, wenn Inhaltstyp geändert wird](http://docs.mcneel.com/rhino/5/help/de-de/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm) ab. Wenn aktiviert, werden kompatible Eigenschaften vom alten Inhalt in den neuen Inhalt kopiert.

#### ![images/reset.png](images/reset.png) Auf Standard zurücksetzen
Alle Materialeinstellungen werden gleichzeitig auf ein standardmäßiges weißes, mattes, nicht reflektierendes und nicht texturiertes Material zurückgesetzt.

#### ![images/copy.png](images/copy.png) Kopieren
Kopiert das ausgewählte Material in die Windows Zwischenablage. Der Inhalt der Zwischenablage kann dann in den Editor zur Erzeugung eines neuen Materials oder direkt in einen Ordner zur Erzeugung einer [Bibliotheksdatei](libraries.html) eingefügt werden.

#### ![images/paste.png](images/paste.png) Einfügen
Zur Einfügen eines Materials aus der Zwischenablage.

#### ![images/pasteasinstance.png](images/pasteasinstance.png) Als Instanz einfügen
Erzeugt ein neues Material aus dem Inhalt der Zwischenablage, das mit dem Originalmaterial verknüpft ist.

#### ![images/delete.png](images/delete.png) Löschen
Löscht das ausgewählte Material.

#### ![images/rename.png](images/rename.png) Umbenennen...
Benennt das ausgewählte Material um.

#### ![images/duplicate.png](images/duplicate.png) Duplizieren
Kopiert das ausgewählte Material in ein neues Material mit den gleichen Einstellungen.

#### ![images/removeinstancing.png](images/removeinstancing.png) Instanziierung entfernen
Dadurch wird die Verbindung zwischen [instanziierten](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm) Materialien entfernt.
{% include_relative snippets/snippet-contenteditorpreviewoptions.md %}


#### ![images/contentfilter.png](images/contentfilter.png) Inhaltsfilter
Öffnet das Dialogfenster der [Inhaltsfilter](content_filters.html).

#### ![images/rename.png](images/rename.png) Eigenschaften
Dadurch wird das Dialogfenster der [Vorschaueigenschaften](http://docs.mcneel.com/rhino/5/help/de-de/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm) geöffnet.