---
title: Règles des jeux de données
description: Découvrez comment définir des règles de jeu de données à utiliser dans le cadre de l’harmonisation de vos données dans Mix Modeler.
feature: Harmonized Data, Dataset Rules
exl-id: 57d7940a-2900-4814-a30d-bb02bff7615d
source-git-commit: a8590d604f79268bc8d1f012f2c19271a3b38668
workflow-type: tm+mt
source-wordcount: '1407'
ht-degree: 1%

---

# Règles des jeux de données

Les règles de jeu de données vous aident à mapper vos champs harmonisés avec les champs des données que vous avez ingérées dans Mix Modeler.

* Pour les données agrégées que vous avez ingérées dans Adobe Experience Platform, vous mappez un ou plusieurs des champs de jeux de données disponibles aux champs harmonisés appropriés.
* Pour les données d’événement, vous pouvez mapper individuellement un ou plusieurs champs harmonisés aux champs du jeu de données, directement ou à l’aide de conditions.


## Gestion des règles des jeux de données

Pour afficher un tableau des règles de jeu de données disponibles, dans l’interface du Mix Modeler :

1. Sélectionnez ![Recherche de données](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** dans le rail de gauche.

1. Sélectionnez **[!UICONTROL Dataset rules]** dans la barre supérieure. Un tableau des règles du jeu de données s’affiche.

Les colonnes du tableau spécifient des détails sur les règles du jeu de données :

| Nom de la colonne | Détails |
| ---------------------- | ----------|
| Jeu de données | Nom du jeu de données. |
| Source | Source du jeu de données : Adobe Analytics, Événements d’expérience, Résumé (agrégat) ou Événements d’expérience client. |
| Schéma | Schéma auquel le jeu de données est conforme. Vous pouvez sélectionner rapidement le nom du schéma pour l’ouvrir dans un nouvel onglet de l’éditeur de schémas dans ![Schéma](/help/assets/icons/Schemas.svg) [Schémas](../ingest-data/schemas.md). |
| Granularité | La granularité des données dans le jeu de données. Les valeurs possibles sont Quotidien, Hebdomadaire, Mensuel ou Annuel. |
| Début de la semaine | Indique quel jour de la semaine est considéré comme le début d’une nouvelle semaine pour le jeu de données spécifique. |
| Statut | Statut du champ : <p><span style="color:gray">●</span> Brouillon ou <p><span style="color:green">●</span> Actif |
| Dernière modification | Données et heure de la dernière modification de la règle du jeu de données. |

{style="table-layout:auto"}

### Créer une règle de jeu de données

Pour créer une règle de jeu de données, dans l’interface ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** dans le Mix Modeler, sélectionnez **[!UICONTROL Create a dataset rule]** dans l’assistant de **[!UICONTROL Dataset rules configuration]**.

Dans l’écran **[!UICONTROL Create]**,

1. Dans **[!UICONTROL Dataset details]**, sélectionnez un jeu de données dans **[!UICONTROL Select dataset]** pour commencer la configuration. Dans la liste, les jeux de données sont classés en **[!UICONTROL Consumer Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Experience Event]** et **[!UICONTROL Summary]**.

1. Sélectionnez un jour pour le **[!UICONTROL Start of the week]**.

1. Sélectionnez **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** ou **[!UICONTROL Yearly]** pour **[!UICONTROL Granularity]**.

1. Lorsque vous avez sélectionné un jeu de données de la catégorie **[!UICONTROL Summary]** :

   1. Pour définir si les données du jeu de données agrègent ou remplacent les données existantes, sélectionnez **[!UICONTROL Aggregation]** ou **[!UICONTROL Replacement]** pour **[!UICONTROL Data restatement is by]**.

   1. Mappez chacune des **[!UICONTROL Available dataset fields]** aux **[!UICONTROL Standard harmonized fields]** correspondantes dans **[!UICONTROL Map to harmonized fields]**. Si vous ne souhaitez pas mapper un champ de jeu de données à un champ harmonisé, sélectionnez explicitement **[!UICONTROL -- None --]**.

   1. Si vous avez besoin d’un nouveau champ harmonisé, qui n’est pas disponible dans la liste, sélectionnez **[!UICONTROL Create New]** pour créer un champ harmonisé. La boîte de dialogue s’affiche comme indiqué dans la section [Ajouter un nouveau champ harmonisé](fields.md#add-a-harmonized-field).

   1. Une fois le mappage terminé pour tous les champs de la règle, sélectionnez **[!UICONTROL Save as draft]** pour enregistrer un brouillon de la règle ou **[!UICONTROL Save]** pour enregistrer et activer la règle. Sélectionnez **[!UICONTROL Cancel]** pour annuler la configuration de la règle.

      ![Créer des règles de jeu de données](/help/assets/dataset-create-summary.png)

1. Lorsque vous avez sélectionné un jeu de données de catégorie d’événement (**[!UICONTROL Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Consumer Experience Events]**), dans la zone située sous **[!UICONTROL Map to harmonized fields]** :

   1. Sélectionnez un champ harmonisé dans **[!UICONTROL Standard harmonized field]**.

   1. Lorsque le champ harmonisé sélectionné est de type mesure :

      1. Sélectionnez **[!UICONTROL Count]** ou **[!UICONTROL Sum]** dans **[!UICONTROL Mapping type]**.

      1. Sélectionnez un **[!UICONTROL *champ de jeu de données AEP *]**&#x200B;auquel vous souhaitez que le champ harmonisé soit mappé par défaut.

   1. Lorsque le champ sélectionné est de type dimension :

      1. Sélectionnez **[!UICONTROL Map Into]** ou **[!UICONTROL Case]** dans **[!UICONTROL Mapping type]**.

      1. Lorsque vous avez sélectionné **[!UICONTROL Map Into]**, sélectionnez **[!UICONTROL Field]** et **[!UICONTROL *champ du jeu de données AEP *]**&#x200B;ou **[!UICONTROL Value]**&#x200B;et une valeur par défaut pour mapper le champ harmonisé par défaut au champ du jeu de données ou à la valeur saisie.

      1. Lorsque vous sélectionnez **[!UICONTROL Case]**, sélectionnez **[!UICONTROL Field]** et **[!UICONTROL *champ de jeu de données AEP *]**&#x200B;ou **[!UICONTROL Value]**&#x200B;et une valeur par défaut pour mapper le champ harmonisé par défaut au champ de jeu de données ou à la valeur saisie.

         1. Pour définir explicitement des valeurs, vous définissez un ou plusieurs cas, composés d’une ou de plusieurs conditions. Chaque condition peut rechercher un **[!UICONTROL *champ de jeu de données AEP *]**&#x200B;spécifique, s’il **[!UICONTROL Exists]**&#x200B;ou **[!UICONTROL Not Exists]**&#x200B;ou s’il **[!UICONTROL Contains]**,**[!UICONTROL Not Contains]**,**[!UICONTROL Equals]**,**[!UICONTROL Not Equals]**,**[!UICONTROL Starts With]**&#x200B;ou **[!UICONTROL Ends With]**&#x200B;une valeur saisie à&#x200B;**[!UICONTROL * Entrez la valeur d’entrée *]**.

         1. Pour ajouter un autre cas, sélectionnez ![Ajouter](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add case]**. Pour ajouter une autre condition, sélectionnez ![Ajouter](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add condition]**.

         1. Pour supprimer un cas ou une condition, sélectionnez ![Fermer](/help/assets/icons/Close.svg) dans le conteneur correspondant.

         1. Pour choisir si une ou toutes les conditions doivent s’appliquer à un cas, sélectionnez **[!UICONTROL Any of]** ou **[!UICONTROL All of]**.

         1. Pour définir la valeur de résultat d’un cas, saisissez la valeur à **[!UICONTROL Then]**.

      Exemple ci-dessous

      * utilise un **[!UICONTROL Mapping type]** **[!UICONTROL Map Into]** pour mapper le champ harmonisé **[!UICONTROL Channel Type At Source]** au champ **[!UICONTROL channel_type]** du jeu de données **[!DNL Luma Transactions]**.

      * utilise un **[!UICONTROL Mapping type]** **[!UICONTROL Case]** pour mapper de manière conditionnelle la valeur du champ **[!UICONTROL marketing.campaignName]** dans le jeu de données **[!DNL Luma Transactions]** au champ harmonisé **[!UICONTROL Campaign]**. Le champ harmonisé de la campagne est défini sur :

         * `Black Friday` lorsque la **[!UICONTROL marketing.campaignName]** est `_black_friday` ou `BlackFriday`.
         * à la valeur du **[!UICONTROL marketing.campaignName]** dans tous les autres cas.

        ![Événement de règle du jeu de données](/help/assets/dataset-create-event.png)

1. Sélectionnez ![Ajouter](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add field]** pour définir des champs supplémentaires.

Lorsque vous avez terminé, sélectionnez **[!UICONTROL Save as draft]** pour enregistrer un brouillon de la règle ou **[!UICONTROL Save]** pour enregistrer et activer la règle. Sélectionnez **[!UICONTROL Cancel]** pour annuler la configuration de la règle.


### Modification d’une règle de jeu de données

Pour modifier une règle de jeu de données, dans l’interface ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** dans le Mix Modeler :

1. Sélectionnez ![Plus](/help/assets/icons/More.svg) dans la colonne **[!UICONTROL Dataset]** de la règle de jeu de données à modifier.
1. Dans le menu contextuel, sélectionnez ![Modifier](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** pour commencer à modifier la règle du jeu de données. Pour plus d’informations, voir [Création d’une règle de jeu de données](#create-a-dataset-rule).


### Suppression d’une règle de jeu de données

Pour supprimer une règle de jeu de données, dans l’interface ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** dans le Mix Modeler :

1. Sélectionnez ![Plus](/help/assets/icons/More.svg) dans la colonne **[!UICONTROL Dataset]** de la règle de jeu de données à supprimer.
1. Dans le menu contextuel, sélectionnez ![Supprimer](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** pour supprimer la règle du jeu de données. Vous êtes invité à confirmer l’opération. Sélectionnez **[!UICONTROL Delete]** pour supprimer définitivement la règle de jeu de données sélectionnée.


## Synchroniser les données

Pour synchroniser les données entre vos jeux de données de résumé et/ou d’événement harmonisés lors de l’application de la logique dans vos règles de jeu de données :

1. Sélectionnez **[!UICONTROL Sync data]**.

1. Dans la boîte de dialogue **[!UICONTROL Sync data for dataset rules]**, sélectionnez l’une des options suivantes :
   * **[!UICONTROL Refresh harmonized data for summary datasets]**,
   * **[!UICONTROL Refresh harmonized data for event datasets]**, ou
   * **[!UICONTROL Refresh harmonized data for both summary + event datasets]**.

1. Pour démarrer la synchronisation en fonction des règles de jeu de données définies entre les données harmonisées et les données des jeux de données, sélectionnez **[!UICONTROL Sync]**. Pour annuler la synchronisation, sélectionnez **[!UICONTROL Cancel]**.

   ![Synchroniser les données](/help/assets/sync-data.png)


## Préférences de fusion des données

>[!NOTE]
>
>[!BADGE version bêta]{type=Informative}

Pour garantir des prédictions de modèle précises, vous pouvez définir des préférences de fusion des données. Cette fonctionnalité permet aux utilisateurs de résoudre les conflits après la fusion des données au niveau du résumé et au niveau de l’événement.

Vous pouvez configurer une préférence de mesure par défaut à appliquer en cas de conflits de mises à jour. Cette mesure par défaut peut être l’une des trois options suivantes :

* **[!UICONTROL Summary data]**
* **[!UICONTROL Sum of summary and event data]**
* **[!UICONTROL Event data]**

Lorsque, lors de l’harmonisation, plusieurs sources de données tentent de mettre à jour un champ de mesure pour un canal donné, la préférence par défaut configurée par l’utilisateur est appliquée. Cette préférence est appliquée au niveau du sandbox, sauf si elle est remplacée pour certaines préférences basées sur des mesures configurées en plus.

Sous **[!UICONTROL Metric based preferences]**, l’utilisateur ou l’utilisatrice peut configurer la source spécifique (**[!UICONTROL Summary]** ou **[!UICONTROL Event]**) pour une mesure donnée et le type de conversion correspondant pour cette mesure.

Les cas d’utilisation standard sont les suivants :

* la même mesure publicitaire est mesurée et signalée dans plusieurs jeux de données, ou
* la mesure des mesures peut être incomplète dans certains jeux de données, tandis qu’un autre jeu de données peut être un sur-ensemble d’une mesure particulière, ce qui entraîne un double comptage.

### Configuration

Pour configurer les préférences de fusion des données :


1. Sélectionnez ![Préférences de fusion des données](/help/assets/icons/Merge.svg) [!BADGE version bêta].

1. Dans la **[!UICONTROL Data merge preferences]** [!BADGE version bêta]{type=Informative}

   ![Préférences de fusion des données](/help/assets/data-merge-preferences.png)

   * Sélectionnez un **[!UICONTROL Default metric preference]**. La préférence de mesure par défaut sélectionnée est appliquée lorsque, lors de l’harmonisation, plusieurs sources de données mettent à jour un champ de mesure pour un canal donné. La préférence est appliquée au niveau du sandbox, sauf si elle est remplacée pour des préférences spécifiques basées sur des mesures. Vous pouvez choisir entre **[!UICONTROL Summary data]**, **[!UICONTROL Event data]** et **[!UICONTROL Sum of summary and event data]**.

   * Pour ajouter des préférences spécifiques basées sur des mesures :

      1. Sélectionnez ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a metric]**.
         1. Sélectionnez une mesure dans la liste **[!UICONTROL *Sélection de mesure *]**.
         1. Sélectionnez **[!UICONTROL CHANNELS]** ou **[!UICONTROL CONVERSION TYPES]**. Dans la liste, sélectionnez **[!UICONTROL All]** ou un canal spécifique ou un type de conversion.
         1. Sélectionnez **[!UICONTROL Summary]** ou **[!UICONTROL Event]** pour spécifier si les données de résumé ou les données d’événement sont préférées pour la mesure (et l’ensemble du canal ou le canal sélectionné) lors de la fusion des données.

         Pour ajouter un ou plusieurs types de canal ou de conversion supplémentaires :

         1. Sélectionnez ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a channel]** ou ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion type]**.
         1. Sélectionnez **[!UICONTROL Summary]** ou **[!UICONTROL Event]**.

         Pour supprimer un canal ou un type de conversion, sélectionnez ![Cross](/help/assets/icons/Close.svg).

      1. Pour ajouter des préférences plus spécifiques basées sur des mesures, répétez l’étape précédente.

   * Pour supprimer une préférence spécifique existante basée sur une mesure, sélectionnez ![Supprimer](/help/assets/icons/Delete.svg).

1. Sélectionnez **[!UICONTROL Save]** pour enregistrer les préférences de fusion des données. Une resynchronisation des données est lancée. <br/>Sélectionnez **[!UICONTROL Cancel]** pour annuler.

## Supprimer un jeu de données source

Lorsque vous supprimez un jeu de données source utilisé dans vos données harmonisées, les entrées sous-jacentes de ce jeu de données source sont supprimées du [[!UICONTROL Harmonized data]](/help/harmonize-data/overview.md). Cependant, la règle du jeu de données avec le jeu de données source supprimé reste dans la liste de configuration des règles du jeu de données avec une icône ![DataRemove](/help/assets/icons/DataRemove.svg) indiquant que le jeu de données source a été supprimé. Pour obtenir plus de détails :

* Sélectionnez ![Plus](/help/assets/icons/More.svg) et ![Aperçu](/help/assets/icons/Preview.svg) **[!UICONTROL View]** dans le menu contextuel.
La boîte de dialogue **[!UICONTROL Dataset rule mapping - Fields]** affiche des informations sur le jeu de données source supprimé et les champs utilisés dans la configuration des règles du jeu de données.

Lorsque vous revenez à votre configuration **[!UICONTROL Dataset rules]**, une boîte de dialogue s’affiche pour expliquer qu’un ou plusieurs des jeux de données sources ont été supprimés. Les données harmonisées sont affectées lors d’une synchronisation ad hoc ou planifiée suivante. Vérifiez la configuration des règles du jeu de données.

Les données harmonisées sont mises à jour sans les données source supprimées lors de la synchronisation ad hoc ou planifiée suivante. Cependant, des boîtes de dialogue d’alerte s’affichent toujours vous invitant à supprimer la règle de jeu de données en fonction du jeu de données source supprimé. Cette alerte permet aux utilisateurs d’afficher et d’évaluer les champs concernés dans le jeu de données supprimé. Et pour déterminer l’impact sur les points de contact marketing ou les conversions qui peuvent être utilisés dans n’importe quel modèle. Une fois que vous avez vérifié et atténué cet impact, vous devez supprimer la règle de jeu de données de la liste de configuration des règles de jeu de données.
