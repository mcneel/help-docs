---
title: Pannello Librerie
---

# ![images/libraries.svg](images/libraries.svg){: .inline} {{page.title}}
Il comando Librerie apre il pannello Librerie per gestire le librerie dei materiali, delle texture e degli ambienti.

I contenuti di rendering possono essere salvati su dei file per creare delle librerie esterne che possono essere condivise dai modelli. I contenuti si possono anche trascinare da una sessione all'altra di Rhino e su una cartella.

I campioni di colore si possono trascinare e rilasciare nello stesso modo.

Il pannello Librerie mostra una vista delle cartelle dei contenuti impostate. Lo si usi per trascinare e rilasciare i contenuti nel modello oppure per memorizzare i contenuti del documento all'esterno del modello.

I materiali sono semplicemente dei file che si trovano sul disco rigido.  Le cartelle delle librerie sono semplicemente delle cartelle di Windows.  Tali cartelle si possono copiare ed incollare e spostare, così come si farebbe con qualsiasi altro file o cartella di Windows.

Si usi la barra degli indirizzi della parte superiore della scheda Librerie per accedere a qualsiasi cartella del computer.

Per ritornare velocemente al percorso delle librerie predefinito, si usi l'icona con la chiave inglese in alto a destra. ![images/library_default.png](images/library_default.png){: .inline}

#### Organizzare le librerie
{: organizing_libraries}
Le librerie sono semplicemente dei file.  Le cartelle si possono copiare ed incollare, così come spostare. Per modificare le cartelle ed i documenti, si usi Windows Explorer. Per specificare altre cartelle come cartelle predefinite della scheda Librerie, si usino le [Impostazioni librerie] ![images/library_default.png](images/library_default.png){: .inline}.

## Libreria dei materiali
{: #material}
I materiali delle librerie sono file che si trovano sul disco rigido.  Una volta assegnato al modello, il materiale viene memorizzato e salvato con il modello. Eventuali modifiche al materiale assegnato non modificano il materiale originale che si trova sul disco rigido.

Per assegnare un materiale ad un modello, trascinarlo e rilasciarlo sul modello. L'assegnazione dei materiali può essere di vari tipi:

#### Assegnazione per livello
Trascinare un materiale direttamente sul nome del livello desiderato all'interno del pannello dei livelli. Si tratta del metodo consigliato, visto che di default il materiale viene assegnato a tutti gli oggetti che si trovano su quel determinato livello. Successive modifiche al materiale possono risultare piuttosto veloci rilasciando semplicemente un altro materiale sul livello.

#### Assegnazione per oggetto
Trascinare un materiale direttamente su un oggetto in qualsiasi vista. In questo modo, l'assegnazione del materiale per livello passa ad essere per oggetto.

#### Assegnazione per blocco
Trascinando un materiale su un blocco, tutti gli oggetti del blocco con assegnazione Per genitore assumeranno quel materiale.  Tutti gli oggetti del blocco aventi assegnazione del materiale Per genitore assumeranno il materiale del blocco.

## Libreria delle piante
{: #plant}
Nella cartella delle librerie predefinita, c'è una cartella di piante.  Da qui, si possono sistemare delle piante nel modello.  Una volta sistemata nel modello, la pianta viene memorizzata e salvata con il modello.  Eventuali modifiche alla pianta assegnata non modificano la pianta originale che si trova sul disco rigido. Per sistemare un pianta nel modello, trascinarla e rilasciarla su una vista. Per ulteriori informazioni, si veda l'argomento della guida in linea [Piante](plants.html).

## Libreria degli ambienti
{: #environment}
Gli ambienti si possono salvare nella libreria.  In questo modo, le impostazioni ambiente si possono passare da un modello all'altro.  Per maggiori informazioni, si veda [Ambienti](environment-tab.html).

## Impostazioni delle librerie
{: #settings}
Si usino le ![images/options.png](images/options.png){: .inline} opzioni delle librerie per cambiare le impostazioni predefinite mostrate nel ![images/library_default.png](images/library_default.png){: .inline} menu.

##### Dove trovo questo comando?
Le opzioni delle librerie sono accessibili in tre modi diversi. 

 1. Scheda Librerie > ![images/library_default.png](images/library_default.png){: .inline} nella parte superiore destra del pannello Librerie > Impostazioni...
 1. Menu Strumenti > Opzioni > Librerie.
 1. Menu > Pannelli > Librerie.


### Mostra contenuti di rendering
Si usi questa opzione per mostrare o nascondere il percorso predefinito dei contenuti di rendering.

#### Usa percorso delle librerie predefinito (Documenti)
Di default, le [librerie di contenuti](libraries.html) sono una sottocartella della cartella *Documenti*.

#### Personalizza
Imposta un percorso personalizzato per le [librerie](libraries.html).   Cambia il percorso predefinito delle [librerie di contenuti](libraries.html) per il computer in uso.

##### Pulsante "Sfoglia"
Apre il browser per specificare un file.

#### Mostra cartella "Documenti"
Nel [pannello Librerie](libraries.html), la cartella "Documenti" designata verrà visualizzata nel menu.

#### Mostra cartelle personalizzate
Nel [pannello Librerie](libraries.html), le cartelle personalizzate designate verranno visualizzate nel menu.