---
title: Modèles
description: Découvrez comment configurer et utiliser des modèles dans Mix Modeler.
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: 73534d1aecb6d1513f6f3b5f1801b497ad73278f
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 2%

---

# Modèles

La fonctionnalité de modèle de Mix Modeler vous permet de configurer, de former et de noter des modèles AI/ML spécifiques à vos objectifs commerciaux et pris en charge par l’apprentissage par transfert piloté par l’IA entre l’attribution multipoint et la modélisation de combinaison marketing.

Les modèles sont basés sur les données harmonisées que vous créez dans le cadre du processus de l’application de Mix Modeler.

Un modèle en Mix Modeler est un modèle d’apprentissage automatique utilisé pour mesurer et/ou prédire un résultat spécifié en fonction des investissements d’un spécialiste du marketing. Les points de contact marketing et les données de niveau résumé peuvent être utilisés comme entrée. Mix Modeler vous permet de créer des variantes de modèles basées sur différents ensembles de variables, dimensions et résultats, tels que les revenus, unités vendues et prospects.

Un modèle nécessite :

* une conversion,
* un ou plusieurs points de contact marketing (canaux) composés de données de niveau résumé, de données de point de contact marketing (données d’événement) ou les deux,
* un intervalle de recherche en amont configurable pour
* une fenêtre de formation configurable.

Un modèle peut éventuellement inclure :

* facteurs externes,
* facteurs internes,
* les &quot;primeurs&quot; (distribution de probabilité représentant la connaissance ou l’incertitude des données avant ou avant l’observation de ces données), qui indexe les conversions antérieures par canal,
* le partage des dépenses, qui utilise le partage des dépenses relatif comme proxy lorsque les données marketing sont éparses.


## Création d’un modèle

Pour créer un modèle, utilisez le flux de configuration de modèle guidé étape par étape du Mix Modeler disponible lorsque vous sélectionnez **[!UICONTROL Guide me]**. Voir [Création d’un modèle](create.md) pour plus d’informations.

## Gestion des modèles

Pour afficher un tableau de vos modèles actuels, dans l’interface du Mix Modeler :

1. Sélectionner ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** dans le rail de gauche.

1. Vous voyez un tableau des modèles actuels.

   Les colonnes du tableau spécifient des détails sur le modèle.

   | Nom de la colonne | Détails |
   |---|---|
   | Nom | Nom du modèle |
   | Description | Description du modèle |
   | Événement de conversion | La conversion que vous avez sélectionnée pour le modèle. |
   | Fréquence d’exécution | Fréquence d’exécution de l’entraînement du modèle. |
   | Dernière exécution | Date et heure de la dernière formation du modèle. |
   | Statut | État de la dernière exécution de l’entraînement du modèle. <br/><span style="color:green">●</span> Succès<br/><span style="color:orange">●</span> Problème de formation<br/> <span style="color:orange">●</span> En attente de formation <br/><span style="color:red">●</span> En échec |

   {style="table-layout:auto"}

1. Pour modifier les colonnes affichées pour la liste, sélectionnez ![Paramètres des colonnes](../assets/icons/ColumnSetting.svg) et bascule des colonnes sur ![Vérifier](../assets/icons/Checkmark.svg) ou off.

### Suppression d’un modèle

Pour supprimer un modèle :

1. Sélectionnez le nom du modèle que vous souhaitez supprimer.

1. Dans le menu contextuel, sélectionnez **[!UICONTROL Delete]** pour supprimer le modèle.

### Affichage des détails d’un modèle

Pour afficher plus de détails sur un modèle :

1. Sélectionner ![Infos](../assets/icons/Info.svg) pour un modèle afin d’afficher une fenêtre contextuelle contenant des détails.



### Informations sur les modèles

>[!NOTE]
>
>Cette sélection n’est disponible que sur les modèles formés avec succès.
>

Pour afficher les insights d’un modèle, dans l’interface du Mix Modeler :

1. Sélectionner ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** dans le rail de gauche.

1. Sélectionnez le nom d’un modèle avec une **[!UICONTROL Last run status]** de <span style="color:green">●</span> **[!UICONTROL Success]** de la **[!UICONTROL Models]** table.

1. Dans le menu contextuel, sélectionnez **[!UICONTROL Model Insights]**. Vous êtes redirigé vers [Informations sur les modèles](insights.md).


### Re-score

>[!NOTE]
>
>Cette sélection n’est disponible que sur les modèles formés avec succès.
>

Pour noter à nouveau un modèle, dans l’interface du Mix Modeler :

1. Sélectionner ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** dans le rail de gauche.

1. Sélectionnez le nom d’un modèle avec une **[!UICONTROL Last run status]** de <span style="color:green">●</span> **[!UICONTROL Success]** de la **[!UICONTROL Models]** table.

1. Dans le menu contextuel, sélectionnez **[!UICONTROL Re-score]**. L’affichage d’un état mis à jour du modèle peut prendre quelques minutes.

