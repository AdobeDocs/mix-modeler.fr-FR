---
title: Créer un plan
description: Découvrez comment créer un plan en Mix Modeler.
feature: Plans
source-git-commit: 08cfd4239f6bcaf885565f3ae04cbd51869e8c00
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 1%

---


# Créer un plan

Dans Mix Modeler, vous créez un plan à l’aide du canevas du plan. Dans la zone de travail du plan, vous pouvez configurer les détails et les budgets de votre plan, ainsi que le modèle sous-jacent à utiliser pour votre plan. Une fois que vous avez spécifié les détails, le budget et le modèle, vous pouvez poursuivre un plan recommandé par l’IA ou modifier les dépenses par canal.

Pour créer un plan, dans la variable ![PLan](../assets/icons/FileChart.svg) **[!UICONTROL Plans]** dans Mix Modeler, sélectionnez **[!UICONTROL Open plan canvas]**.

1. Dans l’écran de création du plan :

   1. Dans le **[!UICONTROL Setup]** section

      1. Saisissez un **[!UICONTROL Plan name]**, par exemple `Demo plan`. Saisissez un **[!UICONTROL Description]**, par exemple `Demo plan for Luma company`.
      1. Sélectionnez une **[!UICONTROL Model]** de **[!UICONTROL _Sélectionnez une option._.]**.
      1. Vous pouvez sélectionner ![LinkOut](../assets/icons/LinkOut.svg) **[!UICONTROL Create model]** pour créer un modèle directement dans la création du plan.

         ![Configuration du plan](../assets/plan-setup.png)

   1. Dans le **[!UICONTROL Budget]** section :

      1. Spécifiez une plage de dates en saisissant des dates ou en sélectionnant une plage de dates à l’aide de ![Calendrier](../assets/icons/Calendar.svg).
      1. Saisissez un budget.

      Pour ajouter des plages de dates supplémentaires, sélectionnez ![CalendarAdd](../assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.

      Pour supprimer une plage de dates et le budget associé, sélectionnez ![Fermer](../assets/icons/Close.svg).

      Pour définir un budget maximum spécifié :

      1. Switch **[!UICONTROL Maximize budget]** sur .
      1. Indiquez le budget maximum. Le montant doit être égal ou supérieur au montant total des budgets spécifié pour les périodes.

         ![Planifier le budget](../assets/plan-budget.png)

   1. Sélectionnez **[!UICONTROL Next]**.

1. Dans le **[!UICONTROL Done with all required fields]** dialog :

   ![Plan terminé](../assets/plan-done-required-fields.png)

   * Sélectionner <img src="../assets/icons/NewPlan.svg" width="25" /> **[!UICONTROL Create plan now]** si vous souhaitez générer un plan recommandé d’IA avec un retour sur investissement prévisionnel.

     Sélectionnez **[!UICONTROL OK]**. Votre plan est créé.


   * Sélectionner ![TableEdit](../assets/icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]** si vous souhaitez modifier le budget des canaux avant de créer un plan avec le retour sur investissement prévu.

     Sélectionner **[!UICONTROL OK]**, afin que vous puissiez définir vos dépenses de canal dans **[!UICONTROL Spend selection]** à l’étape suivante.



1. Dans le **[!UICONTROL Spend selection]** , pour chaque période de budget, utilisez la variable ![Chevron](../assets/icons/ChevronRight.svg) ouvrez en haut la vue distribution de canal pour cette plage de données.

   1. Pour définir des budgets pour chaque canal, saisissez une valeur pour **[!UICONTROL Min]** et **[!UICONTROL Max]** ou utilisez les curseur.

   1. Pour basculer entre l’entrée de devise ou de pourcentage, sélectionnez **[!UICONTROL $]** ou **[!UICONTROL %]** pour **[!UICONTROL View spend by]**.

      ![Sélection de la dépense](../assets/plan-spend-selection.png)

   1. Lorsque vous avez terminé, sélectionnez **[!UICONTROL Create]**.

   1. Dans le **[!UICONTROL Create plan]** boîte de dialogue, sélectionnez **[!UICONTROL Create plan]** pour créer votre plan. Sélectionner **[!UICONTROL Cancel]** pour annuler la création de votre plan.



