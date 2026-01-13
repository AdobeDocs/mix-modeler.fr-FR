---
title: Présentation des plans
description: Découvrez comment afficher, sélectionner et agir sur les plans dans Mix Modeler.
feature: Plans
exl-id: 45a8dc30-3259-493d-8ea5-1899903733a6
source-git-commit: 2775c5a3779f6731f7f3143f6ed21db2993c0955
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Présentation des plans

Dans Mix Modeler, les plans vous permettent de répartir les budgets par unité opérationnelle et canal. La fonctionnalité de planification est intégrée aux résultats des modèles entraînés en fonction de vos données harmonisées.

Un plan décrit les investissements discrétionnaires (par exemple, les budgets) qu&#39;une entreprise a l&#39;intention de consacrer à des projets liés au marketing au cours d&#39;une période donnée. Ces investissements sont au service d’indicateurs clés de performance courants (par exemple, commandes, chiffre d’affaires). Les forfaits peuvent inclure des dépenses liées à des canaux comme la publicité payante, le contenu Web parrainé, des événements.

Un plan nécessite :

- un modèle,
- une plage de données,
- un budget.

Un plan peut éventuellement inclure les éléments suivants :

- une fenêtre de reconnaissance configurée,
- plusieurs dates de vol avec chacune un budget cible,
- contraintes budgétaires minimales et maximales par canal et par date de vol.

Si un modèle que vous avez utilisé pour votre plan est noté sur de nouvelles données, vous devez créer un nouveau plan pour prendre en compte les données re-notées.


## Créer des plans

Pour créer un plan, utilisez l’assistant de création de plan Mix Modeler. Voir [Créer des plans](build.md) pour plus d’informations.


## Gestion des plans

Pour afficher un tableau de vos plans actuels, dans l’interface de Mix Modeler :

1. Sélectionnez ![](/help/assets/icons2/FileChart.svg) **[!UICONTROL Plans]** dans le rail de gauche.

1. Vous voyez un tableau des plans actuels et de leur statut.

   Les colonnes du tableau indiquent les détails des plans.

   | Nom de la colonne | Détails |
   |---|---|
   | **[!UICONTROL Name]** | Nom du plan |
   | **[!UICONTROL Model]** | Modèle utilisé comme base du plan. |
   | **[!UICONTROL Date range]** | Période complète d’un plan. |
   | **[!UICONTROL Budget]** | Budget total d’un plan. |
   | **[!UICONTROL Plan target]** | Mesure cible définie pour un plan basé sur une cible. |
   | **[!UICONTROL Forecasted return]** | Le [retour prévu](/help/main-guide/glossary.md) pour un plan |
   | **[!UICONTROL Forecasted ROI]** | Le [retour sur investissement prévu](/help/main-guide/glossary.md) d’un plan. |
   | **[!UICONTROL Forecasted conversion]** | La [conversion prévue](/help/main-guide/glossary.md) pour un plan |
   | **[!UICONTROL Forecasted CPA]** | [CPA prévu](/help/main-guide/glossary.md) pour un plan |
   | **[!UICONTROL Status]** | Statut d’un plan : <br/>![StatusOrange](/help/assets/icons/StatusOrange.svg) **[!UICONTROL Failed]**,<br/>![StatusBlue](/help/assets/icons/StatusBlue.svg) **[!UICONTROL Processing]** ou<br/>![StatusGreen](/help/assets/icons/StatusGreen.svg) **[!UICONTROL Complete]**. |

   Vous pouvez utiliser ![ColumnSetting](/help/assets/icons/ColumnSetting.svg) pour sélectionner ![Checkmark](/help/assets/icons/Checkmark.svg) les colonnes à afficher dans le tableau.

   Pour trier le tableau sur n’importe quelle colonne dans l’ordre croissant ![ArrowMoveUp](/help/assets/icons2/ArrowMoveUp.svg) ou décroissant ![ArrowMoveDown](/help/assets/icons2/ArrowMoveDown.svg)order, sélectionnez le titre de la colonne.

   Pour trier ou redimensionner la colonne **[!UICONTROL Name]**, **[!UICONTROL Model]** ou **[!UICONTROL Date range]**, sélectionnez **[!UICONTROL Name]** ![ChevronDown](/help/assets/icons/ChevronDown.svg), **[!UICONTROL Model]** ![ChevronDown](/help/assets/icons/ChevronDown.svg) ou **[!UICONTROL Date range]** ![ChevronDown](/help/assets/icons/ChevronDown.svg). Dans le menu contextuel, sélectionnez **[!UICONTROL Sort ascending]**, **[!UICONTROL Sort descending]** ou **[!UICONTROL Resize column]**. Vous pouvez également pointer sur le séparateur de colonnes pour ces colonnes afin de redimensionner une colonne.

