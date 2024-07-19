---
title: Administration
description: Découvrez comment administrer le Mix Modeler.
feature: Administration
exl-id: 76d6d15d-a838-4ee2-9929-e55ea8946b80
source-git-commit: 4d84c93121fc476cc6610ad572bab161bbacfc23
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---

# Administration

Utilisez [Adobe Admin Console](https://helpx.adobe.com/fr/enterprise/using/admin-console.html) pour gérer les utilisateurs et les produits Mix Modeler.

Pour que Mix Modeler fonctionne correctement, vous devez définir les autorisations appropriées.

Dans l’interface utilisateur de Adobe Experience Cloud :

1. Sélectionnez **[!UICONTROL Permissions]** dans le rail de gauche, sous **[!UICONTROL ADMINISTRATION]**.

1. Sélectionnez ![User](/help/assets/icons/User.svg) **[!UICONTROL Roles]** dans le panneau de gauche.

1. Sélectionnez un rôle existant ou créez-en un en utilisant **[!UICONTROL Create role]** (par exemple, **Mix Modeler**). Si vous sélectionnez un rôle existant, sélectionnez ![Modifier](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** pour modifier les autorisations du rôle. Voir [Gérer les rôles](https://helpx.adobe.com/fr/enterprise/using/admin-console.html) pour plus d’informations.

1. Vérifiez que vous avez sélectionné un ou plusieurs environnements de test pour le rôle .

1. Ajoutez la ressource **Adobe Mix Modeler** à la liste des ressources pour le rôle .

1. Assurez-vous de sélectionner les autorisations **[!UICONTROL Adobe Mix Modeler]** correctes pour le rôle que vous configurez. Vous pouvez sélectionner un ou plusieurs des rôles suivants :

   - **[!UICONTROL View Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL Manage Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL View Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL View Adobe Mix Modeler Plans Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Plans Configuration]**

     ![RBAC Mix Modeler](/help/assets/mix-modeler-rbac.png)


1. Veillez à sélectionner des autorisations supplémentaires pour le rôle. Par exemple, pour afficher ou gérer des jeux de données et des schémas, vous devez sélectionner :

   - **[!UICONTROL Data Management]** : sélectionnez les options appropriées : **[!UICONTROL View Datasets]** ou **[!UICONTROL Manage Datasets]**.

   - **[!UICONTROL Data Modeling]** : sélectionnez les options appropriées : **[!UICONTROL Manage Schemas]** ou **[!UICONTROL View Schemas]**.

   <!--
    * **[!UICONTROL Data Governance]**: ensure you select **[!UICONTROL View User Activity Log]** and **[!UICONTROL View Data Usage Policies]**.
    -->

   <!--![Permissions](assets/permissions-including-privacy.png)-->

   Sélectionnez **[!UICONTROL Save]** pour enregistrer les autorisations.

1. Dans **[!UICONTROL Details]** dans **[!UICONTROL Role]**, ajoutez les **[!UICONTROL Users]** ou **[!UICONTROL User groups]** appropriés pour permettre aux utilisateurs d&#39;accéder au Mix Modeler.
