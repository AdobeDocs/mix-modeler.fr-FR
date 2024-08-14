---
title: Gouvernance des données
description: Découvrez comment utiliser les services et outils d’Experience Platform qui vous permettent de contrôler les données d’expérience collectées. Vous vous conformez donc à vos pratiques commerciales, obligations légales et processus de développement.
feature: Administration
source-git-commit: 6776a91563f120db1341adef923aab4b0f582c9d
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 11%

---

# Gouvernance des données

L’intégration entre Mix Modeler et Experience Platform offre aux Mix Modeler les fonctionnalités nécessaires pour tirer parti des fonctionnalités de gouvernance des données intrinsèques d’Experience Platform. Cette section de la documentation présente les spécificités des fonctionnalités de gouvernance des données disponibles dans Mix Modeler.

La gouvernance des données Experience Platform vous permet de contrôler et de comprendre vos données tout au long du parcours que les données transitent par l’Experience Platform. Ce parcours implique le maintien de la qualité des données, de la liaison des données, du catalogage des données, etc.

Libellés et stratégies d’utilisation des données créés sur les jeux de données consommés par la surface Experience Platform dans le Mix Modeler, le cas échéant. Par exemple, ces étiquettes arrêtent ou avertissent les utilisateurs lors de la suppression de jeux de données qui font partie d’une règle de jeu de données dans les données harmonisées. Vous pouvez également masquer les champs de schéma limités pour les utilisateurs lors de la création d’une règle de jeu de données.

L’intégration de la gouvernance des données vous permet de gérer la conformité plus efficacement. Les gestionnaires de données de votre entreprise peuvent définir des politiques pour restreindre l’utilisation. Par conséquent, vous pouvez utiliser des données conformes aux stratégies définies par les gestionnaires de données. Lisez la documentation sur les [Libellés et stratégies](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/data-governance) pour en savoir plus.

Les fonctionnalités de gouvernance des données suivantes sont disponibles :

| Fonctionnalité | Détails |
|---|---|
| Contrôles d’accès | Le contrôle d’accès en fonction du rôle et le contrôle d’accès basé sur les attributs (niveau champ) sont pris en charge. Voir [Contrôles d’accès](access-controls.md) pour plus d’informations. |
| Journaux d’audit | Lorsque les utilisateurs créent, mettent à jour ou suppriment des catégories de Mix Modeler spécifiques, la fonctionnalité d’audit des Experience Platform enregistre l’activité dans les journaux d’audit. Voir [Journaux d’audit](audit-logs.md) pour plus d’informations. |
| Politiques | Dans le cadre du processus de données harmonisé, des stratégies définies par l’Experience Platform sont appliquées. Toute violation des libellés d’utilisation des données est signalée et affichée pour l’utilisateur. Voir [Stratégies](policies.md) pour plus d’informations. |
| Chiffrement | Tous les jeux de données utilisés pour l’entrée et la sortie des modèles suivent les instructions Experience Platform. Le cryptage des données Experience Platform s’applique aux données au repos et en transit. |
| Hygiène des données | Tous les jeux de données utilisés pour l’entrée et la sortie des modèles suivent les instructions Experience Platform. Experience Platform fournit un ensemble d’outils pour gérer le cycle de vie des données client, y compris la prise en charge de différents types d’expiration des données. Lorsque vous supprimez un jeu de données source d’Experience Platform, utilisé dans le cadre de vos données harmonisées, vous en êtes informé. Pour plus d’informations, voir [Règles du jeu de données](/help/harmonize-data/dataset-rules.md) . |
| Clés gérées par le client | Lorsque vous possédez un Mix Modeler sous licence avec le module complémentaire Privacy Security Shield ou Healthcare Shield, vous pouvez utiliser la fonctionnalité Customer Managed Keys pour exploiter Azure Key Vault afin d’apporter vos propres clés via des API. Vous avez une gestion complète des données traitées dans les modèles en Mix Modeler. |
