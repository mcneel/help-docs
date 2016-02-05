---
title: Flamingo-nXt-Optionen
---


# ![images/options.svg](images/options.svg){: .inline} {{page.title}}
Diese Optionen dienen der allgemeinen Konfiguration von Flamingo nXt.  Änderungen an diesen Einstellungen beeinflussen die generelle Ausführung von Flamingo.

{: #default-decal-link-state}
{% include_relative snippets/snippet-linking.md %}

#### Ausgabeordner der Farm
{: #farm-output-folder}
Der gemeinsame Ordner für Render-Farm-Aufträge. In diesen Ordner werden auch die Ergebnisse des Farm-Renderings ausgegeben. Zum Einstellen einer neuen Option verwenden Sie die Ordner-Symbolschaltfläche ![images/folderopen32x32.png](images/folderopen32x32.png){: .inline}.

#### Markierte Lichter anzeigen
Bei Auswahl dieser Option wird die Richtung markierter Lichter angezeigt.  Dies funktioniert für Spotlichter und diffuse Lichtverteilungen.

#### Schnelle Vorschau in OpenGL
Zum Anzeigen eines OpenGL-Miniaturbilds, bevor das gerenderte Material angezeigt wird.  Dadurch kann das Material schneller angezeigt werden, es kann aber vorkommen, dass das OpenGL-Bild dem tatsächlichen Material nicht wirklich entspricht.

#### Native Historiendateien nach Abschluss des Renderings speichern
Standardmäßig wird das zuletzt gerenderte Bild für den Fall zwischengespeichert, dass es noch einmal verwendet werden soll.