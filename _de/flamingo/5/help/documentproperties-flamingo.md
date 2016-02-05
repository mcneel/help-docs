---
title: Dokumenteigenschaften von Flamingo nXt
---


# ![images/options.svg](images/options.svg){: .inline} {{page.title}}
Diese Einstellungen gelten nur für das aktuelle Modell. Es gibt eine Wechselbeziehung zwischen der Zeit zum Fertigstellen eines Renderings und der Qualität.

#### Wo befindet sich dieser Befehl?
<!-- These locations are not correct.  They need to be updated. -->

 1. ![images/icon-render.png](images/icon-render.png){: .inline} Werkzeugleiste Renderwerkzeuge > ![images/environments.png](images/environments.png){: .inline} Materialeditor
 1. ![images/menuicon.png](images/menuicon.png){: .inline} Menü > Rendern > Umgebungseditor
 1. Befehl > Umgebungseditor

## Materialien
{: #materials}
Mit diesen Steuerelementen können Sie einstellen, wie Flächen in Flamingo gerendert werden.  Diese Einstellungen ändern nicht das den Objekten und Ebenen zugewiesene Material, sondern wie Flamingo die Farbe einer Fläche erstellt.

#### Materialien verwenden
{: #use-materials}
Führt ein Rendering mit Flamingo-nXt- und Rhino-Materialien aus. Objekte ohne Materialzuweisung werden weiß gerendert. Wenn weder die Option **Material verwenden**, noch die Option **Objekt verwenden** ausgewählt wurde, werden alle Objekte weiß gerendert.

#### Objektfarbe verwenden
{: #use-object-color}
Verwendet beim Rendering die Farben, die über das Rhino-Objekt oder die Ebenenfarbe zugeordnet wurden. Hinweis: Es kann sowohl die Option **Materialien verwenden** als auch die Option **Objektfarbe verwenden** ausgewählt werden. In diesem Fall verwenden die Objekte, die über zugeordnete Materialien verfügen, diese Materialien. Andere Objekte werden anhand ihrer Objekt- oder Ebenenfarbe gerendert.

#### Leuchtkanal
{: #channel}
Materialien mit einem Leuchtkanal sind beleuchtet, werfen aber kein Licht auf andere Objekte. (Markieren Sie ein Objekt als Licht, um damit auch andere Objekte zu beleuchten.)  Durch die Festlegung des Leuchtens auf einen Kanal kann die Helligkeit des Leuchtens nach dem Rendern nachgestellt werden, ohne nochmals rendern zu müssen.

## Rückwurf
{: #bounces}
Wenn ein Strahl auf eine Szene trifft, wird er mehrere Male zurückgeworfen, bevor er erlischt.  Durch die Reduzierung der Anzahl an Rückwürfen wird das Rendering schneller. Wenn die Zahl jedoch zu niedrig angesetzt wird, kann der Effekt verloren gehen.  Die Voreinstellungen sind in der Regel sehr gut für die meisten Renderings, es gibt jedoch Fälle, in denen Änderungen sinnvoll sind.

#### Reflexion
{: #reflective-bounces}
Definiert, wie viele Reflexionsstufen erlaubt sind; in anderen Worten, wie oft ein Lichtstrahl auf Objekten reflektiert wird. Wenn Sie 0 eingeben, gibt es keine Reflexionen. Bei größeren Werten dauert das Rendering länger. Erhöhen Sie diesen Wert, wenn eine Ansicht auf eine reflektierende Fläche blickt, die eine angrenzende Reflexionsfläche zurückwirft und die Reflexionen komplett schwarz werden.

#### Gebrochen
{: #refractive-bounces}
Bestimmt, wie viele Lichtbrechungsstufen erlaubt sind, d.h., wie oft ein Lichtstrahl an Objekten gebrochen wird. Bei Eingabe von 0 werden Brechungen deaktiviert. Bei größeren Werten dauert das Rendering länger. Erhöhen Sie diesen Wert, wenn eine Ansicht durch viele Ebenen blickt und am Ende schwarz statt transparent ist.

#### Indirekt
{: #indirect-bounces}
Bestimmt, wie viele indirekte Lichtstufen erlaubt sind, d.h., wie oft ein indirekter Lichtstrahl an Objekten abprallt. Wenn Sie 0 eingeben, gibt es keine Reflexionen. Bei größeren Werten wird auch die Rendering-Zeit erhöht.

## Indirekte Beleuchtung
{: #indirect-settings}
Die indirekte Beleuchtung beeinflusst nur die Strahlen, die von einer Fläche zurückgeworfen werden und Licht zu einer anderen Fläche tragen.

#### Color Bleeding
{: #color-bleed}
Mit dem Color Bleeding wird die Menge der Farbe gesteuert, die von einem indirekten Lichtstrahl von einer Fläche zu einer anderen übertragen wird.  Hier ist standardmäßig der Maximalwert voreingestellt, um die Dynamik des Renderings zu erhöhen.  

#### Monte-Carlo-Reflexionen
{: #monte-carlo}
Die Monte-Carlo-Einstellung steuert das Sampling indirekter Beleuchtung. Bei Aktivierung dieser Option erfährt das indirekte Licht in den ersten Durchgängen zahlreiche Störungen.  Je mehr Durchgänge jedoch durchgeführt werden, desto subtiler und potentiell detaillierter wird der Monte-Carlo-Effekt. Szenen, die sehr auf indirekte Beleuchtung ausgelegt sind, können von indirekten Monte-Carlo-Reflexionen profitieren.

## Verschiedenes

#### Lichter auf deaktivierten Ebenen verwenden
{: #uselightsonlayersthatareoff}
Verwendet Lichter auf Ebenen, die deaktiviert sind, und ausgeblendete Lichter.

### Renderbeschränkungen
{: #number-of-passes}
{: #time}
{: #render-constraints}
{% include_relative snippets/snippet-renderconstraints.md %}