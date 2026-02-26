---
title: Règles des jeux de données
description: Découvrez comment définir des règles de jeu de données à utiliser dans le cadre de l’harmonisation de vos données dans Mix Modeler.
feature: Harmonized Data, Dataset Rules
exl-id: 57d7940a-2900-4814-a30d-bb02bff7615d
source-git-commit: 9987c845414fa5a3abda201d55f7b1ed6e211780
workflow-type: tm+mt
source-wordcount: '2102'
ht-degree: 1%

---

# Règles des jeux de données

Les règles des jeux de données vous aident à mapper vos champs harmonisés avec les champs des données que vous avez ingérées dans Mix Modeler.

* Pour les données agrégées que vous avez ingérées dans Adobe Experience Platform, vous mappez un ou plusieurs des champs de jeux de données disponibles aux champs harmonisés appropriés.
* Pour les données d’événement, vous pouvez mapper individuellement un ou plusieurs champs harmonisés aux champs du jeu de données, directement ou à l’aide de conditions.


## Gestion des règles des jeux de données

Pour afficher un tableau des règles de jeu de données disponibles, dans l’interface de Mix Modeler :

1. Sélectionnez ![Recherche de données](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** dans le rail de gauche.

1. Sélectionnez **[!UICONTROL Dataset rules]** dans la barre supérieure. Un tableau des règles du jeu de données s’affiche.

Vous pouvez rechercher rapidement un jeu de données en utilisant ![Rechercher](/help/assets/icons/Search.svg) **[!UICONTROL _Entrez un nom de jeu de données_]**.

Les colonnes du tableau fournissent des détails sur les règles du jeu de données :

| Nom de la colonne | Détails |
| ---------------------- | ----------|
| **[!UICONTROL Dataset]** | Nom du jeu de données.  Utilisez ![Plus](/help/assets/icons/More.svg) pour sélectionner des actions pour un jeu de données. Vous pouvez effectuer les actions suivantes :<ul><li>![Prévisualiser](/help/assets/icons/Preview.svg) **[!UICONTROL View]** pour afficher la configuration des règles du jeu de données. Tous les champs sont désactivés.</li><li>![Modifier](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** pour modifier la configuration des règles du jeu de données.</li><li>![Supprimer](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** pour supprimer la configuration des règles du jeu de données. Vous êtes invité à confirmer la suppression dans la boîte de dialogue Supprimer le jeu de données. Sélectionnez **[!UICONTROL Delete]** pour supprimer définitivement la configuration de règle du jeu de données.</li><ul> |
| **[!UICONTROL Source]** | Source du jeu de données : Adobe Analytics, Événements d’expérience, Résumé (agrégat) ou Événements d’expérience client. |
| **[!UICONTROL Schema]** | Schéma auquel le jeu de données est conforme. Vous pouvez sélectionner rapidement le nom du schéma pour l’ouvrir dans un nouvel onglet de l’éditeur de schémas dans ![Schéma](/help/assets/icons/Schemas.svg) [Schémas](../ingest-data/schemas.md). |
| **[!UICONTROL Granularity]** | La granularité des données dans le jeu de données. Les valeurs possibles sont Quotidien, Hebdomadaire, Mensuel ou Annuel. |
| **[!UICONTROL Start of the week]** | Indique quel jour de la semaine est considéré comme le début d’une nouvelle semaine pour le jeu de données spécifique. |
| **[!UICONTROL Status]** | Le statut du champ : ![StatusGray](/help/assets/icons/StatusGray.svg) Draft ou ![StatusGreen](/help/assets/icons/StatusGreen.svg) Active |
| **[!UICONTROL Last modified]** | Données et heure de la dernière modification de la règle du jeu de données. |

{style="table-layout:auto"}

### Créer une règle de jeu de données

Pour créer une règle de jeu de données, dans l’interface ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** de Mix Modeler, sélectionnez **[!UICONTROL Create a dataset rule]** dans l’assistant de **[!UICONTROL Dataset rules configuration]**.

Dans l’écran **[!UICONTROL Create]**,

1. Dans **[!UICONTROL Dataset details]**, sélectionnez un jeu de données dans **[!UICONTROL Select dataset]** pour commencer la configuration. Dans la liste, les jeux de données sont classés par **[!UICONTROL Summary]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Experience Event]**, **[!UICONTROL Factors]** et **[!UICONTROL Consumer Experience Events]**.

1. Sélectionnez un jour pour le **[!UICONTROL Start of the week]**.

1. Sélectionnez **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** ou **[!UICONTROL Yearly]** pour **[!UICONTROL Granularity]**.

1. Lorsque vous avez sélectionné un jeu de données de la catégorie **[!UICONTROL Summary]** ou **[!UICONTROL Factors]**, sélectionnez **[!UICONTROL Aggregation]** ou **[!UICONTROL Replacement]** pour **[!UICONTROL Data restatement is by]**.

   Les données de rapport des éditeurs sont très importantes pour les analystes marketing, car travailler avec les éditeurs implique souvent des dépenses importantes et des modifications dans les données de rapport peuvent entraîner des informations et des plans d’investissement très différents. En outre, les analystes marketing ont besoin de données précises pour obtenir les bonnes informations et présenter des propositions convaincantes afin de gagner la confiance des parties prenantes. Cependant, ces éditeurs, tels que Google et Facebook, retraitent ou suppriment souvent les données de rapports lorsqu’ils réconcilient leurs données. La période pour la plupart des modifications est de moins de 7 jours à compter de la performance multimédia signalée. D’autres modifications des données sont possibles dans les 30 jours. En général, après 30 jours, les livres sont considérés comme fermés et les données sont complètes.

   Mix Modeler prend en charge le retraitement des données. S’assurer que les données utilisées pour la création de rapports, la modélisation et la planification sont exactes. et que les données sont en mesure de soutenir les attentes et les besoins de l’analyste de la marque et du marketing.

   Vous pouvez envoyer des lignes retraitées de données récapitulatives sous forme de lignes incrémentielles dans un jeu de données Experience Platform et le service d’harmonisation met à jour le jeu de données harmonisé avec ces données retraitées. De même, vous pouvez également supprimer des lignes de données récapitulatives qui doivent être reflétées dans le service d’harmonisation.

1. Dans la section **[!UICONTROL Map to harmonized fields]** , sélectionnez un champ harmonisé dans **[!UICONTROL Standard harmonized field]**. Pour [créer rapidement un champ harmonisé](/help/harmonize-data/fields.md#add-a-harmonized-field) sélectionnez **[!UICONTROL Create new]**.

   * Lorsque le champ harmonisé sélectionné est de type mesure :

      1. Sélectionnez **[!UICONTROL Count]** ou **[!UICONTROL Sum]** dans **[!UICONTROL Mapping type]**.

      1. Sélectionnez un champ de jeu de données **[!UICONTROL *AEP *]**&#x200B;auquel vous souhaitez que le champ harmonisé soit mappé par défaut.

   * Lorsque le champ sélectionné est de type dimension :

      1. Sélectionnez **[!UICONTROL Map Into]** ou **[!UICONTROL Case]** dans **[!UICONTROL Mapping type]**.

      1. Lorsque vous avez sélectionné **[!UICONTROL Map Into]**, sélectionnez **[!UICONTROL Field]** et **[!UICONTROL *le champ du jeu de données AEP *]**&#x200B;ou **[!UICONTROL Value]**&#x200B;et une valeur par défaut pour mapper le champ harmonisé par défaut au champ du jeu de données ou à la valeur saisie.

      1. Lorsque vous sélectionnez **[!UICONTROL Case]**, sélectionnez **[!UICONTROL Field]** et **[!UICONTROL *champ de jeu de données AEP *]**&#x200B;ou **[!UICONTROL Value]**&#x200B;et une valeur par défaut pour mapper le champ harmonisé par défaut au champ de jeu de données ou à la valeur saisie.

         1. Pour définir explicitement des valeurs, vous définissez un ou plusieurs cas, composés d’une ou de plusieurs conditions. Chaque condition peut rechercher un champ de jeu de données **[!UICONTROL *AEP spécifique *]**&#x200B;s’il **[!UICONTROL Exists]**&#x200B;ou **[!UICONTROL Not Exists]**&#x200B;ou s’il **[!UICONTROL Contains]**,**[!UICONTROL Not Contains]**,**[!UICONTROL Equals]**,**[!UICONTROL Not Equals]**,**[!UICONTROL Starts With]**&#x200B;ou **[!UICONTROL Ends With]**&#x200B;une valeur saisie à l’adresse&#x200B;**[!UICONTROL * Saisir la valeur d’entrée *]**.

         1. Pour ajouter un autre cas, sélectionnez ![Ajouter](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add case]**. Pour ajouter une autre condition, sélectionnez ![Ajouter](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add condition]**.

         1. Pour supprimer un cas ou une condition, sélectionnez ![Fermer](/help/assets/icons/Close.svg) dans le conteneur correspondant.

         1. Pour choisir si une ou toutes les conditions doivent s’appliquer à un cas, sélectionnez **[!UICONTROL Any of]** ou **[!UICONTROL All of]**.

         1. Pour définir la valeur de résultat d’un cas, saisissez la valeur à **[!UICONTROL Then]**.

     L’exemple ci-dessous :

      * utilise un **[!UICONTROL Map Into]** **[!UICONTROL Mapping type]** pour mapper le champ harmonisé **[!UICONTROL Channel Type At Source]** au champ **[!UICONTROL channel_type]** du jeu de données **[!DNL Luma Transactions]**.

      * utilise un **[!UICONTROL Case]** **[!UICONTROL Mapping type]** pour mapper de manière conditionnelle la valeur du champ **[!UICONTROL marketing.campaignName]** dans le jeu de données **[!DNL Luma Transactions]** au champ harmonisé **[!UICONTROL Campaign]**. Le champ harmonisé de la campagne est défini sur :

         * `Black Friday` lorsque la **[!UICONTROL marketing.campaignName]** est `_black_friday` ou `BlackFriday`.
         * à la valeur du **[!UICONTROL marketing.campaignName]** dans tous les autres cas.

        ![Événement de règle du jeu de données](/help/assets/dataset-create-event.png)

1. Sélectionnez ![Ajouter](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add field]** pour définir des champs supplémentaires.

Lorsque vous avez terminé, sélectionnez **[!UICONTROL Save as draft]** pour enregistrer un brouillon de la règle ou **[!UICONTROL Save]** pour enregistrer et activer la règle. Sélectionnez **[!UICONTROL Cancel]** pour annuler la configuration de la règle.

>[!NOTE]
>
>L’expérience **[!UICONTROL Map to harmonized fields]** dédiée aux règles de jeux de données de résumé est obsolète. Toutes les règles des jeux de données utilisent désormais une expérience **[!UICONTROL Map to harmonized fields]** similaire, quel que soit le type de jeu de données. Pour les jeux de données de résumé pour lesquels vous avez défini des règles à l’aide de l’expérience **[!UICONTROL Map to harmonized fields]** obsolète, vous pouvez vérifier ces règles par rapport à l’expérience **[!UICONTROL Map to harmonized field]** générique.
>

#### Jeux de données récapitulatifs

Lorsque vous mappez un champ harmonisé standard à partir d’un jeu de données de résumé, Mix Modeler tente de déduire le champ de jeu de données Experience Platform correspondant. En cas de réussite :

* Si le champ est de type dimension, **[!UICONTROL Map into]** est sélectionné comme **[!UICONTROL Mapping type]**.
* Si le champ est de type mesure, **[!UICONTROL Sum]** est sélectionné en tant que **[!UICONTROL Mapping type]**.
* **[!UICONTROL Field]** est sélectionné comme type de mappage **[!UICONTROL Default]**.
* Le champ de jeu de données Experience Platform correspondant est inséré automatiquement pour le *champ de jeu de données AEP*.

Vous pouvez modifier les valeurs proposées si elles sont incorrectes ou ne prennent pas en charge votre cas d’utilisation spécifique.


#### Ensembles de données de facteur

Vous mappez des champs harmonisés aux champs d&#39;un jeu de données de facteurs, de sorte que vous puissiez [&#x200B; ajouter des facteurs dans le cadre de la configuration de votre modèle](/help/models/build.md).

Lorsque vous mappez des champs harmonisés à des champs dans des jeux de données de facteur, les conditions suivantes s’appliquent :

##### Nom du facteur

Lorsque vous mappez un champ de facteur harmonisé standard à partir d&#39;un jeu de données de facteur et que le jeu de données de facteur contient un seul facteur, utilisez **[!UICONTROL Map into]** comme **[!UICONTROL Mapping type]** et entrez une valeur par défaut pour le champ harmonisé **[!UICONTROL Factor Name]**.

![Règle du jeu de données - mapper le jeu de données à facteur unique](../assets/dataset-create-rule-factor-single.png)

Si le jeu de données de facteurs contient plusieurs facteurs, utilisez **[!UICONTROL Case As]** comme **[!UICONTROL Mapping Type]** pour définir un mappage entre le champ harmonisé Nom du facteur et chaque nom de facteur distinct.

![Règle de jeu de données - Mapper un jeu de données à facteur unique](../assets/dataset-create-rule-factor-multiple.png)


##### Type de facteur

Ce champ est facultatif dans le jeu de données et le schéma de facteur. Si **[!UICONTROL Factor type]** est défini dans le jeu de données et le schéma de facteur et spécifie **[!UICONTROL Internal]** ou **[!UICONTROL External]**, la valeur fournie est utilisée. Si aucune valeur n’est spécifiée, la **[!UICONTROL Internal]** par défaut est utilisée.

##### Type de valeur

Ce champ est facultatif dans le jeu de données et le schéma de facteur. Si **[!UICONTROL Value type]** est défini dans le jeu de données et le schéma de facteur et spécifie **[!UICONTROL Actual]** ou **[!UICONTROL Forecasted]**, la valeur fournie est utilisée. Si aucune valeur n’est spécifiée, la **[!UICONTROL Actual]** par défaut est utilisée.


##### Granularité

Vous pouvez définir une règle de jeu de données pour la granularité d&#39;un jeu de données de facteur lorsque tous les facteurs du jeu de données de facteur ont la même granularité source.

Dès que les jeux de données de facteurs sont harmonisés, tous les jeux de données sont conformes au niveau de granularité le plus élevé dans le jeu de données harmonisé.


##### Valeur du facteur

Pour le champ harmonisé **[!UICONTROL Factor value]**, utilisez l’un des opérateurs d’agrégation comme **[!UICONTROL Mapping Type]**. Lorsque plusieurs facteurs sont définis dans un jeu de données de facteurs, l&#39;opérateur d&#39;agrégation est appliqué à tous les facteurs.


##### Exemple

* Vous disposez d’un jeu de données de facteur, avec les données d’exemple suivantes :

  | Date et heure | Nom du facteur | Valeur du facteur |
  |---|---|---:|
  | 13 mars 2025 | _definedsp500 | 10 |
  | 13 Mars 2025 | _cpi | 20 |
  | 14 mars 2025 | _definedsp500 | 30 |
  | 14 mars 2025 | _cpi | 40 |
  | 15 Mars 2025 | _definedsp500 | 50 |
  | 15 Mars 2025 | _cpi | 60 |


* Vous définissez également les règles de jeu de données suivantes pour **[!UICONTROL Factor Name]**, **[!UICONTROL Factor Value]** et **[!UICONTROL Granularity]** :

  ![Règles du jeu de données - Exemple de facteurs](../assets/dataset-create-rule-factor-example.png)

* Les données harmonisées suivantes seront alors obtenues :

  | Nom du facteur | Valeur du facteur | Type de facteur | Type de valeur |
  |---|---:|---|---|
  | ICP | 20 | Interne | Réel |
  | S&amp;P 500 | 10 | Interne | Réel |

  Aucune règle de jeu de données n&#39;étant définie pour **[!UICONTROL Factor Type]** et **[!UICONTROL Value Type]**, les valeurs par défaut sont utilisées.

### Modifier une règle de jeu de données

Pour modifier une règle de jeu de données, dans l&#39;interface ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** dans le Mix Modeler :

1. Sélectionnez ![Plus](/help/assets/icons/More.svg) dans la colonne **[!UICONTROL Dataset]** pour la règle du jeu de données que vous souhaitez modifier.
1. Dans le menu contextuel, sélectionnez ![Modifier](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** pour commencer à modifier la règle du jeu de données. Pour plus d’informations, voir [Création d’une règle de jeu de données](#create-a-dataset-rule).


### Supprimer une règle de jeu de données

Pour supprimer une règle de jeu de données, dans l&#39;interface ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** dans le Mix Modeler :

1. Sélectionnez ![Plus](/help/assets/icons/More.svg) dans la colonne **[!UICONTROL Dataset]** pour la règle du jeu de données que vous souhaitez supprimer.
1. Dans le menu contextuel, sélectionnez ![Supprimer](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** pour supprimer la règle du jeu de données. Vous êtes invité à confirmer. Sélectionnez **[!UICONTROL Delete]** pour supprimer définitivement la règle de jeu de données sélectionnée.



## Synchroniser les données

Pour synchroniser les données entre vos jeux de données de résumé et/ou d’événement harmonisés lors de l’application de la logique dans vos règles de jeu de données :

1. Sélectionnez **[!UICONTROL Sync data]**.

1. Dans la boîte de dialogue **[!UICONTROL Sync data for dataset rules]**, sélectionnez l’une des options suivantes :
   * **[!UICONTROL Refresh harmonized data for summary datasets]**,
   * **[!UICONTROL Refresh harmonized data for event datasets]**, ou
   * **[!UICONTROL Refresh harmonized data for both summary + event datasets]**.

1. Pour démarrer la synchronisation en fonction des règles de jeu de données définies entre les données harmonisées et les données des jeux de données, sélectionnez **[!UICONTROL Sync]**. Pour annuler la synchronisation, sélectionnez **[!UICONTROL Cancel]**.

   ![Synchroniser les données](/help/assets/sync-data.png)


## Préférences de fusion des données {#data-merge-preferences}


>[!CONTEXTUALHELP]
>id="harmonizeddata_datasetrules_datamergepreferences"
>title="Préférence de mesure par défaut"
>abstract="La préférence par défaut est appliquée lorsque, lors de l’harmonisation, plusieurs sources de données tentent de mettre à jour un champ de mesure pour un canal donné. Cette préférence est appliquée au niveau du sandbox, sauf si elle est remplacée pour certaines préférences de mesures définies ci-dessous."


>[!NOTE]
>
>[!BADGE bêta]{type=Informative} Les préférences de fusion des données sont une fonctionnalité bêta et ses fonctionnalités peuvent changer.

Pour garantir des prédictions de modèle précises, vous pouvez définir des préférences de fusion des données. Cette fonctionnalité permet aux utilisateurs de résoudre les conflits après la fusion des données au niveau du résumé et au niveau de l’événement.

Vous pouvez configurer une préférence de mesure par défaut à appliquer en cas de conflits de mises à jour. Cette mesure par défaut peut être l’une des trois options suivantes :

* **[!UICONTROL Summary data]**
* **[!UICONTROL Sum of summary and event data]**
* **[!UICONTROL Event data]**

Lorsque, lors de l’harmonisation, plusieurs sources de données tentent de mettre à jour un champ de mesure pour un canal donné, la préférence par défaut configurée par l’utilisateur est appliquée. Cette préférence est appliquée au niveau du sandbox, sauf si elle est remplacée pour certaines préférences basées sur des mesures configurées en plus.

Sous **[!UICONTROL Metric based preferences]**, l&#39;utilisateur peut configurer la source spécifique (**[!UICONTROL Summary]** ou **[!UICONTROL Event]**) pour une mesure donnée et le type de conversion correspondant pour cette mesure.

Les cas d’utilisation standard sont les suivants :

* la même mesure publicitaire est mesurée et signalée dans plusieurs jeux de données, ou
* la mesure des mesures peut être incomplète dans certains jeux de données, tandis qu’un autre jeu de données peut être un sur-ensemble d’une mesure particulière, ce qui entraîne un double comptage.

### Configuration

Pour configurer les préférences de fusion des données :


1. Sélectionnez ![Préférences de fusion des données](/help/assets/icons/Merge.svg) [!BADGE bêta].

1. Dans la boîte de dialogue **[!UICONTROL Data merge preferences]** [!BADGE Beta]{type=Informative} :

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

Lorsque vous revenez à votre configuration **[!UICONTROL Dataset rules]**, une boîte de dialogue s’affiche pour expliquer qu’un ou plusieurs des jeux de données sources ont été supprimés. Les données harmonisées sont affectées lors d’une prochaine synchronisation ad hoc ou planifiée. Vérifiez la configuration de la règle du jeu de données.

Les données harmonisées sont mises à jour sans les données source supprimées lors de la prochaine synchronisation ad hoc ou synchronisation planifiée. Cependant, vous continuez à voir des boîtes de dialogue d’alerte vous invitant à supprimer la règle du jeu de données en fonction du jeu de données source supprimé. Cette alerte permet aux utilisateurs d’afficher et d’évaluer les champs affectés dans le jeu de données supprimé. et pour déterminer l’impact sur les points de contact marketing ou les conversions pouvant être utilisées dans n’importe quel modèle. Une fois que vous avez examiné et atténué cet impact, vous devez supprimer la règle du jeu de données de la liste de configuration de la règle du jeu de données.
