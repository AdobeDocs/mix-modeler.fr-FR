---
title: Ingestion de données
description: Découvrez comment ingérer des données dans Mix Modeler.
feature: Datasets, Event Datasets, Summary Datasets, Aggregate Datasets
source-git-commit: 7778c235b4d34bc91869098961b053b2455ff5b3
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 16%

---


# Ingestion de données

Mix Modeler fonctionne avec des données au niveau de l’événement, des données agrégées d’effort marketing provenant de divers jardins muraux et des données agrégées ou récapitulatives provenant de toute autre source, comme la publicité hors ligne, des facteurs internes ou des facteurs externes.

Les clients peuvent utiliser n’importe quel type de données ingéré dans Adobe Experience Platform en tant que jeux de données et basé sur des schémas à l’aide de XDM ExperienceEvent ou de XDM Summary Metrics en tant que classe de base.

Par exemple :

* les données collectées à l’aide du connecteur source Adobe Analytics et transformées en jeux de données conformes à la version par défaut ou personnalisée du schéma Adobe Analytics, ou, à l’inverse,
* données collectées à l’aide du SDK Web Adobe Experience Platform, du SDK mobile ou de l’API Edge Network Server pour collecter les interactions des clients sur le web, le mobile ou tout autre type d’appareil,
* données agrégées provenant de jardins muraux (comme Facebook, YouTube), de sources de trafic ou de données publicitaires hors ligne,
* données agrégées ou récapitulatives non marketing contenant des facteurs internes ou externes utiles à la création de modèles.

Vous pouvez utiliser n’importe quel mécanisme, pris en charge par Adobe Experience Platform, pour ingérer votre niveau d’événement d’expérience, des données agrégées sur l’effort marketing et des données provenant d’autres sources. Tels que les SDK Adobe Experience Platform, les API, les connecteurs source et l’ingestion par flux et par lots.


## Instructions

Pour ingérer des données dans Adobe Experience Platform en vue de les utiliser avec Mix Modeler, suivez ces instructions :

* Il ne doit pas y avoir de chevauchement dans les données incrémentielles ajoutées aux jeux de données.
* Toutes les données provenant d’une seule source doivent être de la même granularité.
* La date et la granularité sont des champs obligatoires du schéma sous-jacent pour toutes les données agrégées ingérées en tant que jeux de données.
* Le canal est un champ obligatoire dans le schéma sous-jacent pour toutes les données de dépenses/efforts marketing ingérées en tant que jeux de données.


## Exemples

Vous trouverez ci-dessous quelques exemples de données généralement utilisées en Mix Modeler au-delà des données d’événement d’expérience standard.

+++ Agréger les données de l’effort marketing

| Géo | Date | Type de date | Canal | Campaign | Cliquez sur | Gagné | Engagement | Impression | Ouvrir | Détenu | Envoyés |
|---|:--|---|:---:|---|--:|---|--:|---|---|---|--:|
| AMER | 2021-10-31 | day | EMAIL | | 12752 | | | | | | 1132945 |
| AMER | 2021-10-31 | day | FB | | 148844 | | | | | | |
| AMER | 2021-10-31 | day | YT | | | | 2314452 | | | | |
| JPN | 2021-10-21 | day | EMAIL | | 21089 | | | | | | 3283626 |
| JPN | 2021-10-21 | day | SOCIAL | | | | 621 | | | | |

{style="table-layout:auto"}

+++

+++ Agrégat des données de conversion

| Géo | Date | Type de date | Produit | Unités vendues | Recettes |
|---|:---|:---:|---|--:|--:|
| EMEA | 2021-09-13 | day | L&#39;économie créatrice | 603 | 36537.68 |
| EMEA | 2021-09-13 | day | Métaverse | 55 | 21704.37 |
| JPN | 2022-05-30 | day | Pro Imaging | 487 | 64469.60 |
| JPN | 2022-05-30 | day | Document Cloud | 642 | 100509.07 |

{style="table-layout:auto"}

+++

+++ Données de facteurs externes

| Données | Type de date | Facteur | Valeur |
|---|:---:|:---:|:---|
| 2020-08-02 |  semaine | SPX | 3325.866 |
| 2020-08-09 |  semaine | SPX | 3364.158 |
| 2020-08-16 |  semaine | SPX | 3385.858 |
| 2020-08-23 |  semaine | SPX | 3497.965 |

{style="table-layout:auto"}

+++

Pour utiliser des données dans Mix Modeler, vous avez besoin de données collectées dans des jeux de données et modélisées selon des schémas dans Adobe Experience Platform. L’interface du Mix Modeler permet d’accéder facilement à l’interface utilisateur des schémas et des jeux de données.


>[!MORELIKETHIS]
>
>Voir pour plus d’informations sur la gestion des schémas et des jeux de données :
>
>* [Schémas](schemas.md)
>* [Jeux de données](datasets.md)
