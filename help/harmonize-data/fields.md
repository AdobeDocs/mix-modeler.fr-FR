---
title: Champs harmonisés
description: Découvrez comment définir des champs à utiliser dans le cadre de l’harmonisation de vos données dans Mix Modeler.
feature: Harmonized Data, Harmonized Fields
exl-id: f051279a-1ae9-49bd-a946-abfc34c90413
TQID: https://experienceleague.adobe.com/NlB6aA4AO-0Tpbb9SibgUz0eVUgs8roO9Mju2M8tl7s
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: a567f0f7-0057-4079-8ded-5b24cc25af15
subfeature_v2:
  - id: d4b8ba18-64c1-4413-be54-74405ec7f558
  - id: b4655f7e-1a6e-4fa3-a7c5-3c34d4786e49
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
autotag-review: '2026-05-01T09:13:17.577Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 688
ht-degree: 11%

---

# Champs harmonisés

Les champs harmonisés vous permettent de définir des champs pour des données conceptuellement identiques, provenant de différentes sources, chacune ayant sa propre définition de ces données. Par exemple, une mesure clics peut être définie et nommée différemment en fonction de la source des données. Un champ harmonisé de clics vous permet de définir une nomenclature commune pour une mesure de clics en fonction de ces différentes sources de données de clics.

Les champs harmonisés vous permettent de définir les champs à utiliser dans le cadre du workflow d’harmonisation des données. Les champs que vous définissez peuvent être utilisés dans la définition de règles de jeux de données, de points de contact marketing et de conversions.

## Champs d’harmonisation globale

Les champs d’harmonisation globale disponibles par défaut dans Mix Modeler sont les suivants :


| Nom du champ | Nom d’affichage | Catégorie | Type de données | Commentaire |
| ---------------------- | ---------------------- | --------- | --------- | --------- |
| marque | Marque | Dimension | Chaîne |           |
| campagne | Campaign | Dimension | Chaîne |           |
| channel | Canal | Dimension | Chaîne |           |
| channel_id | Identifiant du canal | Dimension | Chaîne |           |
| channel_type_at_source | Type De Canal Au Niveau De Source | Dimension | Chaîne |           |
| channel | Canal | Dimension | Chaîne |           |
| clics | Clics | Mesure | Nombre |           |
| conversiontype | Type de conversion | Dimension | Chaîne |           |
| coût | Coût | Mesure | Devise |           |
| Jeu de données | Jeu de données | Dimension | Chaîne |           |
| date_type | Type de date | Dimension | Chaîne | jour, semaine |
| emailssent | E-mails envoyés | Mesure | Nombre |           |
| event_date | Date | Dimension | Date et heure |           |
| brut_demand | Demande Brute | Mesure | Devise |           |
| impressions | Impressions | Mesure | Nombre |           |
| last_updated_date | Date de la dernière mise à jour | Dimension | Date et heure |           |
| linkvisites | Lier les visites | Mesure | Nombre |           |
| mediatype | Type de média | Dimension | Chaîne |           |
| net_sales | Ventes nettes | Mesure | Devise |           |
| commandes | Commandes | Mesure | Nombre |           |
| type de source | Type de Source | Dimension | Chaîne |           |
| dépenser | Dépenses | Mesure | Devise |           |
| source du trafic | Source de trafic | Dimension | Chaîne |           |

{style="table-layout:auto"}

Vous pouvez ajouter, modifier ou supprimer vos propres champs harmonisés en plus de ces champs harmonisés globaux.

## Gestion des champs harmonisés

Pour afficher un tableau des champs harmonisés disponibles, dans l’interface de Mix Modeler :

