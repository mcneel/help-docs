---
layout: fullwidth-page
---

# Guida introduttiva a Flamingo nXt 5®
 
## Installazione

La beta di Flamingo 5 richiede l'installazione di una versione precedente di Flamingo nXt.
Per poter eseguire Flamingo nXt 5, è necessaria la Service Release 12 di Rhino 5.
Dopo aver scaricato ed eseguito il programma di installazione RHI, avviare Rhino.
Note per l'avvio

Questa versione di Flamingo presenta un'interfaccia che si integra con gli strumenti di rendering di Rhino 5. Ciò ha reso necessarie varie modifiche a livello dell'interfaccia di rendering. Al primo avvio di Flamingo, è importante trovarne l'interfaccia:

Il pannello di controllo di Flamingo si trova alla voce del menu Rendering > Flamingo nXt 5 > Mostra pannello di controllo
La scheda Flamingo nXt contiene i controlli specifici di Flamingo:
Cielo
Gestore delle luci
Controlli di illuminazione personalizzati
Opzioni di rendering
Una volta nel pannello di controllo, cliccare con il tasto destro sulla zona del titolo della scheda e selezionare i pannelli:
Librerie
Ambiente
Piano d'appoggio
Etcâ€¦
 
## Per accedere al pannello di controllo di Flamingo
  * Dal menu **Flamingo nXt**, cliccare su **Pannello di controllo**.

  ## Il pannello di controllo di Flamingo nXt
Il **Pannello di controllo** di **Flamingo nXt** fornisce le seguenti schede per impostare un modello per il rendering:

 *  [Materiali](..\materials\materials-tab.html) 
 *  [Illuminazione](../lighting/lighting-tab.html) 
 *  [Ambiente](../environment/environment-tab.html) 
 *  [Rendering](../render/render-tab.html) 

## Nozioni di base sul rendering
 
Il rendering di un modello ultimato comprende quattro passi fondamentali:

 *  [Impostare i materiali](..\materials\materials-tab.html) 
 *  [Impostare l'illuminazione](../lighting/lighting-tab.html) 
 *  [Impostare un ambiente](../environment/environment-tab.html) 
 *  [Impostare le condizioni di rendering](../render/render-tab.html) 

#### Per avviare un rendering

 * Dal menu **Rendering** o **Flamingo nXt**, cliccare su **Renderizza/Rendering**.
- Oppure -

 * Nella barra degli strumenti **Standard**, cliccare sul pulsante **Rendering**.

### Arresta rendering
 

Di default, il processo di rendering continua a rifinire l'immagine, passata dopo passata, fino a quando l'utente non fa clic sul pulsante **Arresta rendering**. In questo modo, è possibile gestire il compromesso tra tempo e qualità. Quanto più si fa durare il rendering, tanto più l'immagine si avvicinerà al risultato &quot;corretto&quot; del rendering completo. È possibile interrompere un rendering in qualsiasi momento.


###  <kbd>Riprendi rendering</kbd> 
 

Cliccando sul pulsante **Arresta rendering**, il processo di rendering viene sospeso una volta completata la passata corrente.

Il pulsante mostra quindi la scritta **Riprendi rendering**. Se si è arrestato il rendering prima di aver raggiunto il numero di passate o le restrizioni di tempo impostate, si può fare clic sul pulsante **Riprendi rendering** per continuare.

Si usino le impostazioni [Numero di passate](..\render\render-window.html#number-of-passes) o [Tempo](..\render\render-window.html#time) che si trovano nella [finestra di rendering](..\render\render-window.html) o in [Proprietà del documento &gt; Flamingo nXt](..\render\documentproperties-flamingo.html) per impostare un punto di arresto automatico.

&#160;

Ultima revisione: 22 Dic 2011 14:45

