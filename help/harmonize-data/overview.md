---
title: Harmonisation des données
description: Découvrez comment harmoniser les données en Mix Modeler.
feature: Harmonized Data
exl-id: 6cb70762-e3b2-46a0-b028-1d6daf3edae5
source-git-commit: 4f4c7f05e90d73a0ab4865150b1ec4c2af88fc12
workflow-type: tm+mt
source-wordcount: '893'
ht-degree: 8%

---

# Harmonisation des données

Les données en Mix Modeler sont de nature différente selon la source de données. Les données peuvent être les suivantes :

* des données agrégées ou récapitulatives, par exemple, collectées à partir de sources de données de jardins clôturés ou de données publicitaires hors ligne collectées (comme les dépenses) à partir de l’exécution d’une campagne d’affichage, d’un événement ou d’une campagne publicitaire physique,
* données d’événement, provenant par exemple de sources de données propriétaires. Ces données d’événement peuvent être collectées via le connecteur source Adobe Analytics à partir d’Adobe Analytics, ou via le SDK web ou mobile Experience Platform ou l’API réseau Edge, ou encore les données ingérées à l’aide des connecteurs source.

Le service d’harmonisation de Mix Modeler intègre les données agrégées et d’événement dans une vue de données cohérente. Cette vue de données, combinée aux données de facteurs internes et externes, est la source des modèles en Mix Modeler. Le service utilise la granularité la plus élevée parmi les différents jeux de données. Si, par exemple, un jeu de données est avec une granularité mensuelle et les jeux de données restants sont avec une granularité hebdomadaire et quotidienne, le service d’harmonisation crée une vue de données à l’aide d’une granularité mensuelle.

## Exemple de données harmonisées

Imaginez que les jeux de données suivants soient disponibles pour Mix Modeler.

**Jeu de données 1**

Contient le jeu de données des efforts marketing de YouTube, avec une granularité quotidienne de l’ensemble de données agrégées.

| Date | Type de date | Canal | Campaign | Marque | Géo | Clics | Dépenser |
|---|:--:|---|---|---|---|---:|---:|
| 12-31-2021 | day | YouTube | Y_Fall_02 | BrandX | US | 10000 | 100 |
| 01-01-2022 | day | YouTube | Y_Fall_02 | BrandX | US | 1000 | 10 |
| 01-03-2022 | day | YouTube | Y_Fall_01 | BrandY | CA | 10000 | 100 |
| 01-04-2022 | day | YouTube | Y_Summer_01 | Null | CA | 9000 | 80 |

{style="table-layout:auto"}


**Jeu de données 2**

Contient le jeu de données des efforts marketing de Facebook, avec une granularité du jeu de données agrégé sur hebdomadaire.

| Date | Type de date | Canal | Campaign | Géo | Clics | Dépenser |
|--- |:---:|--- |---|---|---:|---:|
| 01-01-2022 | week | Facebook | FB_Fall_01 | US | 8000 | 100 |
| 01-08-2022 | week | Facebook | FB_Fall_02 | US | 1000 | 10 |
| 01-08-2022 | week | Facebook | FB_Fall_01 | US | 7000 | 100 |
| 01-16-2022 | week | Facebook | FB_Summer_01 | CA | 10000 | 80 |

{style="table-layout:auto"}


**Jeu de données 3**

Jeu de données de conversion avec une granularité quotidienne du jeu de données agrégé.

| Date | Type de date | Géo | Objectif | Recettes |
|--- |:---: |---|---|---:|
| 01-01-2022 | day | US | Mode | 200 |
| 01-08-2022 | day | US | Mode | 10 |
| 01-08-2022 | day | US | Bijoux | 1100 |
| 01-16-2022 | day | CA | Bijoux | 80 |

{style="table-layout:auto"}


**Jeu de données 4**

Un exemple de jeu de données d’événement d’expérience (événements SDK Web) du client.

| Date et heure | Espace de noms d’identité | Identité | Canal | Clics |
|--- |--- |--- |--- |---:|
| 01-01-2022 00:01:01,000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 01-01-2022 00:01:01,000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 01-08-2022 00:01:01,000 | ECID | 2ca2a16e-caf0-4fa9-9a8b-9774b39547c4 | CSE | 1 |
| 01-08-2022 00:01:01,000 | ECID | 5ce99bfb-e44a-40d9-b8cd-c5408bda7cdc | CSE | 1 |

{style="table-layout:auto"}


Vous souhaitez créer un jeu de données harmonisé, avec une granularité définie sur hebdomadaire. Les données d’événement sont agrégées à la granularité hebdomadaire et ajoutées au jeu de données harmonisé. Le résultat est :

**Jeu de données harmonisé**

