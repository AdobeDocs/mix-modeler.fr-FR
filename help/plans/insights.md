---
title: Informations sur le plan
description: Découvrez comment obtenir des informations sur votre plan et modifier un plan dans Mix Modeler.
feature: Plans
exl-id: 91385595-284f-4fcb-b54b-9539905e552b
source-git-commit: fbed53a1c394d6d110db6a8a181ca815056377de
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# Informations sur le plan


Les informations de votre plan sont [!UICONTROL Plan insights] créées et indiquent les [!UICONTROL Model], les [!UICONTROL Data range] et les [!UICONTROL Total budget] sur lesquels le plan est basé.

Une fois la récupération terminée, un aperçu de votre plan s’affiche, comprenant les éléments suivants :

- Visualisation [!UICONTROL Forecasted paid channel ROI]
- Visualisation [!UICONTROL Forecasted revenue]
- Visualisation [!UICONTROL Forecasted conversion]
- Visualisation [!UICONTROL Marginal channel return]
- [!UICONTROL Data range breakdown] tableau du plan, affichant les colonnes pour

   - Canal
   - RSI
   - CPA
   - Chiffre d’affaires
   - Objectif de conversion
   - Dépenses

Pour fermer l’interface, sélectionnez **[!UICONTROL Close]**.

Pour modifier l’affichage du retour sur investissement de votre plan, sélectionnez **[!UICONTROL X]** ou **[!UICONTROL  %]** à l’**[!UICONTROL View ROI]**.

## Dépenses et retour sur investissement prévus pour les canaux payants

Cette visualisation présente un graphique de dispersion des dépenses et du retour sur investissement prévus pour vos canaux payants, en fonction du modèle, de la période et du budget.

![Visualisation des prévisions de dépenses et du RSI du canal payant](../assets/overview-plan-forecasted-paid-channel-send-roi.png)


## Chiffre d&#39;affaires prévu

Cette visualisation sous forme de graphique à barres présente les prévisions de revenus pour vos canaux en fonction du modèle, de la période et du budget.

![Visualisation du chiffre d’affaires prévu](../assets/overview-plan-forecasted-revenue.png)


## Conversions prévues

Cette visualisation sous forme de graphique à barres présente les conversions prévues pour vos canaux en fonction du modèle, de la période et du budget.

![ Visualisation des conversions prévues ](../assets/overview-plan-forecasted-conversions.png)


## Retour de canal marginal

Cette visualisation sous forme de graphique linéaire présente une courbe de retour marginale pour le canal sélectionné avec des indicateurs pour les **[!UICONTROL Marginal break-even]** et les **[!UICONTROL Return point]**. Cette visualisation vous aide à comprendre comment les dépenses pour un canal vont d’un point d’équilibre marginal à un autre, et si vous avez la possibilité d’augmenter les dépenses dans un canal ou si vous devriez dépenser moins pour un canal afin d’améliorer l’efficacité de ces dépenses.

![Visualisation du retour du canal marginal](../assets/overview-plan-marginal-channel-return.png)

Pour sélectionner un canal spécifique pour la visualisation, sélectionnez-le dans le menu déroulant **[!UICONTROL View]**.


## Répartition des périodes

Le tableau [!UICONTROL Date range breakdown] présente les données granulaires détaillées par canal pour [!UICONTROL ROI], [!UICONTROL Revenue], [!UICONTROL CPA], [!UICONTROL Conversions] et [!UICONTROL Spend].

![Tableau de répartition des périodes](../assets/overview-plan-date-range-breakdown.png)

1. Pour télécharger un fichier CSV contenant les données de la répartition des périodes, sélectionnez ![Télécharger](/help/assets/icons/Download.svg) **[!UICONTROL Download CSV]**. Dans le menu contextuel :

   - Sélectionnez ![Télécharger](/help/assets/icons/Download.svg) **[!UICONTROL Detailed CSV]** pour obtenir des données détaillées au format CSV.
   - Sélectionnez ![Télécharger](/help/assets/icons/Download.svg) **[!UICONTROL Summary CSV]** pour obtenir un résumé des données au format CSV.

   Les données détaillées sont des données granulaires indexées par semaine. Les données récapitulatives sont des données indexées par la période fournie par le modèle.

1. Pour afficher la répartition des périodes par catégorie de canaux, sélectionnez **[!UICONTROL All channels]**, **[!UICONTROL Paid channels]** ou **[!UICONTROL Non-paid channels]** dans la sélection **[!UICONTROL View]**.


## Modifier le plan

1. Pour modifier votre plan, sélectionnez ![Modifier](/help/assets/icons/Edit.svg) **[!UICONTROL Edit plan]** :

   1. Dans la section **[!UICONTROL Spend selection]**, pour chaque période de budget, utilisez le ![Chevron](/help/assets/icons/ChevronRight.svg) afin d’ouvrir la vue de distribution des canaux pour cette période.

   1. Pour modifier les budgets de chaque canal, modifiez les valeurs de **[!UICONTROL Min]** et **[!UICONTROL Max]** ou utilisez les curseurs.

   1. Pour basculer entre les entrées de devise ou de pourcentage, sélectionnez **[!UICONTROL $]** ou **[!UICONTROL %]** pour **[!UICONTROL View spend by]**.

      ![Sélection des dépenses](/help/assets/spend-selection.png)

   1. Pour modifier les détails de votre plan, sélectionnez **[!UICONTROL Edit details]** :

      1. Dans la section **[!UICONTROL Setup]** , le cas échéant, modifiez la **[!UICONTROL Plan name]** et le **[!UICONTROL Description]** .

      1. Dans la section **[!UICONTROL Budget]** :

         1. Modifiez la **[!UICONTROL Date range]** d’une ou de plusieurs périodes de votre plan en saisissant des dates ou en sélectionnant une période à l’aide du ![Calendrier](/help/assets/icons/Calendar.svg).

         1. Modifiez le **[!UICONTROL Budget]** pour une ou plusieurs périodes de votre plan.

         Pour ajouter des périodes supplémentaires, chacune associée à son budget, sélectionnez ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.

         Pour supprimer une période et le budget associé, sélectionnez ![Fermer](/help/assets/icons/Close.svg).

         Pour définir un budget maximum :

         1. Activez **[!UICONTROL Maximize budget]**.
         1. Spécifiez le montant du budget maximum. Le montant doit être égal ou supérieur au montant total des budgets spécifiés pour les périodes.

      1. Sélectionnez **[!UICONTROL Next]** pour revenir à la section **[!UICONTROL Spend]** . Sélectionnez **[!UICONTROL Cancel]** pour revenir à l’aperçu de vos plans.

         ![Détails du plan](/help/assets/plan-details.png)


1. Une fois la modification du plan terminée, sélectionnez **[!UICONTROL Edit]**.

   Dans la boîte de dialogue **[!UICONTROL All changes are final]**, sélectionnez **[!UICONTROL OK]** pour mettre à jour l’affectation actuelle des dépenses du plan, ainsi que les prévisions de retour sur investissement et de revenus. Sélectionnez **[!UICONTROL Cancel]** pour annuler la mise à jour de votre plan.

1. Pour annuler les mises à jour de votre plan, sélectionnez **[!UICONTROL Cancel]**.

   Dans la boîte de dialogue **[!UICONTROL No work will be saved]**, sélectionnez **[!UICONTROL Cancel]** pour continuer à travailler sur votre plan ou sélectionnez **[!UICONTROL OK]** pour revenir à l’interface Plans.
