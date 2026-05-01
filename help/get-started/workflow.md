---
title: Workflow Mix Modeler
description: Comprenez le processus type pour Mix Modeler.
feature: Ingest Data, Plans, Harmonized Data, Models
exl-id: 200ff846-5d78-4b25-a425-bfd558b88c88
TQID: https://experienceleague.adobe.com/PAKsHAqpIeBVCJGIPS2ZqWw-vVpS9LUpYdJRFKP0ynY
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: e0abf868-dae2-4c1c-83e9-b21799232845
  - id: fbd94e4b-f9b8-42a4-8df5-3f917aabae24
  - id: a567f0f7-0057-4079-8ded-5b24cc25af15
  - id: f40f1683-8300-4054-aab8-77da06ad63ff
  - id: d822825b-9821-40d5-9b0d-42a9e3f317c5
subfeature_v2:
  - id: ad7101f7-ae92-401b-a25a-d3060d42989d
  - id: a4dc3e7d-bd07-4ac8-8e49-ff2e8fecf1e7
  - id: ee1bf083-e090-4def-936b-c111d29f42d0
  - id: d1167c89-f64a-42ca-ac95-1d91b7790df2
  - id: bc2f5225-03d4-4bc8-89ec-99d78c30e6dd
  - id: d4b8ba18-64c1-4413-be54-74405ec7f558
  - id: ba4fd72c-282e-4fb6-abc1-08e6fb87b2ad
  - id: b4655f7e-1a6e-4fa3-a7c5-3c34d4786e49
  - id: b2d4aeb9-eabe-49f6-8edb-bb2862d5980b
  - id: c89e26b6-808d-4500-8b01-450a63466999
  - id: a9505d76-24a1-4ffe-bd01-6ac32d5af453
  - id: cb40363e-1205-4921-971c-9ee6bdb18329
  - id: d7b067e6-4f39-41e9-a081-7650346a84cd
  - id: b2520ae7-8f6c-4952-935e-aacc2c10256f
  - id: e6c284e0-b6e6-4f82-bf96-e96bb5157b90
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
autotag-review: '2026-05-01T09:15:33.908Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 238
ht-degree: 1%

---

# Workflow Mix Modeler

Regardez cette vidéo pour une présentation du workflow de l’utilisateur dans Mix Modeler.

>[!VIDEO](https://video.tv.adobe.com/v/3424854/?learn=on)


Un workflow type dans Mix Modeler se compose des activités suivantes :

![Texte de remplacement](/help/assets/ApplicationWorkflow.svg)

|  | Activité | Description |
|---|---|---|
| ![Data](/help/assets/icons/Data.svg){width="100"} (Données) | [**Ingérer des données**](../ingest-data/overview.md) | Ingérez des données d’événement à partir d’Experience Platform (par exemple, Adobe Analytics, Web SDK et d’autres sources), des données agrégées provenant de canaux marketing (par exemple, la télévision, les jardins clos, les e-mails, les activités détenues et exploitées), des données de facteurs externes provenant des clients (par exemple, les changements de prix dans le service d’abonnement) et des données de facteurs internes (par exemple, les plans de vacances). |
| ![DataCheck](/help/assets/icons/DataCheck.svg){width="100"} | [**Harmoniser les données**](../harmonize-data/overview.md) | Configurez les règles de mappage et de résolution de conflit pour fusionner les différents jeux de données marketing nécessaires pour mesurer et planifier les performances des campagnes dans Mix Modeler. |
| ![FileConfig](/help/assets/icons/FileGear.svg){width="100"} | [**Créer des modèles**](../models/overview.md) | Créez des instances de modèle avec les points de contact marketing (par exemple, les canaux), les définitions de conversion et les facteurs internes et externes. |
| ![FileData](/help/assets/icons/FileData.svg){width="100"} | [**Former et noter des modèles**](../models/overview.md) | Créez des scores agrégés et au niveau de l’événement à l’aide de la formation et des scores de machine learning. |
| ![FileChart](/help/assets/icons/FileChart.svg){width="100"} | [**Créer des plans**](../plans/overview.md) | Créer des plans. Déterminez la meilleure allocation des fonds marketing pour atteindre un objectif commercial en utilisant la sortie des modèles de Mix Modeler. |
| ![Tableau de bord](/help/assets/icons/Dashboard.svg){width="100"} | [**Tableau de bord de présentation**](../dashboard/overview.md) | Obtenez des informations sur des données, des modèles et des plans harmonisés, à l’aide de diverses visualisations configurables. |

{style="table-layout:auto"}

Vous trouverez ci-dessous un aperçu de la manière dont les données d’entrée peuvent circuler dans Mix Modeler et dont Mix Modeler peut produire des données de sortie pour sa propre interface, mais également pour d’autres solutions telles que Customer Journey Analytics.

![Flux de données d’entrée/sortie &#x200B;](../assets/mm-input-output.png)

<!--
The detailed data-oriented flowchart below illustrates how:

* harmonized data is based on:

  * experience event data (originating from Analytics source connector, collected through Experience Platform SDKs and APIs, ingested through source connectors, or using streaming ingestion),
  * aggregate or summary data from walled gardens (like Facebook, YouTube), traffic sources, or offline advertising data, and 
  * definitions of harmonized fields and dataset rules.

* a model is based on:

  * the conversion and marketing touchpoint definitions resulting from the harmonized data and 
  * non-marketing aggregate or summary data containing internal or external factors.

* mult-touch attribution event scores can potentially be fed back into Experience Platform data lake for use in subsequent model configuration, training and scoring.

![Comprehensive workflow](/help/assets/comprehensive-workflow.svg)
-->
