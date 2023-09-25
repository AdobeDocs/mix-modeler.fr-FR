---
title: Harmonisation des données
description: Découvrez comment harmoniser les données dans Adobe Mix Modeler.
feature: Harmonized Data
source-git-commit: ac17f5a9fcf036c8e689879578e4b745b789cea3
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 17%

---


# Harmonisation des données

Les données de Adobe Mix Modeler sont de nature différente selon la source de données. Les données peuvent être les suivantes :

* des données agrégées, par exemple, collectées à partir de sources de données du jardin fortifié,
* données d’événement, provenant par exemple de sources de données propriétaires. Ces données d’événement peuvent être collectées via le connecteur source Adobe Analytics à partir d’Adobe Analytics, ou via le SDK Web ou mobile Adobe Experience Platform ou l’API réseau Edge, ou des données ingérées à l’aide des connecteurs source.

Le service d’harmonisation de Adobe Mix Modeler intègre les données agrégées et d’événement dans une vue de données cohérente. Cette vue de données est la source des plans et des modèles dans Adobe Mix Modeler.

## Exemple de données harmonisées

Imaginez que vous disposez des jeux de données suivants pour Adobe Mix Modeler.

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
| 01-01-2022 |  semaine | Facebook | FB_Fall_01 | US | 8000 | 100 |
| 01-08-2022 |  semaine | Facebook | FB_Fall_02 | US | 1000 | 10 |
| 01-08-2022 |  semaine | Facebook | FB_Fall_01 | US | 7000 | 100 |
| 01-16-2022 |  semaine | Facebook | FB_Summer_01 | CA | 10000 | 80 |

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
| 01-01-2022 00:01:01.000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 01-01-2022 00:01:01.000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 01-08-2022 00:01:01.000 | ECID | 2ca2a16e-caf0-4fa9-9a8b-9774b39547c4 | CSE | 1 |
| 01-08-2022 00:01:01.000 | ECID | 5ce99bfb-e44a-40d9-b8cd-c5408bda7cdc | CSE | 1 |

{style="table-layout:auto"}


Vous souhaitez créer un jeu de données harmonisé, avec une granularité définie sur hebdomadaire. Les données d’événement sont agrégées à la granularité hebdomadaire et ajoutées au jeu de données harmonisé. Le résultat est :

**Jeu de données harmonisé**

| Date | Type de date | Canal | Campaign | Marque | Géo | Objectif | Clics | Dépenser | Recettes |
|--- |:---:|--- |--- |--- |---|---|---:|---:|---:|
| 12-27-2021 |  semaine | YouTube | Y_Fall_02 | BrandX | US | Null | 11000 | 110 | Null |
| 01-03-2022 |  semaine | YouTube | Y_Fall_01 | BrandY | CA | Null | 10000 | 100 | Null |
| 01-03-2022 |  semaine | YouTube | Y_Summer_01 | Null | CA | Null | 9000 | 80 | Null |
| 01-01-2022 |  semaine | Facebook | FB_Fall_01 | Null | US | Null | 8000 | 100 | Null |
| 01-08-2022 |  semaine | Facebook | FB_Fall_02 | Null | US | Null | 1000 | 10 | Null |
| 01-08-2022 |  semaine | Facebook | FB_Fall_01 | Null | US | Null | 7000 | 100 | Null |
| 01-16-2022 |  semaine | Facebook | FB_Summer_01 | Null | CA | Null | 10000 | 80 | Null |
| 12-27-2021 |  semaine | Null | Null | Null | US | Mode | Null | Null | 200 |
| 01-03-2022 |  semaine | Null | Null | Null | US | Mode | Null | Null | 10 |
| 01-03-2022 |  semaine | Null | Null | Null | US | Bijoux | Null | Null | 1100 |
| 01-10-2022 |  semaine | Null | Null | Null | CA | Bijoux | Null | Null | 80 |
| 01-01-2022 |  semaine | CSE | Null | Null | Null | Null | 2 | Null | Null |
| 01-08-2022 |  semaine | CSE | Null | Null | Null | Null | 2 | Null | Null |

{style="table-layout:auto"}


## Configurer des données harmonisées

Pour créer un jeu de données harmonisé, comme dans la [example](#an-example-of-harmonized-data), procédez comme suit :

1. Définir d’autres [Champs harmonisés](fields.md) que vous souhaitez utiliser au-delà des champs harmonisés globaux déjà disponibles.
1. Configuration [règles du jeu de données](dataset-rules.md) pour mapper des champs de vos jeux de données d’événements d’agrégat ou d’expérience à des champs harmonisés.
1. Définir [points de contact marketing](marketing-touchpoints.md) en utilisant les champs standards et additionnels que vous avez définis.
1. Définir [conversions](conversions.md) en utilisant les champs standards et additionnels que vous avez définis.


## Affichage des données harmonisées

Pour afficher vos données harmonisées, dans l’interface Adobe Mix Modeler :

1. Sélectionner ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized datasets]** dans le rail de gauche.

1. Sélectionner **[!UICONTROL Harmonized Data]** dans la barre supérieure. Vous voyez un récapitulatif de vos données harmonisées basées sur les champs, les règles de jeu de données, les points de contact marketing et les conversions que vous avez définis.

   1. Pour redéfinir la période sur laquelle repose la récapitulation des données harmonisées, saisissez une période pour la variable **[!UICONTROL Date range]** ou utilisez ![Calendrier](../assets/icons/Calendar.svg) pour sélectionner une période.

   1. Pour modifier les colonnes affichées pour le tableau des données harmonisées, utilisez ![Paramètres](../assets/icons/Setting.svg) pour ouvrir le **[!UICONTROL Column settings]** boîte de dialogue.

      1. Sélectionner ![SelectBox](../assets/icons/SelectBox.svg) une ou plusieurs colonnes de **[!UICONTROL AVAILABLE COLUMNS]** et utilisez ![Chevron à droite](../assets/icons/ChevronRight.svg) pour ajouter ces colonnes à **[!UICONTROL SELECTED COLUMNS]**.

      1. Sélectionner ![SelectBox](../assets/icons/SelectBox.svg) une ou plusieurs colonnes de **[!UICONTROL SELECTED COLUMNS]** et utilisez ![Chevron à gauche](../assets/icons/ChevronLeft.svg) pour supprimer les colonnes sélectionnées et renvoyer ces colonnes à **[!UICONTROL AVAILABLE COLUMNS]**.

      1. Sélectionnez une colonne parmi **[!UICONTROL DEFAULT SORT]** et basculer entre **[!UICONTROL Ascending]** ou **[!UICONTROL Descending]**.

      1. Pour modifier l’ordre d’affichage des colonnes, vous pouvez déplacer une colonne dans **[!UICONTROL SELECTED COLUMNS]** vers le haut et vers le bas par glisser-déposer .

   1. Sélectionner **[!UICONTROL Submit]** pour envoyer vos modifications de paramètres de colonne. Sélectionner **[!UICONTROL Close]** pour annuler les modifications que vous avez apportées.


