---
title: Afficher les notes de mise à jour actuelles de Mix Modeler
description: Dernières notes de mise à jour de Mix Modeler
feature-set: Experience Cloud
feature: Release Notes
exl-id: 38a47672-2af2-437c-b769-4d5febb941f5
TQID: https://experienceleague.adobe.com/8o2hpkneIUMbBNEZfw9TsQLaGuPOxqF-XA2TV9cJnqc
product_v2: id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2: id: ca6bcd6f-f5ca-4e5f-a5ae-7dce7177bde9
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: e1e0219c-f879-479f-8427-888ed2a6e9c2
autotag-review: '2026-05-01T09:06:55.437Z'
source-git-commit: 1e6444e672e85d9f3f666bc865d020fb67c45b09
workflow-type: tm+mt
source-wordcount: 524
ht-degree: 6%

---

# Notes de mise à jour actuelles de Mix Modeler

**Dernière mise à jour** : 19 août 2026.

Ces notes de mise à jour présentent la dernière version de Mix Modeler. Les versions de Mix Modeler fonctionnent sur un modèle de diffusion continu, ce qui permet une cadence de publication mensuelle approximative. Par conséquent, ces notes de mise à jour sont mises à jour. Consultez-les régulièrement.

## Août 2026

| Fonctionnalité | Description | [ Début du déploiement ](#release-strategy) | [Disponibilité générale](#release-strategy) |
|---|---|---|---|
| **Filtrer sur les règles du jeu de données** | Dans la configuration des jeux de données harmonisés, vous pouvez [filtrer les règles des jeux de données selon la source, la granularité et le début de la semaine](/help/harmonize-data/dataset-rules.md#manage-dataset-rules). | 19 Août 2026 | 19 Août 2026 |
| **Thème de canal média payant** | Vous pouvez choisir de [se concentrer sur la contribution de canal média payant](/help/models/insights.md#contribution-by-channel) dans les informations sur le modèle. | 19 Août 2026 | 19 Août 2026 |
| **Configuration du résumé des performances marketing** | Vous pouvez [sélectionner une mesure et mode d’affichage de la mesure](/help/models/insights.md#marketing-performance-summary) pour le résumé des performances marketing des modèles basés sur le chiffre d’affaires dans les informations sur les modèles. | 19 Août 2026 | 19 Août 2026 |


## Mars 2026

| Fonctionnalité | Description | [ Début du déploiement ](#release-strategy) | [Disponibilité générale](#release-strategy) |
|---|---|---|---|
| **Stock publicitaire de canal** | Vous pouvez incorporer l’expertise de domaine, les résultats d’expérimentation ou les analyses de canaux précédentes directement dans la configuration avancée du modèle par le biais d’[Adstock de canaux](/help/models/build.md#channel-adstock). et afficher des [informations sur les stocks publicitaires des canaux](/help/models/insights.md#channel-adstock) dans l’analyse des canaux d’un modèle. | 30 mars 2026 | 30 mars 2026 |

## Février 2026

| Fonctionnalité | Description | [ Début du déploiement ](#release-strategy) | [Disponibilité générale](#release-strategy) |
|---|---|---|---|
| **Workflow des facteurs harmonisés** | Les facteurs sont désormais gérés dans le cadre d’un [ workflow de facteurs harmonisés ](/help/harmonize-data/overview.md#factors). Cela simplifie la [définition des données de facteur](/help/ingest-data/schemas.md#factor-standard-fields-field-group), la [gestion des facteurs internes et externes dans le cadre des règles de votre jeu de données](/help/harmonize-data/dataset-rules.md#factor-datasets) et l&#39;utilisation des données de facteur dans les [modèles](/help/models/build.md#configure). | 25 Février 2026 | 25 Février 2026 |
| **[!UICONTROL Granular incrementality reporting]** | Définissez des champs harmonisés afin de pouvoir analyser en profondeur le compte rendu des performances de votre modèle à l’aide de [champs de compte rendu des performances granulaires](/help/models/build.md#granular-insights-reporting-fields), au lieu d’avoir à créer des modèles distincts. | 18 Février 2026 | 18 Février 2026 |

## Janvier 2026

| Fonctionnalité | Description | [ Début du déploiement ](#release-strategy) | [Disponibilité générale](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Dataset rules]** | [Mise à jour du tableau des règles du jeu de données](/help/harmonize-data/dataset-rules.md). Vous pouvez rechercher une ou plusieurs règles de jeu de données et afficher, modifier ou supprimer une règle de jeu de données directement à partir du tableau. | 13 janvier 2026 | 13 janvier 2026 |
| **[!UICONTROL Current spend]** | Ajoutez un point de dépense actuel dans la [visualisation de la courbe de réponse marginale](/help/models/insights.md#marginal-response-curves) des informations sur le modèle. | 13 janvier 2026 | 13 janvier 2026 |
| **[!UICONTROL Sort and resize columns]** | Ajout du tri et du redimensionnement des colonnes dans le tableau [Modèles](/help/models/overview.md) et [Plans](/help/plans/overview.md). | 13 janvier 2026 | 13 janvier 2026 |
| **Correctifs** | Correctifs pour les tickets suivants : <ul><li>AMM-3328 : entrée de champ désactivée pour les nouveaux opérateurs pour les facteurs</li><li>AMM-3359 : verrouillage du sélecteur de date et de la zone de liste modifiable.</li><li>AMM-3441 : la duplication d’un plan ne remplit pas automatiquement la période et le budget.</li></ul> | 13 janvier 2026 | 13 janvier 2026 |


## Stratégie de publication

[!UICONTROL Mix Modeler] utilise des indicateurs de fonctionnalité (également appelés « bascules ») pour contrôler la visibilité des nouvelles fonctionnalités, ce qui permet de les tester à échelle contrôlée avant la mise à jour complète. Cette stratégie de publication comprend les phases suivantes :

* **Tests limités** : la publication par étapes commence par un test réalisé par les utilisateurs et utilisatrices Adobe internes. Elle est ensuite mise à la disposition d’un petit groupe de comptes clients afin de s’assurer que la fonctionnalité répond aux besoins et aux attentes des clients.

* **Début du déploiement** : le déploiement d’une publication par phases commence par la phase Tests limités. La mise à jour passe ensuite de 0 % à 100 % de disponibilité pour les clients en quelques mois. Le déploiement échelonné se produit au niveau de l’organisation Experience Cloud, de sorte que tous les utilisateurs autorisés d’une organisation bénéficient de la même expérience.

