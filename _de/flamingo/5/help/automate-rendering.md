---
title: Automatisiertes Rendering
---

# {{page.title}}


## Stapel-Rendering
{: #batch-rendering}
Stapelaufträge dienen der automatischen Abarbeitung mehrerer Aufträge. Bei einem Stapelauftrag können die Ansicht, die Auflösung und die Anzahl der Durchgänge eingestellt werden. Stapelrenderings können auf einem einzelnen Computer ausgeführt oder an einer [Renderfarm](render-farm.html) geschickt werden. Öffnen Sie die Stapelliste und fügen Sie neue Aufträge hinzu. Die Stapelaufträge werden im Modell gespeichert.

##### Wo befindet sich dieser Befehl?

 * Menü > Flamingo nXt 5.0 > Weitere Werkzeuge > Stapel-Rendering

### Stapelrenderdialog
{: #batch-render}
Fügen Sie einen Auftrag hinzu und stellen Sie anschließend seine Eigenschaften ein.

#### Hinzufügen
Jedem Stapelauftrag liegt eine im Modell gespeicherte Ansicht zugrunde.  Klicken Sie auf die Schaltfläche Hinzufügen und wählen Sie aus der Liste der im Modell vorhandenen Ansichten.  Alle anderen Menüeinträge werden aktiviert, nachdem ein Auftrag hinzugefügt und ausgewählt wurde.

#### Löschen
Wählen Sie einen vorhandenen Stapelauftrag aus.  Klicken Sie anschließend auf Löschen, um den Auftrag aus der Stapelliste zu entfernen.

#### Eigenschaften
Wählen Sie einen vorhandenen Stapelauftrag aus und bestimmen Sie seine [Stapelrendereigenschaften](#batch-render-properties) über den Menüeintrag Eigenschaften.  In den Eigenschaften können der Dateiname, die Auflösung und die Anzahl Durchgänge eines Auftrags eingestellt werden.

#### Nach oben
Name des Ansichtsfensters in der Liste nach oben verschieben.

#### Nach unten
Name des Ansichtsfensters in der Liste nach unten verschieben.

#### Stapelliste
{: #batch-list}
Zeigt Informationen über die Liste der zu rendernden Ansichten an. Klicken Sie doppelt auf einen vorhandenen Auftrag, um die [Stapelrendereigenschaften](#batch-render-properties) einzustellen.

#### Renderstatus
Zeigt Informationen über Durchgang, Abtastlinie und abgelaufene Zeit des Stapelprozesses an.

####  Rendering anhalten
Stoppt den Stapelprozess.

#### Stapel lokal rendern
{: #render-batch-locally}
Verwendet nur den aktuellen Computer, um die Batch-Aufträge zu rendern. Die gerenderten Bilder werden im Verzeichnis gespeichert, das in den [Stapelrendereigenschaften](#batch-render-properties) eingestellt wurde.

####  Stapel an Farm senden
Die Stapelaufträge werden an eine [Renderfarm](render-farm.html) geschickt. Die Aufträge werden mit allen erhältlichen Farm-Clients gerendert. Die Renderbilder werden in den gemeinsamen Farm-Ordner ausgegeben.

### Stapelrendereigenschaften
{: #batch-render-properties}

#### Zu renderndes Ansichtsfenster
Bestimmt die Anzeige, die von diesem Auftrag gerendert wird. Weitere Infos finden Sie im Reiter Renderoptionen im Abschnitt [Zu renderndes Ansichtsfenster](render-tab.html#viewtorender).

#### Dateiname
Klicken Sie auf die Schaltfläche Speichern ![images/saveimageas.png](images/saveimageas.png){: .inline} und geben Sie einen Dateinamen für das gerenderte Bild an.

#### Alphakanal
Zur Einstellung, ob der Alphakanal ebenfalls im Bild gespeichert werden soll.  Weitere Infos finden Sie im Abschnitt [Alphakanalhintergrund verwenden](environment-tab.html#alpha).

#### Dokumenteinstellungen verwenden
{: #rendering-resolution}
Standardmäßig wird die Auflösung des aktuellen Dokuments für das Rendering verwendet.  Wenn Sie eine andere Auflösung verwenden möchten, deaktivieren Sie diese Option und geben sie die gewünschte Auflösung ein. Weitere Infos finden Sie in der Beschreibung der [Auflösung](render-tab.html#resolution) in den Renderoptionen.

#### Renderbeschränkungen
{: #rendering-constraints}
Zur Angabe der Anzahl der Durchgänge bis zum Abschluss dieses Stapelauftrags.  Weitere Infos finden Sie im Abschnitt [Durchgänge](documentproperties-flamingo.html#number-of-passes).

<!-- TODO: Flamingo nXt 5 runs from the RDK.  The need to Flamingo Automate render is not clear.  What is needed to run animations with nxt right now?
The number of passes and the ability to send a render to the farm are required still.  So the dialog should be smaller.
Alpha channel This needs to be investigated. The rest of this section is commented out.-->

<!-- Commented out until automated render can be determined

## Animations
{: #animation}
There are two ways to create animations in Rhino.  Animations can be configured using [Rhino's Animation toolbar](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#commands/animation.htm) or using the [Bongo](http://bongo.rhino3d.com/) animation plugin.

##### To submit an animation job to the render farm
1. Run the [FlamingoNXtAutomateRender](automate-rendering.html#flamingonxtautomaterender) command.
1. In the Configure Automated Render Command dialog, select **Render to farm**.
&#160;
Specify the Job name,and click the OK button.
&#160;
Set a type of animation from Rhino's Animation setup toolbar. Select Render Full as the Capture method.
&#160;
Record the animation from the Animation toolbar. The render jobs will be sent to Render Farm.
&#160;
When the jobs are finished in Render Farm, run the FlamingoNXtAutomateRender command again and select all the jobs in the dialog.
&#160;
Click the Copy selected files to specified output folder button and select a folder where all the render images will be copied to.


## FlamingoNXtAutomateRender command
{: #flamingonxtautomaterender}


## Configure Automated Render Command

### Enabled
Redirects the default **Render** command to use the **Render Farm**.

### Use default render dialog
Resets the **Render** command to render directly instead of to the farm.

### Number of render passes to render
Specifies the number of render passes.

### Render to farm
Redirects the **Render** command to render to the farm.

### Job name
Specifies the **Render Farm**  [Job name](automate-rendering.html#job-name).

## Render constraints

### Number of render passes to render
Specifies the [number of passes](documentproperties-flamingo.html#number-of-passes).

### Save alpha channel
Saves the [alpha channel](render-window.html#save-with-alpha-channel) background.
-->