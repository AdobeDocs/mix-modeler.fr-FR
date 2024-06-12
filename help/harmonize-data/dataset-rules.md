---
title: Règles du jeu de données
description: Découvrez comment définir des règles de jeu de données à utiliser dans le cadre de l’harmonisation de vos données dans Mix Modeler.
feature: Harmonized Data, Dataset Rules
exl-id: 57d7940a-2900-4814-a30d-bb02bff7615d
source-git-commit: a066cdff03eade86b09f03209a08ebfa2ab32e8e
workflow-type: tm+mt
source-wordcount: '1210'
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
| Source | Source du jeu de données : Adobe Analytics, Événements d’expérience, Résumé (agrégé) ou Événements d’expérience client. |
| Schéma | Schéma auquel le jeu de données se conforme. Vous pouvez sélectionner rapidement le nom du schéma pour ouvrir le schéma dans un nouvel onglet de l’éditeur de schémas dans ![Schéma](../assets/icons/Schemas.svg) [Schémas](../ingest-data/schemas.md). |
| Granularité | Granularité des données du jeu de données. Les valeurs possibles sont Quotidienne, Hebdomadaire, Mensuelle ou Annuelle. |
| Début de la semaine | Indique le jour de la semaine considéré comme le début d’une nouvelle semaine pour le jeu de données spécifique. |
| Statut | État du champ : <p><span style="color:gray">●</span> Version préliminaire ou <p><span style="color:green">●</span> Actif |
| Dernière modification | Données et heure de la dernière modification de la règle du jeu de données. |

{style="table-layout:auto"}

### Créer une règle de jeu de données

Pour créer une règle de jeu de données, dans la variable ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** dans Mix Modeler, sélectionnez **[!UICONTROL Create a dataset rule]** dans le **[!UICONTROL Dataset rules configuration]** assistant.

Dans le **[!UICONTROL Create]** écran,

1. Dans **[!UICONTROL Dataset details]**, sélectionnez un jeu de données dans **[!UICONTROL Select dataset]** pour commencer la configuration. Dans la liste, les jeux de données sont classés dans **[!UICONTROL Consumer Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Experience Event]** et **[!UICONTROL Summary]**.

1. Sélectionnez un jour pour le **[!UICONTROL Start of the week]**.

1. Sélectionner **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** ou **[!UICONTROL Yearly]** pour **[!UICONTROL Granularity]**.