1. Utilisez ![Rechercher](/help/assets/icons/Search.svg) pour rechercher et filtrer la table pour un ou plusieurs plans spécifiques.

### Informations sur le plan

Pour afficher les informations d’un plan et modifier un plan :

1. Sélectionnez ![PLan](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** dans le rail de gauche.

1. Sélectionnez le nom du plan.

Vous êtes redirigé vers [&#x200B; Informations sur le plan &#x200B;](insights.md).


### Dupliquer un plan

Pour dupliquer un plan :

- Sélectionnez ![Plus](/help/assets/icons/More.svg) pour un plan. Dans le menu contextuel, sélectionnez **[!UICONTROL Duplicate]**.
- Vous pouvez également sélectionner un plan dans le tableau ![SelectBox](/help/assets/icons/SelectBox.svg) et sélectionner ![Copy](/help/assets/icons/Copy.svg) **[!UICONTROL Duplicate]** dans la barre d’actions bleue.

Un nouveau plan est créé, dont le nom est composé du nom du plan d’origine suivi de **[!UICONTROL (Copy)] (_n_)**. Vous êtes automatiquement redirigé vers [Création du plan](build.md) pour fournir des détails mis à jour pour le plan copié.

- Les détails (tels que la description, le budget, etc.) du plan d’origine sont copiés.
- Les contraintes budgétaires du plan d&#39;origine sont copiées dans le plan nouvellement créé.
- Vous avez la possibilité de sélectionner un autre modèle comme base du plan copié.
   - Pour les points de contact ou les canaux qui existent dans le plan copié mais qui n’existent pas dans le modèle nouvellement sélectionné, les contraintes de ces points de contact ou canaux sont supprimées du plan.
   - Pour les points de contact ou les canaux qui n’existent pas dans le plan copié, mais qui existent dans le modèle nouvellement sélectionné, les contraintes sont définies sur :
      - une valeur minimale de `0`,
      - valeur maximale conforme au budget de la plage de vol du plan.



### Comparer les plans

Pour comparer des plans :

1. Sélectionnez deux plans dans le tableau.
1. Sélectionnez ![Comparer](/help/assets/icons/Compare.svg) **[!UICONTROL Compare]** dans la barre d’actions bleue. L’interface utilisateur de **[!UICONTROL Compare plans]** s’affiche.


### Supprimer des plans

Pour supprimer un plan :

1. Sélectionnez ![Plus](/help/assets/icons/More.svg) pour un plan. Dans le menu contextuel, sélectionnez **[!UICONTROL Delete]**. <br/>Vous pouvez également sélectionner un plan dans le tableau ![SelectBox](/help/assets/icons/SelectBox.svg) et sélectionner ![Delete](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** dans la barre d’actions bleue.
1. Sélectionnez **[!UICONTROL Delete]** dans la boîte de dialogue de confirmation de **[!UICONTROL Delete plan]** pour supprimer le plan. Sélectionnez **[!UICONTROL Cancel]** pour annuler.

Pour supprimer plusieurs plans :

1. Sélectionnez plusieurs plans.
1. Dans la barre d’actions bleue, sélectionnez ![Supprimer](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** de supprimer les plans.
1. Sélectionnez **[!UICONTROL Delete]** dans la boîte de dialogue de confirmation **[!UICONTROL Delete *x *plans]**&#x200B;pour supprimer les plans. Sélectionnez **[!UICONTROL Cancel]**&#x200B;pour annuler.


