---
title: Umgebungspanel
---

# ![images/environment.svg](images/environment.svg) {{page.title}}
{: #environment-tab}
Umgebungen bestimmen nicht nur den Hintergrund eines Renderings, sondern steuern eine unendliche Kugel rund um das Modell. Objekte in der Szene reflektieren und brechen die Umgebung. Die Umgebungskugel ist kein Objekt, das Sie auswählen können, sondern eine Referenzfläche für Hintergrundeffekte.

Die Umgebung hat Einfluss auf den sichtbaren Teil des Hintergrunds und auf Reflexionen.  Effekte für die Beleuchtung der Szene sind im Hilfethema [Himmel](sun-and-sky.html) beschrieben.

Flamingo wird mit einer *[Flamingo-Standardumgebung](environment.html)* geliefert.  Diese Umgebung wird mit den aktuellen [Beleuchtungsvoreinstellungen](lighting-tab.html) synchronisiert. Bei Verwendung der [Beleuchtungsvoreinstellungen](lighting-tab.html) werden sowohl die Beleuchtung als auch die Umgebung auf geeignete Standardwerte eingestellt.

![images/environment-editor-panel.svg](images/environment-editor-panel.svg){:  #panel_map height="600px" style="float: right"}

##### Wo befindet sich dieser Befehl?
 1. ![images/environments.png](images/environments.png)Umgebungsreiter
 1. ![images/icon-render.png](images/icon-render.png)Werkzeugleiste Renderwerkzeuge > ![images/environments.png](images/environments.png) Umgebungseditor
 1. ![images/menuicon.png](images/menuicon.png)Menü > Render > Umgebungseditor
 1. Befehl > Umgebungseditor

Das Umgebungseditor-Panel ist in mehrere Abschnitte unterteilt.  Je nach Umgebungstyp werden andere erweiterte Optionen angezeigt.

Farben und Texturen können per Drag&Drop aus dem Farbenrad in ein anderes Farbenrad oder eine sonstige Steuerung im Materialeditor, der [Texturenpalette](texturepalette.html) oder dem [Umgebungseditor](environmenteditor.html) gezogen werden.
Umgebungspanel

 1. [Hintergrundtyp](#type)
 1. [Einstellungsleiste](#Einstellungen)
 1. [Umgebungsliste](#environment_list)
 1. [Fensterteiler](#divider)
 1. [Umgebungseigenschaften](#properties)
 1. [Name](#name)
 1. [Umgebungseigenschaften-Panels](#panels)

## [Hintergrundtyp](#panel_map) ![images/callout_1.svg](images/callout_1.svg)
{: #type style="clear: both;"}
Zur Auswahl des Hintergrundtyps des Modells.  Eine [Umgebung](#flamingo-environment) ist eine vollständige Renderumgebung und für Flamingo als Standard voreingestellt.  Die anderen drei Optionen bieten einen weitaus einfacheren Satz an Einstellungen, mit dem Hintergründe in einer traditionelleren Art eingestellt werden können. Weitere Informationen dazu finden Sie im Hilfethema [Grundlegender Rhino-Hintergrund](http://docs.mcneel.com/rhino/5/help/de-de/commands/environmenteditor.htm#Basic_settings).



## [Einstellungsleiste](#panel_map) ![images/callout_2.svg](images/callout_2.svg)
{: #settings}
In dieser Leiste können Sie durch die Liste der Umgebungen navigieren.

#### ![images/met_leftarrow.png](images/met-leftarrow.png) Pfeil zurück
Zum Zurückblättern durch die bereits vorher ausgewählten Umgebungen.  Zum Beispiel eine Umgebung mit reflektierenden oder gebrochenen Ebenen.  Mit diesem Pfeil können Sie auch von den Reflexions- oder Brechungsdetails zurück zur übergeordneten Umgebung gehen.

####  ![images/met_rightarrow.png](images/met-rightarrow.png) Pfeil vorwärts
Zum Vorwärtsblättern durch die bereits vorher ausgewählten Umgebungen.  Zum Beispiel eine Umgebung mit reflektierenden oder gebrochenen Ebenen.  Mit diesem Pfeil können Sie auch von der übergeordneten Umgebung vorwärts zu den Reflexions- oder Brechungsdetails gehen.

#### ![images/material_editor.png](images/material_editor.png)![images/texture-2dchecker.png](images/texture-2dchecker.png) Aktuell ausgewählter Umgebungsname
Zeigt den aktuellen Umgebungsnamen und die Bearbeitungsebene an.  Wenn es beispielsweise eine reflektierende oder gebrochene Ebene gibt, wird ein ">" angezeigt. Hier können Sie nachsehen, welche Umgebung als aktuell eingestellt ist.

#### ![images/library_default.png](images/library_default.png) Werkzeugmenü
Zeigt das [Werkzeugmenü](#tools_menu) an.  Dies ist ein umfassendes Menü mit Befehlen, Einstellungsmöglichkeiten und Werkzeugen für Umgebungen.

#### ![images/help_topics.png](images/help_topics.png) Hilfe

## [Umgebungsliste](#panel_map) ![images/callout_3.svg](images/callout_3.svg)
{: #environment_list}
Die Liste aller im Modell verwendeten Umgebungen. Die als aktuelle Umgebung eingestellte Umgebung wird für das Rendering verwendet. Farbig hervorgehobene Ecken zeigen an, welche Umgebung die aktuelle ist.

Funktionen dieser Liste:

* Durch Doppelklick auf eine Umgebung wird diese als aktuell eingestellt. Nach Auswahl einer Umgebung werden ihre Eigenschaften in den Panels unten angezeigt. Weitere Informationen finden Sie im Hilfethema zu den [Umgebungseigenschaften](#properties).
* Sie können durch die Liste scrollen und sich so alle Umgebungen im Modell ansehen.
* Durch Klick auf die Plus-Schaltfläche ![images/add_material.png](images/add_material.png) am Ende der Liste kann eine neue Umgebung hinzugefügt werden.
* Durch Klick mit der rechten Maustaste auf eine Umgebung wird das Kontextmenü der Umgebung angezeigt.
* Durch Klick mit der rechten Maustaste in den leeren Bereich der Liste wird das Kontextmenü für eine neue Umgebung angezeigt.

###  ![images/add_material.png](images/add_material.png) Hinzufügen einer neuen Umgebung
{: #add_environment}
Scrollen Sie ans untere Ende der Liste der Umgebungen und klicken Sie auf die Plus-Schaltfläche.

Dadurch wird die [Bibliothek](libraries.html) der Renderumgebungen angezeigt.
Die Umgebungen der Bibliothek sind wie Vorlagen zur Erzeugung von Umgebungen im Modell.

### Umgebungskontextmenü
{: environment_context}
Dieses Menü wird durch Klick mit der rechten Maustaste auf eine Umgebung geöffnet.  Weitere Infos zu den zahlreichen Optionen in diesem Menü finden Sie im Hilfethema zum [Werkzeugmenü](#tools_menu).

### Kontextmenü für neue Umgebung
{: new_envrionment_context}
Dieses Menü kann durch einen Rechtsklick in den leeren Bereich der Umgebungsliste geöffnet werden.

#### ![images/toolbarlus.png](images/toolbarplus.png) Neue Umgebung anlegen
Zum Anlegen einer neuen Flamingo-Umgebung.

#### ![images/import.png](images/import.png) Umgebung aus Datei importieren...
Mit diesem Befehl können Sie eine vorher exportierte Umgebung auswählen.

#### ![images/paste.png](images/paste.png) Einfügen
Zum Anlegen einer neuen Umgebung aus dem Inhalt der Zwischenablage.

#### ![images/pasteasinstance.png](images/pasteasinstance.png) Als Instanz einfügen
Zum Anlegen einer neuen Umgebung aus dem Inhalt der Zwischenablage, die über Instanziierung mit dem Original verknüpft ist.

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
Zeigt das Vorschaubild in einem schwebenden Fenster an.

#### Miniaturansichten

##### ![images/small.png](images/small.png) Klein
Miniaturansichten werden klein angezeigt.

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
Zur manuellen Aktualisierung der Vorschau, wenn die Option Vorschau mit autom. Aktualisierung deaktiviert ist.

## [Fensterteiler](#panel_map) ![images/callout_4.svg](images/callout_4.svg)
{: #divider}
Durch Ziehen an diesem Element kann die Länge der Umgebungsliste gegenüber der Länge des Abschnitts der Umgebungseigenschaften angepasst werden.

## [Umgebungseigenschaften](#panel_map) ![images/callout_5.svg](images/callout_5.svg)
{: #properties}

### [Name der Umgebung](#panel_map) ![images/callout_6.svg](images/callout_6.svg)
{: #name}
Der Name der Umgebung. Der Name der Umgebung wird beim Export der Umgebung in eine Bibliothek als Dateiname verwendet. **Hinweis:** Umgebungen werden im Rhino-Modell gespeichert, sodass verschiedene Umgebungen in unterschiedlichen Modellen denselben Namen haben können.

### [Umgebungspanels](l#panel_map) ![images/callout_7.svg](images/callout_7.svg)
{: #panels}
Im Abschnitt der Umgebungseigenschaften gibt es mehrere Panels mit Einstellungsmöglichkeiten. Durch Klick auf die Titelleiste eines Panels kann dieses zu- bzw. aufgeklappt werden.

Je nach Art der Umgebung und dem aktuell eingestellten Umgebungsniveau werden andere Panels angezeigt. Weitere Informationen zu den einzelnen Umgebungspanels finden Sie im Hilfethema [Flamingo-Umgebung](environment.html)

## Werkzeugmenü ![images/library_default.png](images/library_default.png)
{: #tools_menu}
Diese Einstellungen erscheinen auch auf Kontextmenüs (Klick mit der rechten Maustaste) für Miniaturansichten und Miniaturansichtshintergründe.

#### ![images/currentenvironment.png](images/currentenvironment.png) Als aktuelle Umgebung einstellen
Dadurch wird die entsprechende Umgebung als aktuell eingestellt.  Die aktuelle Umgebung wird im nächsten Rendering verwendet.

#### ![images/toolbarlus.png](images/toolbarplus.png) Neue Umgebung anlegen
Zum Anlegen einer neuen Flamingo-Umgebung.
<!-- This comes from the page http://docs.mcneel.com/rhino/5/help/en-us/popup_moreinformation/materialthumbnail_contextmenu.htm -->
Diese Einstellungen sind auch in Kontextmenüs (Klick mit der rechten Maustaste) für Miniaturansichten und Miniaturansichtshintergründe verfügbar.

#### ![images/import.png](images/import.png) Umgebung aus Datei importieren
Importiert Umgebungen aus einer gespeicherten Rhino-RENV-Datei.

#### ![images/savetofile.png](images/savetofile.png) In Datei speichern
Speichert eine Umgebung in eine Rhino-RENV-Datei.

#### ![images/changetype.png](images/changetype.png) Typ ändern
Wechselt den Umgebungstyp.

#### ![images/changetype.png](images/changetype.png) Typ ändern (ähnliche Einstellungen kopieren)
Wechselt den Umgebungstyp.
Das Standardverhalten hängt vom aktuellen Status der [Renderoptionen](http://docs.mcneel.com/rhino/5/help/de-de/options/rendering.htm) >  [Ähnliche Einstellungen kopieren, wenn Inhaltstyp geändert wird](http://docs.mcneel.com/rhino/5/help/de-de/options/rendering.htm#Copy_similar_settings_when_content_type_is_changed) ab. Wenn aktiviert, werden kompatible Eigenschaften vom alten Inhalt in den neuen Inhalt kopiert.

#### ![images/reset.png](images/reset.png) Auf Standard zurücksetzen
Zum Zurücksetzen aller Umgebungseinstellungen auf einen standardmäßigen schwarzen Hintergrund mit den Einstellungsmerkmalen "Reflektiert > Himmel" und "Gebrochen > Sichtbarer Hintergrund".

#### ![images/copy.png](images/copy.png) Kopieren
Kopiert die ausgewählte Umgebung in die Windows-Zwischenablage. Der Inhalt der Zwischenablage kann dann in den Editor zur Erzeugung einer neuen Umgebung oder direkt in einen Ordner zur Erzeugung einer [Bibliotheksdatei](libraries.html) eingefügt werden.

#### ![images/paste.png](images/paste.png) Einfügen
Zum Anlegen einer neuen Umgebung aus dem Inhalt der Zwischenablage.

#### ![images/pasteasinstance.png](images/pasteasinstance.png) Als Instanz einfügen
Zum Anlegen einer neuen Umgebung aus dem Inhalt der Zwischenablage, die über Instanziierung mit dem Original verknüpft ist.

#### ![images/delete.png](images/delete.png) Löschen
Löscht die ausgewählte Umgebung.

#### ![images/rename.png](images/rename.png) Umbenennen...
Benennt die ausgewählte Umgebung um.

#### ![images/duplicate.png](images/duplicate.png) Duplizieren
Kopiert die ausgewählte Umgebung in eine neue Umgebung mit den gleichen Einstellungen.

#### ![images/removeinstancing.png](images/removeinstancing.png) Instanziierung entfernen
Entfernt die Verbindung zwischen [instanziierten](#paste-as-instance) Umgebungen.

{% include_relative snippets/snippet-contenteditorpreviewoptions.md %}

#### ![images/contentfilter.png](images/contentfilter.png) Inhaltsfilter
Öffnet das Dialogfenster der [Inhaltsfilter](content_filters.html).

#### ![images/rename.png](images/rename.png) Eigenschaften
Öffnet das Dialogfenster der [Vorschaueigenschaften](previewproperties.html).