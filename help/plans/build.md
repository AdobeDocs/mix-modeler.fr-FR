---
title: Créer des plans
description: Découvrez comment créer des plans dans Mix Modeler.
feature: Plans
exl-id: 6d61d0b2-5871-4d00-9a35-73fff0a1c3e5
source-git-commit: 20985d0f9e9d2990b881ab448f6475e4bb8244d1
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 1%

---


# Créer des plans

Dans Mix Modeler, vous créez un plan à l’aide de l’assistant de plan. Dans l’assistant de plan, vous pouvez configurer les détails et les budgets ou les mesures cibles de votre plan et le modèle sous-jacent à utiliser pour votre plan. Une fois que vous avez spécifié des détails, un budget, des mesures cibles et un modèle, vous pouvez poursuivre un plan recommandé par l’IA ou modifier les dépenses par canal. Vous avez la possibilité de définir des configurations avancées sur le chiffre d’affaires moyen par conversion et les coûts de canal.

Vous devez définir l’objectif pour lequel vous souhaitez optimiser votre plan. Cet objectif peut être soit un budget que vous pouvez dépenser, soit une cible que vous voulez atteindre. Si l’objectif est une cible, vous devez en outre spécifier les valeurs de la mesure cible à utiliser : conversion, chiffre d’affaires, CPA ou RSI.

Pour créer un plan, dans l’interface ![ ](/help/assets/icons/FileChart.svg)PLan **[!UICONTROL Plans]** de Mix Modeler, sélectionnez **[!UICONTROL Create plan]**.


1. Dans l’écran **[!UICONTROL Plan creation]** :

   1. Dans la section **[!UICONTROL Setup]** :

      1. Saisissez un **[!UICONTROL Plan name]**, par exemple `Goal based plan`. Saisissez un **[!UICONTROL Description]**, par exemple `A goal based plan`.
      1. Sélectionnez une **[!UICONTROL Model]** dans **[!UICONTROL _Sélectionner une option.._,]**

         ![Configuration du plan](/help/assets/plan-setup.png)

   1. Dans la section **[!UICONTROL Goal]** , sélectionnez l’objectif vers lequel vous souhaitez optimiser votre plan. Vous pouvez choisir entre

      * **[!UICONTROL I have a budget to spend]**

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


      * **[!UICONTROL I have a target to achieve]** [!BADGE Beta]

        ![Cible du plan](../assets/plan-target.png)

         1. Dans le conteneur **[!UICONTROL Optimize]**
            1. Sélectionnez une conversion dans le menu déroulant **[!UICONTROL Select conversion]** .
            1. Sélectionnez une mesure cible dans le menu déroulant **[!UICONTROL Select target metric]** . Vous pouvez choisir entre **[!UICONTROL Conversion]**, **[!UICONTROL CPA]**, **[!UICONTROL Revenue]** ou **[!UICONTROL ROI]**.
            1. Sélectionnez un modèle dans le menu déroulant **[!UICONTROL Select model]**.
         1. Spécifiez une période en saisissant des dates ou en sélectionnant une période à l’aide du ![Calendrier](/help/assets/icons/Calendar.svg).
         1. Saisissez une valeur pour la mesure cible sélectionnée. Par exemple, un nombre pour **[!UICONTROL Total Conversions]**, un pourcentage pour **[!UICONTROL Paid Marketing ROI]** ou des valeurs de devise pour **[!UICONTROL Paid Marketing CPA]** et **[!UICONTROL Total Revenue]**.
Pour ajouter des périodes supplémentaires, chacune avec sa mesure cible, sélectionnez ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.
Pour supprimer une période et une mesure cible associée, sélectionnez ![Fermer](/help/assets/icons/Close.svg).
         1. Pour définir un budget maximum facultatif dans lequel vous souhaitez contraindre le plan :
            1. Activez **[!UICONTROL Maximize budget]**.
            1. Spécifiez le montant du budget maximum.


   1. Sélectionnez **[!UICONTROL Next]**.

1. Dans la boîte de dialogue **[!UICONTROL Done with all required fields]** :

   ![Planification terminée](/help/assets/plan-done-required-fields.png)

   * Sélectionnez ![NouveauPlan](/help/assets/icons/NewPlan.svg) **[!UICONTROL Create plan now]** si vous souhaitez générer un plan recommandé par l’IA avec le retour sur investissement prévu. Sélectionnez **[!UICONTROL OK]**. Votre plan est créé.





   * Sélectionnez ![TableEdit](/help/assets/icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]** si vous souhaitez modifier le budget du canal et définir des configurations avancées avant de créer un plan avec le retour sur investissement prévu.  Sélectionnez **[!UICONTROL OK]** afin de définir les dépenses de canal en **[!UICONTROL Spend selection]** à l’étape suivante.


     >[!IMPORTANT]
     >
     >Les informations ci-dessous ne sont pertinentes que si vous avez sélectionné le ![ ](/help/assets/icons/TableEdit.svg)TableEdit **[!UICONTROL Edit channel budgets first]**


