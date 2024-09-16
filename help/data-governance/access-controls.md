---
title: Contrôles d’accès
description: Découvrez comment configurer les contrôles d’accès dans Mix Modeler.
feature: Administration
exl-id: c9ec97d9-b9a2-41f5-8626-1cf967d5d7fe
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 32%

---

# Contrôles d’accès

Le contrôle d’accès du Mix Modeler est fourni via Experience Platform dans [Adobe Admin Console](https://adminconsole.adobe.com/) et par [Permissions](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#platform-permissions) dans Experience Platform. Cette fonctionnalité exploite les profils de produit dans l’Admin Console, qui lient les utilisateurs à des autorisations et des environnements de test.

Pour plus d’informations sur le contrôle d’accès, consultez la [présentation du contrôle d’accès](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home).

## Contrôle d’accès en fonction du rôle

Voir [Administration](../main-guide/administration.md) sur la configuration des autorisations d’accès en fonction du rôle pour les utilisateurs et les groupes d’utilisateurs Mix Modeler dans Experience Platform.

## Contrôle d’accès basé sur les attributs

[Le contrôle d’accès basé sur les attributs](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) est une fonctionnalité d’Experience Platform qui permet aux administrateurs de contrôler l’accès à des objets et/ou fonctionnalités spécifiques en fonction d’attributs. Les attributs peuvent être des métadonnées ajoutées à un objet, comme un libellé ajouté à un champ ou à un segment de schéma. Un administrateur définit des politiques d’accès qui comprennent des attributs afin de gérer les autorisations d’accès des utilisateurs.

Cette fonctionnalité vous permet d’étiqueter les champs de schéma d’un modèle de données d’expérience (XDM) avec des libellés définissant l’utilisation de l’organisation ou des données. En parallèle, les administrateurs peuvent utiliser l’interface d’administration des utilisateurs et des rôles pour définir des stratégies d’accès sur les champs de schéma XDM. Et mieux gérer l’accès attribué aux utilisateurs ou groupes d’utilisateurs (utilisateurs internes, externes ou tiers). Enfin, le contrôle d’accès basé sur les attributs permet aux administrateurs de gérer l’accès à des segments spécifiques.

Grâce au contrôle d’accès basé sur les attributs, les administrateurs et administratrices de votre organisation peuvent contrôler l’accès des utilisateurs et utilisatrices aux données personnelles sensibles (SPD) et aux informations d’identification personnelle (PII) sur l’ensemble des workflows et ressources de Platform. Les administrateurs et administratrices peuvent définir des rôles d’utilisation qui n’ont accès qu’à des champs spécifiques et aux données correspondant à ces champs.

Lors de la configuration des règles de jeu de données pour les jeux de données harmonisés, le [contrôle d’accès basé sur les attributs](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) de l’Experience Platform est appliqué au niveau du champ. Un champ est restreint lorsqu’un libellé est associé à un champ de schéma. Une stratégie active est activée, qui vous refuse l’accès à ce champ. Par conséquent :

* vous ne voyez pas les champs de schéma qui sont limités pour vous lorsque vous créez une règle de jeu de données,
* vous ne pouvez pas afficher ni modifier le mappage d’un ou de plusieurs champs de schéma limités pour vous. Lorsque vous modifiez ou affichez une règle de jeu de données contenant ces champs restreints, l’écran suivant s’affiche.
  ![Action non autorisée](/help/assets/action-not-permitted.png)
