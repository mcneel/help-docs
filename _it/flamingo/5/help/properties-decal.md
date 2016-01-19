---
title: Decal
---
<--TODO: This page should be updated. There are at least, 3 points to improve, more likely some more: 1. Compare instructions to add decal with actual process in the program. 2. There is another decal type, "spherical", that's not mentioned in the text. 3. Clicking on "Properties" doesn't open a dialog but returns an error message. -->

# {{page.title}}
Le decal sono mappe immagine non a mattonella applicabili direttamente sugli oggetti (anziché indirettamente tramite un materiale). Le decal si possono usare per modificare, in una zona determinata, il colore di un oggetto, la sua riflettività o i rilievi della sua superficie.
Le decal sono costituite da singole istanze di immagini, anziché da immagini affiancate, come accade quando sono usate nella [definizione di un materiale](materials-tab.html).
Le decal possono essere usate per:

>Decorare pareti interne con lavori artistici.
>Disporre etichette e loghi su prodotti.
>Inserire simboli nei modelli.
>Creare vetrate.

![images/freshmilk.png](images/freshmilk.png)
 **Nota:** Le anteprime delle decal si visualizzano nelle viste wireframe solo se l'OpenGL è attivato per la modalità wireframe. L'impostazione **Pipeline** deve essere **OpenGL** in **Opzioni**  &gt; **Vista**  &gt; **Modalità di visualizzazione**  &gt; **Wireframe**  &gt; **Altre impostazioni**  &gt; **Mostra assegnazione pipeline**.

