
### Mascheratura
Nasconde parti dell'immagine in base al valore di colore o al canale alfa memorizzato nell'immagine. Ciò consente alle texture di avere dei contorni dalle forme complesse e di creare effetti complessi quali fori in una superficie.

In questo esempio, un'immagine con uno sfondo con canale alfa viene sistemata come una decal su una superficie rettangolare. La mascheratura funziona allo stesso modo per i materiali.

![images/airplane.png](images/airplane.png)  ![images/masking-004.png](images/masking-004.png)
*Immagine decal originale. La parte a scacchiera grigia rappresenta il canale alfa dell'immagine.*

Le informazioni sulla mascheratura possono provenire da tre fonti della bitmap:

> [Nessuno](#nomask)
> [Canale alfa](#alphamask)
> [Colore](#colormask)

#### Nessuno
{: #nomask}
Senza mascheratura, l'immagine nasconde il materiale sottostante. La mascheratura fa sì che il materiale sia visibile in trasparenza nei punti in cui si sono applicati il canale alfa o la mascheratura per colore. In questo esempio, il materiale assegnato alla superficie planare ha un colore base rosso.

![images/masking-002.png](images/masking-002.png)
*Senza mascheratura (sinistra) l'immagine ricopre la superficie, mentre con mascheratura (destra) il materiale rosso è visibile in trasparenza.*

#### Canale alfa
{: #alphamask}
Usa il [canale alfa](environment-tab.html#alpha) dell'immagine per definire l'area macherata, se esistente.

![images/airplane.png](images/airplane.png)  ![images/masking-004.png](images/masking-004.png)
*Originale sulla sinistra. La parte a scacchiera grigia rappresenta il canale alfa dell'immagine. Sulla destra, l'immagine su una superficie d'acqua.*

Il canale alfa è una porzione dei dati di ciascun pixel, riservata alle informazioni sulla trasparenza. I canali alfa creano e memorizzano maschere che consentono di isolare e proteggere parti di un'immagine quando si applicano un colore, un filtro o altri effetti che possono influire sul resto dell'immagine. In un'immagine, ciascun pixel viene descritto da canali di dati che definiscono la composizione della miscela dei colori rosso, verde e blu (RGB). Il canale alfa è una rappresentazione a 8 bit (256 livelli) in scala di grigio dell'immagine usata per mascherare il colore del pixel sottostante. Il valore della maschera per canale alfa determina l'intensità del colore del pixel. Se il canale alfa è pari al 100%, i pixel dell'immagine saranno completamente trasparenti.  Ad altre intensità di alfa, i pixel dell'immagine si fondono con la trasparenza.

#### Colore
{: #colormask}
Se in un'immagine non esiste il canale alfa, si può specificare un colore dell'immagine come maschera. Esiste anche un valore di sensibilità per rendere la maschera più o meno sensibile ad un colore specifico come colore mascherato. Selezionando l'opzione Colore, si attivano il contagocce, il selettore dei colori ed i controlli di sensibilità.

#### Contagocce colore
Fare clic per selezionare il colore della maschera dalla bitmap. Fare clic sul contagocce e quindi sulla bitmap per selezionare il colore. Questo controllo è disponibile solo quando si è selezionata l'opzione Colore.

{% include_relative snippets/snippet-material-color-select.md %}

#### Sensibilità
Il valore indica le dimensioni dell'area mascherata attorno al colore. Affinché la mascheratura per colore possa avere luogo, questo parametro deve essere maggiore di zero. Questo controllo è disponibile solo quando si è selezionata l'opzione Colore.

#### Sfocatura
Maschera i pixel parzialmente. Il valore determina l'ampiezza della mascheratura parziale attorno al colore mascherato. Questo controllo è disponibile solo quando si è selezionata l'opzione Colore.

#### Inverti
Inverte la maschera, ossia, si invertono i pixel mascherati con quelli non mascherati e viceversa.
<!-- TODO: Does this make sense? -->

![images/masking-007.png](images/masking-007.png)  

#### Trasparente
Rende trasparente l'area mascherata dell'oggetto sottostante, in modo da poter vedere gli altri oggetti o lo sfondo dietro all'oggetto stesso. Normalmente, nell'area in cui usa una maschera, il materiale dell'oggetto può essere visto in trasparenza.

L'aggiunta di trasparenza alla mascheratura consente di ottenere un'ombreggiatura più naturale e fa sì che gli oggetti sullo sfondo siano visibili. Si potrebbe semplicemente usare un materiale trasparente, tuttavia, a volte è utile rendere trasparente la superficie sottostante la decal, mantenendo opache le aree rimanenti della superficie.

![images/masking-003.png](images/masking-003.png)    ![images/masking-004.png](images/masking-004.png)

#### Mostra colori mascherati
Mostra graficamente gli effetti della mascheratura al variare dei parametri. Si usi il [Selettore dei colori](select-color.html) ![images/colorswatch-001.png](images/colorswatch-001.png) fornito per selezionare il colore di visualizzazione dei pixel mascherati. La modifica di questo colore o delle impostazioni del riquadro di selezione non produce alcun effetto sul colore mascherato. Si tratta di un semplice aiuto visuale per l'editing della maschera.

![images/masking-008.png](images/masking-008.png)