---
title: Règles du jeu de données
description: Découvrez comment définir des règles de jeu de données à utiliser dans le cadre de l’harmonisation de vos données dans Mix Modeler.
feature: Harmonized Data, Dataset Rules
exl-id: 57d7940a-2900-4814-a30d-bb02bff7615d
source-git-commit: 4f4c7f05e90d73a0ab4865150b1ec4c2af88fc12
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 1%

---

# Règles du jeu de données

Les règles de jeu de données vous aident à mapper vos champs harmonisés avec les champs des données que vous avez ingérées dans Mix Modeler.

* Pour les données agrégées que vous avez ingérées dans Adobe Experience Platform, vous mappez un ou plusieurs des champs de jeu de données disponibles aux champs harmonisés appropriés.
* Pour les données d’événement, vous pouvez mapper un ou plusieurs champs harmonisés aux champs du jeu de données, directement ou à l’aide de conditions.


## Gestion des règles de jeu de données

Pour afficher un tableau des règles de jeu de données disponibles, dans l’interface du Mix Modeler :

1. Sélectionner ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** dans le rail de gauche.

1. Sélectionner **[!UICONTROL Dataset rules]** dans la barre supérieure. Un tableau des règles du jeu de données s’affiche.

Les colonnes du tableau spécifient des détails sur les règles du jeu de données :

| Nom de la colonne | Détails |
| ---------------------- | ----------|
| Jeu de données | Nom du jeu de données. |
| Source | La source du jeu de données, qui peut être Adobe Analytics, les événements d’expérience, le résumé (agrégé) ou les événements d’expérience client. |
| Schéma | Schéma auquel le jeu de données se conforme. Vous pouvez sélectionner rapidement le nom du schéma pour ouvrir le schéma dans un nouvel onglet de l’éditeur de schémas de Mix Modeler - Schémas. |
| Granularité | Granularité des données du jeu de données. Les valeurs possibles sont Quotidienne, Hebdomadaire, Mensuelle ou Annuelle. |
| Début de la semaine | Indique le jour de la semaine considéré comme le début d’une nouvelle semaine pour le jeu de données spécifique. |
| Statut | État du champ : <p><span style="color:gray">●</span> Version préliminaire ou <p><span style="color:green">●</span> Actif |
| Dernière modification | Données et heure de la dernière modification de la règle du jeu de données. |

{style="table-layout:auto"}

### Créer une règle de jeu de données

Pour créer une règle de jeu de données, dans la variable ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** dans Mix Modeler, sélectionnez **[!UICONTROL Create Dataset rule]** dans le **[!UICONTROL Dataset rules configuration]** assistant.

Dans le **[!UICONTROL Create]** écran,

1. Dans **[!UICONTROL Dataset details]**, sélectionnez un jeu de données dans **[!UICONTROL Select dataset]** pour commencer la configuration. Dans la liste, les jeux de données sont classés dans **[!UICONTROL Consumer Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Experience Event]** et **[!UICONTROL Summary]**.

1. Sélectionnez un jour pour le **[!UICONTROL Start of the week]**.

1. Sélectionner **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** ou **[!UICONTROL Yearly]** pour **[!UICONTROL Granularity]**.

