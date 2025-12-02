---
title: Afficher les notes de mise à jour actuelles de Mix Modeler
description: Dernières notes de mise à jour de Mix Modeler
feature-set: Experience Cloud
feature: Release Notes
exl-id: 38a47672-2af2-437c-b769-4d5febb941f5
source-git-commit: 5f3b5462bd2174534692051f61c57f0d3f9d4db0
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 4%

---

# Notes de mise à jour actuelles de Mix Modeler

**Dernière mise à jour** : 12 novembre 2025.

Ces notes de mise à jour présentent la dernière version de Mix Modeler. Les versions de Mix Modeler fonctionnent sur un modèle de diffusion continu, ce qui permet une cadence de publication mensuelle approximative. Par conséquent, ces notes de mise à jour sont mises à jour. Consultez-les régulièrement.



## Novembre 2025

| Fonctionnalité | Description | [ Début du déploiement ](#release-strategy) | [Disponibilité générale](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Plans tracking]** | Permet aux utilisateurs de comprendre comment l’exécution des plans marketing suit ce qui est prévu. Vous pouvez ainsi avoir confiance dans les performances du marketing. Vous pouvez également identifier les opportunités et les risques plus tôt pour corriger le cap et atteindre les objectifs commerciaux. Les [Performances pour planifier les visualisations](/help/dashboard/plans.md#performance-to-plan) sont mises à jour et permettent de configurer les mesures et la granularité. | 12 Novembre 2025 | 12 Novembre 2025 |
| **[!UICONTROL Channel synergy insights]** | Découvrez comment les canaux marketing fonctionnent ensemble pour créer un impact plus important. Grâce à ces informations, vous pouvez expliquer en toute confiance la performance marketing passée et ajuster les dépenses marketing en conséquence afin de maximiser le rendement global de votre portefeuille marketing. Une matrice de synergie des canaux est disponible dans [Informations sur les modèles](/help/models/insights.md#channel-synergy) et [Informations sur les plans](/help/plans/insights.md#channel-synergies). | 12 Novembre 2025 | 12 Novembre 2025 |
| **Correctifs** | Correctifs pour les tickets suivants : <ul><li>AMM-2920 : flux de création et de migration des plans.</li><li>AMM-3282 : notation scientifique pour varier les petits nombres dans les grands réseaux.</li></ul> | 12 Novembre 2025 | 12 Novembre 2025 |


## Septembre 2025

| Fonctionnalité | Description | [ Début du déploiement ](#release-strategy) | [Disponibilité générale](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Dataset mapping validations]** | Ajout de validations aux mappages de jeux de données Experience Platform pour les champs harmonisés. | mercredi 9 septembre 2025 | mercredi 9 septembre 2025 |
| **[!UICONTROL Context menu on links to model and plans]** | Activation du menu contextuel du navigateur sous forme de liens vers des modèles et des plans. Vous pouvez désormais utiliser ce menu contextuel du navigateur pour ouvrir un plan ou un modèle spécifique dans un nouvel onglet ou une nouvelle fenêtre. | mercredi 9 septembre 2025 | mercredi 9 septembre 2025 |
| **Correctifs** | Correctifs pour les tickets suivants : <ul><li>AMM-3101 : correction d’une création de mappage incorrecte pour les règles : `event_date` a été transmis comme nom de champ au lieu de `timestamp`.</li><li>AMM-3092 : correction d’une erreur qui empêchait de modifier la valeur de contrainte maximale de canal sur un plan basé sur un budget dupliqué.</li><li>AM3130 : correction d’informations **[!UICONTROL Run frequency]** incorrectes sur une fenêtre contextuelle de détail d’un modèle.</li><li>AMM3158 : mise à jour des libellés des options de **[!UICONTROL Select target metric]** dans le volet **[!UICONTROL Optimize]** de l’interface [Création de plans](/help/plans/build.md).</li><li>AMM 3176 : correction d’une erreur qui empêchait l’affichage de la visualisation [Répartition par canal](/help/models/insights.md#breakdown) dans **[!UICONTROL Attribution]**’onglet de **[!UICONTROL Model Insights]**.</li></ul> | mercredi 9 septembre 2025 | mercredi 9 septembre 2025 |
| **Correctifs** | Correctifs pour les tickets suivants : <ul><li>AMM-3174 : expérience améliorée lorsqu’aucun plan existant n’est disponible.</li><li>AMM-3216 : validation améliorée des périodes personnalisées.</li><li>AMM-3240 : affichage de la fréquence du modèle d’exécution fixe.</ul> | 23 septembre 2025 | 23 septembre 2025 |

## Juillet - Août 2025

| Fonctionnalité | Description | [ Début du déploiement ](#release-strategy) | [Disponibilité générale](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Compare plans update]** | L’interface utilisateur [Comparer des plans](/help/plans/compare.md) affiche désormais des détails supplémentaires sur le marketing payant : RSI ou CPA, et chiffre d’affaires. | 20 Août 2025 | 20 Août 2025 |
| **Mises à jour de l’harmonisation** | Toutes les règles des jeux de données utilisent désormais une [expérience de mappage générique aux champs harmonisés](/help/harmonize-data/dataset-rules.md) similaire, quel que soit le type de jeu de données. Lorsque vous mappez un champ harmonisé standard à partir d’un jeu de données de résumé, Mix Modeler tente de déduire automatiquement le champ de jeu de données Experience Platform correspondant. | mercredi 29 juillet 2025 | mercredi 29 juillet 2025 |
| **Optimisation améliorée du retour sur investissement/CPA marginal** | Permet d’améliorer la répartition des budgets marketing au fil du temps. Au lieu de faire converger le RSI/CPA marginal sur toute la période de planification, vous pouvez [optimiser sur plusieurs mois](/help/plans/build.md) tout en préservant les schémas de dépenses mensuelles. | mercredi 8 juillet 2025 | mercredi 8 juillet 2025 |


## Mai - Juin 2025

| Fonctionnalité | Description | [ Début du déploiement ](#release-strategy) | [Disponibilité générale](#release-strategy) |
|---|---|---|---|
| **Plans basés sur des objectifs** | En regard des budgets, vous pouvez définir un objectif (cible) lorsque vous [créez](/help/plans/build.md) ou [modifiez](/help/plans/insights.md#edit-plan) un plan. Parmi les exemples de mesures cibles figurent le chiffre d’affaires, la conversion, le CPA ou le retour sur investissement. | 18 Juin 2025 | mercredi 8 juillet 2025 |
| **Configuration du modèle de dépense** | Lorsque vous créez un plan, vous avez désormais la possibilité d’utiliser des données [de référence historique](/help/plans/build.md) (comme les données et les informations sur les dépenses marketing antérieures) lors de la définition du modèle de dépenses pour chaque période du budget. | 14 Mai 2025 | 14 Mai 2025 |
| **Configurations de plan avancées** | Vous pouvez définir des [configurations avancées](/help/plans/build.md) pour votre formule, comme le chiffre d’affaires moyen par conversion et les coûts de canal. | 14 Mai 2025 | 14 Mai 2025 |

## Mars - Avril 2025

| Fonctionnalité | Description | [ Début du déploiement ](#release-strategy) | [Disponibilité générale](#release-strategy) |
|---|---|---|---|
| **Détection de dérive du modèle** | Lorsque vous ouvrez un modèle, vous êtes [invité à entraîner à nouveau le modèle lorsque la dérive du modèle est détectée](/help/models/insights.md#model-drift). | 3 Avril 2025 | 7 mai 2025 |
| **Retour marginal du canal dans les informations sur le plan** | Une visualisation [retour marginal sur canal](/help/plans/insights.md#marginal-channel-return) est ajoutée au plan Insights, qui affiche le seuil de rentabilité marginal et le retour marginal sur l’ensemble des canaux ou des canaux sélectionnés. | 3 Avril 2025 | 24 Avril 2025 |


## Janvier - Février 2025

| Fonctionnalité | Description | [ Début du déploiement ](#release-strategy) | [Disponibilité générale](#release-strategy) |
|---|---|---|---|
| **Conditions imbriquées** | Vous pouvez créer des conditions imbriquées à l’aide des opérateurs AND et OR lorsque vous définissez une population de données éligible dans le cadre de la [configuration d’un modèle](/help/models/build.md#configure). | 15 janvier 2025 | 18 Février 2025 |
| **Affichage des rapports** | Vous pouvez afficher un rapport sur un [conversion](/help/harmonize-data/conversions.md#view-report) ou un [point de contact marketing](/help/harmonize-data/marketing-touchpoints.md#view-report) que vous avez défini dans le cadre de l’harmonisation des données. | 15 janvier 2025 | 18 Février 2025 |
| **Supprimer les confirmations** | Vous êtes invité à confirmer la suppression d’un [plan](/help/plans/overview.md#delete-plans) ou d’un [modèle](/help/models/overview.md#delete-models). | 15 janvier 2025 | 18 Février 2025 |
| **Amélioration de l’interface utilisateur des facteurs** | Vous pouvez sélectionner les [facteurs](/help/models/insights.md#factors-beta) à afficher dans les informations sur le modèle. | 15 janvier 2025 | 18 Février 2025 |
| **Gestion des erreurs** | Messages d’erreur conviviaux et amélioration de l’expérience utilisateur pour les scénarios d’erreur dans l’harmonisation des données et les plans. | 18 Février 2025 | 18 Février 2025 |
| **Statut du modèle** | Redéfinition des [états du modèle](/help/models/overview.md#manage-models) tout au long du cycle de vie du modèle. | 18 Février 2025 | 18 Février 2025 |


## Stratégie de publication

[!UICONTROL Mix Modeler] utilise des indicateurs de fonctionnalité (également appelés « bascules ») pour contrôler la visibilité des nouvelles fonctionnalités, ce qui permet de les tester à échelle contrôlée avant la mise à jour complète. Cette stratégie de publication comprend les phases suivantes :

* **Tests limités** : la publication par étapes commence par un test réalisé par les utilisateurs et utilisatrices Adobe internes. Elle est ensuite mise à la disposition d’un petit groupe de comptes clients afin de s’assurer que la fonctionnalité répond aux besoins et aux attentes des clients.

* **Début du déploiement** : le déploiement d’une publication par phases commence par la phase Tests limités. La mise à jour passe ensuite de 0 % à 100 % de disponibilité pour les clients en quelques mois. Le déploiement échelonné se produit au niveau de l’organisation Experience Cloud, de sorte que tous les utilisateurs autorisés d’une organisation bénéficient de la même expérience.
