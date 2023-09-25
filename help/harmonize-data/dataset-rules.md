---
title: Règles du jeu de données
description: Découvrez comment définir des règles de jeu de données à utiliser dans le cadre de l’harmonisation de vos données dans Adobe Mix Modeler.
feature: Harmonized Data, Dataset Rules
source-git-commit: ac17f5a9fcf036c8e689879578e4b745b789cea3
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 1%

---


# Règles du jeu de données

Les règles de jeu de données vous aident à mapper vos champs harmonisés avec les champs des données que vous avez ingérées dans Adobe Mix Modeler.

* Pour les données agrégées que vous avez ingérées dans Adobe Experience Platform, vous mappez un ou plusieurs des champs de jeu de données disponibles aux champs harmonisés appropriés.
* Pour les données d’événement, vous pouvez mapper un ou plusieurs champs harmonisés aux champs du jeu de données, directement ou à l’aide de conditions.


## Gestion des règles et des mappages de jeux de données

Pour afficher un tableau des mappages de jeux de données disponibles, dans l’interface Adobe Mix Modeler :

1. Sélectionner ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** dans le rail de gauche.

1. Sélectionner **[!UICONTROL Dataset rules]** dans la barre supérieure. Un tableau des mappages de jeux de données s’affiche.

Les colonnes du tableau spécifient des détails sur les mappages de jeux de données :

| Nom de la colonne | Détails |
| ---------------------- | ----------|
| Jeu de données | Nom du jeu de données. |
| Source | La source du jeu de données, qui peut être Adobe Analytics, les événements d’expérience, le résumé (agrégé) ou les événements d’expérience client. |
| Schéma | Schéma auquel le jeu de données se conforme. Vous pouvez sélectionner rapidement le nom du schéma pour ouvrir le schéma dans un nouvel onglet de l’éditeur de schémas dans Adobe Mix Modeler - Schémas. |
| Granularité | Granularité des données du jeu de données. Les valeurs possibles sont Quotidienne, Hebdomadaire, Mensuelle ou Annuelle. |
| Début de la semaine | Indique le jour de la semaine considéré comme le début d’une nouvelle semaine pour le jeu de données spécifique. |
| Dernière modification | Données et heure de la dernière modification du mappage du jeu de données. |

{style="table-layout:auto"}

### Création d’un mappage de jeu de données

Pour créer un mappage de jeu de données, dans la variable ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** dans Adobe Mix Modeler, sélectionnez **[!UICONTROL Create Dataset Mapping]**.

Dans le **[!UICONTROL Create]** écran,

1. Dans **[!UICONTROL Dataset Details]**, sélectionnez un jeu de données dans **[!UICONTROL Select dataset]** pour commencer la configuration.

1. Sélectionnez un jour pour le **[!UICONTROL Start of the week]**.

1. Sélectionner **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** ou **[!UICONTROL Yearly]** pour **[!UICONTROL Granularity]**.

