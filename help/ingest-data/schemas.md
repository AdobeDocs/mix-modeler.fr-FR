---
title: Schémas
description: Découvrez comment gérer les schémas requis pour ingérer des données dans Mix Modeler.
feature: Schemas
exl-id: 08289581-5af9-4422-b049-8c24105e2a8e
source-git-commit: b0306ad6fad8966822ed14c67f159a4aefb4e3f8
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 6%

---

# Schémas

Pour gérer les schémas, en prenant en charge les données que vous souhaitez ingérer dans Experience Platform et utiliser dans Mix Modeler :

1. Accédez à l’interface de Mix Modeler.

1. Sélectionnez ![Schémas](/help/assets/icons/Schemas.svg) **[!UICONTROL Schemas]**, sous **[!UICONTROL SETUP]**.

Consultez la [ Présentation de l’interface utilisateur des schémas ](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=fr) pour plus d’informations.

## Données agrégées ou récapitulatives

Il est vivement recommandé d’utiliser la classe Mesures récapitulatives XDM comme base du schéma sous-jacent à toutes les données agrégées ou récapitulatives que vous souhaitez ingérer dans Experience Platform et utiliser dans Mix Modeler.

Utilisez la classe Mesures récapitulatives XDM pour :

- Données de jardin clos ; par exemple, données provenant de Facebook ou de YouTube.

- des données sur les facteurs externes, comme les données de SPX (indices boursiers S&amp;P 500), les données météorologiques,

- données de facteurs internes, par exemple les modifications de prix, un calendrier des vacances.

>[!IMPORTANT]
>
>La définition du schéma doit contenir au moins un champ numérique (de type Entier, Doublon, Booléen ou autre) pour prendre en charge les mesures requises pour les données ingérées.

Un schéma utilisant la classe de base **[!DNL XDM Summary Metrics]** peut être simple, comme illustré dans l’**[!DNL ExternalFactorSummarySchema]** ci-dessous.

![Schéma des facteurs externes](/help/assets/external-factors-schema.png)

Ce schéma simple peut être utilisé pour ingérer des jeux de données contenant des données pour, par exemple :

- Données sur l’index des concurrents

  | date et heure | date_type | facteur | valeur |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | semaine | concurrent_index | 289,8 |
  | 2020-12-05T00:00:00.000Z | semaine | concurrent_index | 291,2 |
  | 2020-12-12T00:00:00.000Z | semaine | concurrent_index | 280,07 |
  | … | … | … | … |

- Données de jour férié

  | date et heure | date_type | facteur | valeur |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | semaine | all_Holidays_flag | 0,0 |
  | 2020-12-05T00:00:00.000Z | semaine | all_Holidays_flag | 0,0 |
  | 2020-12-12T00:00:00.000Z | semaine | all_Holidays_flag | 0,0 |
  | 2020-12-19T00:00:00.000Z | semaine | all_Holidays_flag | 0,0 |
  | 2020-12-26T00:00:00.000Z | semaine | all_Holidays_flag | 1.0 |
  | … | … | … | … |


Consultez ci-dessous un exemple plus complet d’**[!DNL LumaPaidMarketingSchema]** utilisant la **[!DNL XDM Summary Metrics]** comme classe de base. Le schéma utilise des groupes de champs dédiés (annotés avec des couleurs) pour les mesures (**[!DNL AMMMetrics]**), les dimensions (**[!DNL AMMDimensions]**) et d’autres informations spécifiques au client (**[!DNL CustomerSpecific]**).

![Schéma récapitulatif](/help/assets/summary-schema.png)

Compte tenu de la nature asynchrone de l’ingestion de profil, lors de la collecte de données agrégées ou récapitulatives à partir de sources externes, il est recommandé d’utiliser le groupe de champs Détails de l’audit du système Source externe dans le cadre d’un schéma. Ce groupe de champs définit un ensemble de propriétés d’audit pour les sources externes.


## Types de données pris en charge

Actuellement, Mix Modeler ne prend pas en charge un sous-ensemble de types de données Experience Platform. Les types de données de base suivants (champs), mentionnés dans [Principes de base de la composition des schémas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=fr#data-type), sont pris en charge :

- Chaîne
- Entier
- Double
- Booléen
- Long
- Short
- Byte
- Date
- Date-time


>[!MORELIKETHIS]
>
>- [Schémas](schemas.md)
