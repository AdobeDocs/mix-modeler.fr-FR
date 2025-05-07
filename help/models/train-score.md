---
title: Modèles de formation et de notation
description: Découvrez comment entraîner et noter des modèles.
feature: Models
source-git-commit: 6855d19347b7f6f1477a6265310df5950b8463c9
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---

# Modèles de formation et de notation

Une fois que vous avez [créé](/help/models/build.md) un modèle, il est automatiquement entraîné et noté. Vous pouvez entraîner ou noter à nouveau manuellement un modèle.

## Entraîner

Pensez à recycler un modèle lorsque vous souhaitez inclure de nouvelles données de facteur et de marketing incrémentiel. Par exemple, au cours du dernier trimestre, la dynamique du marché a changé ou votre répartition des données marketing a considérablement changé.

Pour recycler un modèle :

1. Sélectionnez ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dans le rail de gauche.

1. Sélectionnez ![Plus](/help/assets/icons/More.svg) pour un modèle, puis sélectionnez **[!UICONTROL Train]** dans le menu contextuel. Vous pouvez également sélectionner ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Train]** dans la barre d’actions bleue.

   Dans la boîte de dialogue **[!UICONTROL Train model]**, sélectionnez l’option pour :

   * **[!UICONTROL Train model with last 2 years of marketing data]**, ou
   * **[!UICONTROL Train model using specific date range of data]**.
Spécifiez la période. Vous pouvez utiliser le ![Calendrier](/help/assets/icons/Calendar.svg) pour sélectionner une période. Vous devez sélectionner une plage de données d’au moins un an.

   ![Reformer un modèle](../assets/retrain-model.png)

1. Sélectionnez **[!UICONTROL Train]** pour entraîner à nouveau le modèle.


Vous ne pouvez recycler un modèle que lorsque l&#39;entraînement du modèle a réussi.


## Score


Vous pouvez attribuer un score incrémentiel à un modèle en fonction de nouvelles données marketing ou attribuer un score à un modèle pour une période spécifique.

Pensez à attribuer un score à un modèle lorsque vous souhaitez :

* Corriger les données marketing incorrectes. Par exemple, les données de référencement payant récentes que vous avez incluses dans la formation et la notation du modèle ont manqué une semaine de données.
* Utilisez les nouvelles données de marketing incrémentielles qui sont devenues disponibles par le biais des mises à jour dans les jeux de données que vous avez configurés dans le cadre de vos données harmonisées.

Pour noter ou noter un modèle :

1. Sélectionnez ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dans le rail de gauche.

1. Sélectionnez ![Plus](/help/assets/icons/More.svg) pour un modèle, puis sélectionnez **[!UICONTROL Score]** dans le menu contextuel. Vous pouvez également sélectionner ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Score]** dans la barre d’actions bleue.

   Dans la boîte de dialogue **[!UICONTROL Score marketing data]**, sélectionnez l’option pour :

   * **[!UICONTROL Score new marketing data from *jj/mm/aaaa *]**, pour noter votre modèle de manière incrémentielle à l’aide de nouvelles données marketing, ou
   * **[!UICONTROL Score specific date range of marketing data]** d’attribuer un score pour une période spécifique.
Spécifiez la période. Vous pouvez utiliser le ![Calendrier](/help/assets/icons/Calendar.svg) pour sélectionner une période.

   ![Attribuer un score à un modèle](../assets/rescore-model.png)

1. Sélectionnez **[!UICONTROL Score]**. Lors de la nouvelle notation d’un modèle à l’aide d’une période spécifique, une boîte de dialogue **[!UICONTROL Existing model is replaced]** s’affiche, vous invitant à confirmer le remplacement du modèle par de nouveaux scores pour la période sélectionnée. Sélectionnez **[!UICONTROL Replace model]** pour confirmer.

>[!IMPORTANT]
>
>L’évaluation d’un modèle ne modifie aucun des plans déjà créés sur la base du modèle restauré. Pour utiliser le nouveau modèle enregistré dans un plan, vous devez créer un nouveau plan.

