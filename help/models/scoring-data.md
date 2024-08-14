---
title: Données de notation
description: Découvrez comment les données de notation d’un modèle en Mix Modeler sont conservées.
feature: Models
exl-id: 2f2c3d20-7b14-41cc-a11a-03e8ad9e5d7a
source-git-commit: b6045176e82b97f848113f4e0ffbbb995c48b3d4
workflow-type: tm+mt
source-wordcount: '675'
ht-degree: 24%

---

# Données de notation

Dans le cadre de la notation d’un modèle, les données de notation sont conservées dans un jeu de données dans Experience Platform. Lorsque vous avez activé l’attribution multipoint lors de la création du modèle, d’autres données de score d’événement sont conservées dans un jeu de données dans Experience Platform.

Chacun de ces jeux de données est conforme à un schéma. Cet article documente ces schémas.


## Schéma de données de notation agrégée

Le schéma des données de notation est appelé comme `AMM AI Schema - <name of model> <id>`. Par exemple : `AMM AI Schema - Model for Online Conversion 10120`.

Le jeu de données, qui conserve les données de notation d’un modèle, est appelé comme `AMM AI Aggregrate Scores - <id>`, par exemple `AMM AI Aggregrate Scores - 10120`.

Le schéma comprend un groupe de champs avec un objet contenant des détails sur les scores. L’objet se compose des champs suivants.

| Nom du champ | Type | Définition |
|---|---|---|
| `campaignGroup` | Chaîne | Nom du groupe de campagnes. |
| `campaignName` | Chaîne | Nom de la campagne. |
| `contribution` | Double | Contribution attribuée à cette conversion pour le point de contact donné. |
| `conversionEndDate` | Date | Date de fin de la fenêtre de conversion. |
| `conversionName` | Chaîne | Nom de la conversion qui a été créée lors de l’étape de configuration de la définition de conversion. |
| `conversionStartDate` | Date | Date de début de la fenêtre de conversion. |
| `geo` | Chaîne | Emplacement géographique où la conversion s’est produite. |
| `mediaChannel` | Chaîne | Nom du canal utilisé lors de l’étape de configuration du point de contact. |
| `mediaSubChannel` | Chaîne | Nom du sous-canal. |
| `revenue` | Double | Recettes attribuées à cette conversion pour le point de contact donné. |
| `scoreCreatedTime` | DateTime | Horodatage de création de cet enregistrement de score. |
| `touchpointEndDate` | Date | Date de fin de la fenêtre du point de contact. |
| `touchpointName` | Chaîne | Nom du point de contact créé lors de l’étape de configuration de la définition du point de contact. Actuellement, le point de contact est défini sur le canal multimédia. |
| `touchpointStartDate` | Date | Date de début de la fenêtre du point de contact. |


## Schéma de données de notation des événements

Le schéma des données de notation est appelé comme `Attribution AI Scores - <name of model> <id> - Schema`. Par exemple : `Attribution AI Scores - Model for Online Conversion 10120 - Schema`.

Le jeu de données, qui conserve les données de notation d’un modèle, est appelé comme `Attribution AI Scores - <name of model> <id>`, par exemple `Attribution AI Scores - Model for Online Conversion 10120 `.

Le schéma comprend un groupe de champs contenant un objet contenant des détails sur les noyaux. L’objet est nommé comme `attibution_AI_scores__<name of model> id`.

Le groupe de champs contient les champs suivants.

