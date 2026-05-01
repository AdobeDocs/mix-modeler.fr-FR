---
title: Tableau de bord de données harmonisé
description: Découvrez comment utiliser le tableau de bord de présentation des données harmonisées dans Mix Modeler.
feature: Dashboard, Harmonized Data
exl-id: fbb01613-d648-4db1-a782-a7720b7a03ad
TQID: https://experienceleague.adobe.com/umAqsiCgpFt4eLBuWPJahtwglXaQKD-iv91yCazIbkE
autotag-review: '2026-05-01T09:17:34.958Z'
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: a567f0f7-0057-4079-8ded-5b24cc25af15
subfeature_v2:
  - id: bc2f5225-03d4-4bc8-89ec-99d78c30e6dd
  - id: b2d4aeb9-eabe-49f6-8edb-bb2862d5980b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 298
ht-degree: 0%

---

# Données harmonisées

L’onglet **[!UICONTROL Harmonized data]** dans Mix Modeler ![Accueil](/help/assets/icons/Home.svg) **[!UICONTROL Overview]** fournit des informations sur les données harmonisées que vous avez configurées pour être utilisées dans le cadre des données ingérées et de la configuration des données harmonisées.

La présentation présente quatre visualisations de carte de statut des KPI (ligne supérieure) et six autres visualisations configurables .

Pour modifier la période des données à afficher dans les visualisations, saisissez une date de début et une date de fin manuellement ou sélectionnez une période à l’aide du ![Calendrier](/help/assets/icons/Calendar.svg).

## Filtres de données

Vous pouvez filtrer les données affichées pour toutes les visualisations à l’aide du volet **[!UICONTROL Category Filters]** ![Filtrer](/help/assets/icons/Filter.svg).

Sélectionnez un ou plusieurs filtres pour chaque catégorie (**[!UICONTROL Brands]**, **[!UICONTROL Campaigns]**, **[!UICONTROL Channels Type]**, **[!UICONTROL Conversion types]**, **[!UICONTROL Datasets]**, **[!UICONTROL Media types]**, **[!UICONTROL Source types]** et **[!UICONTROL Traffic Source]**).

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
