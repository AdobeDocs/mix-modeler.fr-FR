---
title: Créer des plans
description: Découvrez comment créer des plans dans Mix Modeler.
feature: Plans
exl-id: 6d61d0b2-5871-4d00-9a35-73fff0a1c3e5
source-git-commit: f12eea7454d1c81b347dc4960f5c491d81725f7d
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 1%

---


# Créer des plans

Dans Mix Modeler, vous créez un plan à l’aide de la zone de travail Plan. Dans la zone de travail Plan, vous pouvez configurer les détails et les budgets de votre plan, ainsi que le modèle sous-jacent à utiliser pour votre plan. Une fois que vous avez spécifié les détails, le budget et le modèle, vous pouvez poursuivre un plan recommandé par l’IA ou modifier les dépenses par canal.

Pour créer un plan, dans l’interface **[!UICONTROL Plans]** de ![PLan](/help/assets/icons/FileChart.svg) dans Mix Modeler, sélectionnez **[!UICONTROL Create plan]**.

1. Dans l’écran de création du plan :

   1. Dans la section **[!UICONTROL Setup]**

      1. Saisissez un **[!UICONTROL Plan name]**, par exemple `Demo plan`. Saisissez un **[!UICONTROL Description]**, par exemple `Demo plan for Luma company`.
      1. Sélectionnez une **[!UICONTROL Model]** dans **[!UICONTROL _Sélectionner une option.._.]**.
      1. Vous pouvez sélectionner ![LinkOut](/help/assets/icons/LinkOut.svg) **[!UICONTROL Create model]** pour créer un modèle directement à partir de la création du plan. Un nouvel onglet s’ouvre alors dans votre navigateur et l’interface [Modèles](../models/overview.md) s’affiche.

         ![Configuration du plan](/help/assets/plan-setup.png)

   1. Dans la section **[!UICONTROL Budget]** :

      1. Spécifiez une période en saisissant des dates ou en sélectionnant une période à l’aide du ![Calendrier](/help/assets/icons/Calendar.svg).
      1. Saisissez un budget.

      Pour ajouter des périodes supplémentaires, chacune associée à son budget, sélectionnez ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.

      Pour supprimer une période et le budget associé, sélectionnez ![Fermer](/help/assets/icons/Close.svg).

      Pour définir un budget maximum spécifié, procédez comme suit :

      1. Activez **[!UICONTROL Maximize budget]**.
      1. Spécifiez le montant du budget maximum. Le montant doit être égal ou supérieur au montant total des budgets spécifiés pour les périodes.

         ![Planifier le budget](/help/assets/plan-budget.png)

   1. Sélectionnez **[!UICONTROL Next]**.

1. Dans la boîte de dialogue **[!UICONTROL Done with all required fields]** :

   ![Planification terminée](/help/assets/plan-done-required-fields.png)

   * Sélectionner <img src="/help/assets/icons/NewPlan.svg" width="25" /> **[!UICONTROL Create plan now]** si vous souhaitez générer un plan recommandé par l’IA avec le retour sur investissement prévu.

     Sélectionnez **[!UICONTROL OK]**. Votre plan est créé.


   * Sélectionnez ![TableEdit](/help/assets/icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]** si vous souhaitez modifier le budget du canal avant de créer un plan avec le retour sur investissement prévu.

     Sélectionnez **[!UICONTROL OK]** afin de définir les dépenses de canal en **[!UICONTROL Spend selection]** à l’étape suivante.



1. Dans la section **[!UICONTROL Spend selection]**, pour chaque période du budget, utilisez le ![Chevron](/help/assets/icons/ChevronRight.svg) en haut pour ouvrir la vue de distribution des canaux pour cette période.

   1. Pour définir les budgets de chaque canal, saisissez une valeur pour **[!UICONTROL Min]** et **[!UICONTROL Max]** ou utilisez les curseurs.

   1. Pour basculer entre les entrées de devise ou de pourcentage, sélectionnez **[!UICONTROL $]** ou **[!UICONTROL %]** pour **[!UICONTROL View spend by]**.

      ![Sélection des dépenses](/help/assets/plan-spend-selection.png)

   1. Lorsque vous avez terminé, sélectionnez **[!UICONTROL Create]**.

   1. Dans la boîte de dialogue **[!UICONTROL Create plan]**, sélectionnez **[!UICONTROL Create plan]** pour créer votre plan. Sélectionnez **[!UICONTROL Cancel]** pour annuler la création de votre plan. Une boîte de dialogue de **[!UICONTROL No work is saved]** s’affiche pour confirmer l’opération.
