---
title: Schémas
description: Découvrez comment gérer les schémas requis pour ingérer des données dans Mix Modeler.
feature: Schemas
exl-id: 08289581-5af9-4422-b049-8c24105e2a8e
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 5%

---

# Schémas

Pour gérer les schémas, en prenant en charge les données que vous souhaitez ingérer dans Experience Platform et utiliser dans Mix Modeler :

1. Accédez à l’interface du Mix Modeler.

1. Sélectionnez ![Schémas](/help/assets/icons/Schemas.svg) **[!UICONTROL Schemas]** sous **[!UICONTROL SETUP]**.

Pour plus d’informations, consultez la [présentation de l’interface utilisateur des schémas](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=fr) .

## Agrégat ou données récapitulatives

Il est vivement recommandé d’utiliser la classe XDM Summary Metrics comme base du schéma sous-jacent à tout agrégat ou donnée de résumé que vous souhaitez ingérer dans Experience Platform et utiliser dans Mix Modeler.

Utilisez la classe XDM Summary Metrics pour :

- les données de jardin fortifiées, par exemple les données provenant de Facebook ou de YouTube ;

- les données de facteurs externes, comme les données de SPX (indices boursiers S&amp;P 500), les données météorologiques,

- données de facteurs internes, par exemple les changements de prix, un calendrier des fêtes.

>[!IMPORTANT]
>
>La définition de schéma doit contenir au moins un champ numérique (à l’aide d’un type Entier, Double, Booléen ou autre numérique) pour prendre en charge les mesures requises pour les données ingérées.

Un schéma utilisant la classe de base **[!DNL XDM Summary Metrics]** peut être simple, comme illustré dans la **[!DNL ExternalFactorSummarySchema]** ci-dessous.

![Schéma de facteurs externes](/help/assets/external-factors-schema.png)

Ce schéma simple peut être utilisé pour ingérer des jeux de données contenant des données, par exemple :

- Données de l’index des concurrents

  | date et heure | date_type | facteur | value |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | week | concurrent_index | 289,8 |
  | 2020-12-05T00:00:00.000Z | week | concurrent_index | 291,2 |
  | 2020-12-12T00:00:00.000Z | week | concurrent_index | 280,07 |
  | … | … | … | … |

- Données des fêtes publiques

  | date et heure | date_type | facteur | value |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | week | all_vacances_flag | 0,0 |
  | 2020-12-05T00:00:00.000Z | week | all_vacances_flag | 0,0 |
  | 2020-12-12T00:00:00.000Z | week | all_vacances_flag | 0,0 |
  | 2020-12-19T00:00:00.000Z | week | all_vacances_flag | 0,0 |
  | 2020-12-26T00:00:00.000Z | week | all_vacances_flag | 1.0 |
  | … | … | … | … |


Voir ci-dessous un exemple plus complet d’un **[!DNL LumaPaidMarketingSchema]** utilisant **[!DNL XDM Summary Metrics]** comme classe de base. Le schéma utilise des groupes de champs dédiés (annotés avec des couleurs) pour les mesures (**[!DNL AMMMetrics]**), les dimensions (**[!DNL AMMDimensions]**) et d’autres informations spécifiques au client (**[!DNL CustomerSpecific]**).

![Schéma de résumé](/help/assets/summary-schema.png)

Étant donné la nature asynchrone de l’ingestion des profils, lors de la collecte de données agrégées ou récapitulatives à partir de sources externes, il est conseillé d’utiliser le groupe de champs Détails de l’audit du système Source externe dans le cadre d’un schéma. Ce groupe de champs définit un ensemble de propriétés d’audit pour les sources externes.


## Types de données pris en charge

Actuellement, Mix Modeler prend en charge un sous-ensemble de types de données Experience Platform. Les types de données de base suivants (champs), mentionnés dans [Principes de base de la composition des schémas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#data-type), sont pris en charge :

- Chaîne
- Entier
- Double
- Booléen
- Long
- Short
- Byte
- Date
- Date-time
