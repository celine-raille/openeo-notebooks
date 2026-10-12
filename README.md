# openeo-notebooks
Ce dépôt contient des notebooks permettant d'exécuter des traitements sur l'aggrégateur OpenEO CNES avec le clien python OpenEO.

Il contient actuellement les notebooks suivants :
- *decouvrir_microservices.ipynb :* Pour se familiariser avec les différents microservices OpenEO.
- *demo_ndwi.ipynb :* Calcul du NDWI moyen mensuel sur Toulouse pour l'année 2022.
- *demo_ndwi_with_udp.ipynb :* Le même que le précédent mais en utilisant une UDP (user-defined process) pour le calcul du NDWI.
- *masques_de_neige.ipynb :* Génération d'un masque de neige sur la tuile 31TCH pour une sélection de dates.
- *flags_points_valide.ipynb :* Calcul du NOBS (nombre d'observations claires) sur les mêmes images que le notebook précédent.
- *masques_de_sol.ipynb :* Génération d'un masque de sol (eau et végétation) sur Tournefeuille.

## Prérequis

**Avoir un compte sur le backend OpenEO CNES.**

Pour cela, lors de votre première connexion (avec le notebook de votre choix), vous devez vous créer un compte (bouton *Create account*).

Une fois les champs remplis et le compte créé, vous allez tomber sur une erreur : c'est normal et lié au fait que l'envoi de mails n'a pas encore été intégré.

Ce n'est pas bloquant : vous pouvez fermer la pop-up puis vous reconnecter avec le compte que vous venez de créer.


## Exécution sur TREX

Un kernel **openeo_kernel_comet** a été mis à disposition et contient toutes les bibliothèques requises pour l'exécution de ces notebooks.

Pour y accéder, il faut ajouter dans son .bashrc les deux lignes suivantes :
```
export JUPYTER_PATH="$JUPYTER_PATH:/softs/projets/openeo"
export JUPYTER_PATH_INHERIT=true
```

En vous connectant au JupyterHub, vous pourrez voir et sélectionner le kernel.


## Exécution hors de TREX

Les notebooks peuvent s'exécuter sur n'importe quel jupyter local.
Bibliothèques requises:
- openeo
- xarray
- zarr
- rasterio
- matplotlib

Il est également possible de les exécuter en ligne. Nous vous recommandons [Google Colab](https://colab.research.google.com/) (attention, il faut un compte Google).
