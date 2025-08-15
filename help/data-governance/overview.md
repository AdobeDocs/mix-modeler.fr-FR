---
title: Présentation de la gouvernance des données
description: Découvrez comment utiliser les services et outils d’Experience Platform qui vous permettent de contrôler les données d’expérience collectées. Ainsi, vous respectez vos pratiques commerciales, vos obligations légales et votre processus de développement.
feature: Administration
exl-id: 87407c29-e158-48bf-bde9-b3c16a16107e
source-git-commit: bdde574b150bda2b0c82a9f5a20160fed26cb69d
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 10%

---

# Présentation de la gouvernance des données

L’intégration entre Mix Modeler et Experience Platform permet à Mix Modeler d’exploiter les fonctionnalités intrinsèques de gouvernance des données d’Experience Platform. Cette section de la documentation détaille les détails des fonctionnalités de gouvernance des données disponibles dans Mix Modeler.

La gouvernance des données d’Experience Platform vous permet de contrôler et de comprendre vos données dans l’ensemble du parcours que les données empruntent via Experience Platform. Ce parcours implique le maintien de la qualité des données, de la traçabilité des données, du catalogage des données, etc.

Les libellés et politiques d’utilisation des données créés sur les jeux de données consommés par Experience Platform apparaissent dans Mix Modeler, le cas échéant. Par exemple, ces libellés arrêtent ou avertissent les utilisateurs lors de la suppression de jeux de données qui font partie d’une règle de jeu de données dans les données harmonisées. Vous pouvez également masquer les champs de schéma qui sont restreints pour les utilisateurs lors de la création d’une règle de jeu de données.

L’intégration de la gouvernance des données vous permet de gérer la conformité plus efficacement. Les gestionnaires de données de votre entreprise peuvent définir des politiques pour restreindre l’utilisation. Par conséquent, vous pouvez utiliser des données conformes aux stratégies définies par les gestionnaires de données. Lisez la documentation sur les [Libellés et stratégies](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-dataviews/data-governance) pour en savoir plus.

Les fonctionnalités de gouvernance des données suivantes sont disponibles :

| Fonctionnalité | Détails |
|---|---|
| Contrôles d’accès | Le contrôle d’accès basé sur les rôles et le contrôle d’accès basé sur les attributs (au niveau du champ) sont pris en charge. Voir [Contrôles d’accès](access-controls.md) pour plus d’informations. |
| Journaux d’audit | Lorsque les utilisateurs créent, mettent à jour ou suppriment des catégories Mix Modeler spécifiques, la fonctionnalité d’audit Experience Platform enregistre l’activité dans les journaux d’audit. Voir [Journaux d’audit](audit-logs.md) pour plus d’informations. |
| Politiques | Dans le cadre du workflow de données harmonisées, les politiques définies par Experience Platform sont appliquées. Toute violation des libellés d’utilisation des données est signalée et affichée à l’utilisateur. Pour plus d’informations, consultez la section [Politiques](policies.md). |
| Chiffrement | Tous les jeux de données utilisés pour l’entrée et la sortie des modèles suivent les directives d’Experience Platform. Le chiffrement des données d’Experience Platform s’applique aux données au repos et en transit. |
| Hygiène des données | Tous les jeux de données utilisés pour les modèles d’entrée et de sortie suivent les directives d’Experience Platform. Experience Platform fournit un ensemble d’outils pour gérer le cycle de vie des données client, notamment la prise en charge de différents types d’expiration des données. Lorsque vous supprimez un jeu de données source d’Experience Platform, qui est utilisé dans le cadre de vos données harmonisées, vous en êtes informé. Voir [Règles du jeu de données](/help/harmonize-data/dataset-rules.md) pour plus d’informations. |
| Clés gérées par le client | Lorsque vous disposez d’une licence Mix Modeler avec le module complémentaire Privacy Security Shield, vous pouvez utiliser la fonctionnalité Clés gérées par le client pour tirer parti du coffre de clés Azure Key Vault afin d’apporter vos propres clés via les API. Vous disposez d’une gestion complète des données traitées dans les modèles de Mix Modeler. |
