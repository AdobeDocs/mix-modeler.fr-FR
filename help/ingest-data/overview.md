---
title: Présentation de l’ingestion de données
description: Découvrez comment ingérer des données dans Mix Modeler.
feature: Datasets, Event Datasets, Summary Datasets, Aggregate Datasets
exl-id: dc16a601-bbd9-467b-8a7e-c32654d4069a
TQID: https://experienceleague.adobe.com/XPr8Av7skzHBYoU6WtNw8PtHFrPH-MokICrLwoB2-J0
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: e0abf868-dae2-4c1c-83e9-b21799232845
  - id: fbd94e4b-f9b8-42a4-8df5-3f917aabae24
subfeature_v2:
  - id: ad7101f7-ae92-401b-a25a-d3060d42989d
  - id: d1167c89-f64a-42ca-ac95-1d91b7790df2
  - id: ee1bf083-e090-4def-936b-c111d29f42d0
  - id: a4dc3e7d-bd07-4ac8-8e49-ff2e8fecf1e7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
autotag-review: '2026-05-01T09:11:34.506Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 584
ht-degree: 17%

---

# Présentation de l’ingestion de données

Mix Modeler fonctionne avec des données au niveau de l’événement, des données d’effort marketing agrégées ou récapitulatives provenant de divers jardins muraux. Et avec des données agrégées ou récapitulatives provenant de toute autre source, comme de la publicité hors ligne, des facteurs internes ou des facteurs externes.

Les clients peuvent utiliser tous les types de données ingérés dans Experience Platform en tant que jeux de données et basés sur des schémas utilisant XDM ExperienceEvent ou XDM Summary Metrics comme classe de base.

Par exemple :

* Données collectées à l’aide du connecteur source Adobe Analytics. et transformés en jeux de données conformes à la version par défaut ou personnalisée du schéma Adobe Analytics.
* Données collectées à l’aide de l’API Experience Platform Web SDK, Mobile SDK ou Edge Network Server pour collecter les interactions des clients sur le web, les appareils mobiles ou tout autre type d’appareil.
* Données agrégées ou récapitulatives provenant de jardins clos (comme Facebook, YouTube), de sources de trafic ou de données publicitaires hors ligne.
* Données agrégées ou récapitulatives non marketing contenant des facteurs internes ou externes utiles à la création de modèles.

Vous pouvez utiliser n’importe quel type de mécanisme, pris en charge par Experience Platform, pour ingérer vos données au niveau de l’événement d’expérience, vos données d’effort marketing agrégées et vos données provenant d’autres sources. Tels que les SDK Experience Platform, les API, les connecteurs source, ainsi que l’ingestion par lots et en flux continu. Pour en savoir plus sur l’ingestion de vos données dans Experience Platform en vue de leur utilisation dans Adobe Mix Modeler, consultez la [présentation de l’ingestion des données](https://experienceleague.adobe.com/fr/docs/experience-platform/ingestion/home).

## Instructions

Pour ingérer des données dans Experience Platform en vue de les utiliser avec Mix Modeler, suivez ces instructions :

* Il ne doit y avoir aucun chevauchement dans les données incrémentielles ajoutées aux jeux de données.
* Toutes les données d’une seule source doivent être de la même granularité.
* La date et la granularité sont des champs obligatoires dans le schéma sous-jacent pour toutes les données agrégées ingérées en tant que jeux de données
* Le canal est un champ obligatoire dans le schéma sous-jacent pour toutes les données d’effort marketing/de dépenses ingérées en tant que jeux de données.


## Exemples

Vous trouverez ci-dessous quelques exemples de données généralement utilisées dans Mix Modeler au-delà des données d’événement d’expérience plus standard.

+++ Données agrégées sur l’effort marketing

| Géo | Date | Type de date | Canal | Campaign | Click | Gagné | Engagement | Impression | Ouverte | Owned | Envoyés | Dépenses |
|---|:--|---|:---:|---|--:|---|--:|---|---|---|--:|--:|
| AMER | 2021-10-31 | jour | EMAIL | | 12752 | | | | | | 1132945 | |
| AMER | 2021-10-31 | jour | FB | | 148844 | | | | | | | 42111 |
| AMER | 2021-10-31 | jour | YT | | | | 2314452 | | | | | 10540 |
| JPN | 2021-10-21 | jour | EMAIL | | 21089 | | | | | | 3283626 | |
| JPN | 2021-10-21 | jour | SOCIAL | | | | 621 | | | | | 74512 |

{style="table-layout:auto"}

+++

+++ Données de conversion agrégées

| Géo | Date | Type de date | Produit | Unités vendues | Recettes |
|---|:---|:---:|---|--:|--:|
| EMEA | 2021-09-13 | jour | Économie Créatrice | 603 | 36537.68 |
| EMEA | 2021-09-13 | jour | Métaverse | 55 | 21704.37 |
| JPN | 2022-05-30 | jour | Imagerie professionnelle | 487 | 64469.60 |
| JPN | 2022-05-30 | jour | Document Cloud | 642 | 100509.07 |

{style="table-layout:auto"}

+++

+++ Données des facteurs externes

| Données | Type de date | Facteur | Valeur |
|---|:---:|:---:|:---|
| 2020-08-02 | semaine | SPX | 3325.866 |
| 2020-08-09 | semaine | SPX | 3364.158 |
| 2020-08-16 | semaine | SPX | 3385.858 |
| 2020-08-23 | semaine | SPX | 3497.965 |

{style="table-layout:auto"}

+++

Pour utiliser les données dans Mix Modeler, vous avez besoin de données collectées dans des jeux de données et modélisées selon des schémas dans Experience Platform. L’interface de Mix Modeler permet d’accéder facilement aux schémas Experience Platform et à l’interface utilisateur des jeux de données.


## Valider

Pour vérifier si vos données sont correctement disponibles dans Mix Modeler, procédez comme suit :

* Utilisez des visualisations dans la [Présentation](/help/overview.md).
* Téléchargez et examinez des données provenant de l’[Données harmonisées](/help/harmonize-data/overview.md) dans des jeux de données harmonisés.

Pour vérifier si vos données sont correctement ingérées dans Experience Platform, vous pouvez [écrire et exécuter des requêtes SQL à l’aide d’Experience Platform Query Service](https://experienceleague.adobe.com/fr/docs/experience-platform/query/home).


>[!MORELIKETHIS]
>
>Consultez pour plus d’informations sur la gestion des schémas et des jeux de données :
>
>* [Schémas](schemas.md)
>* [Jeux de données](datasets.md)