1. Sélectionnez ![Recherche de données](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** dans le rail de gauche.

1. Sélectionnez **[!UICONTROL Fields]** dans la barre supérieure. Un tableau des champs harmonisés s’affiche. Si d’autres pages sont disponibles, utilisez ![Flèche vers la gauche](/help/assets/icons/ChevronLeft.svg) ou ![Flèche vers la droite](/help/assets/icons/ChevronRight.svg) à **[!UICONTROL Page _x _de_x_]** pour vous déplacer entre les pages du tableau.

   Les colonnes du tableau indiquent des détails sur les champs harmonisés

   | Nom de la colonne | Détails |
   | ---------------------- | ----------|
   | Nom du champ | Nom du champ harmonisé. |
   | Nom d’affichage | Nom d’affichage du champ harmonisé. Ce nom d’affichage est utilisé lors de la définition de règles de jeux de données, de points de contact marketing et de définitions de conversion. |
   | Catégorie | Indique si un champ de données harmonisé est un [!UICONTROL Dimension], un [!UICONTROL Metric] ou un [!UICONTROL Derived]. Une catégorie dérivée est un champ harmonisé utilisant une définition de formule basée sur des mesures. |
   | Type de données | Indique le type de données ([!UICONTROL Number], [!UICONTROL String], [!UICONTROL Currency], [!UICONTROL Date time]). |
   | Date de création | Date et heure de création du champ harmonisé. |
   | Propriétaire | Indique si un champ harmonisé est un champ par défaut ([!UICONTROL Global]) ou s’il est défini par vous ([!UICONTROL Client]). |
   | Date de dernière modification | Données et heure de la dernière modification du champ harmonisé. |
   | Formule | Spécifie la formule d&#39;un champ harmonisé basé sur une catégorie dérivée. |

   {style="table-layout:auto"}

1. Pour rechercher un champ harmonisé spécifique, utilisez ![Rechercher](/help/assets/icons/Search.svg) **[!UICONTROL *Rechercher le champ harmonisé&#x200B;*]**.


### Ajouter un champ harmonisé

Pour ajouter un champ harmonisé, dans l’interface ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** de Mix Modeler :

1. Sélectionnez ![Ajouter](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add field]**.

1. Dans la boîte de dialogue **[!UICONTROL Create]** :

   1. Saisissez un **[!UICONTROL Field name]**, par exemple `region`.
   1. Saisissez un **[!UICONTROL Display name]**, par exemple `Region`.
   1. Sélectionnez un **[!UICONTROL Category]** : **[!UICONTROL Dimension]**, **[!UICONTROL Metric]** ou **[!UICONTROL Derived]**.

      Lorsque vous sélectionnez **[!UICONTROL Derived]**, spécifiez un **[!UICONTROL Formula]**. Pour créer une expression arithmétique valide, combinez une ou plusieurs mesures issues de **[!UICONTROL Insert Metric]** avec un ou plusieurs opérateurs **[!UICONTROL + - * / ( )]** . Par exemple, `[orders]/[impressions]`

   1. Sélectionnez un **[!UICONTROL Data type]**.

      - **[!UICONTROL String]** ou **[!UICONTROL Date time]**, lorsque Catégorie sélectionnée est Dimension.
      - **[!UICONTROL Number]** ou **[!UICONTROL Currency]** lorsque la catégorie sélectionnée est Mesure ou Dérivé.

   1. Sélectionnez **[!UICONTROL Submit]** pour ajouter le champ harmonisé. Sélectionnez **[!UICONTROL Close]** pour fermer la boîte de dialogue sans ajouter le champ harmonisé.

      ![Créer un champ](/help/assets/create-field.png)


### Modifier un champ harmonisé

Vous pouvez uniquement modifier les champs harmonisés que vous avez créés précédemment (le propriétaire est le client). Vous ne pouvez pas modifier un champ harmonisé global.

Pour modifier un champ harmonisé, dans l’interface ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** de Mix Modeler :

1. Sélectionnez le champ harmonisé à modifier. Par exemple : **[!UICONTROL Region]**.

1. Dans le volet de **[!UICONTROL Edit harmonization values]**, modifiez les valeurs de **[!UICONTROL Display name]**, **[!UICONTROL Category]** et **[!UICONTROL Data type]**. Voir [Ajouter un champ harmonisé](#add-a-harmonized-field) pour plus d’informations.

1. Sélectionnez **[!UICONTROL Submit]** pour appliquer les modifications au champ harmonisé.

   ![Modifier un champ](/help/assets/edit-field.png)

### Supprimer un champ harmonisé

Vous ne pouvez supprimer que les champs harmonisés que vous avez créés précédemment (le propriétaire est le client). Vous ne pouvez pas supprimer un champ harmonisé global.

Pour supprimer un champ harmonisé, dans l’interface ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** de Mix Modeler :

1. Sélectionnez le champ harmonisé à supprimer, par exemple **[!UICONTROL Region]**.

1. Sélectionnez ![Supprimer](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** dans le volet **[!UICONTROL Edit harmonization values]** gauche.

   >[!WARNING]
   >
   >   Le champ sera immédiatement supprimé.

