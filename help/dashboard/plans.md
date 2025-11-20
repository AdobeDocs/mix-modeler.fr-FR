---
title: Performances à planifier
description: Découvrez comment utiliser la fonction Performances pour planifier la vue d’ensemble dans Mix Modeler.
feature: Dashboard, Plans, Models
exl-id: 930fc1d5-8e28-4610-af7b-c4ec91f86a8a
source-git-commit: 89def3d6f5a1415d8f7a91b05d68d70ca881bdf4
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# Performances à planifier

>[!NOTE]
>
>L’onglet **[!UICONTROL Performance to plan]** [!BADGE Beta]{type=Informative} dans Mix Modeler ![Accueil](/help/assets/icons/Home.svg) **[!UICONTROL Overview]** est une fonctionnalité en version bêta et ses fonctionnalités peuvent changer. La fonctionnalité est disponible pour un nombre limité de clientes et clients.

L’onglet **[!UICONTROL Plans]** [!BADGE Beta]{type=Informative} dans Mix Modeler ![Accueil](/help/assets/icons/Home.svg) **[!UICONTROL Overview]** fournit un tableau de bord de suivi pour surveiller les performances de votre marketing par rapport au plan. Vous pouvez comparer les performances réelles aux performances prévues à l’aide de cartes de statut et de visualisations.

Le tableau de bord vous aide à cerner les lacunes, à repérer les risques ou les occasions et à apporter des ajustements opportuns à vos plans et budgets.

Pour sélectionner les données affichées pour les cartes de statut des indicateurs de performance clés et les visualisations :

* Sélectionnez un plan dans le menu déroulant **[!UICONTROL Plan name]** à l’aide de l’option **[!UICONTROL _Sélectionner un plan_]**.

* Spécifiez une période. Pour modifier la période, saisissez une date de début et une date de fin manuellement ou sélectionnez une période à l’aide du ![Calendrier](/help/assets/icons/Calendar.svg).

L’onglet **[!UICONTROL Plans]** [!BADGE Beta]{type=Informative} affiche :

* [Cartes de statut des KPI](#kpi-status-cards) :

   * [Budget](#budget)
   * [Chiffre d’affaires](#revenue)
   * [RSI](#roi)
   * [KPI](#kpi)

* [Visualisations](#visualizations) :
   * [*Mesure*](#metric-actual-vs-planned)
   * [*Mesure*](#metric-actual-vs-planned-by-granularity)
   * [Canal ](#channel-metric-by-granularity)
   * [*Mesure*](#metric-vs-metric-by-channel)
   * [*Mesure*](#metric-by-granularity)
   * [*Mesure*](#metric-by-channel)

## Cartes de statut des KPI

![Cartes de statut des KPI](../assets/performance-to-plan-kpi-cards.png)


### Budget

Une visualisation de progression circulaire qui affiche la comparaison entre vos dépenses marketing et le budget de votre plan pour la période.

### Chiffre d’affaires

Visualisation de la progression circulaire qui affiche le niveau du chiffre d’affaires réel par rapport au chiffre d’affaires cible prévu pour la période.


### RSI

Visualisation en ligne qui affiche le retour sur investissement pour la période.


### KPI

Visualisation en ligne qui affiche l’indicateur de performance clé pour la période.

Pour sélectionner un autre indicateur de performance clé :

1. Sélectionnez ![Modifier](/help/assets/icons/Edit.svg).
1. Dans la boîte de dialogue **[!UICONTROL KPI status card]**, sélectionnez un indicateur de performance clé dans le menu déroulant **[!UICONTROL KPI]**. Les options disponibles sont : [!UICONTROL Conversions], [!UICONTROL CPA], [!UICONTROL Revenue], [!UICONTROL ROI] et [!UICONTROL Spend].


## Visualisations

Six visualisations sont disponibles et vous pouvez modifier chacune d’elles.

Pour redimensionner une visualisation, utilisez la poignée ┛ située dans le coin inférieur droit. Pour déplacer une visualisation, il vous suffit de la faire glisser et de la déposer à l’emplacement souhaité.

Vous pouvez pointer sur n’importe quel élément de ligne, de barre ou de nuage de points d’une visualisation pour afficher une fenêtre contextuelle avec des informations supplémentaires.

![ Visualisation ](../assets/performance-to-plan-visualizations.png)

### *Mesure* : Réel/prévu

Visualisation sous forme de barres empilées qui compare les valeurs des mesures sélectionnées pour le cumul, le cumul prévu et les totaux.


### *Mesure* : Réel ou prévu par *granularité*

Visualisation en ligne qui affiche les valeurs réelles et prévues pour la mesure sélectionnée et la granularité sélectionnée.


### Canal *mesure* par *granularité*

Visualisation sous forme de barres empilées qui affiche les barres empilées affichant les canaux pour la mesure sélectionnée et la granularité sélectionnée.


### *Mesure* vs *Mesure* par canal

Visualisation de la dispersion qui affiche un graphique de dispersion pour les canaux dans les mesures sélectionnées.


### *Mesure* par *granularité*

Une visualisation sous forme de barre qui affiche les valeurs réelles et prévues pour la mesure sélectionnée.


### *Mesure* par canal

Visualisation multiligne qui affiche la mesure sélectionnée avec la granularité sélectionnée.


### Modification d’une visualisation

Pour modifier une visualisation :

1. Sélectionnez ![Modifier](/help/assets/icons/Edit.svg) pour ouvrir la boîte de dialogue **[!UICONTROL Edit data]**.
1. Selon la visualisation, vous pouvez modifier les éléments suivants :

   * Une ou deux mesures : sélectionnez une mesure dans le menu déroulant **[!UICONTROL Select metric]**.

      * Pour les plans basés sur le retour sur investissement, les options sont les suivantes : [!UICONTROL Conversions], [!UICONTROL CPA], [!UICONTROL Revenue], [!UICONTROL ROI], [!UICONTROL Spend] et [!UICONTROL Volume].
      * Pour les plans basés sur CPA, les options sont les suivantes : [!UICONTROL Conversions], [!UICONTROL CPA], [!UICONTROL Spend] et [!UICONTROL Volume].
   * **[!UICONTROL Granularity]** : sélectionnez **[!UICONTROL date ranges]** ou **[!UICONTROL week]** dans le menu déroulant **[!UICONTROL Granularity]** .

   Vous pouvez constater dans **[!UICONTROL Preview]** en quoi les modifications diffèrent de la visualisation **[!UICONTROL Current]**.

1. Sélectionnez **[!UICONTROL Apply]** pour appliquer les modifications. Sélectionnez **[!UICONTROL Cancel]** pour annuler toute modification apportée à la visualisation.
