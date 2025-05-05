---
title: Politiques
description: Découvrez comment accéder aux stratégies à partir de Mix Modeler.
feature: Administration
exl-id: 4dba7c30-ad1e-4213-a2b0-afc55f2448a3
source-git-commit: 132dc18b84723358a7d65e2aaadd49cf1deb2dd8
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 11%

---

# Politiques

Une fois que vous avez parcouru le workflow pour créer un modèle et envoyer la configuration du modèle, [l’application de la stratégie](https://experienceleague.adobe.com/fr/docs/experience-platform/data-governance/enforcement/overview#automatic-enforcement) vérifie s’il existe des violations. Si une violation de politique se produit, une fenêtre contextuelle s’affiche indiquant qu’une ou plusieurs politiques ont été violées. Cette vérification permet de s’assurer que vos opérations de données et vos actions marketing dans Experience Platform sont conformes aux stratégies d’utilisation des données.

Par défaut, Mix Modeler recherche les violations des stratégies définies par l’Adobe associées aux libellés et actions marketing suivants :

| Nom de la stratégie | Libellé associé | Action marketing associée |
|---|---|---|
| Limitation des analyses d’utilisation et des mesures basées sur les utilisateurs | C8 | Analytics |
| Limitation de la science des données | C9 | Science des données |
| Limitation de l’exportation des données | C12 | Exportation de données |

Les violations sont également vérifiées pour les stratégies que vous avez définies vous-même et qui contiennent toutes les actions marketing répertoriées dans le tableau ci-dessus.

Lors de la violation d’une stratégie lors de la création d’une règle de jeu de données, une fenêtre contextuelle affiche des informations sur la violation de la stratégie.

Par exemple :

- vous avez activé la stratégie [!UICONTROL Restrict data science] avec le libellé associé [!UICONTROL C9] et l’action marketing associée [!UICONTROL Data Science],
- vous avez appliqué le libellé [!UICONTROL C9] - [!UICONTROL No data science] au champ `totalCost` de votre schéma de données de conversion,
- vous souhaitez configurer une règle de jeu de données qui, entre autres, mappe le champ `totalCost` du schéma de données de conversion au champ harmonisé avec le nom `spend` (et le nom d’affichage `Spend`).

Lorsque vous souhaitez enregistrer la règle du jeu de données, une fenêtre contextuelle **[!UICONTROL Data governance policy violation detected]** s’affiche, affichant une liste de stratégies violées. Lorsque vous sélectionnez le nom de la stratégie, dans le [!UICONTROL Violation summary], une liste de [!UICONTROL Active data governance labels] contenant [!UICONTROL Entity], [!UICONTROL Type], [!UICONTROL Field] et [!UICONTROL Government labels] est appliquée.

<!-- pending screenshot -->

Lorsque vous appliquez un libellé d’utilisation des données à un champ de schéma déjà utilisé dans les données harmonisées, une fenêtre contextuelle affiche des informations sur la violation de la politique.

Par exemple :

- vous avez configuré une règle de jeu de données qui, entre autres, mappe le champ `totalCost` de votre schéma de données de conversion vers le champ harmonisé avec le nom `spend` (et le nom d’affichage `Spend`).
- vous avez synchronisé les données harmonisées avec succès au moins une fois (voir [Règles du jeu de données - Synchroniser les données](/help/harmonize-data/dataset-rules.md#sync-data)).
- vous activez la stratégie [!UICONTROL Restrict data science] avec le libellé associé [!UICONTROL C9] et l&#39;action marketing associée [!UICONTROL Data Science],
- vous souhaitez appliquer l’étiquette [!UICONTROL C9] - [!UICONTROL No data science] au champ `totalCost` de votre schéma de données de conversion.

Lorsque vous souhaitez enregistrer la mise à jour de votre schéma, une fenêtre contextuelle **[!UICONTROL Data governance policy violation detected]** s’affiche, affichant une liste de stratégies violées. Sélectionnez le nom de la stratégie dans [!UICONTROL Violation summary] pour trouver plus de détails dans la liste [!UICONTROL Data Lineage].

<!-- pending screenshot -->

## Violation des variables contextuelles détectées

La violation de la politique de gouvernance des données détectée fournit des informations spécifiques sur la violation. Vous pouvez résoudre ces violations par le biais des paramètres de la politique et d’autres mesures qui ne sont pas directement liées au workflow de configuration. Par exemple, vous pouvez modifier les étiquettes afin que certains champs soient autorisés à utiliser à des fins de science des données. Vous pouvez également modifier la configuration du modèle lui-même, de sorte que le modèle n’utilise pas d’objet avec un libellé d’utilisation des données.

La sélection ![ ](/help/assets/icons/Privacy.svg) **[!UICONTROL Policies]** dans le rail de gauche permet d’accéder à l’interface [!UICONTROL Policies] de l’Experience Platform, ce qui vous permet de gérer vos stratégies, vos étiquettes et vos actions marketing.

<!--
Currently,  Mix Modeler does not support all of the data governance functionality offered by Experience Platform. Field level access control is supported. See [Field level access control](../harmonize-data/dataset-rules.md#field-level-access-control)
-->

>[!MORELIKETHIS]
>
>[Présentation des politiques d’utilisation des données](https://experienceleague.adobe.com/fr/docs/experience-platform/data-governance/policies/overview)
>
>

