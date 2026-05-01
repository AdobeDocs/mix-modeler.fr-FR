---
title: Politiques
description: Découvrez comment accéder aux politiques depuis Mix Modeler.
feature: Administration
exl-id: 4dba7c30-ad1e-4213-a2b0-afc55f2448a3
TQID: https://experienceleague.adobe.com/fk6qAZS7Uymx2dzptcazBieXIJ3mGF2pjG-EDhm-Kh4
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: f6633d1c-3d2d-4f48-95d4-4bbc9913db52
subfeature_v2:
  - id: fd80ec6b-9b9e-448a-a6d0-b0c9a15da6b8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
autotag-review: '2026-05-01T09:17:02.907Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 507
ht-degree: 9%

---

# Politiques

Une fois que vous avez parcouru le workflow pour créer un modèle et envoyé la configuration du modèle, [application des politiques](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/enforcement/overview#automatic-enforcement) vérifie s’il existe des violations. Si une violation de politique se produit, une fenêtre contextuelle s’affiche indiquant qu’une ou plusieurs politiques ont été violées. Ce contrôle permet de s’assurer que vos opérations de données et vos actions marketing dans Experience Platform sont conformes aux politiques d’utilisation des données.

Par défaut, Mix Modeler vérifie les violations des politiques définies par Adobe associées aux libellés et aux actions marketing suivants :

| Nom de la stratégie | Libellé associé | Action marketing associée |
|---|---|---|
| Limiter l’analyse de l’utilisation et la mesure basée sur l’utilisateur | C8 | Analytics |
| Limitation de la science des données | C9 | Science des données |
| Limiter l’exportation des données | C12 | Exportation de données |

Les violations sont également vérifiées pour les politiques que vous avez définies vous-même et qui contiennent des actions marketing répertoriées dans le tableau ci-dessus.

Lors de la violation d’une politique lors de la création d’une règle de jeu de données, une fenêtre contextuelle qui affiche des informations sur la violation de la politique s’affiche.

Par exemple :

- vous avez activé la politique de [!UICONTROL Restrict data science] avec les [!UICONTROL C9] de libellé associés et les [!UICONTROL Data Science] d’action marketing associés,
- vous avez appliqué le libellé [!UICONTROL C9] - [!UICONTROL No data science] au champ `totalCost` dans votre schéma de données de conversion,
- vous souhaitez configurer une règle de jeu de données qui, entre autres, mappe le champ `totalCost` du schéma de données de conversion au champ harmonisé avec le nom `spend` (et le nom d’affichage `Spend`).

Lorsque vous souhaitez enregistrer la règle du jeu de données, une fenêtre contextuelle **[!UICONTROL Data governance policy violation detected]** s’affiche, affichant une liste des politiques enfreintes. Lorsque vous sélectionnez le nom de la politique, dans la [!UICONTROL Violation summary], vous voyez une liste des [!UICONTROL Active data governance labels], contenant les [!UICONTROL Entity], [!UICONTROL Type], [!UICONTROL Field] et [!UICONTROL Government labels] appliqués.

<!-- pending screenshot -->

Lors de l’application d’un libellé d’utilisation des données à un champ de schéma déjà utilisé dans les données harmonisées, une fenêtre contextuelle qui affiche des informations sur la violation de la politique s’affiche.

Par exemple :

- vous avez configuré une règle de jeu de données qui, entre autres, mappe le champ `totalCost` de votre schéma de données de conversion au champ harmonisé avec le nom `spend` (et le nom d’affichage `Spend`).
- vous avez synchronisé les données harmonisées au moins une fois (voir [Règles du jeu de données - Synchroniser les données](/help/harmonize-data/dataset-rules.md#sync-data)).
- vous activez la politique de [!UICONTROL Restrict data science] avec les [!UICONTROL C9] de libellé associées et les [!UICONTROL Data Science] d’action marketing associées,
- vous souhaitez appliquer le libellé [!UICONTROL C9] - [!UICONTROL No data science] au champ `totalCost` dans votre schéma de données de conversion.

Lorsque vous souhaitez enregistrer la mise à jour de votre schéma, une fenêtre contextuelle **[!UICONTROL Data governance policy violation detected]** s’affiche, affichant une liste des politiques enfreintes. Sélectionnez le nom de la politique dans la [!UICONTROL Violation summary] pour obtenir plus de détails dans la liste [!UICONTROL Data Lineage].

<!-- pending screenshot -->

## Fenêtres contextuelles de violation détectée

Les fenêtres contextuelles détectées de violation de la politique de gouvernance des données fournissent des informations spécifiques sur la violation. Vous pouvez résoudre ces violations par le biais des paramètres de la politique et d’autres mesures qui ne sont pas directement liées au workflow de configuration. Par exemple, vous pouvez modifier les libellés afin que certains champs soient autorisés à être utilisés à des fins de science des données. Vous pouvez également modifier la configuration du modèle elle-même, de sorte que le modèle n’utilise pas d’objet avec un libellé d’utilisation des données.

La sélection de l’**[!UICONTROL Policies]** ![Confidentialité](/help/assets/icons/Privacy.svg) dans le rail de gauche permet d’accéder à l’interface [!UICONTROL Policies] d’Experience Platform et de gérer vos politiques, libellés et actions marketing.

<!--
Currently,  Mix Modeler does not support all of the data governance functionality offered by Experience Platform. Field level access control is supported. See [Field level access control](../harmonize-data/dataset-rules.md#field-level-access-control)
-->

>[!MORELIKETHIS]
>
>[Présentation des politiques d’utilisation des données](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/policies/overview)
>
>

