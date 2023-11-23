---
title: Données de notation
description: Découvrez comment les données de notation d’un modèle en Mix Modeler sont conservées.
feature: Models
source-git-commit: 3596b83937b3f61ac453940f3a666d8aaf713679
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 10%

---


# Données de notation

Dans le cadre de la notation d’un modèle, les données de notation sont conservées dans un jeu de données dans Experience Platform. Ce jeu de données est conforme à un schéma créé pour chaque modèle dans votre instance de Mix Modeler.

Le schéma des données de notation est nommé comme `AMM AI Schema - <name of model> <id>`. Par exemple: `AMM AI Schema - Model for Online Conversion 10120`.

Le jeu de données, qui conserve les données de notation d’un modèle, est nommé comme `AMM AI Aggregrate Scores - <id>`, par exemple `AMM AI Aggregrate Scores - 10120`.


## Schéma

Le schéma comprend un groupe de champs avec un objet contenant des détails sur les scores. L’objet se compose des champs suivants.

| Nom du champ | Type | Définition |
|---|---|---|
| **campaignGroup** | Chaîne | Nom du groupe de campagnes. |
| **campaignName** | Chaîne | Nom de la campagne. |
| **contribution** | Double | Contribution attribuée à cette conversion pour le point de contact donné. |
| **conversionEndDate** | Date | Date de fin de la fenêtre de conversion. |
| **conversionName** | Chaîne | Nom de la conversion qui a été créée lors de l’étape de configuration de la définition de conversion. |
| **conversionStartDate** | Date | Date de début de la fenêtre de conversion. |
| **geo** | Chaîne | Emplacement géographique où la conversion s’est produite. |
| **mediaChannel** | Chaîne | Nom du canal utilisé lors de l’étape de configuration du point de contact. |
| **mediaSubChannel** | Chaîne | Nom du sous-canal. |
| **chiffre d’affaires** | Double | Recettes attribuées à cette conversion pour le point de contact donné. |
| **scoreCreatedTime** | DateTime | Heure à laquelle cet enregistrement de score est créé. |
| **touchpointEndDate** | Date | Date de fin de la fenêtre du point de contact. |
| **touchpointName** | Chaîne | Nom du point de contact créé lors de l’étape de configuration de la définition du point de contact. Actuellement, le point de contact est défini sur le canal multimédia. |
| **touchpointStartDate** | Date | Date de début de la fenêtre du point de contact. |

