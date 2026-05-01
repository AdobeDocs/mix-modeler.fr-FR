---
title: Contrôles d’accès
description: Découvrez comment configurer les contrôles d’accès dans Mix Modeler.
feature: Administration
exl-id: c9ec97d9-b9a2-41f5-8626-1cf967d5d7fe
TQID: https://experienceleague.adobe.com/EoiF5ui2Bqq0Oxuv-s5E5pQclj9gnjoKgZ1bOzRK-vY
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: fe2edbb1-46f9-4347-a27c-577cab3640cb
subfeature_v2:
  - id: abe9e290-7d2f-4131-b71e-ef9900865044
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
autotag-review: '2026-05-01T09:20:37.287Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 412
ht-degree: 25%

---

# Contrôles d’accès

Le contrôle d’accès pour Mix Modeler est fourni via Experience Platform dans le Adobe Admin Console [&#128279;](https://adminconsole.adobe.com/) et via [Autorisations](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#platform-permissions) dans Experience Platform. Cette fonctionnalité exploite les profils de produit dans Admin Console, liant les utilisateurs à des autorisations et des sandbox.

Pour plus d’informations sur le contrôle d’accès, voir [Présentation du contrôle d’accès](https://experienceleague.adobe.com/fr/docs/experience-platform/access-control/home).

## Contrôle d’accès en fonction du rôle

Voir [Administration](../main-guide/administration.md) pour savoir comment configurer les autorisations d’accès en fonction du rôle pour les utilisateurs et les groupes d’utilisateurs de Mix Modeler dans Experience Platform.

## Contrôle d’accès basé sur les attributs

Le [contrôle d’accès basé sur les attributs](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) est une fonctionnalité d’Experience Platform qui permet aux administrateurs de contrôler l’accès à des objets et/ou fonctionnalités spécifiques en fonction d’attributs. Les attributs peuvent être des métadonnées ajoutées à un objet, comme un libellé ajouté à un champ ou à un segment de schéma. Un administrateur définit des politiques d’accès qui comprennent des attributs afin de gérer les autorisations d’accès des utilisateurs.

Cette fonctionnalité vous permet d’étiqueter les champs de schéma d’un modèle de données d’expérience (XDM) avec des libellés définissant l’utilisation de l’organisation ou des données. En parallèle, les administrateurs peuvent utiliser l’interface d’administration des utilisateurs et des rôles pour définir des politiques d’accès sur les champs de schéma XDM. et de mieux gérer l’accès accordé aux utilisateurs ou groupes d’utilisateurs (utilisateurs internes, externes ou tiers). Enfin, le contrôle d’accès basé sur les attributs permet aux administrateurs de gérer l’accès à des segments spécifiques.

Grâce au contrôle d’accès basé sur les attributs, les administrateurs peuvent contrôler l’accès des utilisateurs aux données personnelles sensibles (SPD) et aux informations d’identification personnelle (PII) sur l’ensemble des workflows et ressources de Platform. Les administrateurs et administratrices peuvent définir des rôles d’utilisation qui n’ont accès qu’à des champs spécifiques et aux données correspondant à ces champs.

Lors de la configuration de règles de jeux de données pour les jeux de données harmonisés, Experience Platform [contrôle d’accès basé sur les attributs](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) est appliqué au niveau du champ. Un champ est limité lorsqu’un libellé est associé à un champ de schéma. Une politique active est activée qui refuse l’accès à ce champ pour vous. Par conséquent :

* vous ne voyez pas les champs de schéma qui sont restreints pour vous lorsque vous créez une règle de jeu de données ;
* vous ne pouvez pas afficher ni modifier le mappage d’un ou de plusieurs champs de schéma qui sont restreints pour vous. Lorsque vous modifiez ou affichez une règle de jeu de données contenant de tels champs restreints, l’écran suivant s’affiche.
  ![Action non autorisée](/help/assets/action-not-permitted.png)
