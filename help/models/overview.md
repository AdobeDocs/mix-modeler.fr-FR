---
title: Modèles
description: Découvrez comment configurer et utiliser des modèles dans Mix Modeler.
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: a4fdfa97e9d548533a22b1b667cf336f37b83395
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 1%

---

# Modèles

La fonctionnalité de modèle de Mix Modeler vous permet de configurer, d’entraîner et de noter des modèles spécifiques à vos objectifs commerciaux. La formation et la notation prennent en charge l’apprentissage du transfert piloté par l’IA entre l’attribution multipoint et la modélisation du mix marketing.

Les modèles sont basés sur les données harmonisées que vous créez dans le cadre du workflow d’application du Mix Modeler.

Un modèle en Mix Modeler est un modèle de machine learning utilisé pour mesurer et prédire un résultat spécifié en fonction des investissements d’un spécialiste marketing. Les points de contact marketing et les données au niveau du résumé peuvent être utilisés comme entrées. Mix Modeler vous permet de créer des variantes de modèles en fonction de différents ensembles de variables, dimensions et résultats, tels que les revenus, les unités vendues et les prospects.

Un modèle nécessite :

* Une conversion.
* Un ou plusieurs points de contact marketing (canaux) composés de données de niveau résumé, de données de point de contact marketing (données d’événement) ou les deux.
* Intervalle de recherche en amont configurable.
* Un créneau de formation configurable.

Un modèle peut éventuellement inclure :

* Facteurs externes.
* Facteurs internes.
* Connaissance préalable des contributions marketing provenant d’autres sources telles que l’expérience passée des parties prenantes, les tests incrémentiels, d’autres modèles.
* Le partage des dépenses, qui utilise le partage des dépenses relatives comme proxy lorsque les données marketing sont clairsemées.


## Création d’un modèle

Pour créer un modèle, utilisez le flux de configuration de modèle guidé étape par étape du Mix Modeler disponible lorsque vous sélectionnez **[!UICONTROL Open model canvas]**. Voir [Création d’un modèle](create.md) pour plus d’informations.

## Gestion des modèles

Pour afficher un tableau de vos modèles actuels, dans l’interface du Mix Modeler :

1. Sélectionnez ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dans le rail de gauche.

1. Un tableau des modèles actuels s’affiche.

   Les colonnes du tableau indiquent des détails sur le modèle.

   | Nom de la colonne | Détails |
   |---|---|
   | Nom | Nom du modèle |
   | Description | Description du modèle |
   | Événement de conversion | Conversion sélectionnée pour le modèle. |
   | Fréquence d’exécution | Fréquence d’exécution de l’entraînement du modèle. |
   | Dernière exécution | Date et heure du dernier entraînement du modèle. |
   | Statut | Statut de la dernière exécution de l’entraînement du modèle. <br/>![StatusGreen](/help/assets/icons/StatusGreen.svg) Success<br/>![StatusOrange](/help/assets/icons/StatusOrange.svg) Problème de formation<br/> ![StatusOrange](/help/assets/icons/StatusOrange.svg) En attente d’entraînement <br/>![StatusRed](/help/assets/icons/StatusRed.svg) En échec <br/>![StatusGreen](/help/assets/icons/StatusGray.svg) _ (lorsqu’une dernière exécution est en cours) |

   {style="table-layout:auto"}

1. Pour modifier les colonnes affichées pour la liste, sélectionnez ![Paramètres des colonnes](/help/assets/icons/ColumnSetting.svg) et activez/désactivez les colonnes sur ![Vérifier](/help/assets/icons/Checkmark.svg).

Vous pouvez effectuer les actions suivantes sur un modèle spécifique.

### Informations sur le modèle

La fonctionnalité d’informations sur les modèles n’est disponible que sur les modèles entraînés et notés avec succès.

Pour afficher les informations d’un modèle :

1. Sélectionnez ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dans le rail de gauche.

1. Sélectionnez le nom du modèle.

Vous êtes redirigé vers [ Model Insights ](insights.md).


### Afficher les détails

Pour afficher plus de détails sur un modèle :

1. Sélectionnez ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dans le rail de gauche.

1. Sélectionnez ![Infos](/help/assets/icons/Info.svg) pour un modèle afin d’afficher un pop-up avec des détails.


### Dupliquer

Vous pouvez rapidement dupliquer un modèle.

1. Sélectionnez ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dans le rail de gauche.

1. Sélectionnez ![Plus](/help/assets/icons/More.svg) pour un modèle, puis sélectionnez **[!UICONTROL Duplicate]** dans le menu contextuel.


### Modifier

Vous pouvez modifier le nom, la description, la planification de l’entraînement et la notation d’un modèle.

1. Sélectionnez ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dans le rail de gauche.

