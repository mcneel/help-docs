---
title: Pannello Ambienti
---

# ![images/environment.svg](images/environment.svg){: .inline} {{page.title}}
{: #environment-tab}
Gli ambienti non sono solo ciò che si può vedere nello sfondo di un rendering, ma controllano anche una sfera infinita che racchiude il modello. Gli oggetti all'interno della scena riflettono e rifraggono l'ambiente. La sfera dell'ambiente non è un oggetto selezionabile, ma solo una superficie di riferimento per tutti gli effetti relativi allo sfondo.

L'ambiente influisce sulla parte visibile dello sfondo e sulle riflessioni.  Per gli effetti che influiscono sull'illuminazione della scena, si veda l'argomento della guida in linea [Cielo](sun-and-sky.html).

Flamingo presenta un ambiente speciale denominato [Ambiente di Flamingo predefinito](environment.html)*.  Questo ambiente si sincronizza con l'[Impostazione di illuminazione predefinita](lighting-tab.html) corrente. Usando le [impostazioni di illuminazione predefinite](lighting-tab.html), sia l'illuminazione che l'ambiente vengono impostati sui valori predefiniti  appropriati per la scena.

![images/environment-editor-panel.svg](images/environment-editor-panel.svg){:  #panel_map height="600px" style="float: right"}

##### Dove trovo questo comando?
 1. ![images/environments.png](images/environments.png){: .inline} Scheda ambiente
 1. ![images/icon-render.png](images/icon-render.png){: .inline} Barre degli strumenti Strumenti di rendering > ![images/environments.png](images/environments.png){: .inline} Editor degli ambienti
 1. ![images/menuicon.png](images/menuicon.png){: .inline} Menu > Rendering > Editor degli ambienti
 1. Comando > EditorAmbienti

Il pannello dell'editor degli ambienti è suddiviso in varie sezioni.  I pannelli avanzati possono variare in base al tipo di ambiente.

I colori e le texture si possono trascinare dal campione di colore e rilasciare su qualsiasi altro campione di colore o controllo dell'Editor dei materiali, della  [Tavolozza delle texture](texturepalette.html) o dell'[Editor degli ambienti](environmenteditor.html).
Pannello Ambienti

 1. [Tipo di sfondo](#type)
 1. [Barra delle impostazioni](#settings)
 1. [Elenco degli ambienti](#environment_list)
 1. [Divisore della finestra](#divider)
 1. [Sezione delle proprietà dell'ambiente](#properties)
 1. [Nome](#name)
 1. [Pannelli delle proprietà dell'ambiente](#panels)

## [Tipo di sfondo](#panel_map) ![images/callout_1.svg](images/callout_1.svg){: .inline}
{: #type style="clear: both;"}
Selezionare il tipo di sfondo per il modello.  [Ambiente](#flamingo-environment) è un ambiente di rendering completo e dovrebbe essere l'impostazione predefinita per Flamingo.  Le altre tre impostazioni presentano un'insieme di opzioni molto più semplificato, le quali riflettono vecchi modi di definire gli sfondi. Per ulteriori informazioni, si veda l'argomento della guida in linea [Sfondo semplice di Rhinoceros](http://docs.mcneel.com/rhino/5/help/it-it/commands/environmenteditor.htm#Basic_settings) (Impostazioni ambiente di base).

Nel resto di questo argomento della guida in linea, vengono trattati i tipi di ambiente.

## [Barra delle impostazioni](#panel_map) ![images/callout_2.svg](images/callout_2.svg){: .inline}
{: #settings}
Si usi questa barra per la navigazione nell'elenco degli ambienti.

#### ![images/met_leftarrow.png](images/met-leftarrow.png){: .inline} Freccia indietro
Si sposta a ritroso per passare all'ambiente corrente o agli ambienti selezionati in precedenza.  Per esempio, un ambiente con livelli riflettenti o rifrangenti.  Si usi questa freccia per ritornare all'ambiente genitore dai dettagli di riflessione o rifrazione.

####  ![images/met_rightarrow.png](images/met-rightarrow.png){: .inline} Freccia avanti
Si sposta in avanti per passare agli ambienti selezionati in precedenza.  Per esempio, un ambiente con livelli riflettenti o rifrangenti.  Si usi questa freccia per andare verso l'ambiente genitore dai dettagli di riflessione o rifrazione.

#### ![images/material_editor.png](images/material_editor.png){: .inline} ![images/texture-2dchecker.png](images/texture-2dchecker.png){: .inline} Nome dell'ambiente attualmente selezionato
Mostra il nome dell'ambiente corrente ed il livello di modifica.  Per esempio, in presenza di un livello riflettente o rifrangente, viene visualizzata una ">". Utile per vedere dove l'ambiente è corrente.

#### ![images/library_default.png](images/library_default.png){: .inline} Menu Strumenti
Mostra il [menu Strumenti](#tools-menu).  Si tratta di un vasto menu di comandi, impostazioni e utility che hanno a che vedere con gli ambienti.

#### ![images/help_topics.png](images/help_topics.png){: .inline} Aiuti

## [Elenco degli ambienti](#panel_map) ![images/callout_3.svg](images/callout_3.svg){: .inline}
{: #environment_list}
Elenca tutti gli ambienti contenuti nel modello. Uno degli ambienti viene selezionato come ambiente corrente. L'ambiente corrente viene usato nel rendering. Ai vertici dell'ambiente corrente vengono visualizzati dei triangoletti gialli.

Da questo elenco:

* Cliccare su un Ambiente per renderlo corrente. Una volta selezionato, nei pannelli sottostanti verranno visualizzate le proprietà dell'ambiente. Si veda [Proprietà dei materiali di rendering](#properties) per maggiori informazioni
* Scorrere l'elenco verso l'alto e verso il basso per vedere tutti gli ambienti presenti nel modello.
* Aggiungere un nuovo ambiente usando il pulsante Aggiungi nuovo ![images/add_material.png](images/add_material.png){: .inline} che si trova nella parte inferiore dell'elenco.
* Cliccare con il tasto destro su una miniatura per visualizzare il menu di scelta rapida degli ambienti
* Cliccare con il tasto destro sull'area vuota per visualizzare il menu di scelta rapida nuovo ambiente

###  ![images/add_material.png](images/add_material.png){: .inline} Aggiungi nuovo ambiente
{: ###  ![images/add_material.png](images/add_material.png){: 
Scorrere verso il basso l'elenco degli ambienti per visualizzare l'icona Aggiungi.

Apre la [libreria](libraries.html) dei contenuti di rendering degli ambienti.
Gli ambienti della libreria fungono da modelli per la creazione di nuovi ambienti nel modello.

### Menu di scelta rapida degli ambienti
{: environment_context}
Questo menu è disponibile se si clicca con il tasto destro su un elenco di ambienti.  Si veda [Menu Strumenti](#tools_menu) per maggiori dettagli sulle varie opzioni del menu.

### Menu di scelta rapida per i nuovi ambienti
{: new_envrionment_context}
Questo menu è disponibile se si clicca con il tasto destro su un'area vuota dell'elenco di ambienti.

#### ![images/toolbarlus.png](images/toolbarplus.png){: .inline} Crea nuovo ambiente
Crea un nuovo ambiente di Flamingo.

#### ![images/import.png](images/import.png){: .inline} Importa ambiente da file...
Usare questo comando per selezionare un ambiente precedentemente esportato.

#### ![images/paste.png](images/paste.png){: .inline} Incolla
Crea un nuovo ambiente in base ai contenuti degli Appunti.

#### ![images/pasteasinstance.png](images/pasteasinstance.png){: .inline} Incolla come istanza
Crea un nuovo ambiente in base ai contenuti degli Appunti, collegato all'originale tramite la creazione di istanze.

#### ![images/grid.png](images/grid.png){: .inline} Griglia
Mostra le anteprime come una griglia di miniature.

#### ![images/list.png](images/list.png){: .inline} Elenco
Mostra le anteprime come un elenco di miniature.

#### ![images/tree.png](images/tree.png){: .inline} Albero
Mostra le anteprime come un albero con i livelli di nidificazione.

#### ![images/horizontal.png](images/horizontal.png){: .inline} Layout orizzontale
Mostra le anteprime a sinistra dei controlli.

#### ![images/showpreview.png](images/showpreview.png){: .inline} Mostra riquadro di anteprima
Mostra le proprietà anteprima della miniatura attualmente selezionata. Impostare la geometria, le dimensioni, lo sfondo ed il comportamento di rotazione.

#### ![images/floatthumbnail.png](images/floatthumbnail.png){: .inline} Rendi mobile
Rende mobile l'immagine di anteprima in una finestra ridimensionabile.

#### Miniature

##### ![images/small.png](images/small.png){: .inline} Piccolo
Imposta le dimensioni delle miniature sulle dimensioni piccole.

##### ![images/medium.png](images/medium.png){: .inline} Medio
Imposta le dimensioni delle miniature sulle dimensioni medie.

##### ![images/large.png](images/large.png){: .inline} Grande
Imposta le dimensioni delle miniature sulle dimensioni grandi.

##### ![images/showlabels.png](images/showlabels.png){: .inline} Mostra etichette
Mostra le etichette dei nomi delle anteprime quando si è nella modalità Griglia.
La modalità Elenco mostra sempre le etichette.

##### ![images/showunits.png](images/showunits.png){: .inline} Mostra unità
Mostra le dimensioni nelle unità del modello.

##### ![images/autoupdatethumbnail.png](images/autoupdatethumbnail.png){: .inline} Autoaggiornamento anteprima
Aggiorna automaticamente tutte le anteprime man mano che cambiano le impostazioni.

##### ![images/updateallpreviews.png](images/updateallpreviews.png){: .inline} Aggiorna tutte le anteprime
Aggiorna le anteprime manualmente quando l'Autoaggiornamento anteprima è disattivato.

## [Divisore della finestra](#panel_map){: .inline} ![images/callout_4.svg](images/callout_4.svg){: .inline}
{: #divider}
Trascinare questo divisore per cambiare l'estensione dell'elenco degli ambienti rispetto all'estensione della sezione delle proprietà dell'ambiente.

## [Sezione delle proprietà dell’ambiente](#panel_map) ![images/callout_5.svg](images/callout_5.svg){: .inline}
{: #properties}

### [Nome dell’ambiente](#panel_map) ![images/callout_6.svg](images/callout_6.svg){: .inline}
{: #name}
Il nome dell'ambiente. Il nome dell'ambiente viene anche salvato come nome del file quando l'ambiente viene esportato nella libreria. **Nota:** Gli ambienti vengono memorizzati nel modello di Rhino; ambienti unici possono avere lo stesso nome in vari modelli di Rhino.

### [Pannelli degli ambienti](#panel_map) ![images/callout_7.svg](images/callout_7.svg){: .inline}
{: #panels}
La sezione delle proprietà degli ambienti è costituita da una serie di pannelli. Se si fa clic sulla barra del titolo grigia di un pannello, il pannello si chiude ed i suoi contenuti vengono nascosti. Per visualizzarne di nuovo i contenuti, fare di nuovo clic sulla barra del titolo.

I pannelli degli ambienti variano in base al tipo di ambiente ed al livello corrente dell'ambiente attivo. Per ulteriori informazioni sui pannelli specifici degli ambienti, si veda [Ambiente di Flamingo](environment.html)

## Menu Strumenti ![images/library_default.png](images/library_default.png){: .inline}
{: tools_menu}
Queste impostazioni appaiono anche nei menu di scelta rapida tramite clic destro delle anteprime e dello sfondo delle anteprime.

#### ![images/currentenvironment.png](images/currentenvironment.png){: .inline} Imposta come ambiente corrente
Rende corrente l'ambiente di destinazione.  L'ambiente corrente verrà usato nel rendering successivo.

#### ![images/toolbarlus.png](images/toolbarplus.png){: .inline} Crea nuovo ambiente
Crea un nuovo ambiente di Flamingo.
<!-- This comes from the page http://docs.mcneel.com/rhino/5/help/en-us/popup_moreinformation/materialthumbnail_contextmenu.htm -->
Queste impostazioni appaiono anche nei menu di scelta rapida tramite clic destro delle anteprime e dello sfondo delle anteprime.

#### ![images/import.png](images/import.png){: .inline} Importa ambiente da file
Importa gli ambienti da un file .renv di Rhino salvato.

#### ![images/savetofile.png](images/savetofile.png){: .inline} Salva su file
Salva un ambiente su un file .renv di Rhino.

#### ![images/changetype.png](images/changetype.png){: .inline} Cambia tipo
Imposta l'ambiente su un tipo diverso.

#### ![images/changetype.png](images/changetype.png){: .inline} Cambia tipo (copia impostazioni simili)
Imposta l'ambiente su un tipo diverso.
Il comportamento predefinito dipende dallo stato attuale della casella [Opzioni di rendering](http://docs.mcneel.com/rhino/5/help/it-it/options/rendering.htm) >  [Copia impostazioni simili quando il tipo di contenuto viene modificato](http://docs.mcneel.com/rhino/5/help/en-us/options/rendering.htm#Copy_similar_settings_when_content_type_is_changed). Se spuntata, le impostazioni compatibili del contenuto precedente verranno copiate in quello nuovo.

#### ![images/reset.png](images/reset.png){: .inline} Reimposta su predefiniti
Modifica tutte le impostazioni dell'ambiente, impostandole su quelle predefinite: sfondo in tinta unita (nero), sfondo riflesso, cielo e sfondo rifratto visibili.

#### ![images/copy.png](images/copy.png){: .inline} Copia
Copia l'ambiente selezionato negli appunti di Windows. I contenuti degli appunti possono quindi venire incollati nell'editor per creare un nuovo ambiente, oppure si possono incollare direttamente in una cartella per creare un file [libreria](libraries.html).

#### ![images/paste.png](images/paste.png){: .inline} Incolla
Crea un nuovo ambiente in base ai contenuti degli Appunti.

#### ![images/pasteasinstance.png](images/pasteasinstance.png){: .inline} Incolla come istanza
Crea un nuovo ambiente in base ai contenuti degli Appunti, collegato all'originale tramite la creazione di istanze.

#### ![images/delete.png](images/delete.png){: .inline} Elimina
Elimina l'ambiente selezionato.

#### ![images/rename.png](images/rename.png){: .inline} Rinomina...
Rinomina l'ambiente selezionato.

#### ![images/duplicate.png](images/duplicate.png){: .inline} Duplica
Copia l'ambiente selezionato su un nuovo ambiente con le stesse impostazioni.

#### ![images/removeinstancing.png](images/removeinstancing.png){: .inline} Rimuovi istanze
Rimuove il collegamento tra gli ambienti [istanziati](#paste-as-instance).

{% include_relative snippets/snippet-contenteditorpreviewoptions.md %}

#### ![images/contentfilter.png](images/contentfilter.png){: .inline} Filtro dei contenuti
Apre la finestra di dialogo [Filtri dei contenuti](content_filters.html).

#### ![images/rename.png](images/rename.png){: .inline} Proprietà
Apre la finestra di dialogo [Proprietà anteprima](previewproperties.html).