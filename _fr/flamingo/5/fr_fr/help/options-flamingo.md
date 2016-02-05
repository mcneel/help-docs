---
title: Options de Flamingo nXt
---


# ![images/options.svg](images/options.svg){: .inline} {{page.title}}
Ces paramètres concernent l'application Flamingo.  Les modifications réalisées ici sont appliquées à Flamingo en général. 

{: #default-decal-link-state}
{% include_relative snippets/snippet-linking.md %}

#### Dossier partagé de la ferme
{: #farm-output-folder}
Le dossier partagé des travaux de la ferme de rendu. Il s'agit également de l'emplacement où la ferme enregistrera les résultats. Utilisez l'icône du dossier ![images/folderopen32x32.png](images/folderopen32x32.png){: .inline} pour choisir un nouvel emplacement.

#### Afficher les lumières marquées
Utilisez cette propriété pour afficher la direction d'une lumière marquée.  Cette option s'applique aux spots et aux distributions de lumière diffuse.

#### Aperçu rapide dans OpenGL
Les miniatures des matériaux sont affichées avec OpenGL avant l'affichage du matériau rendu.  L'affichage des matériaux peut être ainsi plus rapide mais l'image OpenGL peut être différente du matériau réel.

#### Enregistrer les fichiers natifs de l'historique à la fin du rendu
Par défaut, Flamingo enregistre la dernière image rendue en cache au cas où il soit nécessaire de la réafficher dans le futur.