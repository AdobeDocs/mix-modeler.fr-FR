---
title: Modèles
description: Découvrez comment configurer et utiliser des modèles dans Mix Modeler.
feature: Models
source-git-commit: 08cfd4239f6bcaf885565f3ae04cbd51869e8c00
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 4%

---


# Modèles

La fonctionnalité de modèle de Mix Modeler vous permet de configurer, de former et de noter des modèles AI/ML spécifiques à vos objectifs commerciaux et pris en charge par l’apprentissage par transfert piloté par l’IA entre l’attribution multipoint et la modélisation de combinaison marketing.

Les modèles sont basés sur les données harmonisées que vous créez dans le cadre du processus de l’application de Mix Modeler.

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
   | Événements de conversion | La conversion que vous avez sélectionnée pour le modèle. |
   | Jeu de données | Jeu de données que le modèle utilise pour entraîner et noter. Il s’agit par défaut du jeu de données harmonisé. |
   | Fréquence d’exécution | Fréquence d’exécution de l’entraînement du modèle. |
   | Dernière exécution | Date et heure de la dernière formation du modèle. |
   | Statut de la dernière exécution | État de la dernière exécution de l’entraînement du modèle. <br/><span style="color:green">●</span> Succès<br/><span style="color:orange">●</span> Problème de formation<br/> <span style="color:orange">●</span> En attente de formation <br/><span style="color:red">●</span> En échec |

   {style="table-layout:auto"}

1. Pour modifier les colonnes affichées pour la liste, sélectionnez ![Paramètres des colonnes](../assets/icons/ColumnSetting.svg) et bascule des colonnes sur ![Vérifier](../assets/icons/Checkmark.svg) ou off.

### Suppression d’un modèle

Pour supprimer un modèle :

1. Sélectionnez le nom du modèle que vous souhaitez supprimer.

1. Dans le menu contextuel, sélectionnez **[!UICONTROL Delete]** pour supprimer le modèle.

### Affichage des détails d’un modèle

Pour afficher plus de détails sur un modèle :

1. Sélectionnez le nom du modèle dont vous souhaitez afficher plus de détails.

1. Dans le menu contextuel, sélectionnez **[!UICONTROL More]**. Les détails du modèle sélectionné s’affichent dans le volet de droite.



### Informations sur les modèles

>[!NOTE]
>
>Cette sélection n’est disponible que sur les modèles formés avec succès.
>

Pour afficher les insights d’un modèle, dans l’interface du Mix Modeler :

1. Sélectionner ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** dans le rail de gauche.

1. Sélectionnez le nom d’un modèle avec une **[!UICONTROL Last run status]** de <span style="color:green">●</span> **[!UICONTROL Success]** de la **[!UICONTROL Models]** table.

1. Dans le menu contextuel, sélectionnez **[!UICONTROL Model Insights]**. Vous êtes redirigé vers [Informations sur les modèles](insights.md).


