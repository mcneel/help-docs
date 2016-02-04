---
title: Rendering con una Render Farm
---

# {{page.title}}
La Render Farm di Flamingo nXt usa la potenza di vari computer per renderizzare singole immagini, lavori batch di varie immagini o animazioni basate sulle viste. Sui computer usati solo come client della render farm non è necessario installare né Rhino né Flamingo nXt.

#### Schema tipico di una render farm
{: #render-farm}

![images/renderfarm-002.png](images/renderfarm-002.png){: style="margin-top:25px;"}

>![images/01.png](images/01.png)Un computer con Rhino e Flamingo nXt.
>![images/02.png](images/02.png)Server di rete o cartella farm condivisa.
>![images/03.png](images/03.png)Due client della render farm. (La Render Farm di nXt include due copie gratuite del software client.)
>![images/04.png](images/04.png)Altri client della render farm acquistati a parte.

La Render Farm è gratuita se si hanno al massimo due computer client. Per aggiungere ulteriori computer client, è necessario acquistare la licenza della Render Farm di nXt da [https://www2.mcneel.com/commerce/accurender/buy-farm.asp](https://www2.mcneel.com/commerce/accurender/buy-farm.asp).

#### Cartella farm condivisa
{: farm-folder}
La chiave di una Render Farm funzionale è una cartella condivisa a cui possano accedere sia la macchina master che tutti i computer client.  Di solito si tratta di una cartella di rete condivisa.  Può essere una cartella della macchina master oppure di rete.  Non occorre che la cartella venga assegnata allo stesso nome su ciascun client, tuttavia, tutti i client devono disporre d'accesso completo (lettura, scrittura, eliminazione) alla cartella. La cartella condivisa deve avere almeno 20GB di memoria disponibile.

#### La Render Farm di nXt è costituita da due applicazioni:

##### Il client di rendering Farmer (nXtFarmer64.exe)
Un piccolo programma che viene eseguito su ciascun client di rendering della rete e che attende la generazione dei lavori. Normalmente, le render farm procedono in modo invisibile, senza mostrare i rendering su un monitor man mano che questi avanzano. Questa modalità di rendering consente di sfruttare la potenza di più macchine per realizzare dei task lunghi, ma non consente l'interazione con il rendering man mano che esso avanza.

##### Il Farm Monitor (nXtFarmMonitor64.exe)
Un applet che mostra all'utente lo stato dei lavori di rendering e che fornisce alcuni semplici strumenti di controllo.
Nel caso di installazioni avanzate, il software della Render Farm di nXt consente di lavorare con gestori di rendering di terze parti. I seguenti procedimenti sono relativi alla Render Farm inclusa con Flamingo nXt. Se prevedete di usare uno dei prodotti di terze parti per il rendering con render farm, alcuni di questi procedimenti saranno diversi.

#### Come funziona la Render Farm
{: #the-farm-process}
 1. Per avviare un rendering con la Farm di Flamingo nXt, anziché usare il comando Rendering standard, si usi la Render Farm *(Menu Flamingo nXt 5.0 &gt; Render Farm)*. In tal modo, si invierà un lavoro di rendering alla [cartella di output Farm](options-flamingo.html#farm-output-folder). Tutti i materiali e le informazioni di supporto verranno inviati automaticamente insieme al relativo lavoro.
 2. I lavori di rendering vengono suddivisi in varie attività diverse. I client della Render Farm controllano continuamente la cartella di output di farm per verificare la disponibilità di nuove attività. Ciascun client sceglie un'attività ed inizia a renderizzare. Il Farm Monitor *(Flamingo nXt 5.0 &gt; Render Farm &gt; Farm Monitor...)* è utile per tenere traccia dello stato di avanzamento dei lavori.
 3. Ciascun client farm deposita i risultati nella cartella farm, sotto *nome lavoro* \Output.
 3. Una volta ultimato un lavoro, ciascun client continua a selezionare dei nuovi lavori, man mano che questi vengono inviati alla farm.
 4. I risultati della Farm saranno nel [formato immagine di nXt (.nXtImage)](image-editor.html). Le immagini con questo formato si possono modificare usando l'[Editor delle immagini di nXt](image-editor.html). Dall'[Editor delle immagini di nXt](image-editor.html), i risultati si possono salvare anche come file TGA, PNG, TIF o JPG.

## Installare e configurare la Farm
{: #install}
Il client di rendering Farmer ed il Farm Monitor vengono installati con Flamingo sulla macchina Rhino master.  Sugli altri computer client che non hanno Rhino e Flamingo nXt, occorre installare il client Farmer.

##### Installare il Render Farmer
Sulle macchine senza Rhino e Flamingo, installare il client Farmer:

 1. Scaricare il [software Render Farmer](http://www.rhino3d.com/download/The-Farm/1.0/release) corrente.
 1. Eseguire il programma di installazione scaricato su ciascun computer client.
 1. Dal menu Start, eseguire il Render Farmer su ciascuna macchina.
 1. Il Render Farmer apparirà sotto forma di icona sulla barra delle applicazioni.

##### Per configurare la Render Farm
{: #configure-the-render-farm}
1.  [Cliccare con il tasto destro](mouse-button-right.html) sull'icona e selezionare Ripristina.
1. Nella finestra nXt Farmer, dal menu Opzioni, cliccare su Percorso e selezionare il percorso della cartella Render Farm.

Sul computer con Rhino e Flamingo nXt, impostare la cartella Zoo in Rhino. Dal menu Strumenti, fare clic su Opzioni ed impostare il percorso comune sulla [cartella di output Farm](options-flamingo.html#farm-output-folder).

La Render Farm ora è configurata.

## Usare la Render Farm
{: #using-the-render-farm-from-flamingo-nxt}
Attualmente la farm può essere usata in tre modi diversi per l'elaborazione dei rendering su più computer: singoli lavori di rendering, lavori batch ed animazioni.

##### Per verificare che le stazioni di lavoro client rispondano
Dopo aver avviato il client Render Farmer su tutti i computer client:

 1. In un computer qualsiasi, dal menu Start di Windows, cliccare su [Farm Monitor](#render-farm-monitor).
 1. Le macchine client dovrebbero apparire nella casella di riepilogo superiore.
 1. Ciascun client Render Farmer dovrebbe apparire sotto l'elenco Macchina.  Lo Stato dovrebbe essere Attivo.

In caso di problemi, rivedere i punti relativi all'[installazionel](#install) ed alla [configurazione](#configure-the-render-farm).


##### Per inviare un lavoro alla Render Farm
1. In Rhino, configurare il rendering e la vista come lo si farebbe per un rendering normale.
1. Dal menu Flamingo nXt, cliccare su Avvia Farm Render.
1. Dovrebbe apparire la finestra di dialogo [Lavoro Farm](#farm-job).
1. Verificare la correttezza delle opzioni e fare clic su OK.


##### Monitoraggio della Farm
Dopo aver inviato un lavoro alla Render Farm, si usi il [Farm Monitor](#render-farm-monitor).

 1. Nel computer master, dal menu Start di Windows, cliccare su [Farm Monitor](#render-farm-monitor).
 1. Nell'elenco dei Lavori dovrebbe apparire un lavoro recente. Ciò può richiedere alcuni minuti per i lavori grandi.
 1. Lo stato del lavoro passa ad essere attivo.
 1. Dopo un certo periodo di tempo, le macchine soprastanti nell'elenco dovrebbero occuparsi delle attività con la stessa data.
 1. La percentuale di completamento aumenta man mano che le attività vengono completate.
 1. Quando il lavoro è finito, il suo stato appare come Completato.


## Opzioni del lavoro Farm
{: #farm-job}

#### Nome
{: #job-name}
Data ed ora vengono anteposte automaticamente al nome scelto. Nella cartella condivisa Render Farm, viene creata una sottocartella per il lavoro. Nella nuova cartella del lavoro, viene inoltre creata una cartella di output.
Una volta ultimato un lavoro, l'output ad esso corrispondente verrà sistemato nella relativa cartella di output.

#### Avvia lavoro
Un lavoro può essere avviato immediatamente dopo il suo invio, in un secondo momento oppure manualmente tramite il Farm Monitor.

#### Ora
Avvia il lavoro ora.

#### Più tardi (manualmente)
Avvia il lavoro più tardi usando il [Farm Monitor](#render-farm-monitor) di nXt.

#### Dopo
Avvia il lavoro quando specificato.

#### Restrizioni di rendering relative al numero di passate
{: #rendering-constraints}
Imposta il numero di passate necessarie per finire il lavoro batch.  Vedi [Passate](documentproperties-flamingo.html#number-of-passes) per maggiori informazioni.


## Farm Monitor della Render Farm
{: #render-farm-monitor}
Il Farm Monitor è un programma autonomo che indica lo stato delle stazioni di lavoro client e riporta i lavori attualmente nella Farm. Dal monitor, i lavori possono essere sospesi e riavviati ed è inoltre possibile escludere una stazione di lavoro client dalla partecipazione alla Render Farm.

Per accedere al Farm Monitor da Rhino, andare al menu di Flamingo nXt 5.0 > Render Farm > Farm Monitor.

Per accedere al Farm Monitor da Windows, dal menu Start, cliccare su **Tutti i programmi > Render Farm di nXt > Farm Monitor**.

#### Opzioni
Cliccare con il tasto destro su una Macchina o su un Lavoro per accedere alle opzioni.

#### Aggiorna
Aggiorna l'elenco dei lavori.

#### Sospendi macchina
Esclude la stazione di lavoro dalla partecipazione alla Render Farm.

#### Riprendi macchina
Fa riprendere alla stazione di lavoro la partecipazione alla Render Farm.

#### Sospendi lavoro
Mette in pausa il lavoro specificato.

#### Riprendi lavoro
Riprende il lavoro specificato.

#### Rimuovi lavoro
Elimina il lavoro specificato dall'elenco.

## Licenze Render Farm
{: #licensing-the-render-farm-}
La Render Farm consente ai computer di rete (nodi) di operare contemporaneamente sui lavori di rendering.  [Scarica ed installa il software client della Render Farm](http://nxt.flamingo3d.com/page/nxt-render-farm).


##### Per autorizzare il nodo
1. Prima di iniziare il processo di ottenimento della licenza, attendere il completamento di eventuali lavori farm attivi.
1. Salvare il codice del prodotto (XF10-J9G2-H006-T8AJ-GBB9-0027) su un file di testo su un percorso di rete in modo tale da poter tagliarlo ed incollarlo facilmente su ciascun nodo.
1. Se il nodo è attualmente attivo, sulla barra delle applicazioni di Windows, [cliccare con il tasto destro](mouse-button-right.html) sull'icona Render Farm e quindi cliccare su **Chiudi**.
1. Cliccare sul pulsante **Start di Windows** e quindi su **Tutti i programmi**.
Nella cartella Render Farm di nXt, cliccare su **Autorizza Farm**.
1. Nella casella di modifica, incollare oppure digitare il codice del prodotto e quindi cliccare su **OK**.

##### Per avviare il nodo
1. Cliccare sul pulsante **Start di Windows** e quindi su **Tutti i programmi**.
Nella cartella Render Farm di nXt, cliccare su **Render Farmer**.
1. [Cliccare con il tasto destro](mouse-button-right.html) sull'icona della barra delle applicazioni e, dal menu, cliccare su **Ripristina**.
1. Dal menu Aiuti, cliccare su **Informazioni**.
Se il numero della versione indica una versione di valutazione, significa che la gestione licenze non è riuscita.
1. Ridurre a icona la finestra Render Farmer per riportarla sulla barra.