1. Sélectionnez ![Plus](/help/assets/icons/More.svg) pour un modèle, puis sélectionnez **[!UICONTROL Edit]** dans le menu contextuel.

   Dans la boîte de dialogue **[!UICONTROL Edit model]** :

   * Saisissez un nouveau **[!UICONTROL Name]** et une nouvelle **[!UICONTROL Description]**.

   * Pour activer la planification, activez **[!UICONTROL Status]**. Vous pouvez uniquement activer la planification pour les modèles entraînés et notés.

      1. Sélectionner un **[!UICONTROL Scoring frequency]** :

         * **[!UICONTROL Daily]** : saisissez une heure valide (par exemple, `05:22 pm`) ou utilisez ![Horloge](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Weekly]** : sélectionnez un jour de la semaine et saisissez une heure valide (par exemple, `05:22 pm`) ou utilisez ![Horloge](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Monthly]** : sélectionnez un jour du mois dans le menu déroulant Exécuter sur chaque et saisissez une heure valide (par exemple `05:22 pm`) ou utilisez ![Horloge](/help/assets/icons/Clock.svg).

      1. Sélectionnez un **[!UICONTROL Training frequency]** dans le menu déroulant : **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** ou **[!UICONTROL None]**.

     ![Modifier un modèle](../assets/model-edit.png)

1. Sélectionnez **[!UICONTROL Save]**.



### Recycler


La réentraînement d’un modèle n’est disponible que sur les modèles entraînés avec succès.

Envisagez de former à nouveau un modèle lorsque vous souhaitez :

* Incluez les nouvelles données relatives aux facteurs et au marketing incrémentiel. Par exemple, au cours du dernier trimestre, la dynamique du marché a changé ou votre répartition des données marketing a considérablement changé.

Pour entraîner à nouveau un modèle :

1. Sélectionnez ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dans le rail de gauche.

1. Sélectionnez ![Plus](/help/assets/icons/More.svg) pour un modèle, puis sélectionnez **[!UICONTROL Train]** dans le menu contextuel. Vous pouvez également sélectionner ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Train]** dans la barre d’actions bleue.

   Dans la boîte de dialogue **[!UICONTROL Train model]**, sélectionnez l’option pour :

   * **[!UICONTROL Train model with last 2 years of marketing data]**, ou
   * **[!UICONTROL Train model using specific date range of data]**.
Spécifiez la période. Vous pouvez utiliser le ![Calendrier](/help/assets/icons/Calendar.svg) pour sélectionner une période. Vous devez sélectionner une plage de données d’au moins un an.

   ![Entraînement d’un modèle](../assets/re-train-model.png)

1. Sélectionnez **[!UICONTROL Train]** pour entraîner à nouveau le modèle.


### Score ou re-score


Vous pouvez attribuer une note incrémentielle à un modèle en fonction de nouvelles données marketing ou attribuer une nouvelle note à un modèle pour une période spécifique.

Envisagez de noter à nouveau un modèle lorsque vous souhaitez :

* Corriger les données marketing incorrectes. Par exemple, les données de référencement payant récentes que vous avez incluses dans la formation et la notation du modèle ont manqué une semaine de données.
* Utilisez les nouvelles données de marketing incrémentielles qui sont devenues disponibles par le biais des mises à jour dans les jeux de données que vous avez configurés dans le cadre de vos données harmonisées.

Pour noter ou noter à nouveau un modèle :

1. Sélectionnez ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dans le rail de gauche.

1. Sélectionnez ![Plus](/help/assets/icons/More.svg) pour un modèle, puis sélectionnez **[!UICONTROL Score]** dans le menu contextuel. Vous pouvez également sélectionner ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Score]** dans la barre d’actions bleue.

   Dans la boîte de dialogue **[!UICONTROL Score marketing data]**, sélectionnez l’option pour :

   * **[!UICONTROL Score new marketing data from *jj/mm/aaaa *]**, pour noter votre modèle de manière incrémentielle à l’aide de nouvelles données marketing, ou
   * **[!UICONTROL Score specific date range of marketing data]** de noter à nouveau pour une période spécifique.
Spécifiez la période. Vous pouvez utiliser le ![Calendrier](/help/assets/icons/Calendar.svg) pour sélectionner une période.

   ![Entraînement d’un modèle](../assets/re-score-model.png)

1. Sélectionnez **[!UICONTROL Score]**. Lors de la nouvelle notation d’un modèle à l’aide d’une période spécifique, une boîte de dialogue **[!UICONTROL Existing model is replaced]** s’affiche, vous invitant à confirmer le remplacement du modèle par de nouveaux scores pour la période sélectionnée. Sélectionnez **[!UICONTROL Replace model]** pour confirmer.


### Suppression de modèles

Pour supprimer un modèle :

1. Sélectionnez ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dans le rail de gauche.
1. Sélectionnez ![Plus](/help/assets/icons/More.svg) pour un modèle, puis sélectionnez **[!UICONTROL Delete]** dans le menu contextuel. Vous pouvez également sélectionner ![Supprimer](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** dans la barre d’actions bleue.
1. Sélectionnez **[!UICONTROL Delete]** dans la boîte de dialogue de confirmation de **[!UICONTROL Delete model]** pour supprimer le modèle. Sélectionnez **[!UICONTROL Cancel]** pour annuler.

Pour supprimer plusieurs modèles :

1. Sélectionnez plusieurs modèles.
1. Dans la barre d’actions bleue, sélectionnez ![Supprimer](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** pour supprimer les modèles.
1. Sélectionnez **[!UICONTROL Delete]** dans la boîte de dialogue de confirmation **[!UICONTROL Delete *x *models]**pour supprimer les modèles. Sélectionnez **[!UICONTROL Cancel]**pour annuler.


