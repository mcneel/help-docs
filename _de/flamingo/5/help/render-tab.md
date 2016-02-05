---
title: Renderoptionen
---

# ![images/flamingotab.svg](images/flamingotab.svg){: .inline} {{page.title}}
Im Renderreiter sind die wichtigsten Funktionen zur Einstellung des Render-Ergebnisses zu finden.  In diesem Reiter können Sie die Qualität und Maximaldauer eines Renderings einstellen.  Die Gesamtrenderzeit hängt wesentlich von der Auflösung des Renderbilds ab.

Hinweis: Es wird empfohlen, für Probe-Renderings eine niedrige Auflösung zu verwenden. Eine hohe Auflösung sollte erst für das endgültige Renderbild verwendet werden.

#### Wo befindet sich die Flamingo-Beleuchtungssteuerung?

 1. ![images/options.png](images/options.png){: .inline} Werkzeugleisten >![images/flamingo-icon.png](images/flamingo-icon.png){: .inline} Flamingo-nXt-Werkzeugleiste > Renderoptionen
 1. ![images/menuicon.png](images/menuicon.png){: .inline} Rhino-Menü > Flamingo nXt 5.0 > Bedienfenster anzeigen > Flamingo nXt > Renderoptionen


## Zu renderndes Ansichtsfenster
{: #viewtorender}
Hier können Sie die Ansicht einstellen, die von Flamingo nXt 5 gerendert wird.  Dies ist besonders dann nützlich, wenn immer eine bestimmte Ansicht gerendert werden soll.  Die perspektivische Ansicht ist beispielsweise oftmals die gewünschte Renderansicht.  Bei Auswahl dieser Option müssen Sie nicht immer wieder sicherstellen, dass die gewünschte Renderansicht auch die gerade aktuelle Modellierungsansicht ist.

#### Aktive Ansicht
Bei Auswahl dieser Option wird immer die momentan aktive Ansicht gerendert.  Dies ist die Standardeinstellung.

#### Liste verfügbarer Ansichtsfenster
Eine Liste aller im Modell verwendeten benannten Ansichten.  Wählen Sie hier die Ansicht aus, die immer gerendert werden soll.

## Renderauflösung
{: #resolution}
Die Renderauflösung ist eine der wichtigsten Einstellungen für das Rendering.  Damit wird die Größe und Auflösung des Bilds eingestellt.  Eine höhere Auflösung hat eine exponentiell längere Renderzeit zur Folge.  Es ist daher wichtig, bei dieser Einstellung behutsam vorzugehen.

#### Gesamtpixel
{: #resolutionimagepixels}
Zur Einstellung der Gesamtzahl der Pixel des Renderbilds unter Verwendung der aktuellen Ansicht zur Berechnung des Seitenverhältnisses.  Diese Option bietet sich während der Arbeit an einem Rendering an.  Sie passt sehr gut zur Auswahl der aktuellen Ansicht als Renderansicht. Es ist damit sehr einfach, durch die Änderung der Gesamtzahl der Pixel die Auflösung eines Bilds zu erhöhen oder zu reduzieren.

### Auflösung des Ansichtsfensters
Verwendet die Ansichtsfenstergröße in Pixel zur Bestimmung der Größe des Renderbilds.  Dadurch wird eine 1-zu-1-Abbildung des Seitenverhältnisses und der Auflösung des Ansichtsfensters erzeugt.  Dies ist ein nützlicher Modus, kann aber auch zu langsameren Renderings führen, wenn der Vollbildmodus verwendet wird.

### Bildgröße
{: #resolutionprintedsize}
Die Bildgröße bestimmt die Auflösung des Renderbilds anhand verschiedener Variablen.  Diese Methode ist die beste zur Einstellung einer präzisen Größe und Auflösung des endgültigen Bilds. Wenn das Seitenverhältnis des Bilds nicht mit demjenigen des zu rendernden Ansichtsfensters übereinstimmt, wird die Ansicht oben und unten bzw. an den Seiten zugeschnitten. Hinweis: Bei dieser Option können leicht Renderings mit sehr hoher Auflösung entstehen, die sehr lange brauchen, bis sie fertiggestellt sind.  Verwenden Sie diese Einstellungsmöglichkeiten daher für hoch auflösende Renderings.

Dazu können vier Einheiten verwendet werden:

* Pixel
* Zoll
* Millimeter
* Zentimeter

#### Pixel
Zur Verwendung von Pixel als Einheit für die Größe des Renderbilds.  Mit dieser Einstellung kann die Höhe und Breite des fertigen Renderbilds über die Anzahl Pixel definiert werden.

#### Zoll
Zur Verwendung von Zoll als Einheit für die Größe des Renderbilds. Bei dieser Option wird die Auflösung des Renderbilds aus der Größe und der Pixeldichte abgeleitet.  Zur Bestimmung der endgültigen Auflösung multiplizieren Sie die Höhe und Breite in Zoll mit der Anzahl der Pixel pro Zoll

#### Millimeter
Zur Verwendung von Millimetern als Einheit für die Größe des Renderbilds. Bei dieser Option wird die Auflösung des Renderbilds aus der Größe und der Pixeldichte abgeleitet.  Zur Bestimmung der endgültigen Auflösung multiplizieren Sie die Höhe und Breite in Millimetern mit der Anzahl der Pixel pro Millimeter.

#### Zentimeter
Zur Verwendung von Zentimetern als Einheit für die Größe des Renderbilds. Bei dieser Option wird die Auflösung des Renderbilds aus der Größe und der Pixeldichte abgeleitet.  Zur Bestimmung der endgültigen Auflösung multiplizieren Sie die Höhe und Breite in Zentimetern mit der Anzahl der Pixel pro Zentimeter.

#### Auflösung der Ansicht übernehmen
Bei Auswahl dieser Option wird das Seitenverhältnis zwischen Höhe und Breite des Renderbilds aus der aktuellen Ansicht abgeleitet.  Dadurch kann sichergestellt werden, dass die gesamte Ansicht gerendert wird.

#### Breite
Die Breite des Renderbilds in der aktuell ausgewählten Maßeinheit.  Durch Multiplizierung dieses Werts mit der Auflösung pro Maßeinheit erhalten Sie die Anzahl der Pixel pro Spalte.

#### Höhe
Die Höhe des Renderbilds in der aktuell ausgewählten Maßeinheit.  Durch Multiplizierung dieses Werts mit der Auflösung pro Maßeinheit erhalten Sie die Anzahl der Pixel pro Zeile.

### Auflösung
{: #printsizepixelsperunit}
{: #printsizedpi}
{: #printsizeresolution}

#### Anzeige
Das Bild wird mit der Auflösung des Ansichtsfensters gerendert. Dabei wird die Pixeldichte des Geräts verwendet.  Diese wird normalerweise in [DPI](https://de.wikipedia.org/wiki/Punktdichte) angegeben.

#### Benutzerdefiniert
Das Bild wird unter Verwendung einer benutzerdefinierten Auflösung gerendert. Geben Sie die benutzerdefinierte Höhe und Breite im Feld **Pixel pro ___** ein.

#### Drucker, Entwurfsqualität
100 Pixel pro Zoll oder 4 Pixel pro mm.

#### Drucker, Normale Qualität
150 Pixel pro Zoll oder 6 Pixel pro mm.

#### Drucker, Hohe Qualität
300 Pixel pro Zoll oder 12 Pixel pro mm. Dies ist eine sehr hohe Auflösung für ein Rendering.  Sie ist in erster Linie für kleinere Renderings geeignet, während für große Poster oder Wandbilder kleinere Auflösungen ausreichend sind. Eine hohe Auflösung kann zudem dazu führen, dass das Rendering sehr lange dauert.

#### Pixel pro
Wenn die Auflösung auf *Benutzerdefiniert* eingestellt ist, können Sie mit diesem Steuerelement die Auflösung der ausgewählten Einheit auswählen. Wenn eine vordefinierte Auflösung ausgewählt wird, zeigt das Element die aktuelle Auflösung an.

## Schärfentiefe
{: #depthoffieldoption}
Dieser Effekt erzeugt unterschiedliche Schärfenregionen, mit denen die Linse eines Fotografen nachgeahmt wird. Eine Linse kann nur in einem bestimmten Abstand genau fokussieren und die Schärfe nimmt graduell rund um den Brennpunkt ab.

#### Aktiviert
Zur Aktivierung der Schärfentiefe.

#### Intensität
Kontrolliert die Größe des Fokusbereichs. Wenn die Intensität auf Null eingestellt wird, ist das ganze Bild scharf. Je höher die Intensität, desto unschärfer sind die Bereiche außerhalb der Brennweite und desto kleiner ist der Fokusbereich.

#### Hyperfokale Distanz
{: #focaldistance}
Definiert den Abstand für die Tiefenschärfe. Der Abstand um den Tiefenschärfepunkt, an dem Objekte scharf sind. Wenn die Hyperfokale Distanz auf zehn Einheiten eingestellt ist, sind Objekte sieben Einheiten hinter dem Schärfentiefenpunkt und drei Einheiten davor scharf.

#### Wählen >>
Einen Punkt im Modell für die Brennweite auswählen.

## Render Engine
{: #render-engine}
Flamingo wird mit drei Render Engines geliefert.  Jede produziert bei normalen Renderbedingungen etwas andere Ergebnisse.

Flamingo verwendet progressive mehrstufige Rendertechniken zur Erzeugung eines Renderbilds. Bei einem progressiven Vorgehen kann es bei jedem Durchgang zu unfertigen Artefakten im Rendering kommen. Artefakte sind Rendereffekte, die ungewöhnliche und unfertige Effekte in einem Rendering zur Folge haben.  Theoretisch ergeben alle Render Engines nach Ablauf einer bestimmten Zeit dasselbe Renderbild.  In der Praxis ist die Zeit allerdings immer ein beschränkender Faktor. Es ist daher entscheidend, diejenige Render Engine auszuwählen, mit der das bestmögliche Ergebnis mit der kleinstmöglichen Anzahl Durchgänge erreicht wird.

Wählen Sie dazu einfach die unterschiedlichen Render Engines aus und sehen Sie sich die unterschiedlichen Ergebnisse an.

### Standard
Der standardmäßige Algorithmus erzeugt eine qualitativ sehr hochwertige Simulation. Die Standard-Render-Engine ist eine gute Wahl für zahlreiche verschiedene Szenen.  Die anderen beiden Engines haben einerseits größere Stärken und andererseits größere Schwächen.  Die Standardauswahl ist daher ein guter Ausgangspunkt.

In den ersten Durchgängen erzeugt die Standard-Engine ein bedeutendes Artefakt.  Dieses besteht im harten Überlagern von Schatten.  Je mehr Durchgänge durchgeführt werden, desto weicher werden die Schatten.  Dadurch kann sehr schnell ein Ergebnis erzielt werden, das jedoch eventuell mehr Durchgänge benötigt, bis die Schatten wirklich weich erscheinen.

Der Qualitätsunterschied zwischen der Standardmethode und der Pfadverfolgung kann vor allem dann subtil sein, wenn die indirekte Beleuchtung aktiviert ist. Dieser Unterschied ist die zusätzliche Bearbeitungszeit unter Umständen nicht wert.

### Pfadverfolgung
{: #path-tracer}
Bei der Pfadverfolgung wird zuerst ein sehr körniges Bild erzeugt, das nach und nach feiner und glatter wird. Dieser Prozess ist auch als *Konvergenz* bekannt. Die Pfadverfolgung bietet für viele Modelle mit einfacherer Konfiguration ein qualitativ hochwertigeres Endprodukt auf Kosten einer komplexeren und zeitaufwändigeren Berechnung. **Hinweis:** Die Pfadverfolgung kann helle Flecken oder Fleckenartefakte während eines Renderprozesses verursachen. Diese Artefakte sind normal für die Pfadverfolgung und werden mit der Zeit aufgelöst.

Bestimmte fortgeschrittene Effekte wie Kaustiken oder unscharfe Übertragungen können mit der Pfadverfolgung präziser berechnet werden. Bilder mit Instanzen, Pflanzen und Displacement-Maps konvergieren schneller. Die Pfadverfolgung ist normalerweise einfacher einzustellen als die Standardmethode. Weitere Einstellungen wie Tageslichtportale und Umgebungsbeleuchtung werden nicht verwendet, wenn die Pfadverfolgung ausgewählt ist.

Mit Pfadverfolgung gerenderte Bilder benötigen normalerweise mehr Zeit für die Konvergenz als Bilder, die mit der Standardmethode gerendert wurden. Simulationen mit Innentageslicht, insbesondere Szenen mit relativ kleinen Fenstern, können sehr viel länger benötigen, bis sie abgeschlossen sind.

### Hybrid
Die Hybrid Engine ist der Versuch einer Kombinationen der positiven Seiten des Standard- und des Pfadverfolgungsverfahrens.  Dabei werden Effekte von beiden verwendet.  Die Hybrid Engine berechnet immer indirektes Licht.  Das Artefakt der Hybrid Engine ist ein extensives Punktmuster, das während des Renderings nach und nach reduziert wird. In einigen Fällen kann es sehr viele Durchgänge dauern, bis das Punktmuster verschwunden ist. Für viele Renderings ist dies die beste Render Engine.

###  **Erweitert**
Diese Schaltfläche öffnet den Abschnitt [Flamingo nXt](documentproperties-flamingo.html) in den Rhino-Dokumenteigenschaften. Hier können Sie mehrere fortgeschrittene Rendereigenschaften einstellen, um die Qualität des fertigen Renderbilds weiter zu verfeinern.