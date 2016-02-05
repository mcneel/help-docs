---
title: Editor delle immagini
---

# {{page.title}}
L'editor delle immagini di nXt è in grado di modificare i file immagine nativi (.nXtImage) generati da una qualsiasi delle piattaforme nXt. Questi file nativi mantengono tutte le informazioni raccolte durante il rendering.
Usando l'editor delle immagini di nXt è possibile:


* Regolare le impostazioni dell'[indicatore dei toni](image-editor.html#tone-mapping).
* Cambiare l'intensità dei canali di illuminazione.
* Aggiungere degli effetti speciali basati sulle immagini: [Nebbia](image-editor.html#haze), [Sfocatura profondità](image-editor.html#depth-blur) e [Glare](image-editor.html#glare).
* [Salvare](image-editor.html#save-tonemapped-image-as) un'immagine sottoposta a mappatura dei toni in un formato bitmap quale .jpg o .png.
* Salvare le informazioni sulla luminanza in un [formato HDR](image-editor.html#save-hdr-image-as).
* Visualizzare e salvare dei canali mascherati aggiuntivi ( [alfa](image-editor.html#alpha-channel), [distanza](image-editor.html#distance-channel), [materiale](image-editor.html#material-channel) ), da usare in operazioni di compositing avanzato.
* Salvare nel formato file [PiranesiÂ©](http://www.piranesi.co.uk/) (*.epx), il quale può essere usato per realizzare dei rendering non fotorealistici.
* Usare l'[aritmetica](image-editor.html#arithmetic) delle immagini per operazioni quali la fusione di un'immagine generata dai diversi nodi della render farm.
* Salvare le [impostazioni di illuminazione](image-editor.html#save-lighting-settings-as) usate per generare un rendering. Queste impostazioni di illuminazione possono essere usate per generare ulteriori rendering.

Per lanciare l'editor

> Dal menu **Flamingo nXt 5.0**, cliccare su **Altri strumenti &gt; Editor delle immagini di Flamingo nXt**.

## Menu File
{: #file-menu}

### Apri
Apre un file salvato nel formato .nXtImage per modificarlo.

### Salva immagine sorgente
Salva il file .nXtImage.

### Salva immagine sorgente come
Salva il file .nXtImage con un nome diverso.

### Salva immagine con tone mapping come
{: #save-tonemapped-image-as}
Salva l'immagine modificata come file immagine bitmap.

 * JPEG (.jpg)
 * TIFF (.tif)
 * TIFF con canale alfa (.tif)
 * PNG (.png)
 * PNG con canale alfa (.png)
 * [File Piranesi EPix (.epx)](http://www.piranesi.co.uk/)

Piranesi è uno strumento per l'illustrazione 3D che crea delle immagini con effetti di pittura a mano libera.

### Salva immagine HDR come
{: #save-hdr-image-as}

 * File HDR (.hdr)
 * File EXR (.exr)
 * EXR con canale alfa (.exr)

### Salva maschera
{: #save-mask}
I file .nXtImage contengono tre canali aggiuntivi che possono essere usati come maschere nella maggior parte degli editor di bitmap per operazioni di compositing avanzato. Questi canali contengono informazioni sulla trasparenza, sulla distanza e sul materiale di ciascun pixel, codificate in un'immagine a gradazioni di grigio. Ciascun canale può essere visualizzato e salvato su un file .png.

##### Note:

 1. Il canale alfa può essere incluso in un'immagine con tone mapping selezionando un formato file con canale alfa quando si salva l'immagine.
 1. I canali Distanza e Materiali non hanno filtri anti-aliasing, per cui possono mostrare alcuni artefatti di scalettatura. L'aggiunta di una piccola quantità di sfocatura gaussiana ad una maschera prima di usarla può aiutare ad attenuare queste scalettature.
 1. Il canale Materiali codifica solamente 255 materiali diversi. Se un modello contiene un numero maggiore di materiali, alcuni colori vengono ripetuti.

#### Canale Materiali
{: #material-channel}
Salva la maschera del canale del materiale.
![images/materialchannel.png](images/materialchannel.png)

#### Canale alfa
{: #alpha-channel}
Salva la maschera del canale alfa.
![images/alphachannel.png](images/alphachannel.png)

#### Canale di distanza
{: #distance-channel}
Salva la maschera del canale di distanza.
![images/distancechannel.png](images/distancechannel.png)

### Salva impostazioni di illuminazione come
{: #save-lighting-settings-as}
Salva lo [schema di illuminazione](lighting-tab.html#open-lighting-scheme).

## Menu Immagine
{: #renderwindowimage}

### Info
{: #info}
Mostra una serie di informazioni sull'immagine.

### Aritmetica
{: #arithmetic}
Consente di unire tra di loro o di sovrapporre le porzioni di immagine renderizzate usando la funzione di [rendering di singole immagini della Render Farm](automate-rendering.html#single-images).

##### Per unire le porzioni di immagine:

 1. Nel menu **File**, cliccare su **Apri**.
 1. Selezionare la prima immagine della sequenza, per esempio, 000000.nXtImage.
 1. Nel menu **Immagine**, cliccare su **Aritmetica** e quindi su **Aggiungi**.
 1. Selezionare tutte le altre immagini della sequenza.

 **Nota:** Attenzione a non selezionare di nuovo la prima immagine (000000.nXtImage), altrimenti verrà aggiunta due volte.

#### Aggiungi
Aggiunge i valori dei pixel di un livello ai valori dei pixel dell'altro livello. Quando i valori sono superiori a 255 (nel caso dell'RGB), viene visualizzato il bianco.

#### Sottrai
Sottrae i valori dei pixel di un livello dai valori dei pixel dell'altro livello. Quando i valori sono negativi, viene visualizzato il nero.

#### Differenza
Sottrae il livello superiore da quello inferiore o viceversa, per ottenere sempre un valore positivo. La fusione con il nero non produce nessun cambiamento, visto che i valori di tutti i colori sono 0. La fusione con il bianco inverte l'immagine.

#### Aggiungi maschera
Tiene conto della maschera del canale alfa quando effettua la fusione.

#### Combina Path Tracing
Combina tra di loro varie immagini renderizzate con il motore Path Tracer in modo che, per esempio, la combinazione di dieci immagini renderizzate con 20 passate ciascuna equivalga ad un'immagine renderizzata con 200 passate.

![images/combinedpathtrace200.png](images/combinedpathtrace200.png)
*Immagine renderizzata con 20 passate (sinistra); 10 immagini renderizzate con 20 passate per creare un'immagine renderizzata con 200 passate (destra).*

### Applica patch
{: #apply-patch}
Inserisce un'immagine renderizzata come porzione selezionata nell'immagine renderizzata.

### Animazione
È possibile animare modificando le informazioni sull'immagine.

##### Per animare gli effetti

 1. Impostare la prima immagine. Cliccare sul pulsante **Più (+)** accanto alla casella di modifica **Fotogrammi/secondo**.
 1. Modificare l'immagine ed aggiungere i fotogrammi.
 1. Cliccare su **Immagine &gt; Animazione** e, nella finestra di dialogo, cliccare su **Anteprima**.
 1. Se è tutto a posto, cliccare su **Anima**.

### Creare una cartella.
Verrà creata una sequenza di immagini che può essere usata per creare un'animazione usando software disegnati a tale scopo.

## Menu Vista
{: #view-menu}
Specifica cosa visualizzare nell'immagine.

### Immagine
Mostra l'immagine renderizzata originale.

![images/fx-001.png](images/fx-001.png)

### Immagine e maschera alfa
Mostra sia l'immagine che la maschera del canale alfa.

![images/imageandalpha.png](images/imageandalpha.png)

### Maschera materiale
Mostra la [maschera del materiale](image-editor.html#material-channel).

![images/materialchannel.png](images/materialchannel.png)

### Maschera distanza
Mostra la [maschera di distanza](image-editor.html#distance-channel).

![images/distancechannel.png](images/distancechannel.png)

## Uso dell'editor delle immagini

##### Caricare un'immagine

 1.  [Save](render-window.html#export-to-nxtimage) your rendering results as an **.nXtImage**.
 1. Dal menu **Flamingo nXt**, cliccare su **Utility &gt; Editor delle immagini di Flamingo nXt**.
 1. Nell'**Editor delle immagini di nXt**, dal menu File, cliccare su **Apri** per caricare l'immagine nell'editor.


## Mappatura dei toni
{: #tone-mapping}
La mappatura dei toni è un processo che consiste nel convertire i dati sulla luminanza usati da nXt in pixel RGB che possono essere visualizzati oppure stampati.


#### Luminosità
{: #brightness}
Vedi [Finestra di rendering: Luminosità](render-window.html#brightness).
{% include_relative snippets/snippet-brightness.md %}

#### Sovraesposizione
Vedi [Finestra di rendering: Sovraesposizione](render-window.html#burn).

#### Saturazione
Vedi [Finestra di rendering: Saturazione](render-window.html#saturation).

#### Istogramma
Vedi [Finestra di rendering: Istogramma](render-window.html#histogram).

## Campi di stato
I campi di stato si trovano nella parte inferiore dello schermo. Questi campi mostrano una serie di informazioni su ciascun pixel dell'immagine man mano che si sposta il cursore su di essa.

#### Pixel
{: #pixel}
Le coordinate del pixel, misurate dal vertice sinistro inferiore.

#### Colore
{: #color}
I primi tre campi mostrano i colori RGB visualizzati nell'immagine dopo la mappatura dei toni. Il quarto campo mostra il canale alfa (trasparenza), il quale viene usato nelle operazioni di compositing.

#### Valore
{: #value}
I valori di luminanza di ciascun sottocanale (rosso, verde e blu).

#### Lum
{: #lum}
La media ponderata dei valori di luminanza memorizzati in ciascun pixel.

#### Profondità
{: #depth}
La distanza in metri di ciascun pixel dall'osservatore. Valori negativi indicano un pixel sullo sfondo.

#### Materiale
{: #material}
Il nome del materiale usato per renderizzare il pixel.

## Impostazioni FX
Si possono applicare degli effetti speciali alle immagini.  Molti di questi effetti usano le informazioni extra memorizzate nel formato .nXtImage.  Per esempio, il glare usa lo spazio della luminanza lavorando su valori di luce reali e la nebbia usa la distanza nell'immagine.

### Nebbia
{: #haze}
Aggiunge colore ai pixel più lontani dalla camera. Questo effetto può essere usato per applicare un effetto foschia o nebbia ad una scena oppure per mascherare uno sfondo con colore o cambiare il colore dello sfondo.

![images/golden gate.png](images/golden gate.png)
*Immagine originale (sinistra) e con effetto nebbia (destra).*

#### Intensità
Specifica l'intensità del colore della nebbia.

#### Vicino
La distanza dalla camera in corrispondenza della quale l'effetto nebbia inizia ad aggiungere colore a ciascun pixel.

#### Selezione
Selezionare un punto sull'immagine per specificare la distanza.

#### Lontano
La distanza in corrispondenza della quale l'effetto nebbia raggiunge il suo massimo. A ciascun pixel oltre questo punto viene applicato l'effetto massimo di nebbia.
Ai pixel che si trovano nell'intervallo vicino-lontano l'effetto nebbia viene applicato in modo lineare dai pixel più vicini a quelli più lontani.

#### Selezione
Selezionare un punto sull'immagine per specificare la distanza.

#### Colore
Il colore della nebbia.

#### Selezione
Selezionare un punto sull'immagine per specificare il colore.

### Sfocatura profondità
{: #depth-blur}
Il valore di distanza contenuto in ciascun pixel può essere usato per sfuocare l'immagine tra le distanze specificate.

![images/fx-depth-001.png](images/fx-depth-001.png)
*Immagine originale (sinistra) e con sfocatura profondità (destra).*

#### Intensità
Specifica la quantità di sfocatura.

#### Fuoco
{: #depthblurfocus}
Specifica una distanza di messa a fuoco nell'immagine.

#### Selezione
Selezionare un punto sull'immagine per specificare la distanza di messa a fuoco.

#### Zona a fuoco
{: #in-focus-zone}
L'estensione della zona nitida attorno al **Fuoco**. Questo valore si misura in metri. Tutti i pixel all'interno di questa zona saranno nitidi e verranno ignorati dal filtro di sfocatura. I pixel oltre questa zona si confonderanno progressivamente con i pixel contigui per dare un'illusione ottica di profondità.

#### Sfocatura
Controlla la direzione dell'effetto del filtro di sfocatura. L'impostazione di default è **Sfondo**. Ciò significa che tutti i pixel più lontani dalla camera rispetto all'intervallo della **Zona a fuoco** verranno sfuocati progressivamente.

![images/blur-001.png](images/blur-001.png)
*Sfocatura primo piano (sinistra) e sfondo (destra).*

#### Sfondo
Sfuoca i pixel più lontani dalla camera rispetto all'intervallo della **Zona a fuoco**.

#### Primo piano
Sfuoca i pixel più vicini alla camera rispetto all'intervallo della **Zona a fuoco**.

#### Entrambi
Sfuoca sia i pixel sul davanti che quelli posteriori rispetto all'intervallo della **Zona a fuoco**. Si tratta di un modo veloce di ottenere un effetto profondità di campo. Esso non è comunque tanto accurato quanto l'effetto integrato di pre-rendering [Profondità di campo](render-tab.html#depthoffieldoption).

### Glare
{: #glare}
Il glare ha effetto sui pixel più luminosi rispetto alla Soglia in lumen, creando un effetto alone sui pixel circostanti. Vengono influenzati solo i pixel più luminosi dell'immagine.
Portare il cursore sui pixel per visualizzarne il glare e leggere il totale dei lumen in corrispondenza dei pixel indicati.

![images/glare-001.png](images/glare-001.png)
*Immagine originale (sinistra) e con effetto glare (destra).*

#### Intensità
Regola la quantità di alone che ha effetto sui pixel circostanti.

#### Soglia
Il limite inferiore del valore di riferimento per l'applicazione del filtro glare. Il filtro avrà effetto su tutti i pixel più luminosi di questo valore.

#### Selezione
Selezionare un punto sull'immagine per specificare il valore di luminosità.

### Vignetta
{: #vignette}
Sfuma i colori sui bordi dell'immagine per creare un effetto alone.

![images/fx-vignette-001.png](images/fx-vignette-001.png)
*Immagine originale (sinistra) e con effetto vignetta (destra).*