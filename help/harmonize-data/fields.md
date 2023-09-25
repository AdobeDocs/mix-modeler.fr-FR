---
title: Champs harmonisés
description: Découvrez comment définir des champs à utiliser dans le cadre de l’harmonisation de vos données dans Adobe Mix Modeler.
feature: Harmonized Data
source-git-commit: abbfc78e9fa774a240d000131f35d3dc257c15ea
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 11%

---


# Champs harmonisés

Les champs harmonisés permettent de définir des champs pour les mêmes données conceptuellement, provenant de sources différentes, chacune ayant sa propre définition de ces données. Par exemple, une mesure des clics peut être définie et nommée différemment selon la source de données. Un champ harmonisé de clics vous permet de définir une nomenclature commune pour une mesure de clics basée sur ces différentes sources de données de clics.

Les champs harmonisés permettent de définir les champs que vous souhaitez utiliser dans le cadre du workflow d&#39;harmonisation des données. Les champs que vous définissez peuvent être utilisés pour définir des règles de jeu de données, des points de contact marketing et des conversions.

## Champs d&#39;harmonisation globaux

Les champs d’harmonisation globale par défaut disponibles dans Adobe Mix Modeler sont les suivants :


| Nom du champ | Nom d’affichage | Catégorie | Type de données | Commentaire |
| ---------------------- | ---------------------- | --------- | --------- | --------- |
| marque | Marque | Dimension | Chaîne |           |
| campaign | Campaign | Dimension | Chaîne |           |
| channel | Canal | Dimension | Chaîne |           |
| channel_id | Identifiant de canal | Dimension | Chaîne |           |
| channel_type_at_source | Type de canal à la source | Dimension | Chaîne |           |
| channel | Canal | Dimension | Chaîne |           |
| clics | Clics | Mesure | Nombre |           |
| conversionType | Type de conversion | Dimension | Chaîne |           |
| coût | Coût | Mesure | Devise |           |
| dataset | Jeu de données | Dimension | Chaîne |           |
| date_type | Type de date | Dimension | Chaîne | jour, semaine |
| emailsent | Emails envoyés | Mesure | Nombre |           |
| event_date | Date | Dimension | DateTime |           |
| brut_demand | Demande brute | Mesure | Devise |           |
| impressions | Impressions | Mesure | Nombre |           |
| last_updated_date | Date de dernière mise à jour | Dimension | DateTime |           |
| linkvisites | Visites de lien | Mesure | Nombre |           |
| mediatype | Type de média | Dimension | Chaîne |           |
| net_sales | Ventes nettes | Mesure | Devise |           |
| commandes | Commandes | Mesure | Nombre |           |
| sourceType | Type de source | Dimension | Chaîne |           |
| dépenser | Dépenser | Mesure | Devise |           |
| trafficsource | Traffic Source | Dimension | Chaîne |           |

{style="table-layout:auto"}

Vous pouvez ajouter, modifier ou supprimer vos propres champs harmonisés en plus de ces champs harmonisés globaux.

## Gérer les champs harmonisés

Pour afficher un tableau des champs harmonisés disponibles, dans l’interface Adobe Mix Modeler :

1. Sélectionner ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** dans le rail de gauche.

1. Sélectionner **[!UICONTROL Fields]** dans la barre supérieure. Un tableau des champs harmonisés s’affiche.

   Les colonnes du tableau spécifient les détails des champs harmonisés

   | Nom de la colonne | Détails |
   | ---------------------- | ----------|
   | Nom du champ | Nom du champ harmonisé. |
   | Nom d’affichage | Nom d’affichage du champ harmonisé. Ce nom d’affichage est utilisé lors de la définition de règles de jeu de données, de points de contact marketing et de définitions de conversion. |
   | Catégorie | Indique si un champ de données harmonisé est une [!UICONTROL Dimension], un [!UICONTROL Metric] ou [!UICONTROL Derived]. Une catégorie dérivée est un champ harmonisé à l’aide d’une définition de formule basée sur des mesures. |
   | Propriétaire | Indique si un champ harmonisé est un champ par défaut ([!UICONTROL Global]), ou est défini par vous ([!UICONTROL Client]). |
   | Type de données | Spécifie le type de données ([!UICONTROL Number], [!UICONTROL String], [!UICONTROL Currency], [!UICONTROL DateTime]). |
   | Date et heure de création | Date et heure de création du champ harmonisé. |
   | Date et heure de la dernière modification | Données et heure de la dernière modification du champ harmonisé. |
   | Formule | Indique la formule d’un champ harmonisé en fonction d’une catégorie dérivée. |

   {style="table-layout:auto"}