| Date | Type de date | Canal | Campaign | Marque | Géo | Objectif | Clics | Dépenser | Recettes |
|--- |:---:|--- |--- |--- |---|---|---:|---:|---:|
| 12-27-2021 | week | YouTube | Y_Fall_02 | BrandX | US | Null | 11000 | 110 | Null |
| 01-03-2022 | week | YouTube | Y_Fall_01 | BrandY | CA | Null | 10000 | 100 | Null |
| 01-03-2022 | week | YouTube | Y_Summer_01 | Null | CA | Null | 9000 | 80 | Null |
| 01-01-2022 | week | Facebook | FB_Fall_01 | Null | US | Null | 8000 | 100 | Null |
| 01-08-2022 | week | Facebook | FB_Fall_02 | Null | US | Null | 1000 | 10 | Null |
| 01-08-2022 | week | Facebook | FB_Fall_01 | Null | US | Null | 7000 | 100 | Null |
| 01-16-2022 | week | Facebook | FB_Summer_01 | Null | CA | Null | 10000 | 80 | Null |
| 12-27-2021 | week | Null | Null | Null | US | Mode | Null | Null | 200 |
| 01-03-2022 | week | Null | Null | Null | US | Mode | Null | Null | 10 |
| 01-03-2022 | week | Null | Null | Null | US | Bijoux | Null | Null | 1100 |
| 01-10-2022 | week | Null | Null | Null | CA | Bijoux | Null | Null | 80 |
| 01-01-2022 | week | CSE | Null | Null | Null | Null | 2 | Null | Null |
| 01-08-2022 | week | CSE | Null | Null | Null | Null | 2 | Null | Null |

{style="table-layout:auto"}


## Configurer des données harmonisées

Pour créer un jeu de données harmonisé, comme dans la [example](#an-example-of-harmonized-data), procédez comme suit :

1. Définir d’autres [Champs harmonisés](fields.md) que vous souhaitez utiliser au-delà des champs harmonisés globaux déjà disponibles.
1. Configuration [règles du jeu de données](dataset-rules.md) pour mapper des champs de vos jeux de données d’événements d’agrégat ou d’expérience à des champs harmonisés.
1. Définir [points de contact marketing](marketing-touchpoints.md) en utilisant les champs standards et additionnels que vous avez définis.
1. Définir [conversions](conversions.md) en utilisant les champs standards et additionnels que vous avez définis.


## Affichage des données harmonisées

Pour afficher vos données harmonisées, dans l’interface du Mix Modeler :

1. Sélectionner ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized datasets]** dans le rail de gauche.

1. Sélectionner **[!UICONTROL Harmonized Data]** dans la barre supérieure. Un récapitulatif de vos données harmonisées s’affiche en fonction des champs, des règles de jeu de données, des points de contact marketing et des conversions que vous avez définis.

   1. Pour redéfinir la période sur laquelle repose la récapitulation des données harmonisées, saisissez une période pour la variable **[!UICONTROL Date range]** ou utilisez ![Calendrier](../assets/icons/Calendar.svg) pour sélectionner une période.

   1. Pour modifier les colonnes de champ harmonisées affichées pour le tableau Données harmonisées, utilisez ![Paramètres](../assets/icons/Setting.svg) pour ouvrir le **[!UICONTROL Column settings]** boîte de dialogue.

      1. Sélectionner ![SelectBox](../assets/icons/SelectBox.svg) une ou plusieurs colonnes de **[!UICONTROL AVAILABLE COLUMNS]** et utilisez ![Chevron à droite](../assets/icons/ChevronRight.svg) pour ajouter ces colonnes à **[!UICONTROL SELECTED COLUMNS]**.

      1. Sélectionner ![SelectBox](../assets/icons/SelectBox.svg) une ou plusieurs colonnes de **[!UICONTROL SELECTED COLUMNS]** et utilisez ![Chevron à gauche](../assets/icons/ChevronLeft.svg) pour supprimer les colonnes sélectionnées et renvoyer ces colonnes à **[!UICONTROL AVAILABLE COLUMNS]**.

      1. Sélectionnez une colonne parmi **[!UICONTROL DEFAULT SORT]** et basculer entre **[!UICONTROL Ascending]** ou **[!UICONTROL Descending]**.

      1. Pour modifier l’ordre d’affichage des colonnes, vous pouvez déplacer une colonne dans **[!UICONTROL SELECTED COLUMNS]** vers le haut et vers le bas par glisser-déposer .

   1. Sélectionner **[!UICONTROL Submit]** pour envoyer vos modifications de paramètres de colonne. Sélectionner **[!UICONTROL Close]** pour annuler les modifications que vous avez apportées.

1. Si d’autres pages sont disponibles, utilisez ![Flèche vers la gauche](../assets/icons/ChevronLeft.svg) ou ![Flèche vers la droite](../assets/icons/ChevronRight.svg) at **[!UICONTROL Page _x _de_x_]** pour passer d’une page à l’autre.
