---
title: de conversions
description: Découvrez comment créer des conversions à utiliser dans le cadre de l’harmonisation de vos données dans Mix Modeler.
feature: Harmonized Data, Conversions
exl-id: a8559426-452a-43e8-9a60-0c0bc97d863c
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 2%

---

# de conversions

Les événements de conversion sont des objectifs commerciaux qui identifient l’impact des activités marketing. Exemples : commandes e-commerce, achats en magasin, visites sur le site web, etc.

Vous définissez des conversions marketing pour l’analyse d’attribution.

## Gestion des conversions

Pour afficher un tableau des conversions disponibles, dans l’interface du Mix Modeler :

1. Sélectionnez ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** dans le rail de gauche.

1. Sélectionnez **[!UICONTROL Conversions]** dans la barre supérieure. Un tableau des conversions s’affiche.

Les colonnes du tableau spécifient les détails de la conversion :

| Nom de la colonne | Détails |
| --- | ---|
| Nom | Nom de la conversion. |
| Recettes | Mesure de données harmonisée à utiliser pour calculer les recettes d’une conversion. |
| Mesure de conversion | Mesure de données harmonisée à utiliser comme mesure de conversion à des fins d’analyse. |
| Catégorie | La catégorie de conversion de la conversion. |
| Créé | Date et heure de création de la conversion. |
| Dernière modification | Date et heure de la dernière modification de la conversion. |

{style="table-layout:auto"}

## Ajouter une conversion

Pour ajouter une conversion, dans l’interface ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Conversion]** en Mix Modeler :

1. Sélectionnez ![Ajouter](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add a conversion]**.

1. Dans la boîte de dialogue **[!UICONTROL Create conversion]** :

   1. Saisissez un nom pour **[!UICONTROL Conversion]**, par exemple `Store Conversions`.

   1. Définissez le **[!UICONTROL Conversion category]**.

      1. Sélectionnez une valeur dans **[!UICONTROL *Sélectionner une harmonisation...*]**, par exemple `Conversion types`.

      1. Sélectionnez une valeur pour l’opérateur ![Chevron](/help/assets//icons/ChevronDown.svg), par exemple **[!UICONTROL is]**.

      1. Sélectionnez une valeur **[!UICONTROL *Select value *]**ou saisissez une valeur, par exemple **[!UICONTROL Store]**.

   1. Sélectionnez un champ harmonisé à partir de **[!UICONTROL Conversion metric for analysis]**, par exemple **[!UICONTROL Orders]**.

   1. Sélectionnez un champ harmonisé à partir de **[!UICONTROL Revenue field]**, par exemple **[!UICONTROL Gross Demand]**.

   1. Pour créer la conversion, sélectionnez **[!UICONTROL Create]**. Pour annuler la création d’une conversion, sélectionnez **[!UICONTROL Cancel]**.

      ![Texte secondaire](/help/assets//create-conversion.png)

1. Une fois créée, la conversion est ajoutée au tableau des conversions.


## Afficher une conversion

Pour afficher une conversion :

1. Sélectionnez ![Plus](/help/assets//icons/More.svg) lorsque vous placez le pointeur de la souris sur un nom de conversion dans le tableau.

1. Sélectionnez ![Affichage](/help/assets//icons/ViewDetail.svg) **Affichage**. Une boîte de dialogue affiche les détails de la conversion. Pour plus d’informations, voir [Ajout d’une conversion](#add-a-conversion) . Sélectionnez **[!UICONTROL Cancel]** pour fermer la boîte de dialogue.


## Suppression d’une conversion

Pour supprimer une conversion :

1. Sélectionnez ![Supprimer](/help/assets//icons/Delete.svg) **Supprimer** lorsque vous placez le pointeur de la souris sur un nom de conversion dans la table.
1. Dans la boîte de dialogue de confirmation **[!UICONTROL Delete conversion]**, sélectionnez **[!UICONTROL Delete]** pour supprimer définitivement la conversion.
