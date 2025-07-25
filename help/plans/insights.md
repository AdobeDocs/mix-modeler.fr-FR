---
title: Informations sur le plan
description: Découvrez comment obtenir des informations sur votre plan et modifier un plan dans Mix Modeler.
feature: Plans
exl-id: 91385595-284f-4fcb-b54b-9539905e552b
source-git-commit: f0871834ec665c907caf0af3edeeed4fb2549a58
workflow-type: tm+mt
source-wordcount: '1134'
ht-degree: 0%

---

# Informations sur le plan


Les informations de votre plan sont [!UICONTROL Plan insights] créées et indiquent le [!UICONTROL Model], le [!UICONTROL Data range] et le [!UICONTROL Plan target] sur lesquels le plan est basé.


Lorsque les informations sont créées, vous voyez un aperçu de votre plan, composé des éléments suivants :

- En-tête qui affiche le [!UICONTROL Model], le [!UICONTROL Data range] et le [!UICONTROL Plan target] sur lesquels le plan est basé.
   - Si vous avez défini un plan basé sur des objectifs, un badge indique le statut de votre cible. Les options possibles sont les suivantes :

      - [!BADGE Objectif réalisable]{type=Positive}
      - [!BADGE Objectif inatteignable]{type=Negative}

   - Sélectionnez ![ChevronDown](/help/assets/icons/ChevronDown.svg) **[!UICONTROL Show more]** pour afficher plus de détails.