1. Lorsque vous avez sélectionné un jeu de données de **[!UICONTROL Summary]** catégorie :

   1. Pour définir si les données du jeu de données doivent être agrégées ou remplacent des données existantes, sélectionnez **[!UICONTROL Aggregation]** ou **[!UICONTROL Replacement]** pour **[!UICONTROL Data restatement is by]**.

   1. Faites correspondre chacune des **[!UICONTROL Available dataset fields]** à **[!UICONTROL Standard harmonized fields]** in **[!UICONTROL Map to harmonized fields]**. Si vous ne souhaitez pas mapper un champ de jeu de données à un champ harmonisé, sélectionnez explicitement **[!UICONTROL -- None --]**.

   1. Si vous avez besoin d’un nouveau champ harmonisé, non disponible dans la liste, sélectionnez **[!UICONTROL Create New]** créer un champ harmonisé. La boîte de dialogue s’affiche, comme indiqué dans la section [Ajouter un nouveau champ harmonisé](fields.md#add-a-harmonized-field) pour vous permettre d’ajouter rapidement un nouveau champ harmonisé.

   1. Lorsque le mappage est renseigné pour tous les champs de la règle, sélectionnez **[!UICONTROL Save as draft]** pour enregistrer une version préliminaire de la règle ou **[!UICONTROL Save]** pour enregistrer et activer la règle. Sélectionner **[!UICONTROL Cancel]** pour annuler la configuration de la règle.

      ![Création de règles de jeu de données](../assets/dataset-create-summary.png)

1. Lorsque vous avez sélectionné un jeu de données de catégorie d’événements (**[!UICONTROL Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Consumer Experience Events]**), dans la zone située en dessous **[!UICONTROL Map to harmonized fields]**:

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

      * utilise une **[!UICONTROL Case]** **[!UICONTROL Mapping type]** pour mapper de manière conditionnelle la valeur de la variable **[!UICONTROL marketing.campaignName]** dans le champ **[!DNL Luma Transactions]** du jeu de données **[!UICONTROL Campaign]** Champ harmonisé. Le champ Harmonisation de la campagne est défini sur :

         * `Black Friday` lorsque la variable **[!UICONTROL marketing.campaignName]** is `_black_friday` ou `BlackFriday`.
         * à la valeur de la variable **[!UICONTROL marketing.campaignName]** dans tous les autres cas.

        ![Événement de règle de jeu de données](../assets/dataset-create-event.png)

1. Sélectionner ![Ajouter](../assets/icons/AddCircle.svg) **[!UICONTROL Add field]** pour définir des champs supplémentaires.

Lorsque vous avez terminé, sélectionnez **[!UICONTROL Save as draft]** pour enregistrer une version préliminaire de la règle ou **[!UICONTROL Save]** pour enregistrer et activer la règle. Sélectionner **[!UICONTROL Cancel]** pour annuler la configuration de la règle.


### Modification d’une règle de jeu de données

Pour modifier une règle de jeu de données, dans la variable ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** dans Mix Modeler :

1. Sélectionner ![Plus](../assets/icons/More.svg) dans le **[!UICONTROL Dataset]** pour la règle du jeu de données que vous souhaitez modifier.
1. Dans le menu contextuel, sélectionnez ![Modifier](../assets/icons/Edit.svg) **[!UICONTROL Edit]** pour commencer à modifier la règle du jeu de données. Voir [Créer une règle de jeu de données](#create-a-dataset-rule) pour plus d’informations.


### Suppression d’une règle de jeu de données

Pour supprimer une règle de jeu de données, dans la variable ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** dans Mix Modeler :

1. Sélectionner ![Plus](../assets/icons/More.svg) dans le **[!UICONTROL Dataset]** pour la règle du jeu de données que vous souhaitez supprimer.
1. Dans le menu contextuel, sélectionnez ![Supprimer](../assets/icons/Delete.svg) **[!UICONTROL Delete]** pour supprimer la règle du jeu de données. Vous êtes invité à confirmer l’opération. Sélectionner **[!UICONTROL Delete]** pour supprimer définitivement la règle de jeu de données sélectionnée.


## Synchroniser les données

Pour synchroniser les données entre vos données harmonisées et vos jeux de données de résumé et/ou d’événement, en suivant toute la logique de vos règles de jeu de données :

1. Sélectionnez **[!UICONTROL Sync data]**.

1. Dans la **[!UICONTROL Sync data for dataset rules]** , sélectionnez l’une des options suivantes : **[!UICONTROL Refresh harmonized data for summary datasets]**, **[!UICONTROL Refresh harmonized data for event datasets]**, ou **[!UICONTROL Refresh harmonized data for both summary + event datasets]**.

1. Pour lancer la synchronisation en fonction des règles de jeu de données définies entre les données harmonisées et les données des jeux de données, sélectionnez **[!UICONTROL Sync]**. Pour annuler la synchronisation, sélectionnez **[!UICONTROL Cancel]**.

   ![Synchroniser les données](../assets/sync-data.png)


## Préférences de fusion des données

Vous pouvez définir des préférences pour résoudre les conflits à mesure que les données issues des sources résumées et d’événements sont fusionnées. Pour ce faire :

1. Sélectionner ![Préférences de fusion des données](../assets/icons/Merge.svg) **Préférences de fusion des données**.

1. Dans le **[!UICONTROL Data merge preferences]** dialog :

   ![Préférences de fusion des données](../assets/data-merge-preferences.png)

   1. Sélectionnez une préférence de mesure par défaut dans la **[!UICONTROL Default metric preference]** liste. <p>Une préférence par défaut est appliquée lors de l’harmonisation. Plusieurs sources de données tentent de mettre à jour un champ de mesure pour un canal donné. Cette préférence est appliquée au niveau de l’environnement de test, sauf si elle est remplacée pour certaines préférences de mesure définies à l’adresse **[!UICONTROL Metric based preference]**.

   1. Utilisation ![Plus](../assets/icons/AddCircle.svg) **[!UICONTROL Add a metric]**, pour ajouter une ou plusieurs mesures ci-dessous **[!UICONTROL Metric based preference]**.



      * Sélectionnez une mesure dans le **[!UICONTROL _Sélection de mesure_]** list, et
      * Sélectionnez **[!UICONTROL Summary]** ou **[!UICONTROL Event]**.

      Utilisation ![Supprimer](../assets/icons/Close.svg) pour supprimer une entrée de la liste.

   1. Sélectionner **[!UICONTROL Save]** pour enregistrer les préférences de fusion des données. Sélectionner **[!UICONTROL Cancel]** pour annuler.