1. Lorsque vous avez sélectionné une **[!UICONTROL Summary]** type de jeu de données :

   1. Faites correspondre chacune des **[!UICONTROL Available dataset fields]** à **[!UICONTROL Standard harmonized fields]**. Si vous ne souhaitez pas mapper un champ de jeu de données à un champ harmonisé, sélectionnez explicitement **[!UICONTROL -- None --]**.

   1. Si vous avez besoin d’un nouveau champ harmonisé, non disponible dans la liste, sélectionnez **[!UICONTROL Create New]** créer un champ harmonisé. La boîte de dialogue s’affiche, comme indiqué dans la section [Ajouter un nouveau champ harmonisé](fields.md#add-a-harmonized-field) pour vous permettre d’ajouter rapidement un nouveau champ harmonisé.

   1. Lorsque le mappage est terminé pour tous les champs, sélectionnez **[!UICONTROL Save]**. Sélectionner **[!UICONTROL Cancel]** pour annuler le mappage.

      ![Création de règles de jeu de données](../assets/dataset-create-summary.png)

1. Lorsque vous avez sélectionné un type d’événement d’un jeu de données, dans la zone ombrée en dessous **[!UICONTROL Map to harmonized fields]**:

   1. Sélectionnez un champ harmonisé depuis **[!UICONTROL Standard harmonized field]**.

   1. Lorsque le champ harmonisé sélectionné est de type mesure :

      1. Sélectionner **[!UICONTROL Count]** ou **[!UICONTROL Sum]** de **[!UICONTROL Mapping type]**.

      1. Sélectionnez une **[!UICONTROL *Champ de jeu de données AEP *]**que vous souhaitez que le champ harmonisé soit mappé par défaut.

   1. Lorsque le champ sélectionné est de type dimension :

      1. Sélectionner **[!UICONTROL Map Into]** ou **[!UICONTROL Case]** de **[!UICONTROL Mapping type]**.

      1. Lorsque vous avez sélectionné **[!UICONTROL Map Into]**, sélectionnez **[!UICONTROL Field]** et **[!UICONTROL *Champ de jeu de données AEP *]**ou **[!UICONTROL Value]**et une valeur par défaut pour mapper le champ harmonisé par défaut au champ du jeu de données ou à la valeur saisie.

      1. Lorsque vous sélectionnez **[!UICONTROL Case]**, sélectionnez **[!UICONTROL Field]** et **[!UICONTROL *Champ de jeu de données AEP *]**ou **[!UICONTROL Value]**et une valeur par défaut pour mapper le champ harmonisé par défaut au champ du jeu de données ou à la valeur saisie.

         1. En outre, vous définissez un ou plusieurs cas, composés d’une ou de plusieurs conditions pour définir explicitement des valeurs. Chaque condition peut rechercher une **[!UICONTROL *Champ de jeu de données AEP *]**si **[!UICONTROL Exists]**ou **[!UICONTROL Not Exists]**ou **[!UICONTROL Contains]**,**[!UICONTROL Not Contains]**,**[!UICONTROL Equals]**,**[!UICONTROL Not Equals]**,**[!UICONTROL Starts With]**, ou **[!UICONTROL Ends With]**une valeur saisie à l’adresse**[!UICONTROL * Entrée de la valeur *]**.

         1. Pour ajouter un autre cas, sélectionnez ![Ajouter](../assets/icons/AddCircle.svg) **[!UICONTROL Add case]**, pour ajouter une autre condition, sélectionnez ![Ajouter](../assets/icons/AddCircle.svg) **[!UICONTROL Add condition]**.

         1. Pour supprimer un cas ou une condition, sélectionnez ![Fermer](../assets/icons/Close.svg) dans le conteneur correspondant.

         1. Pour sélectionner si l’une des conditions ou toutes celles qui s’appliquent à un cas, sélectionnez **[!UICONTROL Any of]** ou **[!UICONTROL All of]**.

         1. Pour définir la valeur de résultat d’un cas, saisissez la valeur à l’adresse **[!UICONTROL Then]**.

      L’exemple ci-dessous

      * utilise une **[!UICONTROL Map Into]** **[!UICONTROL Mapping type]** pour mapper la variable **[!UICONTROL Channel Type At Source]** du champ harmonisé vers le champ **[!UICONTROL channel_type]** du champ **[!DNL Luma Transactions]** jeu de données.

      * utilise une **[!UICONTROL Case]** **[!UICONTROL Mapping]** type pour mapper de manière conditionnelle la valeur de la variable **[!UICONTROL marketing.campaignName]** dans le champ **[!DNL Luma Transactions]** du jeu de données **[!UICONTROL Campaign]** Champ harmonisé. Le champ Harmonisation de la campagne est défini sur :

         * `Black Friday` lorsque la variable **[!UICONTROL marketing.campaignName]** is `_black_friday` ou `BlackFriday`.
         * à la valeur de la variable **[!UICONTROL marketing.campaignName]** dans tous les autres cas.

        ![Événement de règle de jeu de données](../assets/dataset-create-event.png)

1. Sélectionner ![Ajouter](../assets/icons/AddCircle.svg) **[!UICONTROL Add field]** pour définir des champs supplémentaires.

Lorsque vous avez terminé, sélectionnez **[!UICONTROL Save]** pour enregistrer le mappage, ou sélectionnez **[!UICONTROL Cancel]** pour annuler le mappage.


### Modification d’un mappage de jeu de données

Pour modifier un mappage de jeu de données, dans la variable ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** Interface dans Adobe Mix Modeler :

1. Sélectionner ![Plus](../assets/icons/More.svg) dans le **[!UICONTROL Dataset]** pour le mappage du jeu de données que vous souhaitez modifier.
1. Dans le menu contextuel, sélectionnez ![Modifier](../assets/icons/Edit.svg) **[!UICONTROL Edit]** pour commencer à modifier le mappage du jeu de données. Voir [Création d’un mappage de jeu de données](#create-a-dataset-mapping) pour plus d’informations.


### Suppression d’un mappage de jeu de données

Pour supprimer un mappage de jeu de données, dans la variable ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** Interface dans Adobe Mix Modeler :

1. Sélectionner ![Plus](../assets/icons/More.svg) dans le **[!UICONTROL Dataset]** pour le mappage du jeu de données que vous souhaitez supprimer.
1. Dans le menu contextuel, sélectionnez ![Supprimer](../assets/icons/Delete.svg) **[!UICONTROL Delete]** pour supprimer le mappage du jeu de données.


## Synchroniser les données

Pour synchroniser les données entre vos données harmonisées et vos jeux de données de résumé et/ou d’événement, en suivant toute la logique de vos règles de jeu de données :

1. Sélectionnez **[!UICONTROL Sync data]**.

1. Dans la **[!UICONTROL Sync data for dataset rules]** , sélectionnez l’une des options suivantes : **[!UICONTROL Refresh harmonized data for summary datasets]**, **[!UICONTROL Refresh harmonized data for event datasets]**, ou **[!UICONTROL Refresh harmonized data for both summary + event datasets]**.

1. Sélectionner **[!UICONTROL Sync]** pour démarrer la synchronisation en fonction des règles définies du jeu de données entre les données harmonisées et les données des jeux de données. Pour annuler la synchronisation, sélectionnez **[!UICONTROL Cancel]**.

   ![Synchroniser les données](../assets/sync-data.png)