| Nom du champ | Type | Description |
|---|---|---|
| `conversion` | Objet | Colonnes de métadonnées de conversion. |
|     `passThrough` | Objet |  |
|         `eventType` | Chaîne | |
|         `channel_typeAtSource` | Chaîne | |
|      `dataSource` | Chaîne | Identification globale unique d’une source de données. <br> **Exemple :** `Adobe Analytics` |
|      `eventSource` | Chaîne | Source de l’événement réel. <br> **Exemple :** `Adobe.com` |
|      `eventType` | Chaîne | Type d’événement principal pour cet enregistrement de série temporelle. <br> **Exemple :** `Order` |
|      `geo` | Chaîne | Emplacement géographique où la conversion a été effectuée `placeContext.geo.countryCode`. <br> **Exemple :** `US` |
|      `path` | Chaîne | |
|      `priceTotal` | Double | Recettes obtenues par le biais de la conversion <br> **Exemple :** `99.9` |
|      `product` | Chaîne | Identifiant XDM du produit lui-même. <br> **Exemple :** `RX 1080 ti` |
|      `productType` | Chaîne | Nom d’affichage du produit tel qu’il est présenté à l’utilisateur pour cette consultation de produit. <br> **Exemple :** `Gpus` |
|      `quantity` | Nombre entier | Quantité achetée lors de la conversion. <br> **Exemple :** `1` |
|      `receivedTimeStamp` | DateTime | Date et heure de réception de la conversion. <br> **Exemple :** `2020-06-09T00:01:51.000Z` |
|      `skuId` | Chaîne | Unité de gestion des stocks (SKU), l’identifiant unique d’un produit défini par le fournisseur. <br> **Exemple :** `MJ-03-XS-Black` |
|      `timestamp` | DateTime | Horodatage de la conversion. <br> **Exemple :** `2020-06-09T00:01:51.000Z` |
|      `totalDaysToConversion` | Nombre entier |  |
|      `totalTouchpointCount` | Nombre entier | |
| `customerProfile` | Objet | Détails d’identité de l’utilisateur utilisé pour créer le modèle. |
|      `identity` | Objet | |
|           `id` | Chaîne | |
|           `namespace` | Chaîne | Contient les détails de l’utilisateur utilisé pour créer le modèle, tels que `id` et `namespace`. |
| `touchpointsDetail` | Objet[] | Liste des détails du point de contact menant à la conversion, triée par occurrence du point de contact ou horodatage. |
|      `scores` | Objet | Contribution des points de contact à cette conversion en tant que score. |
|           `algorithmicInfluenced` | Double | Le score influencé représente la fraction de la conversion dont chaque point de contact marketing est à l’origine. |
|           `algorithmicSourced` | Double | Le score incrémentiel représente le degré d’impact marginal directement causé par un point de contact marketing. |
|           `decayUnits` | Double | Score d’attribution basé sur des règles qui attribue plus de crédits aux points de contact les plus proches de la conversion par rapport aux points de contact plus éloignés dans le temps de la conversion. |
|           `firstTouch` | Double | Score d’attribution basé sur des règles qui attribue tous les crédits au point de contact initial d’un chemin de conversion. |
|           `lastTouch` | Double | Score d’attribution basé sur des règles qui attribue tous les crédits au point de contact le plus proche de la conversion. |
|           `linear` | Double | Score d’attribution basé sur des règles qui répartit de manière égale les crédits entre chaque point de contact d’un chemin de conversion. |
|           `uShape` | Double | Score d’attribution basé sur des règles qui attribue 40 % du crédit au premier point de contact et 40 % du crédit au dernier point de contact. Les autres points de contact divisent les 20 % restants à parts égales. |
|      `touchPoint` | Objet | Métadonnées de point de contact. |
|           `passThrough` | Objet | |
|                `eventType` | Chaîne | |
|           `campaignGroup` | Chaîne |  |
|           `campaignName` | Chaîne | |
|           `campaignTag` | Chaîne | |
|           `eventId` | Chaîne | |
|           `geo` | Chaîne | |
|           `mediaAction` | Chaîne | |
|           `mediaChannel` | Chaîne | |
|           `receivedTimeStamp` | DateTime | |
|           `timestamp` | DateTime | |
|      `isFirstInThePosition` | Nombre entier | |
|      `lag` | Nombre entier | |
|      `position` | Chaîne | |
|      `touchpointCountToConversion` | Nombre entier | |
|      `touchpointName` | Chaîne | Nom du point de contact configuré lors de la configuration. <br> **Exemple :** `PAID_SEARCH_CLICK` |
| `conversionName` | Chaîne | Nom de la conversion qui a été configurée lors de la configuration. <br> **Exemple :** `Order`, `Lead`, `Visit` |
| `scoreCreatedTime` | DateTime | |
| `segmentation` | Chaîne | Segment de conversion, tel que la géosegmentation, par rapport auquel le modèle est créé. Lorsque des segments sont absents, `segmentation` est identique à `conversionName`. <br> **Exemple :** `ORDER_US` |





Voir [Schémas](../ingest-data/schemas.md) pour plus d’informations.
