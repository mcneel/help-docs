---
---


# ![images/options.svg](images/options.svg){:height="75px" width="75px"} Proprietà del documento: Flamingo nXt
Queste impostazioni si applicano solo al modello corrente. Vi è un compromesso tra il tempo richiesto a completare il rendering e la qualità dell'immagine desiderata.

#### Dove trovo questo comando?
<!-- These locations are not correct.  They need to be updated. -->

 1. ![images/icon-render.png](images/icon-render.png)Barre degli strumenti Strumenti di rendering > ![images/environments.png](images/environments.png) Editor dei materiali
 1. ![images/menuicon.png](images/menuicon.png)Menu > Rendering > Editor degli ambienti
 1. Comando > EditorAmbienti

## Materiali
{: #materials}
Usate questi controlli per cambiare velocemente il modo in cui Flamingo renderizza le superfici di un rendering.  Queste impostazioni non modificano le assegnazioni dei materiali sugli oggetti e sui livelli, ma cambiano il modo in cui Flamingo produce il colore di ciascuna superficie.

#### Usa materiali
{: #use-materials}
Renderizza usando i materiali creati in Flamingo nXt ed i materiali di Rhino. Gli oggetti che non hanno nessun materiale assegnato vengono renderizzati in bianco. Se non sono spuntate né Usa materiali né Usa colore oggetto, tutti gli oggetti verranno renderizzati in bianco.

#### Usa colore oggetto
{: #use-object-color}
Renderizza usando i colori assegnati agli oggetti o ai livelli di Rhino. Nota : Si possono spuntare sia Usa materiali che Usa colore oggetto allo stesso tempo. In tal caso, gli oggetti a cui si sono assegnati dei materiali useranno quei determinati materiali. Gli altri oggetti verranno renderizzati usando i colori assegnati per oggetto o per livello.

#### Canale bagliore
{: #channel}
I materiali che contengono un qualsiasi livello di bagliore si illuminano, ma senza illuminare gli altri oggetti. (Etichettate l'oggetto come luce per fare in modo che illumini gli altri oggetti.)  Impostate il bagliore su un canale per consentire alla luminosità del bagliore di venir regolata dopo il rendering senza dover eseguire di nuovo il rendering.

## Rimbalzi
{: #bounces}
Quando un raggio entra in una scena, esso rimbalza alcune volte prima di essere eliminato.  Limitare il numero di rimbalzi consente un rendering molto più veloce. Tuttavia, se i limiti sono troppo bassi, può mancare qualche effetto oppure si può generare un rendering nero.  I valori predefiniti si addicono alla maggior parte dei rendering, ma in alcuni casi possono richiedere qualche modifica.

#### Riflettente
{: #reflective-bounces}
Determina quanti livelli di riflessione sono permessi; in altre parole, quante volte un raggio di luce viene riflesso da un oggetto. Un valore pari a zero disattiva le riflessioni. Valori maggiori allungano i tempi di rendering. Si aumenti questo valore se c'è una vista rivolta verso una superficie riflettente che riflette una superficie riflettente adiacente ed i riflessi diventano completamente neri.

#### Rifrangente
{: #refractive-bounces}
Determina quanti livelli di rifrazione sono permessi; in altre parole, quante volte un raggio di luce viene rifratto da un oggetto. Un valore pari a zero disattiva le rifrazioni. Valori maggiori allungano i tempi di rendering. Si aumenti questo valore se c'è una vista che guarda attraverso vari strati ed alla fine non ha un aspetto trasparente ma nero.

#### Indiretta
{: #indirect-bounces}
Determina quanti livelli di luce indiretta sono permessi; in altre parole, quante volte un raggio di luce indiretta viene fatto rimbalzare da un oggetto. Un valore pari a zero disattiva le riflessioni. Valori maggiori allungano i tempi di rendering.

## Illuminazione indiretta
{: #indirect-settings}
Le impostazioni di illuminazione indiretta hanno effetto solo sui raggi che rimbalzano da una superficie e portano la luce verso un'altra superficie.

#### Color bleeding
{: #color-bleed}
Il color bleeding controlla la quantità di colore trasferita in un rimbalzo indiretto di luce da una superficie all'altra.  Di default, è impostato sul valore massimo per aumentare la dinamica nel rendering.  

#### Riflessioni Monte Carlo
{: #monte-carlo}
Nell'illuminazione indiretta, Monte Carlo controlla in che modo Flamingo campiona la luce indiretta. Quando è attivo, la luce indiretta presenta abbastanza disturbo nelle prime passate.  Tuttavia, con l'avanzare delle passate, l'effetto complessivo di Monte Carlo diventa un effetto di illuminazione indiretta più sottile e potenzialmente più dettagliato. Le scene che dipendono in gran misura dalla luce indiretta possono trarre vantaggio dalle riflessioni indirette Monte Carlo.

## Miscellanea

#### Usa luci sui livelli disattivi
{: #uselightsonlayersthatareoff}
Usa le sorgenti di luce sui livelli disattivi e le sorgenti di luce nascoste.

### Restrizioni rendering
{: #number-of-passes}
{: #time}
{: #render-constraints}
{% include_relative snippets/snippet-renderconstraints.md %}