1. Pour rechercher un champ harmonisé spécifique, utilisez ![Rechercher](../assets/icons/Search.svg) **[!UICONTROL *Rechercher un champ harmonisé&#x200B;*]**.




### Ajouter un champ harmonisé

Pour ajouter un champ harmonisé, dans ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** dans le Adobe Mix Modeler :

1. Sélectionner ![Ajouter](../assets/icons/AddCircle.svg)Ajouter un champ.

1. Dans le **[!UICONTROL Create]** dialog :

   1. Saisissez un **[!UICONTROL Field name]**, par exemple `region`.
   1. Saisissez un **[!UICONTROL Display name]**, par exemple `Region`.
   1. Sélectionnez une **[!UICONTROL Category]**: **[!UICONTROL Dimension]**, **[!UICONTROL Metric]** ou **[!UICONTROL Derived]**.

      Lorsque vous sélectionnez **[!UICONTROL Derived]**, spécifiez une **[!UICONTROL Formula]**. Pour créer une expression arithmétique valide, combinez une ou plusieurs mesures à partir de **[!UICONTROL Insert Metric]** avec un ou plusieurs opérateurs **[!UICONTROL + - * / ( )]** . Par exemple, `[orders]/[impressions]`

   1. Sélectionnez une **[!UICONTROL Data type]**.

      - **[!UICONTROL String]** ou **[!UICONTROL DateTime]**, lorsque la catégorie sélectionnée est Dimension.
      - **[!UICONTROL Number]** ou **[!UICONTROL Currency]** lorsque la catégorie sélectionnée est Mesure ou Dérivée.

   1. Sélectionner **[!UICONTROL Submit]** ajouter le champ harmonisé. Sélectionner **[!UICONTROL Close]** pour fermer la boîte de dialogue sans ajouter le champ harmonisé.

      ![Création d’un champ](../assets/create-field.png)


### Modifier un champ harmonisé

Vous ne pouvez modifier que les champs harmonisés que vous avez créés précédemment. Vous ne pouvez pas modifier un champ harmonisé global.

Pour modifier un champ harmonisé, dans ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** dans le Adobe Mix Modeler :

1. Sélectionnez le champ harmonisé que vous souhaitez modifier. Par exemple, **[!UICONTROL Region]**.

1. Dans le **[!UICONTROL Edit harmonization values]** volet, modifier les valeurs de **[!UICONTROL Display name]**, **[!UICONTROL Category]**, et **[!UICONTROL Data type]**.

1. Sélectionner **[!UICONTROL Submit]** pour appliquer les modifications au champ harmonisé.

   ![Modifier un champ](../assets/edit-field.png)

### Supprimer un champ harmonisé

Vous ne pouvez supprimer que les champs harmonisés que vous avez créés précédemment. Vous ne pouvez pas supprimer un champ harmonisé global.

Pour supprimer un champ harmonisé, dans ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** dans le Adobe Mix Modeler :

1. Sélectionnez le champ harmonisé à supprimer, par exemple **[!UICONTROL Region]**.

1. Sélectionner ![Supprimer](../assets/icons/Delete.svg) **[!UICONTROL Delete]** de la **[!UICONTROL Edit harmonization values]** volet de gauche.


