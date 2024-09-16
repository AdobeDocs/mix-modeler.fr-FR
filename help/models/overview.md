---
title: Modèles
description: Découvrez comment configurer et utiliser des modèles dans Mix Modeler.
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 1%

---

# Modèles

La fonctionnalité de modèle de Mix Modeler vous permet de configurer, de former et de noter des modèles spécifiques aux objectifs de votre entreprise. La formation et la notation prennent en charge l’apprentissage du transfert piloté par l’IA entre l’attribution multipoint et la modélisation du mix marketing.

Les modèles sont basés sur les données harmonisées que vous créez dans le cadre du processus de l’application de Mix Modeler.

Un modèle en Mix Modeler est un modèle d’apprentissage automatique utilisé pour mesurer et prédire un résultat spécifié en fonction des investissements d’un spécialiste du marketing. Les points de contact marketing et les données de niveau résumé peuvent être utilisés comme entrée. Mix Modeler vous permet de créer des variantes de modèles basées sur différents ensembles de variables, dimensions et résultats, tels que les revenus, unités vendues et prospects.

Un modèle nécessite :

* Une conversion.
* Un ou plusieurs points de contact marketing (canaux) composés de données de niveau résumé, de données de point de contact marketing (données d’événement) ou des deux.
* Une fenêtre rétroactive configurable.
* Une fenêtre de formation configurable.

Un modèle peut éventuellement inclure :

* Facteurs externes.
* Facteurs internes.
* Connaissance préalable des contributions marketing provenant d’autres sources, telles que l’expérience passée des parties prenantes, les tests incrémentiels, d’autres modèles.
* Partage des dépenses, qui utilise le partage des dépenses relatif comme proxy lorsque les données marketing sont éparses.


## Création d’un modèle

Pour créer un modèle, utilisez le flux de configuration de modèle guidé étape par étape du Mix Modeler disponible lorsque vous sélectionnez **[!UICONTROL Open model canvas]**. Pour plus d’informations, voir [Création d’un modèle](create.md) .

## Gestion des modèles

Pour afficher un tableau de vos modèles actuels, dans l’interface du Mix Modeler :

1. Sélectionnez ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dans le rail de gauche.

1. Vous voyez un tableau des modèles actuels.

   Les colonnes du tableau spécifient des détails sur le modèle.

   | Nom de la colonne | Détails |
   |---|---|
   | Nom | Nom du modèle |
   | Description | Description du modèle |
   | Événement de conversion | La conversion que vous avez sélectionnée pour le modèle. |
   | Fréquence d’exécution | Fréquence d’exécution de l’entraînement du modèle. |
   | Dernière exécution | Date et heure de la dernière formation du modèle. |
   | Statut | État de la dernière exécution de l’entraînement du modèle. <br/>![StatusGreen](/help/assets/icons/StatusGreen.svg) Succès<br/>![StatusOrange](/help/assets/icons/StatusOrange.svg) Problème d’entraînement<br/> ![StatusOrange](/help/assets/icons/StatusOrange.svg) En attente de formation <br/>![StatusRed](/help/assets/icons/StatusRed.svg) Échec <br/>![StatusGreen](/help/assets/icons/StatusGray.svg) _ (lorsqu’une dernière exécution est en cours) |

   {style="table-layout:auto"}

1. Pour modifier les colonnes affichées pour la liste, sélectionnez ![Paramètres de colonne](/help/assets/icons/ColumnSetting.svg) et activez ou désactivez les colonnes sur ![Vérifier](/help/assets/icons/Checkmark.svg).

Vous pouvez effectuer les actions suivantes sur un modèle spécifique.

### Afficher les détails

Pour afficher plus de détails sur un modèle :

1. Sélectionnez ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dans le rail de gauche.

1. Sélectionnez ![Info](/help/assets/icons/Info.svg) pour un modèle afin d’afficher une fenêtre contextuelle contenant des détails.



### Dupliquer

Vous pouvez rapidement dupliquer un modèle.

1. Sélectionnez ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dans le rail de gauche.

1. Sélectionnez ![Plus](/help/assets/icons/More.svg) pour un modèle et, dans le menu contextuel, sélectionnez **[!UICONTROL Duplicate]**.


### Informations sur les modèles

