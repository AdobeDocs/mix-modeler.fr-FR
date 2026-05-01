---
title: Schémas
description: Découvrez comment gérer les schémas requis pour ingérer des données dans Mix Modeler.
feature: Schemas
exl-id: 08289581-5af9-4422-b049-8c24105e2a8e
TQID: https://experienceleague.adobe.com/E41pnyBetoLPOOulNmKh033myMvfF4bV9A2Xd3FXqcs
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: fbd94e4b-f9b8-42a4-8df5-3f917aabae24
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
autotag-review: '2026-05-01T08:56:54.552Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 613
ht-degree: 7%

---

# Schémas

Pour gérer les schémas, en prenant en charge les données que vous souhaitez ingérer dans Experience Platform et utiliser dans Mix Modeler :

1. Accédez à l’interface de Mix Modeler.

1. Sélectionnez ![Schémas](/help/assets/icons/Schemas.svg) **[!UICONTROL Schemas]**, sous **[!UICONTROL SETUP]**.

Consultez la [&#x200B; Présentation de l’interface utilisateur des schémas &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=fr) pour plus d’informations.

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

  | date et heure | date_type | facteur | value |
  |---|---|---|--:|
  | 2020-11-:00:00.000Z | semaine | concurrent_index | 289.8 |
  | 2020-12-:00:00.000Z | semaine | concurrent_index | 291.2 |
  | 2020-12-:00:00.000Z | semaine | concurrent_index | 280.07 |
  | … | … | … | … |

- Données de jour férié

  | date et heure | date_type | facteur | value |
  |---|---|---|--:|
  | 2020-11-:00:00.000Z | semaine | all_Holidays_flag | 0.0 |
  | 2020-12-:00:00.000Z | semaine | all_Holidays_flag | 0.0 |
  | 2020-12-:00:00.000Z | semaine | all_Holidays_flag | 0.0 |
  | 2020-12-:00:00.000Z | semaine | all_Holidays_flag | 0.0 |
  | 2020-12-:00:00.000Z | semaine | all_Holidays_flag | 1.0 |
  | … | … | … | … |


Consultez ci-dessous un exemple plus complet d’**[!DNL LumaPaidMarketingSchema]** utilisant la **[!DNL XDM Summary Metrics]** comme classe de base. Le schéma utilise des groupes de champs dédiés (annotés avec des couleurs) pour les mesures (**[!DNL AMMMetrics]**), les dimensions (**[!DNL AMMDimensions]**) et d’autres informations spécifiques au client (**[!DNL CustomerSpecific]**).

![Schéma récapitulatif](/help/assets/summary-schema.png)

Compte tenu de la nature asynchrone de l’ingestion de profil, lors de la collecte de données agrégées ou récapitulatives à partir de sources externes, il est recommandé d’utiliser le groupe de champs Détails de l’audit du système Source externe dans le cadre d’un schéma. Ce groupe de champs définit un ensemble de propriétés d’audit pour les sources externes.

## Groupe de champs Champs standard de facteur

Pour plus de commodité, Experience Platform prend en charge un groupe de champs standard de facteur dédié pour les données de facteurs internes et externes, qui font souvent partie des données récapitulatives, de facteurs internes ou de facteurs externes. Ce groupe de champs définit les champs suivants :

| Nom d’affichage du champ | Nom du champ | Type de champ | Type de données | Obligatoire | Description |
|---|---|---|---|:-:|---|
| Nom du facteur | factorName | Dimension | Chaîne | ![Coche](/help/assets/icons/Checkmark.svg) | Nom du facteur |
| Valeur du facteur | factorValue | Mesure | Double | ![Coche](/help/assets/icons/Checkmark.svg) | Valeur du facteur |
| Type de facteur | factorType | Dimension | Chaîne (Énumération) | | Type du facteur.<br/>Les valeurs possibles sont : <ul><li>Interne (facteur interne)</li><li>Externe (facteur externe)</li></ul> |
| Type de valeur | valueType | Dimension | Chaîne (Énumération) | | Les valeurs possibles sont les suivantes :<ul><li>Réel (valeur réelle)</li><li>Prévu (valeur prévue)</li></ul>En l’absence de valeur, Réel est la valeur par défaut. |
| Granularité | granularité | Dimension | Chaîne (Énumération) | | Les valeurs possibles sont les suivantes :<ul><li>Quotidien</li><li>Hebdomadaire</li><li>Mensuel</li></ul> |

Un jeu de données de synthèse, de facteur interne ou de facteur externe peut être basé sur :

- Schéma qui **utilise** le groupe Champs standard de facteur. Ce jeu de données s’affiche sous la forme d’un jeu de données **[!UICONTROL Factors]** lorsque vous configurez des règles de jeu de données. De plus, les champs harmonisés que vous définissez, dans le cadre des règles du jeu de données pour le jeu de données, sont disponibles en tant que facteurs lorsque vous créez un modèle.
- Schéma qui **n’utilise pas** le groupe Champs standard de facteur. Ce jeu de données s’affiche sous la forme d’un jeu de données **[!UICONTROL Summary]** lorsque vous configurez des règles de jeu de données. Le jeu de données est configuré en tant que données récapitulatives et n’influence pas les données harmonisées.

## Types de données pris en charge

Actuellement, Mix Modeler ne prend pas en charge un sous-ensemble de types de données Experience Platform. Les types de données de base suivants (champs), mentionnés dans [Principes de base de la composition des schémas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=fr#data-type), sont pris en charge :

- Chaîne
- Nombre entier
- Double
- Booléen
- Long
- Court
- Octet
- Date
- Date-time


>[!MORELIKETHIS]
>
>- [Schémas](schemas.md)