## Posizionamento delle decal
{: #decal-list}
{: #decal-placement}

###  **Aggiungi**
{: #add-decal}
1. Selezionare uno o più oggetti.
1. Dal menu **Modifica**, cliccare su **Proprietà oggetto**.
1. Dall'elenco delle **Proprietà**, fare clic su **Decal di Flamingo nXt**.
1. Fare clic sul pulsante **Aggiungi**.
1. Nella finestra di dialogo **Apri bitmap**, selezionare il nome di una bitmap e fare clic su **Apri**.
{% include_relative snippets/snippet-clearbitmapcache.md %}1. Nella finestra di dialogo **Proprietà decal**, specificare le opzioni e fare clic su **Colloca**.
1. Ai prompt, selezionare dei punti sul modello per posizionare la decal.
La sequenza precisa dipende dal tipo di decal selezionato: [Planare](#decal-planarmapping), [Cilindrica](#decal-cylindricalmapping) o [MappaUV](#decal-uvmapping).

###  **Modifica collocazione**
{: #decal-edit-placement}
1. Cliccare sul pulsante **Modifica collocazione**.
1. Al prompt **Selezionare un punto di controllo**, usare l'editor grafico per cambiare la posizione della decal.
1. Premere **Invio** al termine.

###  **Proprietà**
{: #decal-properties}
1. Cliccare sul pulsante **Proprietà**.
1. Nella finestra di dialogo **Proprietà decal**, usare i controlli per cambiare le proprietà della decal.

###  **Elimina**
{: #decal-delete}

>Cliccare sul pulsante **Elimina**.

###  **Sposta su** / **Sposta giù**
{: #decal-movedown}
{: #decal-moveup}
Quando varie decal sovrapposte sono applicate su un singolo oggetto, il loro ordine di applicazione può essere importante. Le decal vengono applicate seguendo l'ordine di apparizione nel relativo elenco. L'ultima decal dell'elenco è quella più superficiale.

>Cliccare su **Sposta su** o su **Sposta giù** per cambiare la posizione di una decal all'interno dell'elenco.

##### Per sistemare una decal planare
1. Ai prompt, selezionare con un clic i punti per la **Larghezza** e la **Direzione altezza** della decal.
1. Al prompt **Selezionare un punto di controllo...**, selezionare un punto di controllo per regolare le dimensioni, la rotazione e la posizione dell'immagine.
Oppure premere **Invio** per concludere la sistemazione della decal.

### Opzioni

#### Sposta
Sposta la decal. Ai prompt Punto di riferimento e Punto di destinazione, specificare le posizioni come per il comando Sposta di Rhino.

#### UsaAspectRatioImmagine
Ripristina una decal modificata in una direzione alla sua dimensione originaria definita dal rapporto di aspetto della bitmap iniziale.

##### Per sistemare una decal cilindrica
1. Al prompt, specificare un punto per il **Centro** del cilindro.
1. Al prompt **Selezionare un punto di controllo...**, selezionare un punto di controllo per regolare le dimensioni, la rotazione e la posizione dell'immagine.
Oppure premere **Invio** per concludere la sistemazione della decal.

## Impostare o modificare la posizione della decal usando il widget di controllo
Nota: Quando si usa la mappatura planare su un oggetto curvo, la proiezione della bitmap deve giacere sotto la superficie dell'oggetto. Le porzioni di bitmap che giacciono di fronte alla superficie non sono visibili.

#### Per ridimensionare la larghezza e l'altezza della decal allo stesso tempo

>Trascinare i punti di controllo sui vertici del widget di controllo.

#### Per modificare l'altezza di una decal

>Trascinare il punto di controllo centrale dei bordi superiore ed inferiore del widget di controllo.

#### Per modificare la larghezza di una decal

>Trascinare il punto di controllo centrale dei bordi sinistro e destro del widget di controllo.

#### Per spostare la decal

>Trascinare il punto di controllo al centro del widget di controllo.

#### Per ruotare la decal

>Trascinare il punto di controllo degli assi x, y o z sull'icona degli assi del widget.

## Proprietà delle decal
{: #dialogbox-editdecal}
Le informazioni di una bitmap si possono usare per sostituire o combinare i colori di un oggetto con i colori della decal. Si tratta senza dubbio dell'uso più comune di una decal.

## Proiezione
{: #projection}
Lo stile di mappatura determina in che modo viene proiettata la decal sull'oggetto. È consigliabile tracciare delle linee di costruzione di riferimento nella scena per un posizionamento più accurato della decal. Per una decal standard, si può usare un rettangolo guida tracciato giusto dietro alla superficie di destinazione. Per una collocazione più accurata, è opportuno fare uso degli snap all'oggetto.

### Cilindrica
{: #decal-cylindricalmapping}
La mappatura cilindrica è particolarmente idonea per disporre decal su oggetti la cui curvatura si estende in una sola direzione, come ad esempio accade con le etichette di bottiglie.
La proiezione cilindrica mappa la bitmap sul cilindro, con l'asse verticale della bitmap parallelo all'asse del cilindro e l'asse orizzontale lungo il perimetro laterale del cilindro.
![images/cylindricaldecal-002.png](images/cylindricaldecal-002.png)

### Planare
{: #decal-planarmapping}
La mappatura planare è lo stile di mappatura più comune. È specialmente adatta per mappature su oggetti piatti o lievemente incurvati.
I vertici definiscono la posizione della bitmap e la sua estensione. Se il rettangolo non ha le stesse proporzioni di quelle della bitmap, essa verrà stirata o ridotta in modo tale da farla combaciare con il rettangolo.
Quando si usa la mappatura planare su un oggetto curvato, la proiezione della bitmap deve giacere sotto la superficie dell'oggetto. Le porzioni di bitmap che giacciono di fronte alla superficie non sono visibili.
![images/decal-planar-001.png](images/decal-planar-001.png)

### Mappa UV
{: #decal-uvmapping}
La mappatura UV è particolarmente indicata quando la decal viene fatta scorrere lungo una superficie affinché si adatti ad essa.
La decal copre l'intero oggetto, non c'è nessun controllo sulla sua posizione.
La mappatura UV usa la parametrizzazione di u e v della superficie per piegare ed allungare l'immagine.
![images/uvmapdecal-00.png](images/uvmapdecal-00.png)

### Sfoglia
{: #file-browse}
Cambia il file immagine.

{% include_relative snippets/snippet-clearbitmapcache.md %}

## Intensità
{: #decalmappingstrength}

### Colore
{: #decal-color}
Varia l'intensità relativa del colore dell'immagine rispetto al materiale sottostante. Vedi anche [Proprietà texture materiale, Intensità del colore](texture-properties-main.html#color).

### Rilievo
{: #decalmappingbump}
Le mappe di rilievo simulano dei rilievi su una superficie tramite effetti d'ombra e di luce. Vedi anche [Proprietà texture materiale, Intensità del rilievo](texture-properties-main.html#bump).

## Rifinitura riflettente
{: #reflective-finish-and-highlight}
Controllano le stesse proprietà impostate nella definizione di un materiale. Ciò permette all'utente di applicare queste proprietà ad aree specifiche dell'oggetto che sono influenzate dalla decal. Di default, le decal possiedono una rifinitura opaca.

### Intensità
Regola l'intensità delle zone di massima riflessione luminosa. Quanto maggiori i valori, tanto maggiori le dimensioni e l'intensità dei punti di massima illuminazione. Vedi [Proprietà dei materiali avanzate, Intensità](advanced-material-properties-main.html#intensity).

### Nitidezza
Imposta le dimensioni delle zone di massima riflessione luminosa. Valori inferiori definiscono zone di massima riflessione luminosa più ampie; valori maggiori concentrano le riflessioni speculari su un'area minore. Vedi [Proprietà dei materiali avanzate, Nitidezza](advanced-material-properties-main.html#sharpness).

### Metallico
Imposta il colore delle riflessioni speculari in modo che corrisponda al colore base dell'oggetto. Vedi [Proprietà dei materiali avanzate: Metallico](advanced-material-properties-main.html#metallic).
{% include_relative snippets/snippet-linking.md %}
{% include_relative snippets/snippet-masking.md %}
## Avanzato
{: #advanced}

### Due lati
{: #double}
Fa sì che la decal appaia sia sul lato anteriore che su quello posteriore della superficie su cui viene sistemata.

### Copia speculare
{: #mirror}
Riflette l'immagine decal.

## Direzione di proiezione
{: #projection-direction}

### Indietro
Proietta la decal indietro rispetto alla parte posteriore dell'immagine della decal.
![images/projectionbackward1.png](images/projectionbackward1.png)Anteriore (sinistra), posteriore (destra).

### Avanti
Proietta la decal in avanti rispetto alla parte anteriore dell'immagine della decal.
![images/projectionforward1.png](images/projectionforward1.png)Anteriore (sinistra), posteriore (destra).

### Avanti e Indietro
Proietta la decal sia in avanti che indietro rispetto all'immagine della decal.
![images/projectionforwardandback.png](images/projectionforwardandback.png)Anteriore (sinistra), posteriore (destra).

### Trasparenza
Imposta la quantità di trasparenza per la decal. Vedi [Trasparenza](advanced-material-properties-transparency.html).
IOR
Imposta l'indice di rifrazione della decal trasparente. Vedi [Indice di rifrazione](advanced-material-properties-transparency.html#index-of-refraction)