---
title: Ingestion de données
description: Découvrez comment ingérer des données dans Mix Modeler.
feature: Datasets, Event Datasets, Summary Datasets, Aggregate Datasets
exl-id: dc16a601-bbd9-467b-8a7e-c32654d4069a
source-git-commit: 86732fe30637aa72ced232d9f331a3cc64baa39b
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 12%

---

# Ingestion de données

Mix Modeler utilise des données au niveau de l’événement, agrège un résumé des données de l’effort marketing de différents jardins muraux et agrège ou résume les données de toute autre source, comme la publicité hors ligne, les facteurs internes ou les facteurs externes.

Les clients peuvent utiliser n’importe quel type de données ingéré dans Experience Platform en tant que jeux de données et basé sur des schémas à l’aide de XDM ExperienceEvent ou de XDM Summary Metrics en tant que classe de base.

Par exemple :

* les données collectées à l’aide du connecteur source Adobe Analytics et transformées en jeux de données conformes à la version par défaut ou personnalisée du schéma Adobe Analytics, ou, à l’inverse,
* données collectées à l’aide du SDK Web Experience Platform, du SDK mobile ou de l’API Edge Network Server pour collecter les interactions des clients sur le web, le mobile ou tout autre type d’appareil,
* données agrégées ou récapitulatives provenant de jardins murs (comme Facebook, YouTube), de sources de trafic ou de données publicitaires hors ligne,
* données agrégées ou récapitulatives non marketing contenant des facteurs internes ou externes utiles à la création de modèles.

Vous pouvez utiliser n’importe quel mécanisme, pris en charge par Experience Platform, pour ingérer vos données d’événement d’expérience, d’effort marketing agrégé et de données provenant d’autres sources. tels que les SDK, les API, les connecteurs source, ainsi que la diffusion en continu et l’ingestion par lots Experience Platform.


## Instructions

Pour ingérer des données dans Experience Platform en vue de les utiliser avec Mix Modeler, suivez ces instructions :

* Il ne doit pas y avoir de chevauchement dans les données incrémentielles ajoutées aux jeux de données.
* Toutes les données provenant d’une seule source doivent être de la même granularité.
* La date et la granularité sont des champs obligatoires du schéma sous-jacent pour toutes les données agrégées ingérées en tant que jeux de données.
* Le canal est un champ obligatoire dans le schéma sous-jacent pour toutes les données de dépenses/efforts marketing ingérées en tant que jeux de données.


## Exemples

Vous trouverez ci-dessous quelques exemples de données généralement utilisées en Mix Modeler au-delà des données d’événement d’expérience plus standard.

+++ Agréger les données de l’effort marketing

| Géo | Date | Type de date | Canal | Campagne | Cliquez sur | Gagné | Engagement | Impression | Ouvrir | Détenu | Envoyés |
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
| EMEA | 2021-09-13 | day | L&#39;économie créatrice | 603 | 36537,68 |
| EMEA | 2021-09-13 | day | Métaverse | 55 | 21704,37 |
| JPN | 2022-05-30 | day | Pro Imaging | 487 | 64469,60 |
| JPN | 2022-05-30 | day | Document Cloud | 642 | 100509,07 |

{style="table-layout:auto"}

+++

+++ Données de facteurs externes

| Données | Type de date | Facteur | Valeur |
|---|:---:|:---:|:---|
| 2020-08-02 | week | SPX | 3325,866 |
| 2020-08-09 | week | SPX | 3364,158 |
| 2020-08-16 | week | SPX | 3385,858 |
| 2020-08-23 | week | SPX | 3497,965 |

{style="table-layout:auto"}

+++

Pour utiliser des données dans Mix Modeler, vous avez besoin de données collectées dans des jeux de données et modélisées selon des schémas dans Experience Platform. L’interface du Mix Modeler permet d’accéder facilement aux schémas et aux jeux de données Experience Platform.


>[!MORELIKETHIS]
>
>Voir pour plus d’informations sur la gestion des schémas et des jeux de données :
>
>* [Schémas](schemas.md)
>* [Jeux de données](datasets.md)
