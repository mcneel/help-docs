---
---

# Rendering automatizzato


## Rendering batch
{: #batch-rendering}
I processi batch consentono l'invio di vari lavori da renderizzare automaticamente. Un lavoro batch può specificare una vista ed una risoluzione specifica ed un numero di passate. I rendering batch si possono avviare su una sola macchina oppure si possono inviare ad una [Render Farm](render-farm.html). Aprite l'elenco batch ed aggiungete i lavori a tale elenco. L'elenco dei lavori batch verrà salvato nel modello.

##### Dove trovo questo comando?

 * Menu > Flamingo nXt 5.0 > Altri strumenti > Batch rendering

### Finestra di dialogo Batch rendering
{: #batch-render}
Iniziate aggiungendo un lavoro, quindi modificate le proprietà per impostare i lavori batch.

#### Aggiungi
Ciascun lavoro batch si basa su una vista salvata nel modello.  Fate clic su Aggiungi per selezionare da un elenco di viste nel modello.  Tutte le altre voci di menu si attiveranno una volta che un lavoro viene aggiunto e selezionato.

#### Elimina
Selezionate un lavoro batch esistente.  Quindi, usate Elimina per rimuovere il lavoro dall'elenco batch.

#### Proprietà
Selezionate un lavoro batch esistente, quindi usate Proprietà per impostare le [proprietà di batch rendering](#batch-render-properties).  Tra le proprietà si includono il nome del file, la risoluzione ed il numero di passate per ciascun lavoro.

#### Sposta in alto
Sposta il nome della vista verso l'alto nell'elenco.

#### Sposta in basso
Sposta il nome della vista verso il basso nell'elenco.

#### Elenco batch
{: #batch-list}
Mostra informazioni sull'elenco di viste da renderizzare. Fate doppio clic su un lavoro esistente per editare le [proprietà di batch rendering](#batch-render-properties).

#### Stato del rendering
Mostra informazioni sulle passate, la linea di scansione ed il tempo trascorso del processo batch.

####  Arresta rendering
Arresta il processo batch.

#### Batch rendering localmente
{: #render-batch-locally}
Usa solo il computer corrente per renderizzare i lavori batch. Le immagini renderizzate in uscita verranno salvate nel percorso specificato nelle [proprietà di batch rendering](#batch-render-properties).

####  Manda batch a Render Farm
Invia i lavori batch alla [Render Farm](render-farm.html). I lavori verranno renderizzati da tutti i client della Farm disponibili. Le immagini renderizzate in uscita verranno salvate nella cartella Farm condivisa.

### Proprietà batch rendering
{: #batch-render-properties}

#### Vista da renderizzare
Mostra la vista che verrà renderizzata dal lavoro corrente. Vedi: [Scheda Rendering, Vista da renderizzare](render-tab.html#viewtorender).

#### Nome del file
Cliccate sul pulsante Salva ![images/saveimageas.png](images/saveimageas.png) e specificate un nome file per l'immagine renderizzata.

#### Canale alfa
Salva l'immagine con il canale alfa.  Vedi [Usa lo sfondo con canale alfa](environment-tab.html#alpha) per maggiori informazioni.

#### Usa impostazioni del documento
{: #rendering-resolution}
Di default, si usano le impostazioni di risoluzione del documento corrente per il rendering.  Se avete bisogno di un'altra risoluzione, deselezionate questa casella e specificate una risoluzione. Vedi [Scheda rendering, Risoluzione](render-tab.html#resolution) per maggiori informazioni.

#### Restrizioni di rendering relative al numero di passate
{: #rendering-constraints}
Imposta il numero di passate necessarie per finire il lavoro batch.  Vedi [Passate](documentproperties-flamingo.html#number-of-passes) per maggiori informazioni.

<!-- TODO: Flamingo nXt 5 runs from the RDK.  The need to Flamingo Automate render is not clear.  What is needed to run animations with nxt right now? Alpha channel This needs to be investigated. The rest of this section is commented out.-->

<!-- Commented out until automated render can be determined

## Animations
{: #animation}
There are two ways to create animations in Rhino.  Animations can be configured using [Rhino's Animation toolbar](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#commands/animation.htm) or using the [Bongo](http://bongo.rhino3d.com/) animation plugin.

##### To submit an animation job to the render farm
1. Run the [FlamingoNXtAutomateRender](automate-rendering.html#flamingonxtautomaterender) command.
1. In theConfigure Automated Render Commanddialog, select **Render to farm**.
&#160;
Specify theJob name,and click theOKbutton.
&#160;
Set a type of animation from Rhino'sAnimation setuptoolbar. SelectRenderFullas theCapture method.
&#160;
Record the animation from theAnimationtoolbar. The render jobs will be sent to Render Farm.
&#160;
When the jobs are finished in Render Farm, run theFlamingoNXtAutomateRendercommand again and select all the jobs in the dialog.
&#160;
Click theCopy selected files to specified output folderbutton and select a folder where all the render images will be copied to.


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