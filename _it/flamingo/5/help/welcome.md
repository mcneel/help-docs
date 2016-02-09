---
title: Guida introduttiva a Flamingo
---
<!-- TODO: This page mentions "Work in Progress" and "Flamingo Beta" and has to be updated once Flamingo has been released -->

# ![images/flamingotab.svg](images/flamingotab.svg){: .inline} Guida introduttiva a Flamingo nXt®
Flamingo nXt genera immagini ed animazioni fotorealistiche di alta qualità a partire da modelli 3D all'interno di Rhinoceros Â®. Flamingo nXt 5 è un aggiornamento di Flamingo che si integra con le funzionalità di rendering predefinite di Rhino 5. Attualmente è in fase WIP (work in progress).

Scaricate ed installate Flamingo da qui: [Download di Flamingo nXt 5](http://www.rhino3d.com/download/flamingo/5/beta).

Per partecipare alle discussioni tecniche sul programma, aderite al [forum di Discourse su Flamingo](http://discourse.mcneel.com/c/rendering/flamingo).

## Installazione

* La beta di Flamingo 5 richiede l'installazione di una versione precedente di Flamingo nXt.
* Per poter eseguire Flamingo nXt 5, è necessaria la Service Release 12 di Rhino 5.

Dopo aver scaricato ed eseguito il programma di installazione RHI, avviare Rhino.

Per ricevere supporto tecnico e visionare tutorial, esempi ed informazioni introduttive su **Flamingo nXt**, si visiti il [sito web di Flamingo nXt](http://nxt.flamingo3d.com/).

* [Tutorial](http://nxt.flamingo3d.com/page/tutorial-e-documentazione)
* [Galleria](http://nxt.flamingo3d.com/photo)
* [Supporto tecnico](http://nxt.flamingo3d.com/forum)

## Il pannello di controllo di Flamingo nXt
{: #control-panel}
Questa versione di Flamingo presenta un'interfaccia integrata con gli strumenti di rendering di Rhino 5. Il pannello di controllo di Flamingo nXt fornisce le seguenti schede per impostare un modello per il rendering:

* [Materiali](materials-tab.html)
* [Illuminazione](lighting-tab.html)
* [Ambiente](environment-tab.html)
* [Rendering](render-tab.html)

## Per accedere al pannello di controllo di Flamingo
* Dal menu Flamingo nXt 5.0, cliccare su Pannello di controllo.

## Nozioni di base sul rendering
{: #rendering-basics}
Il rendering di un modello ultimato comprende quattro passi fondamentali:

 1. [Impostare i materiali](material-editor.html)
 1. [Impostare l'illuminazione](lighting-tab.html)
 1. [Impostare un ambiente](environment-tab.html)
 1. [Impostare le condizioni di rendering](render-tab.html)

##### Per avviare un rendering
* Dal menu Rendering o Flamingo nXt, cliccare su Renderizza/Rendering.
* Oppure, nella barra degli strumenti Standard, cliccare sul pulsante Rendering.

### Arresta rendering
Di default, il processo di rendering continua a rifinire l'immagine, passata dopo passata, fino a quando l'utente non fa clic sul pulsante Arresta rendering. In questo modo, è possibile gestire il compromesso tra tempo e qualità. Quanto più si fa durare il rendering, tanto più l'immagine si avvicina al risultato del rendering completo. È possibile interrompere un rendering in qualsiasi momento.

###  Riprendi rendering
Cliccando sul pulsante Arresta rendering, il processo di rendering viene sospeso una volta completata la passata corrente.
Il pulsante mostra quindi la scritta Riprendi rendering. Se si è arrestato il rendering prima di aver raggiunto il numero di passate o le restrizioni di tempo impostate, si può fare clic sul pulsante Riprendi rendering per continuare.

Si usino le impostazioni [Numero di passate](render-window.html#number-of-passes) o [Tempo](render-window.html#time) che si trovano nella [finestra di rendering](render-window.html) o in [Proprietà del documento > Flamingo nXt](documentproperties-flamingo.html) per impostare un punto di arresto automatico.