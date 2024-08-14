---
title: Règles du jeu de données
description: Découvrez comment définir des règles de jeu de données à utiliser dans le cadre de l’harmonisation de vos données dans Mix Modeler.
feature: Harmonized Data, Dataset Rules
exl-id: 57d7940a-2900-4814-a30d-bb02bff7615d
source-git-commit: a924eb080866595af3639c4976716e69ef5e7a20
workflow-type: tm+mt
source-wordcount: '1313'
ht-degree: 1%

---

# Règles du jeu de données

Les règles de jeu de données vous aident à mapper vos champs harmonisés avec les champs des données que vous avez ingérées dans Mix Modeler.

* Pour les données agrégées que vous avez ingérées dans Adobe Experience Platform, vous mappez un ou plusieurs des champs de jeu de données disponibles aux champs harmonisés appropriés.
* Pour les données d’événement, vous pouvez mapper un ou plusieurs champs harmonisés aux champs du jeu de données, directement ou à l’aide de conditions.


## Gestion des règles de jeu de données

Pour afficher un tableau des règles de jeu de données disponibles, dans l’interface du Mix Modeler :

1. Sélectionnez ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** dans le rail de gauche.

1. Sélectionnez **[!UICONTROL Dataset rules]** dans la barre supérieure. Un tableau des règles du jeu de données s’affiche.

Les colonnes du tableau spécifient des détails sur les règles du jeu de données :

