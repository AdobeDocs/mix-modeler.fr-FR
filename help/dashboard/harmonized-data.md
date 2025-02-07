---
title: Tableau de bord de données harmonisé
description: Découvrez comment utiliser le tableau de bord de présentation des données harmonisées dans Mix Modeler.
feature: Dashboard, Harmonized Data
exl-id: fbb01613-d648-4db1-a782-a7720b7a03ad
source-git-commit: f073e8f44fc2aa731a69725ebdb99700d1f91a91
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Données harmonisées

L’onglet **[!UICONTROL Harmonized data]** du Mix Modeler ![Accueil](/help/assets/icons/Home.svg) **[!UICONTROL Overview]** fournit des informations sur les données harmonisées que vous avez configurées pour être utilisées dans le cadre de la configuration des données ingérées et des données harmonisées.

La présentation présente quatre visualisations de carte de statut des KPI (ligne supérieure) et six autres visualisations configurables .

Pour modifier la période des données à afficher dans les visualisations, saisissez une date de début et une date de fin manuellement ou sélectionnez une période à l’aide du ![Calendrier](/help/assets/icons/Calendar.svg).

## Filtres de données

Vous pouvez filtrer les données affichées pour toutes les visualisations à l’aide du volet **[!UICONTROL Category Filters]** ![Filtrer](/help/assets/icons/Filter.svg).

Sélectionnez un ou plusieurs filtres pour chaque catégorie (**[!UICONTROL Brands]**, **[!UICONTROL Campaigns]**, **[!UICONTROL Cannels Type]**, **[!UICONTROL Conversion types]**, **[!UICONTROL Datasets]**, **[!UICONTROL Media types]**, **[!UICONTROL Source types]** et **[!UICONTROL Traffic Source]**).

Les filtres sélectionnés s’affichent au-dessus des visualisations à l’**[!UICONTROL FILTERING BY:]**.

1. Pour supprimer un filtre individuel, sélectionnez ![Fermer](/help/assets/icons/Close.svg) sur le filtre, répertorié à l’**[!UICONTROL FILTERING BY:]**.

1. Vous pouvez rapidement effacer tous les filtres à l’aide de **[!UICONTROL Clear All]**.

![Présentation harmonisée des données](/help/assets/harmonized-data-overview.png)


## Configuration d’une visualisation

Vous pouvez configurer chaque visualisation.

* Dans la visualisation de la carte de statut des KPI :

   1. Sélectionnez ![Modifier](/help/assets/icons/Edit.svg) et ![Modifier](/help/assets/icons/Edit.svg) **[!UICONTROL Edit data]** dans le menu contextuel.

   1. Dans la boîte de dialogue **[!UICONTROL KPI status card]** :

      1. Sélectionnez un **[!UICONTROL KPI]** dans la liste.

      1. Sélectionnez **[!UICONTROL Apply]** pour appliquer la modification à la carte. Sélectionnez **[!UICONTROL Cancel]** pour annuler la modification.

* Sur les autres visualisations configurables :

   1. Sélectionnez ![Modifier](/help/assets/icons/Edit.svg) et ![Modifier](/help/assets/icons/Edit.svg) **[!UICONTROL Edit data]** dans le menu contextuel.

   1. Dans la boîte de dialogue **[!UICONTROL Edit Data]** :

      1. Sélectionnez une mesure dans **[!UICONTROL Select a metric]**, par exemple **[!UICONTROL Impressions]**.
      1. Sélectionnez une catégorie dans **[!UICONTROL Select category]**, par exemple **[!UICONTROL Media types]**.
      1. (facultatif) sélectionnez une deuxième catégorie dans **[!UICONTROL Select second category (optional)]**, par exemple **[!UICONTROL Traffic sources]**.
      1. Sélectionnez ![Horloge](/help/assets/icons/Clock.svg) **[!UICONTROL Time]** ou ![Calculateur](/help/assets/icons/Calculator.svg) **[!UICONTROL Total]** comme type d’analyse à **[!UICONTROL Select analysis type]**.

         Si vous sélectionnez ![Horloge](/help/assets/icons/Clock.svg) **[!UICONTROL Time]**, vous pouvez spécifier la fréquence temporelle. Sélectionnez **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** ou **[!UICONTROL Quarterly]** dans **[!UICONTROL Select time frequency]**.

         Un aperçu mis à jour de votre sélection en cours s’affiche dans le [!UICONTROL Preview Area] et votre visualisation actuelle sous [!UICONTROL Current].

         ![Modifier le widget de données harmonisées](/help/assets/edit-harmonized-data-widget.png)

         Si l’aperçu ne peut pas être rendu en raison de l’indisponibilité des données, vous voyez ![Erreur de données](/help/assets/icons/DataUnavailable.svg) [!UICONTROL Insights Not Available] - [!UICONTROL Harmonized fields are not available].

      1. Sélectionnez **[!UICONTROL Apply]** pour appliquer les modifications à la visualisation. Sélectionnez **[!UICONTROL Cancel]** pour annuler toute modification apportée à la visualisation actuelle.