1. Lorsque vous avez sélectionné un jeu de données de la variable **[!UICONTROL Summary]** catégorie :

   1. Pour définir si les données du jeu de données agrègent ou remplacent les données existantes, sélectionnez **[!UICONTROL Aggregation]** ou **[!UICONTROL Replacement]** pour **[!UICONTROL Data restatement is by]**.

   1. Faites correspondre chacune des **[!UICONTROL Available dataset fields]** à **[!UICONTROL Standard harmonized fields]** in **[!UICONTROL Map to harmonized fields]**. Si vous ne souhaitez pas mapper un champ de jeu de données à un champ harmonisé, sélectionnez explicitement **[!UICONTROL -- None --]**.

   1. Si vous avez besoin d’un nouveau champ harmonisé, non disponible dans la liste, sélectionnez **[!UICONTROL Create New]** créer un champ harmonisé. La boîte de dialogue s’affiche, comme indiqué dans la section [Ajouter un nouveau champ harmonisé](fields.md#add-a-harmonized-field).

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

         1. Pour définir explicitement des valeurs, vous définissez un ou plusieurs cas, composés d’une ou de plusieurs conditions. Chaque condition peut rechercher une **[!UICONTROL *Champ de jeu de données AEP *]**si **[!UICONTROL Exists]**ou **[!UICONTROL Not Exists]**ou **[!UICONTROL Contains]**,**[!UICONTROL Not Contains]**,**[!UICONTROL Equals]**,**[!UICONTROL Not Equals]**,**[!UICONTROL Starts With]**, ou **[!UICONTROL Ends With]**une valeur saisie à l’adresse**[!UICONTROL * Entrée de la valeur *]**.

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

1. Dans la **[!UICONTROL Sync data for dataset rules]** , sélectionnez
   * **[!UICONTROL Refresh harmonized data for summary datasets]**,
   * **[!UICONTROL Refresh harmonized data for event datasets]**, ou
   * **[!UICONTROL Refresh harmonized data for both summary + event datasets]**.

1. Pour lancer la synchronisation en fonction des règles de jeu de données définies entre les données harmonisées et les données des jeux de données, sélectionnez **[!UICONTROL Sync]**. Pour annuler la synchronisation, sélectionnez **[!UICONTROL Cancel]**.

   ![Synchroniser les données](../assets/sync-data.png)


## Préférences de fusion des données

>[!NOTE]
>
>[!BADGE bêta]{type=Informative}

Les préférences de fusion de données permettent de résoudre les conflits lorsque des données provenant de sources de données résumées et d’événements sont fusionnées. Les cas pratiques sont les suivants :

* la même mesure publicitaire est mesurée et signalée dans plusieurs jeux de données, ou
* la mesure des mesures peut être incomplète dans certains jeux de données, tandis qu’un autre jeu de données peut être un sur-ensemble d’une mesure spécifique, ce qui entraîne un double comptage.

Pour garantir une prédiction de modèle exacte, vous pouvez définir des préférences de fusion de données :

1. Sélectionner ![Préférences de fusion des données](../assets/icons/Merge.svg) [!BADGE bêta].

1. Dans le **[!UICONTROL Data merge preferences]** [!BADGE bêta]{type=Informative}

   ![Préférences de fusion des données](../assets/data-merge-preferences.png)

   * Sélectionnez une **[!UICONTROL Default metric preference]**. La préférence de mesure par défaut sélectionnée est appliquée lorsque, lors de l’harmonisation, plusieurs sources de données mettent à jour un champ de mesure pour un canal donné. La préférence est appliquée au niveau de l’environnement de test, sauf si elle est remplacée pour des préférences basées sur des mesures spécifiques. Vous pouvez effectuer une sélection parmi **[!UICONTROL Summary data]**, **[!UICONTROL Event data]** et **[!UICONTROL Sum of summmary and event data]**.

   * Pour ajouter des préférences de mesure spécifiques :

      1. Sélectionner ![Plus](../assets/icons/AddCircle.svg) **[!UICONTROL Add a metric]**.
         1. Sélectionnez une mesure dans le **[!UICONTROL *Sélection de mesure *]**liste.
         1. Sélectionnez **[!UICONTROL CHANNELS]** ou **[!UICONTROL CONVERSION TYPES]**. Dans la liste, sélectionnez **[!UICONTROL All]** ou un type de conversion ou canal spécifique.
         1. Sélectionner **[!UICONTROL Summary]** ou **[!UICONTROL Event]** pour indiquer si les données de résumé ou d’événement sont préférées pour la mesure (et tout ou canal sélectionné) lors de la fusion des données.

         Pour ajouter un ou plusieurs types de canal ou de conversion supplémentaires :

         1. Sélectionner ![Plus](../assets/icons/AddCircle.svg) **[!UICONTROL Add a channel]** ou ![Plus](../assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion type]**.
         1. Sélectionnez **[!UICONTROL Summary]** ou **[!UICONTROL Event]**.

         Pour supprimer un canal ou un type de conversion, sélectionnez ![Croix](../assets/icons/Close.svg).

      1. Pour ajouter des préférences de mesure plus spécifiques, répétez l’étape précédente.

   * Pour supprimer une préférence basée sur une mesure spécifique existante, sélectionnez ![Supprimer](../assets/icons/Delete.svg).

1. Sélectionner **[!UICONTROL Save]** pour enregistrer les préférences de fusion des données. Une resynchronisation des données est lancée. <br/>Sélectionner **[!UICONTROL Cancel]** pour annuler.


## Contrôle d’accès au niveau du champ

Lors de la configuration des règles de jeu de données pour les jeux de données harmonisés, Experience Platform [contrôle d’accès basé sur les attributs](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) est appliquée au niveau du champ. Un champ est restreint lorsqu’un libellé est associé à un champ de schéma et qu’une stratégie active est activée, ce qui vous empêche d’y accéder. Par conséquent :

* vous ne voyez pas les champs de schéma qui sont limités pour vous lorsque vous créez une règle de jeu de données,
* vous ne pouvez pas afficher ni modifier le mappage d’un ou de plusieurs champs de schéma limités pour vous. Lorsque vous modifiez ou affichez une règle de jeu de données contenant ces champs restreints, l’écran suivant s’affiche.
  ![Action non autorisée](../assets/action-not-permitted.png)
