---
title: Administration
description: Découvrez comment administrer Mix Modeler.
feature: Administration
exl-id: 76d6d15d-a838-4ee2-9929-e55ea8946b80
TQID: https://experienceleague.adobe.com/0MxMv6Due-i9-8JxKTb3vk2NDZ5mc6Pj4yEe-liCszg
autotag-review: '2026-05-01T09:07:55.299Z'
product_v2: id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2: id: fe2edbb1-46f9-4347-a27c-577cab3640cb
subfeature_v2: id: abe9e290-7d2f-4131-b71e-ef9900865044id: a6da0571-746e-4d59-89a4-7b691b1c3b9a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b23e006f-0a29-4f1d-8fd0-77aa56f3d12bid: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 194
ht-degree: 7%

---

# Administration

Utilisez [](https://helpx.adobe.com/fr/enterprise/using/admin-console.html) pour gérer les produits et les utilisateurs Mix Modeler.

Pour que Mix Modeler fonctionne correctement, vous devez définir les autorisations appropriées.

Dans l’interface utilisateur de Adobe Experience Cloud :

1. Sélectionnez **[!UICONTROL Permissions]** dans le rail de gauche, sous **[!UICONTROL ADMINISTRATION]**.

1. Sélectionnez ![Utilisateur](/help/assets/icons/User.svg) **[!UICONTROL Roles]** dans le panneau de gauche.

1. Sélectionnez un rôle existant ou créez un rôle à l’aide de **[!UICONTROL Create role]** (par exemple, **Mix Modeler**). Si vous sélectionnez un rôle existant, sélectionnez ![Modifier](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** pour modifier les autorisations du rôle. Voir [Gérer les rôles](https://helpx.adobe.com/fr/enterprise/using/admin-console.html) pour plus d’informations.

1. Assurez-vous d’avoir sélectionné un ou plusieurs sandbox pour le rôle.

1. Ajoutez la ressource **** à la liste des ressources pour le rôle.

1. Veillez à sélectionner les autorisations **[!UICONTROL Adobe Mix Modeler]** appropriées pour le rôle que vous êtes en train de configurer. Vous pouvez sélectionner un ou plusieurs des rôles suivants :

   - **[!UICONTROL View Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL Manage Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL View Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL View Adobe Mix Modeler Plans Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Plans Configuration]**

     ![RBAC ](/help/assets/mix-modeler-rbac.png)


1. Veillez à sélectionner des autorisations supplémentaires pour le rôle. Par exemple, pour afficher ou gérer des jeux de données et des schémas, vous devez sélectionner :

   - **[!UICONTROL Data Management]** : sélectionnez les options appropriées : **[!UICONTROL View Datasets]** ou **[!UICONTROL Manage Datasets]**.

   - **[!UICONTROL Data Modeling]** : sélectionnez les options appropriées : **[!UICONTROL Manage Schemas]** ou **[!UICONTROL View Schemas]**.

   <!--
    * **[!UICONTROL Data Governance]**: ensure you select **[!UICONTROL View User Activity Log]** and **[!UICONTROL View Data Usage Policies]**.
    -->

   <!--![Permissions](assets/permissions-including-privacy.png)-->

   Sélectionnez **[!UICONTROL Save]** pour enregistrer les autorisations.

1. Dans **[!UICONTROL Details]** sous **[!UICONTROL Role]**, ajoutez les **[!UICONTROL Users]** ou **[!UICONTROL User groups]** appropriés pour permettre aux utilisateurs d’accéder à Mix Modeler.
