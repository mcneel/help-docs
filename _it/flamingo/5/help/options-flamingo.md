---
title: Opzioni di Flamingo nXt
---


# ![images/options.svg](images/options.svg){: .inline} {{page.title}}
Queste impostazioni sono relative all'applicazione Flamingo.  Le modifiche apportate in questa sezione influiscono sul funzionamento generale di Flamingo.

{: #default-decal-link-state}
{% include_relative snippets/snippet-linking.md %}

#### Cartella condivisa Farm
{: #farm-output-folder}
La cartella condivisa per i lavori eseguiti con la render farm. Si tratta anche del percorso in cui la farm salva i suoi risultati. Usare l'icona Cartella ![images/folderopen32x32.png](images/folderopen32x32.png){: .inline} per specificare un nuovo percorso.

#### Mostra luci contrassegnate
Si usi questa proprietà per visualizzare la direzione di una luce contrassegnata.  Questa opzione funziona con le distribuzioni di luce Riflettore e Diffusa.

#### Anteprima rapida in OpenGL
Questa opzione fa sì che le anteprime in miniatura dei materiali inizino da una miniatura OpenGL prima di restituire il materiale renderizzato.  Ciò può portare a delle risposte più veloci sul materiale, ma l'immagine OpenGL può non avvicinarsi al materiale effettivo.

#### Salva i file di cronologia nativi al completamento del rendering
Di default, Flamingo memorizza nella cache l'ultima immagine renderizzata nel caso in cui ci sia bisogno di ritornare ad essa più avanti.