| Nom de la colonne | Détails |
| ---------------------- | ----------|
| Jeu de données | Nom du jeu de données. |
| Source | Source du jeu de données : Adobe Analytics, Événements d’expérience, Résumé (agrégé) ou Événements d’expérience client. |
| Schéma | Schéma auquel le jeu de données se conforme. Vous pouvez sélectionner rapidement le nom du schéma pour ouvrir le schéma dans un nouvel onglet de l’éditeur de schémas dans ![Schema](/help/assets//icons/Schemas.svg) [Schemas](../ingest-data/schemas.md). |
| Granularité | Granularité des données du jeu de données. Les valeurs possibles sont Quotidienne, Hebdomadaire, Mensuelle ou Annuelle. |
| Début de la semaine | Indique le jour de la semaine considéré comme le début d’une nouvelle semaine pour le jeu de données spécifique. |
| Statut | État du champ : <p><span style="color:gray">●</span> Version préliminaire ou <p><span style="color:green">●</span> actif |
| Dernière modification | Données et heure de la dernière modification de la règle du jeu de données. |

{style="table-layout:auto"}

### Créer une règle de jeu de données

Pour créer une règle de jeu de données, dans l’interface ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** de Mix Modeler, sélectionnez **[!UICONTROL Create a dataset rule]** dans l’assistant **[!UICONTROL Dataset rules configuration]**.

Dans l&#39;écran **[!UICONTROL Create]**,

1. Dans **[!UICONTROL Dataset details]**, sélectionnez un jeu de données dans **[!UICONTROL Select dataset]** pour commencer la configuration. Dans la liste, les jeux de données sont classés dans **[!UICONTROL Consumer Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Experience Event]** et **[!UICONTROL Summary]**.

1. Sélectionnez un jour pour le **[!UICONTROL Start of the week]**.

1. Sélectionnez **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** ou **[!UICONTROL Yearly]** pour **[!UICONTROL Granularity]**.

1. Lorsque vous avez sélectionné un jeu de données de la catégorie **[!UICONTROL Summary]** :

   1. Pour définir si les données du jeu de données agrègent ou remplacent les données existantes, sélectionnez **[!UICONTROL Aggregation]** ou **[!UICONTROL Replacement]** pour **[!UICONTROL Data restatement is by]**.

   1. Mappez chacun des **[!UICONTROL Available dataset fields]** avec les **[!UICONTROL Standard harmonized fields]** correspondants dans **[!UICONTROL Map to harmonized fields]**. Si vous ne souhaitez pas mapper un champ de jeu de données à un champ harmonisé, sélectionnez explicitement **[!UICONTROL -- None --]**.

   1. Si vous avez besoin d&#39;un nouveau champ harmonisé, non disponible dans la liste, sélectionnez **[!UICONTROL Create New]** pour créer un nouveau champ harmonisé. La boîte de dialogue s’affiche comme indiqué dans la section [Ajouter un nouveau champ harmonisé](fields.md#add-a-harmonized-field).

   1. Une fois le mappage terminé pour tous les champs de la règle, sélectionnez **[!UICONTROL Save as draft]** pour enregistrer une version préliminaire de la règle ou **[!UICONTROL Save]** pour enregistrer et activer la règle. Sélectionnez **[!UICONTROL Cancel]** pour annuler la configuration de la règle.

      ![Créer des règles de jeu de données](/help/assets//dataset-create-summary.png)

1. Lorsque vous avez sélectionné un jeu de données de catégorie d’événements (**[!UICONTROL Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Consumer Experience Events]**), dans la zone située sous **[!UICONTROL Map to harmonized fields]** :

   1. Sélectionnez un champ harmonisé dans **[!UICONTROL Standard harmonized field]**.

   1. Lorsque le champ harmonisé sélectionné est de type mesure :

      1. Sélectionnez **[!UICONTROL Count]** ou **[!UICONTROL Sum]** dans **[!UICONTROL Mapping type]**.

      1. Sélectionnez un **[!UICONTROL *champ de jeu de données AEP *]**vers lequel vous souhaitez que le champ harmonisé soit mappé par défaut.

   1. Lorsque le champ sélectionné est de type dimension :

      1. Sélectionnez **[!UICONTROL Map Into]** ou **[!UICONTROL Case]** dans **[!UICONTROL Mapping type]**.

      1. Lorsque vous avez sélectionné **[!UICONTROL Map Into]**, sélectionnez **[!UICONTROL Field]** et **[!UICONTROL *Champ de jeu de données AEP *]**ou **[!UICONTROL Value]**, ainsi qu’une valeur par défaut pour mapper le champ harmonisé par défaut au champ de jeu de données ou à la valeur saisie.

      1. Lorsque vous sélectionnez **[!UICONTROL Case]**, sélectionnez **[!UICONTROL Field]** et **[!UICONTROL *Champ de jeu de données AEP *]**ou **[!UICONTROL Value]**, ainsi qu’une valeur par défaut pour mapper le champ harmonisé par défaut au champ de jeu de données ou à la valeur saisie.

         1. Pour définir explicitement des valeurs, vous définissez un ou plusieurs cas, composés d’une ou de plusieurs conditions. Chaque condition peut vérifier pour un **[!UICONTROL *champ de jeu de données AEP *]**si elle **[!UICONTROL Exists]**ou **[!UICONTROL Not Exists]**ou si elle **[!UICONTROL Contains]**,**[!UICONTROL Not Contains]**,**[!UICONTROL Equals]**,**[!UICONTROL Not Equals]**,**[!UICONTROL Starts With]**ou **[!UICONTROL Ends With]**une valeur saisie à**[!UICONTROL * Saisir la valeur d’entrée *]**.

         1. Pour ajouter un autre cas, sélectionnez ![Ajouter](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add case]**, puis ![Ajouter](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add condition]** pour ajouter une autre condition.

         1. Pour supprimer une condition ou un cas, sélectionnez ![Fermer](/help/assets//icons/Close.svg) dans le conteneur correspondant.

         1. Pour indiquer si toutes les conditions doivent s&#39;appliquer à un cas, sélectionnez **[!UICONTROL Any of]** ou **[!UICONTROL All of]**.

         1. Pour définir la valeur de résultat d’un cas, saisissez la valeur **[!UICONTROL Then]**.

      L’exemple ci-dessous

      * utilise un **[!UICONTROL Map Into]** **[!UICONTROL Mapping type]** pour mapper le champ **[!UICONTROL Channel Type At Source]** harmonisé au champ **[!UICONTROL channel_type]** du jeu de données **[!DNL Luma Transactions]**.

      * utilise un **[!UICONTROL Case]** **[!UICONTROL Mapping type]** pour mapper de manière conditionnelle la valeur du champ **[!UICONTROL marketing.campaignName]** du jeu de données **[!DNL Luma Transactions]** au champ **[!UICONTROL Campaign]** harmonisé. Le champ Harmonisation de la campagne est défini sur :

         * `Black Friday` lorsque le **[!UICONTROL marketing.campaignName]** est `_black_friday` ou `BlackFriday`.
         * à la valeur de **[!UICONTROL marketing.campaignName]** dans tous les autres cas.

        ![Événement de règle de jeu de données](/help/assets//dataset-create-event.png)

1. Sélectionnez ![Ajouter](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add field]** pour définir des champs supplémentaires.

Lorsque vous avez terminé, sélectionnez **[!UICONTROL Save as draft]** pour enregistrer une version préliminaire de la règle ou **[!UICONTROL Save]** pour enregistrer et activer la règle. Sélectionnez **[!UICONTROL Cancel]** pour annuler la configuration de la règle.


### Modification d’une règle de jeu de données

Pour modifier une règle de jeu de données, dans l’interface ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** du Mix Modeler :

1. Sélectionnez ![Plus](/help/assets//icons/More.svg) dans la colonne **[!UICONTROL Dataset]** pour la règle du jeu de données que vous souhaitez modifier.
1. Dans le menu contextuel, sélectionnez ![Modifier](/help/assets//icons/Edit.svg) **[!UICONTROL Edit]** pour commencer à modifier la règle du jeu de données. Pour plus d’informations, voir [Création d’une règle de jeu de données](#create-a-dataset-rule) .


### Suppression d’une règle de jeu de données

Pour supprimer une règle de jeu de données, dans l’interface ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** du Mix Modeler :

1. Sélectionnez ![Plus](/help/assets//icons/More.svg) dans la colonne **[!UICONTROL Dataset]** pour la règle du jeu de données que vous souhaitez supprimer.
1. Dans le menu contextuel, sélectionnez ![Supprimer](/help/assets//icons/Delete.svg) **[!UICONTROL Delete]** pour supprimer la règle du jeu de données. Vous êtes invité à confirmer l’opération. Sélectionnez **[!UICONTROL Delete]** pour supprimer définitivement la règle de jeu de données sélectionnée.


## Synchroniser les données

Pour synchroniser les données entre vos données harmonisées et vos jeux de données de résumé et/ou d’événement lors de l’application de la logique à vos règles de jeu de données :

1. Sélectionnez **[!UICONTROL Sync data]**.

1. Dans la boîte de dialogue **[!UICONTROL Sync data for dataset rules]**, sélectionnez
   * **[!UICONTROL Refresh harmonized data for summary datasets]**,
   * **[!UICONTROL Refresh harmonized data for event datasets]** ou
   * **[!UICONTROL Refresh harmonized data for both summary + event datasets]**.

1. Pour lancer la synchronisation en fonction des règles de jeu de données définies entre les données harmonisées et les données des jeux de données, sélectionnez **[!UICONTROL Sync]**. Pour annuler la synchronisation, sélectionnez **[!UICONTROL Cancel]**.

   ![Synchroniser les données](/help/assets//sync-data.png)


## Préférences de fusion des données

>[!NOTE]
>
>[!BADGE beta]{type=Informative}

Les préférences de fusion de données permettent de résoudre les conflits lorsque des données provenant de sources de données résumées et d’événements sont fusionnées. Les cas pratiques sont les suivants :

* la même mesure publicitaire est mesurée et signalée dans plusieurs jeux de données, ou
* la mesure des mesures peut être incomplète dans certains jeux de données, tandis qu’un autre jeu de données peut être un sur-ensemble d’une mesure spécifique, ce qui entraîne un double comptage.

Pour garantir une prédiction de modèle exacte, vous pouvez définir des préférences de fusion de données :

1. Sélectionnez ![Préférences de fusion de données](/help/assets//icons/Merge.svg) [!BADGE bêta].

1. Dans la **[!UICONTROL Data merge preferences]** [!BADGE version bêta]{type=Informative}

   ![Préférences de fusion de données](/help/assets//data-merge-preferences.png)

   * Sélectionnez un **[!UICONTROL Default metric preference]**. La préférence de mesure par défaut sélectionnée est appliquée lorsque, lors de l’harmonisation, plusieurs sources de données mettent à jour un champ de mesure pour un canal donné. La préférence est appliquée au niveau de l’environnement de test, sauf si elle est remplacée pour des préférences basées sur des mesures spécifiques. Vous pouvez choisir entre **[!UICONTROL Summary data]**, **[!UICONTROL Event data]** et **[!UICONTROL Sum of summary and event data]**.

   * Pour ajouter des préférences de mesure spécifiques :

      1. Sélectionnez ![Plus](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add a metric]**.
         1. Sélectionnez une mesure dans la liste **[!UICONTROL *Sélection de mesure *]**.
         1. Sélectionnez **[!UICONTROL CHANNELS]** ou **[!UICONTROL CONVERSION TYPES]**. Dans la liste, sélectionnez **[!UICONTROL All]** ou un canal ou un type de conversion spécifique.
         1. Sélectionnez **[!UICONTROL Summary]** ou **[!UICONTROL Event]** pour indiquer si les données récapitulatives ou les données d’événement sont préférées pour la mesure (et tout ou canal sélectionné) lors de la fusion des données.

         Pour ajouter un ou plusieurs types de canal ou de conversion supplémentaires :

         1. Sélectionnez ![Plus](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add a channel]** ou ![Plus](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add a conversion type]**.
         1. Sélectionnez **[!UICONTROL Summary]** ou **[!UICONTROL Event]**.

         Pour supprimer un canal ou un type de conversion, sélectionnez ![Cross](/help/assets//icons/Close.svg).

      1. Pour ajouter des préférences de mesure plus spécifiques, répétez l’étape précédente.

   * Pour supprimer une préférence basée sur une mesure spécifique existante, sélectionnez ![Supprimer](/help/assets//icons/Delete.svg).

1. Sélectionnez **[!UICONTROL Save]** pour enregistrer les préférences de fusion de données. Une resynchronisation des données est lancée. <br/>Sélectionnez **[!UICONTROL Cancel]** pour annuler.

## Suppression d’un jeu de données source

Lorsque vous supprimez un jeu de données source utilisé dans vos données harmonisées, les entrées sous-jacentes de ce jeu de données source sont supprimées du [[!UICONTROL Harmonized data]](/help/harmonize-data/overview.md). Cependant, la règle du jeu de données avec le jeu de données source supprimé reste dans la liste de configuration des règles du jeu de données avec une icône ![DataRemove](/help/assets/icons/DataRemove.svg) indiquant que le jeu de données source a été supprimé. Pour plus d’informations :

* Sélectionnez ![Plus](/help/assets/icons/More.svg) et ![Aperçu](/help/assets/icons/Preview.svg) **[!UICONTROL View]** dans le menu contextuel.
La boîte de dialogue **[!UICONTROL Dataset rule mapping - Fields]** affiche des informations sur le jeu de données source supprimé et les champs utilisés dans la configuration des règles du jeu de données.

Lorsque vous revenez à votre configuration **[!UICONTROL Dataset rules]**, une boîte de dialogue vous explique qu’un ou plusieurs jeux de données source ont été supprimés. Les données harmonisées sont affectées lors d’une synchronisation ad hoc ou planifiée suivante. Vérifiez la configuration de votre règle de jeu de données.

Les données harmonisées sont mises à jour sans les données source supprimées lors de la synchronisation ad hoc ou de la synchronisation planifiée suivante. Cependant, les boîtes de dialogue d’alerte vous invitent à supprimer la règle du jeu de données en fonction du jeu de données source supprimé. Cette alerte permet aux utilisateurs d’afficher et d’évaluer les champs concernés dans le jeu de données supprimé. Et pour déterminer l’impact sur les points de contact marketing ou les conversions pouvant être utilisés dans n’importe quel modèle. Une fois que vous avez examiné et atténué cet impact, vous devez supprimer la règle du jeu de données de la liste de configuration de la règle du jeu de données.
