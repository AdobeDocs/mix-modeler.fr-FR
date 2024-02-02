---
title: Tableau de bord de présentation des données harmonisé
description: Découvrez comment utiliser le tableau de bord de présentation des données harmonisé en Mix Modeler.
feature: Dashboard, Harmonized Data
exl-id: fbb01613-d648-4db1-a782-a7720b7a03ad
source-git-commit: 86732fe30637aa72ced232d9f331a3cc64baa39b
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Présentation des données harmonisées

L’onglet Données harmonisées de l’aperçu du Mix Modeler fournit des informations sur les données harmonisées que vous avez configurées pour être utilisées dans le cadre de la configuration des données ingérées et des données harmonisées.

L’aperçu présente quatre widgets de carte d’état des indicateurs de performance clés (ligne supérieure) et six autres widgets configurables.

Pour modifier la période des données à afficher dans les widgets, saisissez une date de début et une date de fin manuellement ou sélectionnez une période en utilisant ![Calendrier](../assets/icons/Calendar.svg).

## Filtres de données

Vous pouvez filtrer les données affichées pour tous les widgets à l’aide de la variable ![Filtrer](../assets/icons/Filter.svg) **[!UICONTROL Category Filters]** volet.

Sélectionnez un ou plusieurs filtres pour chaque catégorie (**[!UICONTROL Brands]**, **[!UICONTROL Campaigns]**, **[!UICONTROL Cannels Type]**, **[!UICONTROL Conversion types]**, **[!UICONTROL Datasets]**, **[!UICONTROL Media types]**, **[!UICONTROL Source types]**, et **[!UICONTROL Traffic Source]**).

Les filtres sélectionnés s’affichent au-dessus des widgets à l’adresse **[!UICONTROL FILTERING BY:]**.

1. Pour supprimer un filtre individuel, sélectionnez ![Fermer](../assets/icons/Close.svg) sur le filtre, répertorié dans **[!UICONTROL FILTERING BY:]**.

1. Vous pouvez effacer rapidement tous les filtres à l’aide de la méthode **[!UICONTROL Clear All]**.

![Présentation des données harmonisées](../assets/harmonized-data-overview.png)


## Configuration d’un widget

Vous pouvez configurer chaque widget.

* Sur le widget de carte d’état des indicateurs de performance clés :

   1. Sélectionner ![Modifier](../assets/icons/Edit.svg) et ![Modifier](../assets/icons/Edit.svg) **[!UICONTROL Edit data]** dans le menu contextuel.

   1. Dans le **[!UICONTROL KPI status card]** dialog :

      1. Sélectionnez une **[!UICONTROL KPI]** dans la liste.

      1. Sélectionner **[!UICONTROL Apply]** pour appliquer la modification à la carte. Sélectionner **[!UICONTROL Cancel]** pour annuler la modification.

* Sur les autres widgets configurables :

   1. Sélectionner ![Modifier](../assets/icons/Edit.svg) et ![Modifier](../assets/icons/Edit.svg) **[!UICONTROL Edit data]** dans le menu contextuel.

   1. Dans le **[!UICONTROL Edit Data]** dialog :

      1. Sélection d’une mesure dans **[!UICONTROL Select a metric]**, par exemple **[!UICONTROL Impressions]**.
      1. Sélectionnez une catégorie parmi **[!UICONTROL Select category]**, par exemple **[!UICONTROL Media types]**.
      1. (facultatif) sélectionnez une deuxième catégorie dans **[!UICONTROL Select second category (optional)]**, par exemple **[!UICONTROL Traffic sources]**.
      1. Sélectionner ![Horloge](../assets/icons/Clock.svg) **[!UICONTROL Time]** ou ![Calculateur](../assets/icons/Calculator.svg) **[!UICONTROL Total]** comme type d’analyse à l’adresse **[!UICONTROL Select analysis type]**.

         Si vous sélectionnez ![Horloge](../assets/icons/Clock.svg) **[!UICONTROL Time]**, vous pouvez spécifier la fréquence. Sélectionner **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** ou **[!UICONTROL Quarterly]** de **[!UICONTROL Select time frequency]**.

         Un aperçu mis à jour de votre sélection actuelle s’affiche dans la [!UICONTROL Preview Area] et votre widget actuel sous [!UICONTROL Current].

         ![Modification du widget de données harmonisé](../assets/edit-harmonized-data-widget.png)

         Si l’aperçu ne peut pas être rendu en raison de l’indisponibilité des données, vous pouvez voir ![Erreur de données](../assets/icons/DataUnavailable.svg) [!UICONTROL Insights Not Available] - [!UICONTROL Harmonized fields are not available].

      1. Sélectionner **[!UICONTROL Apply]** pour appliquer les modifications au widget. Sélectionner **[!UICONTROL Cancel]** pour annuler toute modification apportée au widget actuel.
