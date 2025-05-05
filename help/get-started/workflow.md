---
title: Workflow Mix Modeler
description: Comprendre le processus type pour Mix Modeler.
feature: Ingest Data, Plans, Harmonized Data, Models
exl-id: 200ff846-5d78-4b25-a425-bfd558b88c88
source-git-commit: f12eea7454d1c81b347dc4960f5c491d81725f7d
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 1%

---

# Workflow Mix Modeler

Regardez cette vidéo pour une présentation du workflow de l’utilisateur dans Mix Modeler.

>[!VIDEO](https://video.tv.adobe.com/v/3440205/?learn=on&captions=fre_fr)


Un workflow type en Mix Modeler se compose des activités suivantes :

![Texte de remplacement](/help/assets/ApplicationWorkflow.svg)

|  | Activité | Description |
|---|---|---|
| ![Data](/help/assets/icons/Data.svg){width="100"} (Données) | [**Ingérer des données**](../ingest-data/overview.md) | Ingérez des données d’événement à partir d’Experience Platform (par exemple, Adobe Analytics, Web SDK et d’autres sources), des données agrégées provenant de canaux marketing (par exemple, la télévision, les jardins clos, les e-mails, les activités détenues et exploitées), des données de facteurs externes provenant des clients (par exemple, les changements de prix dans le service d’abonnement) et des données de facteurs internes (par exemple, les plans de vacances). |
| ![DataCheck](/help/assets/icons/DataCheck.svg){width="100"} | [**Harmoniser les données**](../harmonize-data/overview.md) | Configurez les règles de mappage et de résolution de conflit pour fusionner les différents jeux de données marketing nécessaires pour mesurer et planifier les performances des campagnes dans Mix Modeler. |
| ![FileConfig](/help/assets/icons/FileGear.svg){width="100"} | [**Créer des modèles**](../models/overview.md) | Créez des instances de modèle avec les points de contact marketing (par exemple, les canaux), les définitions de conversion et les facteurs internes et externes. |
| ![FileData](/help/assets/icons/FileData.svg){width="100"} | [**Former et noter des modèles**](../models/overview.md) | Créez des scores agrégés et au niveau de l’événement à l’aide de la formation et des scores de machine learning. |
| ![FileChart](/help/assets/icons/FileChart.svg){width="100"} | [**Créer des plans**](../plans/overview.md) | Créer des plans. Déterminez la meilleure allocation des fonds marketing pour atteindre un objectif commercial en utilisant les résultats des modèles du Mix Modeler. |
| ![Tableau de bord](/help/assets/icons/Dashboard.svg){width="100"} | [**Tableau de bord de présentation**](../dashboard/overview.md) | Obtenez des informations sur des données, des modèles et des plans harmonisés, à l’aide de diverses visualisations configurables. |

{style="table-layout:auto"}

<!---
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
