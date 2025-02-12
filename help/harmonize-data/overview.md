---
title: Présentation de l’harmonisation des jeux de données
description: Découvrez comment harmoniser les données dans Mix Modeler.
feature: Harmonized Data
exl-id: 6cb70762-e3b2-46a0-b028-1d6daf3edae5
source-git-commit: beee5fe52188f133b71ed3ef53e40c3aea06ab9c
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 8%

---

# Présentation de l’harmonisation des jeux de données

Les données de Mix Modeler sont de nature différente selon la source de données. Les données peuvent être :

* des données agrégées ou récapitulatives, par exemple collectées à partir de sources de données de jardins clos ou de données publicitaires hors ligne collectées (comme les dépenses) à partir de l’exécution d’une campagne d’affichage, d’un événement ou d’une campagne publicitaire physique,
* Données d’événement, provenant par exemple de sources de données propriétaires. Ces données d’événement peuvent être des données collectées via le connecteur source Adobe Analytics d’Adobe Analytics, ou via l’API Experience Platform Web ou Mobile SDK ou Edge Network, ou des données ingérées à l’aide des connecteurs source.

Le service d’harmonisation de Mix Modeler assimile les données agrégées et d’événement en une vue de données cohérente. Cette vue de données, associée aux [données de facteurs internes et externes](#factors), est la source des modèles dans Mix Modeler. Le service utilise la granularité la plus élevée pour les différents jeux de données. Par exemple, si un jeu de données a une granularité mensuelle et que les jeux de données restants ont une granularité hebdomadaire et quotidienne, le service d’harmonisation crée une vue de données à l’aide de la granularité mensuelle.

## Facteurs

Les facteurs sont essentiels à la création de modèles et vous souhaitez comprendre ce qui a un impact holistique sur l’entreprise. Les facteurs peuvent ne pas être liés aux données marketing.

* Les facteurs internes sont spécifiques à votre organisation et peuvent avoir un impact sur vos conversions. Par exemple, votre saison de vente, vos promotions, etc.

* Les facteurs externes sont des facteurs indépendants de la volonté de votre entreprise, mais qui peuvent tout de même avoir un impact sur les conversions que vous réalisez. Par exemple, CPI, S&amp;P 500, etc.



## Exemple de données harmonisées

Imaginons que les jeux de données suivants soient disponibles pour Mix Modeler.

**Jeu de données 1**

Contient un jeu de données d’effort marketing de YouTube, avec une granularité des données agrégées définie sur quotidienne.

| Date | Type de date | Canal | Campagne | Marque | Géo | Clics | Dépenses |
|---|:--:|---|---|---|---|---:|---:|
| 12-31-2021 | day | YouTube | Y_Fall_02 | BrandX | US | 10000 | 100 |
| 01-01-2022 | day | YouTube | Y_Fall_02 | BrandX | US | 1000 | 10 |
| 01-03-2022 | day | YouTube | Y_Fall_01 | BrandY | CA | 10000 | 100 |
| 01-04-2022 | day | YouTube | Y_Summer_01 | Null | CA | 9000 | 80 |

{style="table-layout:auto"}


**Jeu de données 2**

Contient le jeu de données d’effort marketing de Facebook, avec une granularité des données agrégées définie sur hebdomadaire.

| Date | Type de date | Canal | Campagne | Géo | Clics | Dépenses |
|--- |:---:|--- |---|---|---:|---:|
| 01-01-2022 | semaine | Facebook | FB_Fall_01 | US | 8000 | 100 |
| 01-08-2022 | semaine | Facebook | FB_Fall_02 | US | 1000 | 10 |
| 01-08-2022 | semaine | Facebook | FB_Fall_01 | US | 7000 | 100 |
| 01-16-2022 | semaine | Facebook | FB_Summer_01 | CA | 10000 | 80 |

{style="table-layout:auto"}


**Jeu de données 3**

Un jeu de données de conversion, avec une granularité du jeu de données agrégé sur quotidien.

| Date | Type de date | Géo | Objectif | Chiffre d’affaires |
|--- |:---: |---|---|---:|
| 01-01-2022 | day | US | Mode | 200 |
| 01-08-2022 | day | US | Mode | 10 |
| 01-08-2022 | day | US | Bijoux | 1100 |
| 01-16-2022 | day | CA | Bijoux | 80 |

{style="table-layout:auto"}


**Jeu de données 4**

Exemple de jeu de données d’événement d’expérience (événements Web SDK) du client.

| Date et heure | Espace de noms d’identité | Identifiant De L’Identité | Canal | Clics |
|--- |--- |--- |--- |---:|
| 01-01-2022 00:01:01.000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 01-01-2022 00:01:01.000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 01-08-2022 00:01:01.000 | ECID | 2ca2a16e-caf0-4fa9-9a8b-9774b39547c4 | CSE | 1 |
| 01-08-2022 00:01:01.000 | ECID | 5ce99bfb-e44a-40d9-b8cd-c5408bda7cdc | CSE | 1 |

{style="table-layout:auto"}


Vous souhaitez créer un jeu de données harmonisé, avec une granularité définie sur hebdomadaire. Les données d’événement sont agrégées à la granularité hebdomadaire et ajoutées au jeu de données harmonisé. Le résultat est :

**Jeu de données harmonisé**

| Date | Type de date | Canal | Campagne | Marque | Géo | Objectif | Clics | Dépenses | Chiffre d’affaires |
|--- |:---:|--- |--- |--- |---|---|---:|---:|---:|
| 12-27-2021 | semaine | YouTube | Y_Fall_02 | BrandX | US | Null | 11000 | 110 | Null |
| 01-03-2022 | semaine | YouTube | Y_Fall_01 | BrandY | CA | Null | 10000 | 100 | Null |
| 01-03-2022 | semaine | YouTube | Y_Summer_01 | Null | CA | Null | 9000 | 80 | Null |
| 01-01-2022 | semaine | Facebook | FB_Fall_01 | Null | US | Null | 8000 | 100 | Null |
| 01-08-2022 | semaine | Facebook | FB_Fall_02 | Null | US | Null | 1000 | 10 | Null |
| 01-08-2022 | semaine | Facebook | FB_Fall_01 | Null | US | Null | 7000 | 100 | Null |
| 01-16-2022 | semaine | Facebook | FB_Summer_01 | Null | CA | Null | 10000 | 80 | Null |
| 12-27-2021 | semaine | Null | Null | Null | US | Mode | Null | Null | 200 |
| 01-03-2022 | semaine | Null | Null | Null | US | Mode | Null | Null | 10 |
| 01-03-2022 | semaine | Null | Null | Null | US | Bijoux | Null | Null | 1100 |
| 01-10-2022 | semaine | Null | Null | Null | CA | Bijoux | Null | Null | 80 |
| 01-01-2022 | semaine | CSE | Null | Null | Null | Null | 2 | Null | Null |
| 01-08-2022 | semaine | CSE | Null | Null | Null | Null | 2 | Null | Null |

{style="table-layout:auto"}


## Configurer des données harmonisées

Pour créer un jeu de données harmonisé, comme dans l’exemple simplifié [exemple](#an-example-of-harmonized-data), procédez comme suit :

1. Définissez des [champs harmonisés](fields.md) supplémentaires que vous souhaitez utiliser en plus des champs harmonisés globaux déjà disponibles.
1. Configurez les [règles de jeu de données](dataset-rules.md) pour mapper les champs de vos jeux de données d’événement d’expérience ou agrégés aux champs harmonisés.
1. Définissez les [points de contact marketing](marketing-touchpoints.md) à l’aide des champs standards et harmonisés supplémentaires que vous avez définis.
1. Définissez les [conversions](conversions.md) à l’aide des champs standard et harmonisés supplémentaires que vous avez définis.


## Afficher les données harmonisées

Pour afficher vos données harmonisées, dans l’interface de Mix Modeler :

1. Sélectionnez ![Recherche de données](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized datasets]** dans le rail de gauche.

1. Sélectionnez **[!UICONTROL Harmonized Data]** dans la barre supérieure. Un résumé de vos données harmonisées s’affiche en fonction des champs, des règles des jeux de données, des points de contact marketing et des conversions que vous avez définis.

   1. Pour redéfinir la période sur laquelle est basée la synthèse des données harmonisées, saisissez une période à **[!UICONTROL Date range]** ou utilisez ![Calendrier](/help/assets/icons/Calendar.svg) pour sélectionner une période.

   1. Pour modifier les colonnes de champs harmonisés affichées pour le tableau de données harmonisées, utilisez ![Paramètres](/help/assets/icons/Setting.svg) pour ouvrir la boîte de dialogue **[!UICONTROL Column settings]**.

      1. Sélectionnez ![SelectBox](/help/assets/icons/SelectBox.svg) une ou plusieurs colonnes dans **[!UICONTROL AVAILABLE COLUMNS]** et utilisez ![Chevron droit](/help/assets/icons/ChevronRight.svg) pour ajouter ces colonnes à **[!UICONTROL SELECTED COLUMNS]**.

      1. Sélectionnez ![SelectBox](/help/assets/icons/SelectBox.svg) une ou plusieurs colonnes dans **[!UICONTROL SELECTED COLUMNS]** et utilisez ![Chevron vers la gauche](/help/assets/icons/ChevronLeft.svg) pour supprimer les colonnes sélectionnées et les restaurer dans **[!UICONTROL AVAILABLE COLUMNS]**.

      1. Sélectionnez une colonne dans **[!UICONTROL DEFAULT SORT]** et basculez entre **[!UICONTROL Ascending]** ou **[!UICONTROL Descending]**.

      1. Pour modifier l’ordre des colonnes affichées, vous pouvez déplacer une colonne dans **[!UICONTROL SELECTED COLUMNS]** de haut en bas par glisser-déposer .

   1. Sélectionnez **[!UICONTROL Submit]** pour envoyer les modifications des paramètres des colonnes. Sélectionnez **[!UICONTROL Close]** pour annuler les modifications effectuées.

1. Si d’autres pages sont disponibles, utilisez ![Flèche gauche](/help/assets/icons/ChevronLeft.svg) ou ![Flèche droite](/help/assets/icons/ChevronRight.svg) à **[!UICONTROL Page _x _sur_x_]** pour passer d’une page à l’autre.