1. Dans la section **[!UICONTROL Spend selection]**, pour chaque période de budget, utilisez le ![Chevron](/help/assets/icons/ChevronRight.svg) afin d’ouvrir la vue de distribution des canaux pour cette période.

   Vous pouvez utiliser des données de référence historiques si vous souhaitez utiliser les données et informations sur les dépenses marketing antérieures. Tenez compte des données de référence historiques pour :

   * Améliorez l’allocation du budget en mettant en évidence les canaux hautement performants et les canaux peu performants.
   * Prise en charge de l’analyse des tendances.
   * Identifiez des stratégies efficaces et évitez les erreurs lors de la configuration des plans.

   Si vous sélectionnez une période de référence historique, vous vous alignez sur les préférences de modèle de dépenses précédentes et la fonctionnalité de planification de Mix Modeler peut générer des plans conformes à vos attentes. Ces plans doivent en fin de compte renforcer la confiance des parties prenantes, s’assurer que les plans marketing sont stratégiques et efficaces et que ces plans sont fondés sur des données de rendement éprouvées et sur les besoins de l’entreprise.

   ![Sélection des dépenses](/help/assets/plan-spend-selection.png)

   1. Sélectionnez le **[!UICONTROL Spend pattern]**.

      * L’option par défaut est **[!UICONTROL Automatic]**.
      * Sélectionnez **[!UICONTROL Historical reference]** et saisissez une **[!UICONTROL Start date]** pour faire référence aux données antérieures sur les dépenses marketing déjà disponibles pour Mix Modeler. Le **[!UICONTROL End date]** est automatiquement déterminé en fonction de la période pour laquelle vous définissez le modèle de dépenses. La date de début proposée est la première date de dépense marketing antérieure disponible. Un ![AlertRed](/help/assets/icons/AlertRed.svg) s&#39;affiche pour indiquer que vous avez sélectionné une période de référence historique inexistante ou non valide.

   1. Pour définir les budgets de chaque canal, saisissez une valeur pour **[!UICONTROL Min]** et **[!UICONTROL Max]** ou utilisez les curseurs.

   1. Pour basculer entre les entrées de devise ou de pourcentage, sélectionnez **[!UICONTROL $]** ou **[!UICONTROL %]** pour **[!UICONTROL View spend by]**. Ce bouton est désactivé si vous avez sélectionné des mesures cibles qui ne sont pas basées sur une devise.

   1. Lorsque vous avez terminé, sélectionnez **[!UICONTROL Create]**.
      ![Sélection des dépenses](/help/assets/plan-spend-selection.png)

   1. Sélectionnez **[!UICONTROL Next]**.



1. Dans la section **[!UICONTROL Advanced configurations]** , vous pouvez saisir des configurations avancées facultatives.

   ![Résumé du plan](../assets/plan-advanced-configurations.png)

   * Le nom du plan , le modèle, la période et le budget total sont résumés.

   * Par défaut, Mix Modeler calcule automatiquement le chiffre d’affaires moyen par conversion à l’aide des dernières données saisonnières historiques. Dans **[!UICONTROL Average Revenue per conversion]**, vous pouvez définir un chiffre d’affaires moyen spécifique par conversion.

      1. Pour chaque période de votre budget :

         1. Sélectionnez une période dans le menu déroulant **[!UICONTROL Date range]**.
         1. Saisissez une valeur de **[!UICONTROL Average revenue]**.

      1. Sélectionnez ![AddCircle](/help/assets/icons/AddCircle.svg) Ajouter un chiffre d’affaires moyen personnalisé par unité de conversion pour ajouter une période.
      1. Sélectionnez ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) pour supprimer une période.

     >[!NOTE]
     >
     >Si votre modèle n’inclut pas de données historiques sur le chiffre d’affaires, vous devez définir un chiffre d’affaires moyen par conversion pour chaque période spécifiée pour votre budget.
     >

   * Par défaut, Mix Modeler calcule automatiquement les coûts du canal à l’aide des dernières données saisonnières historiques. Dans **[!UICONTROL Channel costs]**, vous pouvez définir des coûts de canal personnalisés.

      1. Pour chaque canal de votre modèle, définissez un coût de canal personnalisé.

         1. Sélectionnez un canal dans le menu déroulant **[!UICONTROL Channel]**.
         1. Pour chaque période de votre budget :
            1. Sélectionnez une période dans le menu déroulant **[!UICONTROL Date range]**.
            1. Saisissez une valeur de **[!UICONTROL Average revenue]**.
         1. Sélectionnez ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom average revenue per conversion unit]** pour ajouter une période.
         1. Sélectionnez ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) pour supprimer une période.

      1. Sélectionnez ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom channel cost]** pour ajouter un canal.
      1. Sélectionnez ![CrossSize400](/help/assets/icons/CrossSize400.svg) pour supprimer un canal personnalisé.


1. Lorsque vous avez terminé, sélectionnez **[!UICONTROL Create]**.

1. Dans la boîte de dialogue **[!UICONTROL Create plan]**, sélectionnez **[!UICONTROL Create plan]** pour créer votre plan. Sélectionnez **[!UICONTROL Cancel]** pour annuler la création de votre plan. Une boîte de dialogue de **[!UICONTROL No work is saved]** s’affiche pour confirmer l’opération.

