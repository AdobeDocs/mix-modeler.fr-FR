---
title: Présentation de l’ingestion de données
description: Découvrez comment ingérer des données dans Mix Modeler.
feature: Datasets, Event Datasets, Summary Datasets, Aggregate Datasets
exl-id: dc16a601-bbd9-467b-8a7e-c32654d4069a
source-git-commit: bb05cee1d4e2245cf665e5dcea17a30c5c0cf203
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 10%

---

# Présentation de l’ingestion de données

Mix Modeler fonctionne avec des données au niveau de l’événement, des données d’effort marketing agrégées ou récapitulatives provenant de divers jardins muraux, ainsi que des données agrégées ou récapitulatives provenant de toute autre source, comme de la publicité hors ligne, des facteurs internes ou des facteurs externes.

Les clients peuvent utiliser tous les types de données ingérés dans Experience Platform en tant que jeux de données et basés sur des schémas utilisant XDM ExperienceEvent ou XDM Summary Metrics comme classe de base.

Par exemple :

* les données collectées à l’aide du connecteur source Adobe Analytics et transformées en jeux de données conformes à la version par défaut ou personnalisée du schéma Adobe Analytics, ou
* les données collectées à l’aide de l’API Experience Platform Web SDK, Mobile SDK ou Edge Network Server pour collecter les interactions des clients sur le web, les appareils mobiles ou tout autre type d’appareil,
* des données agrégées ou récapitulatives provenant de jardins clos (comme Facebook, YouTube), de sources de trafic ou de données publicitaires hors ligne,
* données récapitulatives ou agrégées non marketing contenant des facteurs internes ou externes utiles à la création de modèles.

Vous pouvez utiliser n’importe quel type de mécanisme, pris en charge par Experience Platform, pour ingérer vos données au niveau de l’événement d’expérience, vos données d’effort marketing agrégées et vos données provenant d’autres sources. Les mécanismes d’ingestion comprennent les SDK Experience Platform, les API, les connecteurs source, l’ingestion par lots et par flux. Pour en savoir plus sur l’ingestion de vos données dans Experience Platform en vue de leur utilisation dans Adobe Mix Modeler, voir [Présentation de l’ingestion des données](https://experienceleague.adobe.com/fr/docs/experience-platform/ingestion/home).

## Instructions

Pour ingérer des données dans Experience Platform en vue de les utiliser avec Mix Modeler, suivez ces instructions :

* Il ne doit y avoir aucun chevauchement dans les données incrémentielles ajoutées aux jeux de données.
* Toutes les données d’une seule source doivent être de la même granularité.
* La date et la granularité sont des champs obligatoires dans le schéma sous-jacent pour toutes les données agrégées ingérées en tant que jeux de données
* Le canal est un champ obligatoire dans le schéma sous-jacent pour toutes les données d’effort marketing/de dépenses ingérées en tant que jeux de données.


## Exemples

Vous trouverez ci-dessous quelques exemples de données généralement utilisées dans Mix Modeler au-delà des données d’événement d’expérience plus standard.

+++ Données agrégées sur l’effort marketing

| Géo | Date | Type de date | Canal | Campagne | Cliquez sur | Gagné | Engagement | Impression | Ouvrir | Owned | Envoyés | Dépenses |
|---|:--|---|:---:|---|--:|---|--:|---|---|---|--:|--:|
| AMER | 31/10/2021 | day | EMAIL | | 12752 | | | | | | 1132945 | |
| AMER | 31/10/2021 | day | FB | | 148844 | | | | | | | 42111 |
| AMER | 31/10/2021 | day | YT | | | | 2314452 | | | | | 10540 |
| JPN | 21/10/2021 | day | EMAIL | | 21089 | | | | | | 3283626 | |
| JPN | 21/10/2021 | day | SOCIAL | | | | 621 | | | | | 74512 |

{style="table-layout:auto"}

+++

+++ Données de conversion agrégées

| Géo | Date | Type de date | Produit | Unités vendues | Chiffre d’affaires |
|---|:---|:---:|---|--:|--:|
| EMEA | 13/09/2021 | day | Économie Créatrice | 603 | 36537,68 |
| EMEA | 13/09/2021 | day | Métaverse | 55 | 21704,37 |
| JPN | 30/05/2022 | day | Imagerie professionnelle | 487 | 64469,60 |
| JPN | 30/05/2022 | day | Document Cloud | 642 | 100509,07 |

{style="table-layout:auto"}

+++

+++ Données des facteurs externes

| Données | Type de date | Facteur | Valeur |
|---|:---:|:---:|:---|
| 2020-08-02 | semaine | SPX | 3325,866 |
| 2020-08-09 | semaine | SPX | 3364,158 |
| 16/08/2020 | semaine | SPX | 3385,858 |
| 23/08/2020 | semaine | SPX | 3497,965 |

{style="table-layout:auto"}

+++

Pour utiliser les données dans Mix Modeler, vous avez besoin de données collectées dans des jeux de données et modélisées selon des schémas dans Experience Platform. L’interface de Mix Modeler permet d’accéder facilement aux schémas Experience Platform et à l’interface utilisateur des jeux de données.


## Valider

Pour vérifier si vos données sont correctement disponibles dans Mix Modeler, procédez comme suit :

* Utilisez des visualisations dans [Aperçu](/help/overview.md).
* Téléchargez et examinez des données provenant de l’[Données harmonisées](/help/harmonize-data/overview.md) dans des jeux de données harmonisés.

Pour vérifier si vos données sont correctement ingérées dans Experience Platform, vous pouvez [écrire et exécuter des requêtes SQL à l’aide d’Experience Platform Query Service](https://experienceleague.adobe.com/en/docs/experience-platform/query/home).


>[!MORELIKETHIS]
>
>Consultez pour plus d’informations sur la gestion des schémas et des jeux de données :
>
>* [Schémas](schemas.md)
>* [Jeux de données](datasets.md)
