---
title: Afficher les notes de mise à jour actuelles de Mix Modeler
description: Dernières notes de mise à jour de Mix Modeler
feature-set: Experience Cloud
feature: Release Notes
exl-id: 38a47672-2af2-437c-b769-4d5febb941f5
source-git-commit: 7581053507bd1a6a07b2f3853f454631ecee8cec
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 3%

---

# Notes de mise à jour actuelles de Mix Modeler

**Dernière mise à jour** : 26 février 2026.

Ces notes de mise à jour présentent la dernière version de Mix Modeler. Les versions de Mix Modeler fonctionnent sur un modèle de diffusion continu, ce qui permet une cadence de publication mensuelle approximative. Par conséquent, ces notes de mise à jour sont mises à jour. Consultez-les régulièrement.

## Février 2026

| Fonctionnalité | Description | [&#x200B; Début du déploiement &#x200B;](#release-strategy) | [Disponibilité générale](#release-strategy) |
|---|---|---|---|
| **Workflow des facteurs harmonisés** | Les facteurs sont désormais gérés dans le cadre d’un [&#x200B; workflow de facteurs harmonisés &#x200B;](/help/harmonize-data/overview.md#factors). Cela simplifie la [définition des données de facteur](/help/ingest-data/schemas.md#factor-standard-fields-field-group), la [gestion des facteurs internes et externes dans le cadre des règles de votre jeu de données](/help/harmonize-data/dataset-rules.md#factor-datasets) et l&#39;utilisation des données de facteur dans les [modèles](/help/models/build.md#configure). | 25 Février 2026 | 25 Février 2026 |
| **[!UICONTROL Granular incrementality reporting]** | Définissez des champs harmonisés afin de pouvoir analyser en profondeur le compte rendu des performances de votre modèle à l’aide de [champs de compte rendu des performances granulaires](/help/models/build.md#granular-insights-reporting-fields), au lieu d’avoir à créer des modèles distincts. | 18 Février 2026 | 18 Février 2026 |

## Janvier 2026

| Fonctionnalité | Description | [&#x200B; Début du déploiement &#x200B;](#release-strategy) | [Disponibilité générale](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Dataset rules]** | [Mise à jour du tableau des règles du jeu de données](/help/harmonize-data/dataset-rules.md). Vous pouvez rechercher une ou plusieurs règles de jeu de données et afficher, modifier ou supprimer une règle de jeu de données directement à partir du tableau. | 13 janvier 2026 | 13 janvier 2026 |
| **[!UICONTROL Current spend]** | Ajoutez un point de dépense actuel dans la [visualisation de la courbe de réponse marginale](/help/models/insights.md#marginal-response-curves) des informations sur le modèle. | 13 janvier 2026 | 13 janvier 2026 |
| **[!UICONTROL Sort and resize columns]** | Ajout du tri et du redimensionnement des colonnes dans le tableau [Modèles](/help/models/overview.md) et [Plans](/help/plans/overview.md). | 13 janvier 2026 | 13 janvier 2026 |
| **Correctifs** | Correctifs pour les tickets suivants : <ul><li>AMM-3328 : entrée de champ désactivée pour les nouveaux opérateurs pour les facteurs</li><li>AMM-3359 : verrouillage du sélecteur de date et de la zone de liste modifiable.</li><li>AMM-3441 : la duplication d’un plan ne remplit pas automatiquement la période et le budget.</li></ul> | 13 janvier 2026 | 13 janvier 2026 |


## Stratégie de publication

[!UICONTROL Mix Modeler] utilise des indicateurs de fonctionnalité (également appelés « bascules ») pour contrôler la visibilité des nouvelles fonctionnalités, ce qui permet de les tester à échelle contrôlée avant la mise à jour complète. Cette stratégie de publication comprend les phases suivantes :

* **Tests limités** : la publication par étapes commence par un test réalisé par les utilisateurs et utilisatrices Adobe internes. Elle est ensuite mise à la disposition d’un petit groupe de comptes clients afin de s’assurer que la fonctionnalité répond aux besoins et aux attentes des clients.

* **Début du déploiement** : le déploiement d’une publication par phases commence par la phase Tests limités. La mise à jour passe ensuite de 0 % à 100 % de disponibilité pour les clients en quelques mois. Le déploiement échelonné se produit au niveau de l’organisation Experience Cloud, de sorte que tous les utilisateurs autorisés d’une organisation bénéficient de la même expérience.