- [Visualisation [!UICONTROL Forecasted paid channel ROI]](#forecasted-paid-channel-spend-and-roi)
- [Visualisation [!UICONTROL Forecasted revenue]](#forecasted-revenue)
- [Visualisation [!UICONTROL Forecasted conversion]](#forecasted-conversions)
- [Visualisation [!UICONTROL Marginal channel return]](#marginal-channel-return)
- [[!UICONTROL Data range breakdown] tableau du plan](#date-range-breakdown) avec les colonnes pour

   - Canal
   - RSI
   - CPA
   - Chiffre d’affaires
   - Objectif de conversion
   - Dépenses

Pour fermer l’interface, sélectionnez **[!UICONTROL Close]**.

Pour modifier l’affichage du retour sur investissement de votre plan, sélectionnez **[!UICONTROL X]** ou **[!UICONTROL &#x200B; %]** à l’**[!UICONTROL View ROI]**.

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

Cette visualisation sous forme de graphique linéaire présente une courbe de retour marginale pour le canal sélectionné avec des indicateurs pour les **[!UICONTROL Marginal break-even]** et les **[!UICONTROL Return point]**. Cette visualisation vous aide à comprendre comment les dépenses d’un canal passent d’un seuil de rentabilité marginal à un seuil de rentabilité. Et si vous avez la possibilité d’augmenter les dépenses dans un canal ou si vous devriez dépenser moins pour un canal afin d’améliorer l’efficacité de ses dépenses.

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

Pour modifier votre plan, sélectionnez ![Modifier](/help/assets/icons/Edit.svg) **[!UICONTROL Edit plan]**.

1. Dans la section **[!UICONTROL Spend selection]**, pour chaque période de budget, utilisez le ![Chevron](/help/assets/icons/ChevronRight.svg) afin d’ouvrir la vue de distribution des canaux pour cette période.

   Vous pouvez utiliser des données de référence historiques si vous souhaitez utiliser les données et informations sur les dépenses marketing antérieures. Tenez compte des données de référence historiques pour :

   - Améliorez l’allocation du budget en mettant en évidence les canaux hautement performants et les canaux peu performants.
   - Prise en charge de l’analyse des tendances.
   - Identifiez des stratégies efficaces et évitez les erreurs lors de la configuration des plans.

   Si vous sélectionnez une période de référence historique, vous vous alignez sur les préférences de modèle de dépenses précédentes et la fonctionnalité de planification de Mix Modeler peut générer des plans conformes à vos attentes. Ces plans doivent en fin de compte renforcer la confiance des parties prenantes, s’assurer que les plans marketing sont stratégiques et efficaces et que ces plans sont fondés sur des données de rendement éprouvées et sur les besoins de l’entreprise.

   ![Sélection des dépenses](/help/assets/plan-spend-selection.png)

   1. Sélectionnez le **[!UICONTROL Spend pattern]**.

      - L’option par défaut est **[!UICONTROL Automatic]**.
      - Sélectionnez **[!UICONTROL Historical reference]** et saisissez une **[!UICONTROL Start date]** pour faire référence aux données antérieures sur les dépenses marketing déjà disponibles pour Mix Modeler. La **[!UICONTROL End date]** est automatiquement déterminée en fonction de la plage de données sélectionnée. La date de début proposée est la première donnée disponible sur les dépenses de marketing antérieures. Un ![AlertRed](/help/assets/icons/AlertRed.svg) s&#39;affiche pour indiquer que vous avez sélectionné une période de référence historique non existante.


   1. Pour modifier les budgets de chaque canal, modifiez les valeurs de **[!UICONTROL Min]** et **[!UICONTROL Max]** ou utilisez les curseurs.

   1. Pour basculer entre les entrées de devise ou de pourcentage, sélectionnez **[!UICONTROL $]** ou **[!UICONTROL %]** pour **[!UICONTROL View spend by]**.

   1. Pour modifier les détails de votre plan, sélectionnez **[!UICONTROL Edit details]** :

      1. Dans la section **[!UICONTROL Setup]** :

         1. Saisissez un **[!UICONTROL Plan name]**, par exemple `Demo plan`. Saisissez un **[!UICONTROL Description]**, par exemple `Demo plan for Luma company`.
         1. Sélectionnez une **[!UICONTROL Model]** dans **[!UICONTROL _Sélectionner une option.._,]**

            ![Configuration du plan](/help/assets/plan-setup.png)

      1. Dans la section **[!UICONTROL Goal]** , sélectionnez l’objectif vers lequel vous souhaitez optimiser votre plan. Vous pouvez choisir entre
         - **[!UICONTROL I have a budget to spend]**

           ![Planifier le budget](../assets/plan-budget.png)

           Cette option vous permet de saisir des budgets pour une ou plusieurs périodes.

            1. Dans le conteneur **[!UICONTROL Optimize]** :
               1. Sélectionnez une conversion dans le menu déroulant **[!UICONTROL Select conversion]** .
               1. Sélectionnez un modèle dans le menu déroulant **[!UICONTROL Select model]**.
            1. Spécifiez une **[!UICONTROL Date range]** en saisissant des dates ou en sélectionnant une période à l’aide du ![Calendrier](/help/assets/icons/Calendar.svg).
            1. Saisissez un **[!UICONTROL Budget]**.
Pour ajouter des périodes supplémentaires, chacune associée à son budget, sélectionnez ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.
Pour supprimer une période et le budget associé, sélectionnez ![Fermer](/help/assets/icons/Close.svg).
            1. Pour définir un budget maximum facultatif dans lequel vous souhaitez contraindre le plan :
               1. Activez **[!UICONTROL Maximize budget]**.
               1. Spécifiez le montant du budget maximum. Le montant doit être égal ou supérieur au montant total des budgets spécifiés pour les périodes.


         - **[!UICONTROL I have a target to achieve]** [!BADGE Beta]

           ![Cible du plan](../assets/plan-target.png)

            1. Dans le conteneur **[!UICONTROL Optimize]**
               1. Sélectionnez une conversion dans le menu déroulant **[!UICONTROL Select conversion]** .
               1. Sélectionnez une mesure cible dans le menu déroulant **[!UICONTROL Select target metric]** . Vous pouvez choisir entre **[!UICONTROL Conversion]**, **[!UICONTROL CPA]**, **[!UICONTROL Revenue]** ou **[!UICONTROL ROI]**.
               1. Sélectionnez un modèle dans le menu déroulant **[!UICONTROL Select model]**.
            1. Spécifiez une période en saisissant des dates ou en sélectionnant une période à l’aide du ![Calendrier](/help/assets/icons/Calendar.svg).
            1. Saisissez une valeur pour la mesure cible sélectionnée. Par exemple, un nombre pour **[!UICONTROL Conversion]**, un pourcentage pour **[!UICONTROL ROI]** ou des valeurs de devise pour **[!UICONTROL CPA]** et **[!UICONTROL Revenue]**.
Pour ajouter des périodes supplémentaires, chacune avec sa mesure cible, sélectionnez ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.
Pour supprimer une période et une mesure cible associée, sélectionnez ![Fermer](/help/assets/icons/Close.svg).
            1. Pour définir un budget maximum facultatif dans lequel vous souhaitez contraindre le plan :
               1. Activez **[!UICONTROL Maximize budget]**.
               1. Spécifiez le montant du budget maximum.

         1. Sélectionnez **[!UICONTROL Next]** pour revenir à la section **[!UICONTROL Spend selection]** .

1. Dans la section **[!UICONTROL Advanced configuration]** :

   ![Modifier la configuration avancée](../assets/edit-plan-advanced-configuration.png)

   - Le nom du plan , le modèle, la période et le budget total sont résumés.

   - Par défaut, Mix Modeler calcule automatiquement le chiffre d’affaires moyen par conversion à l’aide des dernières données saisonnières historiques. Dans **[!UICONTROL Average Revenue per conversion]**, vous pouvez définir un chiffre d’affaires moyen spécifique par conversion.

   1. Pour chaque période de votre budget :
      1. Sélectionnez une période dans le menu déroulant **[!UICONTROL Date range]**.
      1. Saisissez une valeur de **[!UICONTROL Average revenue]**.
   1. Sélectionnez ![AddCircle](/help/assets/icons/AddCircle.svg) Ajouter un chiffre d’affaires moyen personnalisé par unité de conversion pour ajouter une période.
   1. Sélectionnez ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) pour supprimer une période.

   >[!NOTE]
   >
   >Si votre modèle n’inclut pas de données historiques sur le chiffre d’affaires, vous devez définir un chiffre d’affaires moyen par conversion pour chaque période spécifiée pour votre budget.
   >

   - Par défaut, Mix Modeler calcule automatiquement les coûts du canal à l’aide des dernières données saisonnières historiques. Dans **[!UICONTROL Channel costs]**, vous pouvez définir des coûts de canal personnalisés.

   1. Pour chaque canal de votre modèle, définissez le coût du canal personnalisé.
      1. Sélectionnez un canal dans le menu déroulant **[!UICONTROL Channel]**.
      1. Pour chaque période de votre budget :
         1. Sélectionnez une période dans le menu déroulant **[!UICONTROL Date range]**.
         1. Saisissez une valeur de **[!UICONTROL Average revenue]**.
      1. Sélectionnez ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom average revenue per conversion unit]** pour ajouter une période.
      1. Sélectionnez ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) pour supprimer une période.

   1. Sélectionnez ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom channel cost]** pour ajouter un canal.
   1. Sélectionnez ![CrossSize400](/help/assets/icons/CrossSize400.svg) pour supprimer un canal personnalisé.


1. Lorsque vous avez terminé de modifier votre plan, sélectionnez **[!UICONTROL Edit]**.

   Dans la boîte de dialogue **[!UICONTROL All changes are final]**, sélectionnez **[!UICONTROL OK]** pour mettre à jour l’affectation actuelle des dépenses du plan, ainsi que les prévisions de retour sur investissement et de revenus. Sélectionnez **[!UICONTROL Cancel]** pour annuler la mise à jour de votre plan.


- Pour annuler les mises à jour de votre plan à tout moment, sélectionnez **[!UICONTROL Cancel]**. Dans la boîte de dialogue **[!UICONTROL No work will be saved]**, sélectionnez **[!UICONTROL Cancel]** pour continuer à travailler sur votre plan ou sélectionnez **[!UICONTROL OK]** pour revenir à l’interface Plans.
- Pour revenir à l’assistant, sélectionnez **[!UICONTROL Back]**.
