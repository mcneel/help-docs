---
title: Farm-Rendering
---

# {{page.title}}
Die Flamingo-nXt-Renderfarm verwendet die Leistung von mehreren Computern, um einzelne Bilder, Stapelaufträge von mehreren Bildern oder ansichtsgestützte Animationen zu rendern. Auf den Computern, die als Clients der Renderfarm dienen, muss weder Rhino noch Flamingo nXt installiert sein.

#### Eine typische Farm-Konfiguration
{: #render-farm}

![images/renderfarm-002.png](images/renderfarm-002.png){: style="margin-top:25px;"}

>![images/01.png](images/01.png)Ein Computer mit Rhino und Flamingo nXt.
>![images/02.png](images/02.png)Ein Netzwerkserver oder freigegebener Farmordner.
>![images/03.png](images/03.png)Zwei Renderfarm-Clients. (Die nXt Renderfarm enthält zwei kostenlose Kopien der Client-Software.)
>![images/04.png](images/04.png)Zusätzliche Renderfarm-Clients.

Die Renderfarm ist für bis zu zwei Client-Computer kostenlos. Wenn Sie weitere Clients hinzufügen möchten, erwerben Sie die nXt-Renderfarmlizenz [hier](https://www2.mcneel.com/commerce/accurender/buy-farm.asp).

#### Gemeinsamer Farmordner
{: farm-folder}
Der Schlüssel zu einer funktionierenden Renderfarm ist ein gemeinsam genutzter Ordner, auf den der Master-Rechner und alle Client-Computer gleichsam zugreifen können.  Dies ist normalerweise ein gemeinsam genutzter Netzwerkordner.  Dabei kann es sich um einen Ordner auf dem Master-Rechner oder in einem Netzwerk handeln.  Der Ordner muss nicht auf jedem Client demselben Namen zugewiesen sein, aber jeder Client benötigt vollen Lese-, Schreib- und Löschzugriff auf den Ordner.  Der freigegebene Ordner sollte über mindestens 20 GB freien Speicherplatz verfügen.

#### Die nXt-Renderfarm beinhaltet zwei Anwendungen:

##### Farmer-Render-Client (nXtFarmer64.exe)
Ein kleines Programm, das auf jedem Netzwerk-Render-Client ausgeführt wird und darauf wartet, dass Aufträge generiert werden. Normalerweise arbeiten Renderfarmen im Hintergrund, ohne den Rendering-Prozess auf einem Monitor anzuzeigen. Wenn Sie auf diese Weise rendern, können Sie eine höhere Computerleistung für längere Aufgaben verwenden, dafür aber nicht auf das Rendering einwirken.

##### Farm-Monitor (nXtFarmMonitor64.exe)
Ein Applet, das den Status Ihrer Renderaufträge anzeigt und einige einfache Steuerungswerkzeuge bietet.
Für fortgeschrittene Installationen lässt Sie die nXt Renderfarm-Software mit Rendermanagern von Drittenwicklern arbeiten. Die folgenden Anwendungsverfahren gelten für die mit Flamingo nXt mitgelieferte Renderfarm. Wenn Sie Renderfarmen von Drittentwicklern verwenden, können einige dieser Verfahren anders sein.

#### Der Farmprozess
{: #the-farm-process}
 1. Zum Start eines Renderings mit der Flamingo-nXt-Farm verwenden Sie statt des Befehls *Rendern* die Renderfarm *(Flamingo-nXt-5.0-Menü &gt; Renderfarm)*. Dadurch wird ein Renderauftrag an den [Farm-Ausgabeordner](options-flamingo.html#farm-output-folder) übermittelt. Alle Materialien und Support-Informationen werden automatisch mit dem Auftrag mitgeliefert.
 2. Renderaufträge werden in viele verschiedene Farmaufgaben aufgeteilt. Die Renderfarm-Clients überprüfen den Farm-Ausgabeordner beständig nach neuen Aufgaben. Jeder Client nimmt sich eine Aufgabe und beginnt zu rendern. Mit dem Farm-Monitor  *(Flamingo nXt 5.0 &gt; Renderfarm &gt; Farm-Monitor...)* können Sie den Fortschritt eines Auftrags überprüfen.
 3. Jeder Farm-Client speichert die Resultate im Farmordner unter *Auftragsname\Ausgabe*.
 3. Während die Clients ihre Aufträge beenden, werden gleichzeitig neue Aufträge aufgenommen, die an die Farm gesendet werden.
 4. Die Ausgabe einer Farm erfolgt im [nXt-Bildformat (.nXtImage)](image-editor.html). Bilder in diesem Format können mit dem [nXt-Bildeditor](image-editor.html) bearbeitet werden. Die Ergebnisse können im [nXt-Bildeditor](image-editor.html) auch als TGA-, PNG-, TIF- oder JPG-Datei abgespeichert werden.

## Installation und Konfiguration der Farm
{: #install}
Der Farm-Render-Client und der Farm-Monitor werden zusammen mit Flamingo auf dem Rhino-Master-Rechner installiert.  Auf anderen Client-Computern ohne Rhino und Flamingo nXt muss der Farm-Client installiert werden.

##### Installation des Render-Farmers
Client-Computer, auf denen Rhino und Flamingo nicht installiert sind, benötigen den Farmer-Client:

 1. Laden Sie die aktuelle [Render-Farmer-Software](http://www.rhino3d.com/download/The-Farm/1.0/release) herunter.
 1. Führen Sie das heruntergeladene Installationsprogramm auf jedem der Client-Rechner aus.
 1. Führen Sie den Render-Farmer auf jedem Client-Computer aus.
 1. Der Render-Farmer erscheint als Symbol in der Taskleiste.

##### Konfiguration der Renderfarm
{: #configure-the-render-farm}
1.  [Klicken Sie mit der rechten Maustaste](mouse-button-right.html) auf das Symbol und wählen Sie *Wiederherstellen*.
1. Klicken Sie im nXt-Farmer-Fenster im Menü *Optionen* auf *Pfad* und wählen Sie den Pfad zum Ordner der Renderfarm aus.

Stellen Sie auf dem Computer mit Rhino und Flamingo nXt den Rhino-Zoo-Ordner ein. Klicken Sie im Menü *Werkzeuge* auf *Optionen* und stellen Sie den gemeinsam genutzten Farm-Ordner als [Ausgabeordner der Farm](options-flamingo.html#farm-output-folder) ein.

Die Renderfarm ist nun konfiguriert.

## Verwendung der Renderfarm
{: #using-the-render-farm-from-flamingo-nxt}
Die Farm kann zur Zeit auf drei Arten verwendet werden, um Renderings auf mehreren Computern zu bearbeiten: Einzelne Renderaufträge, Stapelaufträge und Animationen.

##### Überprüfung der Client-Rechner auf korrekte Funktionsweise
Nach dem Start des Render-Farmers auf allen Client-Computern:

 1. Klicken Sie auf einem beliebigen Computer im Windows-Startmenü auf [Farm Monitor](#render-farm-monitor).
 1. Die Client-Rechner sollten im oberen Listenkästchen erscheinen.
 1. In der Liste der Rechner sollten alle Render-Farmer-Clients aufgelistet sein.  Ihr Status sollte *Aktiv* sein.

Falls ein Problem auftaucht, konsultieren Sie die Hilfethemen zu [Installation](#install) und [Konfiguration](#configure-the-render-farm).


##### Übermittlung eines Auftrags an die Renderfarm
1. Stellen Sie das Rendering und die Ansicht in Rhino ganz normal ein.
1. Klicken Sie im Flamingo-nXt-Menü auf *Renderfarm* > *Renderfarm starten*.
1. Das Dialogfenster für einen [Farm-Auftrag](#farm-job) wird geöffnet.
1. Wählen Sie die gewünschte Option aus und klicken Sie auf OK.


##### Überwachung der Farm
Verwenden Sie zur Überwachung eines Renderauftrags den [Farm Monitor](#render-farm-monitor).

 1. Gehen Sie dazu auf dem Master-Rechner im Windows-Startmenü auf [Farm Monitor](#render-farm-monitor).
 1. In der Liste der Aufträge sollte ein kürzlich angelegter Auftrag angezeigt werden. Dies kann für große Aufträge eine Weile dauern.
 1. Der Status des Auftrags wird auf *Aktiv* geändert.
 1. Nach einiger Zeit nehmen die Rechner der Farm Aufgaben desselben Datums auf.
 1. Je mehr Aufgaben abgeschlossen werden, desto größer ist der Wert für *Prozent abgeschlossen*.
 1. Wenn der Auftrag abgeschlossen ist, ändert sich der Status auf *Abgeschlossen*.


## Optionen von Farm-Aufträgen
{: #farm-job}

#### Name
{: #job-name}
Datum und Uhrzeit werden automatisch dem Namen, den Sie auswählen, vorangestellt. Es wird ein Unterordner für den Auftrag im freigegebenen Renderfarm-Ordner erstellt. Ein Ausgabeordner wird ebenfalls im neuen Auftragsordner erzeugt.
Nach Abschluss eines Auftrags steht die Ausgabe im Ausgabeordner der Aufträge zur Verfügung.

#### Auftrag starten
Ein Auftrag kann direkt nach dem Anlegen, zu einem späteren Zeitpunkt oder manuell über den Farm-Monitor gestartet werden.

#### Jetzt
Der Auftrag wird sofort gestartet.

#### Später (manuell)
Der Auftrag kann zu einem späteren Zeitpunkt manuell mithilfe des [Farm-Monitors](#render-farm-monitor) gestartet werden.

#### Nach
Der Auftrag wird zu einem bestimmten Zeitpunkt gestartet.

#### Renderbeschränkungen
{: #rendering-constraints}
Zur Angabe der Anzahl der Durchgänge bis zum Abschluss dieses Stapelauftrags.  Weitere Infos finden Sie im Abschnitt [Durchgänge](documentproperties-flamingo.html#number-of-passes).


## Farm-Monitor
{: #render-farm-monitor}
Der Farm-Monitor ist ein eigenständiges Programm, das den Status der Client-Computer und die in der Farm vorhandenen Aufgaben anzeigt. Aufträge können vom Monitor aus unterbrochen und neu gestartet werden und ein Client-Computer kann von der Renderfarm ausgeschlossen werden.

Gehen Sie zum Ausführen des Farm-Monitors im Rhino-Menü auf *Flamingo nXt 5.0 > Renderfarm > Farm-Monitor*.

Sie finden das Programm auch direkt im Windows-Startmenü unter *Alle Programme > nXt Render Farm > Farm Monitor*.

#### Optionen
Klicken Sie mit der rechten Maustaste auf einen Rechner oder Auftrag, um auf die Optionen zuzugreifen.

#### Aktualisieren
Zur Aktualisierung der Auftragsliste.

#### Gerät anhalten
Der Computer wird angehalten und nimmt vorübergehend nicht am Renderprozess teil.

#### Gerät fortsetzen
Der Computer wird wieder in den Renderprozess eingegliedert.

#### Auftrag anhalten
Der Auftrag wird pausiert.

#### Auftrag fortsetzen
Der Auftrag wird fortgesetzt.

#### Auftrag entfernen
Der Auftrag wird aus der Liste entfernt.

## Lizenzierung der Renderfarm
{: #licensing-the-render-farm-}
Mithilfe der Renderfarm können Renderaufträge auf ein Netzwerk verteilt und so auf mehreren Rechnern gleichzeitig bearbeitet werden.  [Download des Renderfarm-Clients](http://nxt.flamingo3d.com/page/nxt-render-farm-de).


##### Autorisierung eines Knotens
1. Warten Sie, bis alle aktiven Farm-Aufträge vervollständigt wurden, bevor Sie mit der Lizenzierung beginnen.
1. Speichern Sie den Produktschlüssel (XF10-J9G2-H006-T8AJ-GBB9-0027) in einer Textdatei auf einem Netzwerkrechner, damit Sie ihn einfach und schnell in jeden Knoten einfügen können.
1. Wenn der Knoten gerade aktiv ist, [klicken Sie mit der rechten Maustaste](mouse-button-right.html) das Symbol der Renderfarm und anschließend auf **Schließen**.
1. Gehen Sie im Windows-Startmenü auf **Alle Programme**.
Klicken Sie im Ordner der nXt-Renderfarm auf **Farm autorisieren**.
1. Geben Sie im Eingabefeld den Lizenzschlüssel ein und klicken Sie auf **OK**.

##### Start eines Knotens
1. Gehen Sie im Windows-Startmenü auf **Alle Programme**.
Klicken Sie im Ordner der Renderfarm auf **Render-Farmer**.
1.  [Klicken Sie mit der rechten Maustaste](mouse-button-right.html) auf das Taskleistensymbol und wählen Sie im Kontextmenü **Wiederherstellen**.
1. Klicken Sie im Hilfe-Menü auf **Info**.
Wenn die Versionsnummer auf eine Testversion hinweist, war die Lizenzierung nicht erfolgreich.
1. Minimieren Sie das Fenster des Render-Farmer.