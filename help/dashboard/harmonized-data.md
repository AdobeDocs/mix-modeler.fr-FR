---
title: Tableau de bord de présentation des données harmonisé
description: Découvrez comment utiliser le tableau de bord de présentation des données harmonisé en Mix Modeler.
feature: Dashboard, Harmonized Data
exl-id: fbb01613-d648-4db1-a782-a7720b7a03ad
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Présentation des données harmonisées

L’onglet Données harmonisées de l’aperçu du Mix Modeler fournit des informations sur les données harmonisées que vous avez configurées pour être utilisées dans le cadre de la configuration des données ingérées et des données harmonisées.

L’aperçu présente quatre widgets de carte d’état des indicateurs de performance clés (ligne supérieure) et six autres widgets configurables.

Pour modifier la période des données à afficher dans les widgets, saisissez manuellement une date de début et une date de fin ou sélectionnez une période à l’aide du ![calendrier](/help/assets//icons/Calendar.svg).

## Filtres de données

Vous pouvez filtrer les données affichées pour tous les widgets à l’aide du volet ![Filter](/help/assets//icons/Filter.svg) **[!UICONTROL Category Filters]** .

Sélectionnez un ou plusieurs filtres pour chaque catégorie (**[!UICONTROL Brands]**, **[!UICONTROL Campaigns]**, **[!UICONTROL Cannels Type]**, **[!UICONTROL Conversion types]**, **[!UICONTROL Datasets]**, **[!UICONTROL Media types]**, **[!UICONTROL Source types]** et **[!UICONTROL Traffic Source]**).

Les filtres sélectionnés s’affichent au-dessus des widgets à l’emplacement **[!UICONTROL FILTERING BY:]**.

1. Pour supprimer un filtre individuel, sélectionnez ![Fermer](/help/assets//icons/Close.svg) sur le filtre, répertorié à l’adresse **[!UICONTROL FILTERING BY:]**.

1. Vous pouvez rapidement effacer tous les filtres à l’aide de **[!UICONTROL Clear All]**.

![Présentation des données harmonisée](/help/assets//harmonized-data-overview.png)


## Configuration d’un widget

Vous pouvez configurer chaque widget.

* Sur le widget de carte d’état des indicateurs de performance clés :

   1. Sélectionnez ![Edit](/help/assets//icons/Edit.svg) et ![Edit](/help/assets//icons/Edit.svg) **[!UICONTROL Edit data]** dans le menu contextuel.

   1. Dans la boîte de dialogue **[!UICONTROL KPI status card]** :

      1. Sélectionnez un **[!UICONTROL KPI]** dans la liste.

      1. Sélectionnez **[!UICONTROL Apply]** pour appliquer la modification à la carte. Sélectionnez **[!UICONTROL Cancel]** pour annuler la modification.

* Sur les autres widgets configurables :

   1. Sélectionnez ![Edit](/help/assets//icons/Edit.svg) et ![Edit](/help/assets//icons/Edit.svg) **[!UICONTROL Edit data]** dans le menu contextuel.

   1. Dans la boîte de dialogue **[!UICONTROL Edit Data]** :

      1. Sélectionnez une mesure **[!UICONTROL Select a metric]**, par exemple **[!UICONTROL Impressions]**.
      1. Sélectionnez une catégorie parmi **[!UICONTROL Select category]**, par exemple **[!UICONTROL Media types]**.
      1. (facultatif) sélectionnez une deuxième catégorie de **[!UICONTROL Select second category (optional)]**, par exemple **[!UICONTROL Traffic sources]**.
      1. Sélectionnez ![Horloge](/help/assets//icons/Clock.svg) **[!UICONTROL Time]** ou ![Calculateur](/help/assets//icons/Calculator.svg) **[!UICONTROL Total]** comme type d’analyse à **[!UICONTROL Select analysis type]**.

         Si vous sélectionnez ![Horloge](/help/assets//icons/Clock.svg) **[!UICONTROL Time]**, vous pouvez spécifier la fréquence. Sélectionnez **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** ou **[!UICONTROL Quarterly]** dans **[!UICONTROL Select time frequency]**.

         Un aperçu mis à jour de votre sélection actuelle s’affiche dans le [!UICONTROL Preview Area] et de votre widget actuel sous le [!UICONTROL Current].

         ![Modifier le widget de données harmonisé](/help/assets//edit-harmonized-data-widget.png)

         Si l’aperçu ne peut pas être rendu en raison de l’indisponibilité des données, ![Erreur de données](/help/assets//icons/DataUnavailable.svg) [!UICONTROL Insights Not Available] - [!UICONTROL Harmonized fields are not available] s’affiche.

      1. Sélectionnez **[!UICONTROL Apply]** pour appliquer les modifications au widget. Sélectionnez **[!UICONTROL Cancel]** pour annuler toute modification apportée au widget actuel.
