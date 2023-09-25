---
title: Schémas
description: Découvrez comment gérer les schémas requis pour ingérer des données dans Adobe Mix Modeler.
feature: Datasets
source-git-commit: abbfc78e9fa774a240d000131f35d3dc257c15ea
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 6%

---


# Schémas

Pour gérer les schémas, en prenant en charge les données que vous souhaitez ingérer dans Adobe Experience Platform et utiliser dans Adobe Mix Modeler :

1. Accédez à l’interface Adobe Mix Modeler .

1. Sélectionner ![Schémas](../assets/icons/Schemas.svg) **[!UICONTROL Schemas]**, sous **[!UICONTROL DATA MANAGEMENT]**.

Voir [Présentation de l’interface utilisateur des schémas](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=fr) pour plus d’informations.

## Agrégat ou données récapitulatives

Il est vivement recommandé d’utiliser la classe XDM Summary Metrics comme base du schéma sous-jacent à tout agrégat ou donnée de résumé que vous souhaitez ingérer dans Experience Platform et utiliser dans Adobe Mix Modeler.

Voir ci-dessous un exemple d’une **[!DNL LumaPaidMarketingSchema]** l’utilisation des mesures de résumé XDM comme classe de base et des groupes de champs dédiés (annotés avec des couleurs) pour la mesure (**[!DNL AMMMetrics]**), dimensions (**[!DNL AMMDimensions]**) et d’autres informations spécifiques au client (**[!DNL CustomerSpecific]**).

![Schéma de résumé](../assets/summary-schema.png)

Pour définir un ensemble de propriétés d’audit, il est vivement conseillé d’utiliser le groupe de champs Détails de l’audit du système source externe dans le cadre d’un schéma utilisé pour la collecte de données agrégées ou récapitulatives provenant de sources externes.