La fonctionnalité d’informations sur les modèles n’est disponible que sur les modèles formés et notés avec succès.

Pour afficher les insights d’un modèle :

1. Sélectionnez ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dans le rail de gauche.

1. Sélectionnez le nom du modèle.

Vous êtes redirigé vers [Model Insights](insights.md).


### Réentraîner


La réorganisation d’un modèle n’est disponible que sur les modèles correctement formés.

Pensez à entraîner à nouveau un modèle lorsque vous souhaitez :

* Incluez de nouvelles données de facteur et de marketing incrémentiel. Par exemple, au cours du dernier trimestre, la dynamique du marché a changé ou votre distribution des données marketing a considérablement changé.

Pour entraîner à nouveau un modèle :

1. Sélectionnez ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dans le rail de gauche.

1. Sélectionnez ![Plus](/help/assets/icons/More.svg) pour un modèle et, dans le menu contextuel, sélectionnez **[!UICONTROL Train]**. Vous pouvez également sélectionner ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Train]** dans la barre d’actions bleue.

   Dans la boîte de dialogue **[!UICONTROL Train model]**, sélectionnez l’option pour :

   * **[!UICONTROL Train model with last 2 years of marketing data]** ou
   * **[!UICONTROL Train model using specific date range of data]**.
Indiquez la période. Vous pouvez utiliser le ![calendrier](/help/assets/icons/Calendar.svg) pour sélectionner une période. Vous devez sélectionner une plage de données d’au moins un an.

   ![Réentraîner un modèle](../assets/re-train-model.png)

1. Sélectionnez **[!UICONTROL Train]** pour entraîner à nouveau le modèle.


### Score ou re-score


Vous pouvez marquer un modèle de manière incrémentielle en fonction de nouvelles données marketing ou noter à nouveau un modèle pour une période spécifique.

Pensez à noter à nouveau un modèle lorsque vous souhaitez :

* Corrigez les données marketing incorrectes. Par exemple, les données de recherche payante récentes que vous avez incluses dans la formation et la notation du modèle ont manqué une semaine de données.
* Utilisez de nouvelles données marketing incrémentielles qui sont devenues disponibles par le biais de mises à jour dans les jeux de données que vous avez configurés dans le cadre de vos données harmonisées.

Pour noter ou noter à nouveau un modèle :

1. Sélectionnez ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dans le rail de gauche.

1. Sélectionnez ![Plus](/help/assets/icons/More.svg) pour un modèle et, dans le menu contextuel, sélectionnez **[!UICONTROL Score]**. Vous pouvez également sélectionner ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Score]** dans la barre d’actions bleue.

   Dans la boîte de dialogue **[!UICONTROL Score marketing data]**, sélectionnez l’option pour :

   * **[!UICONTROL Score new marketing data from *mm/jj/aaaa *]**, pour noter votre modèle de manière incrémentielle à l’aide de nouvelles données marketing, ou
   * **[!UICONTROL Score specific date range of marketing data]** pour noter à nouveau une période spécifique.
Indiquez la période. Vous pouvez utiliser le ![calendrier](/help/assets/icons/Calendar.svg) pour sélectionner une période.

   ![Réentraîner un modèle](../assets/re-score-model.png)

1. Sélectionnez **[!UICONTROL Score]**. Lors de la nouvelle notation d’un modèle à l’aide d’une plage de données spécifique, une boîte de dialogue **[!UICONTROL Existing model is replaced]** s’affiche, vous invitant à confirmer le remplacement du modèle par de nouveaux scores pour la période sélectionnée. Sélectionnez **[!UICONTROL Replace model]** pour confirmer.


### Suppression d’un modèle

Pour supprimer un modèle :

1. Sélectionnez ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dans le rail de gauche.

1. Sélectionnez ![Plus](/help/assets/icons/More.svg) pour un modèle et, dans le menu contextuel, sélectionnez **[!UICONTROL Delete]**. Vous pouvez également sélectionner ![Supprimer](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** dans la barre d’actions bleue.

Pour supprimer plusieurs modèles :

1. Sélectionnez plusieurs modèles.

1. Dans la barre d’actions bleue, sélectionnez ![Supprimer](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** pour supprimer les modèles.

   >[!WARNING]
   >
   >Le modèle est immédiatement supprimé.


