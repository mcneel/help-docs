
### Maskierung
Verdunkelt Teile des Bildes basierend auf einem Farbwert oder einem im Bild gespeicherten Alphakanal. Dadurch können Texturen komplex geformte Begrenzungen haben und komplexe Effekte wie Löcher in einer Fläche aufweisen.

In diesem Beispiel wird ein Bild mit einem Alphakanalhintergrund als Decal auf einer rechteckigen Fläche platziert. Maskierung für Materialien funktioniert auf die gleiche Weise.

![images/airplane.png](images/airplane.png)  ![images/masking-004.png](images/masking-004.png)
*Ursprüngliches Decal-Bild. Der grau karierte Bereich stellt den Alphakanal des Bildes dar.*

Maskierungsinformationen können in der Bitmap aus drei verschiedenen Quellen stammen:

> [Nichts](#nomask)
> [Alphakanal](#alphamask)
> [Farbe](#colormask)

#### Nichts
{: #nomask}
Ohne Maskierung wird das darunter liegende Material durch das Bild verdunkelt. Mit einer Maskierung ist das Material dort sichtbar, wo der Alphakanal oder die Maskenfarbe vorhanden ist. Das Material, das in diesem Beispiel einer planaren Fläche zugeordnet ist, verfügt über eine rote Grundfarbe.

![images/masking-002.png](images/masking-002.png)
*Ohne Maskierung (links) deckt das Bild die Fläche, mit Maskierung (rechts) scheint das rote Material durch.*

#### Alphakanal
{: #alphamask}
Verwenden Sie den [Alphakanal](environment-tab.html#alpha) des Bilds (sofern vorhanden), um den maskierten Bereich festzulegen.

![images/airplane.png](images/airplane.png)  ![images/masking-004.png](images/masking-004.png)
*Links das Original. Der grau karierte Bereich stellt den Alphakanal des Bildes dar. Rechts das Bild über einer Wasseroberfläche.*

Der Alphakanal ist ein Teil der Pixeldaten, der Transparenzinformationen vorbehalten ist. Alphakanäle erzeugen und speichern Masken, mit denen Sie Teile eines Bilds isolieren und schützen können, während Sie Farbänderungen vornehmen, Filter oder andere Effekte am restlichen Bild anbringen. Jeder Pixel eines Bilds wird in Datenkanälen beschrieben, die eine Farbmischung aus Rot, Grün und Blau (RGB) festlegen. Der Alphakanal ist eine 8-Bit-Graustufen-Darstellung (256 Stufen) des Bilds und wird verwendet, um die Farbe des darunter liegenden Pixels zu maskieren. Der Wert der Alphamaske bestimmt die Intensität der Pixelfarbe. Wenn der Alphakanal auf 100 % eingestellt ist, sind die Pixel vollständig transparent.  Bei einer niedrigeren Einstellung werden die Bildpixel mit Transparenz überblendet.

#### Farbe
{: #colormask}
Wenn ein Bild keinen Alphakanal aufweist, kann eine Farbe des Bilds als Maske festgelegt werden. Es kann zudem die Toleranz eingestellt werden, mit der eine Maske eine bestimmte Farbe als Maskenfarbe übernimmt. Bei Auswahl der Option *Farbe* werden die Farbpipette, der Farbwähler und die Empfindlichkeitssteuerung aktiviert.

#### Farbpipette
Damit kann die Maskenfarbe aus der Bitmap ausgewählt werden. Klicken Sie zuerst auf die Farbpipette und anschließend in der Bitmap auf die Stelle, deren Farbe Sie verwenden möchten. Dieses Steuerelement ist nur bei Auswahl der Option *Farbe* aktiviert.

{% include_relative snippets/snippet-material-color-select.md %}

#### Empfindlichkeit
Der Wert zeigt die Größe des Bereichs um jene Farben an, die ebenfalls maskiert sind. Damit eine Farbmaskierung stattfinden kann, muss dieser Wert größer als 0,0 sein. Dieses Steuerelement ist nur bei Auswahl der Option *Farbe* aktiviert.

#### Weichzeichner
Maskiert Pixel teilweise. Dieser Wert definiert den Bereich der Teilmaskierung um die maskierte Farbe herum. Dieses Steuerelement ist nur bei Auswahl der Option *Farbe* aktiviert.

#### Umkehren
Kehrt die Maske um. Alle Pixel, die vorher maskiert waren, sind nun sichtbar und alle, die vorher unmaskiert waren, unsichtbar.

![images/masking-007.png](images/masking-007.png)  

#### Transparent
Macht die maskierte Fläche des darunter liegenden Objekts transparent, so dass andere Objekte oder der Hintergrund hinter dem Objekt durch das Objekt hindurch gesehen werden können. Normalerweise scheint das Material des Objekts in diesem Bereich hindurch.

Durch transparente Maskierung wird ein natürlicherer Schatten erzielt und Hintergrundobjekte sind sichtbar. Das darunter liegende Material könnte ganz einfach transparent sein, aber manchmal ist es von Vorteil, wenn die Fläche hinter dem Decal transparent ist, während andere Bereiche der Fläche undurchsichtig bleiben.

![images/masking-003.png](images/masking-003.png)    ![images/masking-004.png](images/masking-004.png)

#### Maskierte Farben anzeigen
Zeigt die Maskierungsauswirkungen grafisch an, während die Parameter geändert werden. Verwenden Sie den [Farbwähler](select-color.html) ![images/colorswatch-001.png](images/colorswatch-001.png) zur Auswahl der Anzeigefarbe der maskierten Pixel. Wenn diese Farbe oder die Einstellung des Kontrollkästchens geändert wird, hat dies keinen Einfluss auf die maskierte Farbe. Es ist nur ein grafisches Werkzeug zum Bearbeiten der Maske.

![images/masking-008.png](images/masking-008.png)