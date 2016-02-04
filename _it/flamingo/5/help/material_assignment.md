---
title: Assegnazione dei materiali
---

# ![images/paint.svg](images/paint.svg) {{page.title}}
Gli oggetti di una scena hanno un sorgente per i materiali. Si tratta del luogo da cui attingono il loro materiale di rendering.  I materiali si possono assegnare in vari modi. Il metodo usato per l'assegnazione dei materiali ha un grande effetto sul grado di facilità di modifica e mantenimento successivi del modello.

I materiali si possono assegnare in tre modi. Tutti e tre i modi sono delle gerarchie, per cui un'assegnazione più in basso nell'elenco sovrascriverà un'assegnazione superiore. I tre modi sono:

 1. [Livelli](#bylayer) - Tutti gli oggetti che si trovano nel livello assumeranno il materiale, a meno che non siano in un blocco o abbiano un'assegnazione specifica per oggetto.
 2. [Genitore](#byparent) - Questo modo si usa per gli oggetti contenuti in un blocco.  Gli oggetti aventi un'assegnazione Per genitore assumeranno il materiale del blocco in cui si trovano.
 3. [Singoli oggetti](#byobject) - I materiali si possono assegnare direttamente ad un oggetto, sovrascrivendo qualsiasi altra assegnazione.

L'assegnazione per livello è il metodo più raccomandabile. Usando l'assegnazione per livello, risulta molto facile cambiare il materiale di tutti gli oggetti che si trovano sullo stesso livello. Si usi l'assegnazione per oggetto se ci sono pochi oggetti e non si desidera che essi giacciano su livelli diversi.

I file importati possono avere una qualsiasi di queste tre assegnazioni. Molti file importati avranno assegnazioni Per oggetto.  Convertire il modello ad assegnazioni Per livello può risultare laborioso, ma può essere vantaggioso nel caso in cui si prevedano numerose modifiche ai materiali di rendering.

Una volta assegnato, il materiale viene salvato nel modello corrente.  Un'eventuale modifica del materiale non avrà alcun effetto su quello stesso materiale usato in altri modelli.

## Assegnare i materiali ai livelli
{: #bylayer}
L'assegnazione di un materile per livello applica il materiale a tutti gli oggetti contenuti in quel livello. Si tratta del metodo di assegnazione predefinito. Per cambiare l'assegnazione del materiale del livello, si usi la finestra di dialogo dei [Livelli](http://docs.mcneel.com/rhino/5/help/it-it/commands/layer.htm).
Nota: L'eliminazione di un materiale dall'[Editor dei materiali](material-editor.html) fa sì che tutti gli oggetti prima associati a quel materiale ritornino alla tipologia di assegnazione per livello.

##### Trascinare un materiale su un livello
{: #drag-dropmaterialtolayer}
1. In Rhino, aprire la finestra di dialogo dei [Livelli](http://docs.mcneel.com/rhino/5/help/it-it/commands/layer.htm).
1. Nell'[Elenco dei materiali](material-editor.html#material_list) della scheda Libreria o della scheda Editor dei materiali, trascinare un materiale sul nome di un livello nella finestra di dialogo dei [Livelli](http://docs.mcneel.com/rhino/5/help/it-it/commands/layer.htm).

##### Per assegnare un materiale ad un livello
1. In Rhino, aprire la finestra di dialogo dei [Livelli](http://docs.mcneel.com/rhino/5/help/it-it/commands/layer.htm).
1. Selezionare uno o più livelli e cliccare sulla colonna Materiale.
1. Nella finestra di dialogo Materiale livello, selezionare un materiale dall'elenco a discesa dei materiali.

##### Rimuovere un materiale da un livello
{: #detachmaterialfromlayer}
1. In Rhino, aprire la finestra di dialogo dei [Livelli](http://docs.mcneel.com/rhino/5/help/it-it/commands/layer.htm).
1. Selezionare uno o più livelli e cliccare sulla colonna Materiale.
1. Nella finestra di dialogo Materiale livello, selezionare il materiale predefinito dall'elenco a discesa.

## Assegnare un materiale per genitore
{: #byparent}
Anche se l'assegnazione Per genitore viene usata raramente, risulta utile. Gli oggetti contenuti in un'istanza di blocco manterranno le loro assegnazioni Per livello o Per oggetto. Gli oggetti che usano un'assegnazione Per genitore assumeranno il materiale del blocco in cui si trovano.  In questo modo, gli oggetti contenuti in un'istanza di blocco possono assumere il materiale del blocco genitore.

Per esempio, il modello di una macchina può avere i pneumatici sul livello Pneumatici e le ruote sul livello Ruote. Per il rendering, la carrozzeria della macchina può variare tra singole istanze di blocco. Assegnare Per genitore alla carrozzeria.  Assegnando quindi un materiale al blocco inserito, solo la carrozzeria assumerà quel materiale.

##### Per assegnare un materiale dalle proprietà oggetto
1. Selezionare gli oggetti.
1. Dal menu Modifica, cliccare su Proprietà oggetto ![images/properties.png](images/properties.png) per editare l'oggetto.
1. Nella finestra di dialogo [Proprietà](properties-object.html), scheda Materiale ![images/materialtab.png](images/materialtab.png), sotto Assegna per, fare clic su Per genitore.

## Assegnare i materiali agli oggetti
{: #byobject}
È possibile assegnare un materiale proveniente dalla libreria dei materiali ad un livello oppure ad un oggetto. I materiali di rendering vengono assegnati a ciascun oggetto singolarmente e sono utilizzati dal motore di rendering incorporato in Rhino.
Vedi  [Editor dei materiali](material-editor.html).

L'assegnazione per livello è il metodo più raccomandabile. Si assegni un materiale per oggetto se ci sono pochi oggetti e non si desidera che essi giacciano su livelli diversi.

##### Assegnare un materiale dalle proprietà oggetto
1. Selezionare gli oggetti.
1. Dal menu Modifica, cliccare su Proprietà oggetto ![images/properties.png](images/properties.png) per editare l'oggetto.
1. Nella finestra di dialogo [Proprietà](properties-object.html), scheda Materiali ![images/materialtab.png](images/materialtab.png), sotto Assegna per, fare clic su Per oggetto e quindi fare clic sul materiale dall'elenco.

##### Trascinare un materiale su un singolo oggetto
{: #drag-dropmaterialtoobject}

 * Nell'[Elenco dei materiali](material-editor.html#material_list) della scheda Libreria o della scheda Editor dei materiali, trascinare un materiale su un oggetto. L'oggetto viene evidenziato quando il cursore si trova sul punto esatto per il rilascio.

##### Assegnare un materiale agli oggetti selezionati
1. Selezionare gli oggetti.
1. Nell'[Elenco dei materiali](material-editor.html#material_list) della scheda Libreria o della scheda Editor dei materiali, fare clic con il pulsante destro del mouse su un materiale della tavolozza dei materiali nel modello.
1. Dal menu, fare clic su Assegna materiale agli oggetti selezionati.

##### Selezionare gli oggetti per materiale assegnato
{: #select-objects-with-material-assignment}
1. Nell'[Elenco dei materiali](material-editor.html#material_list) della scheda Libreria o della scheda Editor dei materiali, fare clic con il pulsante destro del mouse su un materiale della tavolozza dei materiali nel modello.
1. Dal menu, cliccare su Seleziona oggetti con questo materiale.

##### Rimuovere l'assegnazione di un materiale per oggetto
{: #removematerialfromobject}
1. Selezionare gli oggetti.
1. Dal menu Modifica, cliccare su Proprietà oggetto.
1. Nella finestra di dialogo [Proprietà](properties-object.html), nella scheda Materiale, alla voce Assegna per, selezionare Livello.