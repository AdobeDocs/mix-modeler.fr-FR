---
title: Administration
description: Découvrez comment administrer le Mix Modeler.
feature: Administration
exl-id: 76d6d15d-a838-4ee2-9929-e55ea8946b80
source-git-commit: 995f15b6d2dd99d5304a4cda7b1fa5f8a1d00023
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---

# Administration

Utilisez la variable [Adobe Admin Console](https://helpx.adobe.com/fr/enterprise/using/admin-console.html) pour gérer les produits et les utilisateurs Mix Modeler.

Pour que Mix Modeler fonctionne correctement, vous devez définir les autorisations appropriées.

Dans l’interface utilisateur de Adobe Experience Cloud :

1. Sélectionner **[!UICONTROL Permissions]** depuis le rail de gauche, sous **[!UICONTROL ADMINISTRATION]**.

1. Sélectionner {{user}} **[!UICONTROL Roles]** dans le panneau de gauche.

1. Sélectionnez un rôle existant ou créez-en un en utilisant **[!UICONTROL Create role]** (par exemple, **Mix Modeler**). Si vous sélectionnez un rôle existant, sélectionnez {{edit}} **[!UICONTROL Edit]** pour modifier les autorisations du rôle. Voir [Gestion des rôles](https://helpx.adobe.com/fr/enterprise/using/admin-console.html) pour plus d’informations.

1. Vérifiez que vous avez sélectionné un ou plusieurs environnements de test pour le rôle .

1. Ajoutez la variable **Adobe Mix Modeler** vers la liste des ressources pour le rôle.

1. Assurez-vous de sélectionner les **[!UICONTROL Adobe Mix Modeler]** autorisations pour le rôle que vous configurez. Vous pouvez sélectionner un ou plusieurs des rôles suivants :

   - **[!UICONTROL View Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL Manage Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL View Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL View Adobe Mix Modeler Plans Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Plans Configuration]**

     ![RBAC Mix Modeler](/help/assets/mix-modeler-rbac.png)


1. Veillez à sélectionner des autorisations supplémentaires pour le rôle. Par exemple, pour afficher ou gérer des jeux de données et des schémas, vous devez sélectionner :

   - **[!UICONTROL Data Management]**: sélectionnez les options appropriées : **[!UICONTROL View Datasets]** ou **[!UICONTROL Manage Datasets]**.

   - **[!UICONTROL Data Modeling]**: sélectionnez les options appropriées : **[!UICONTROL Manage Schemas]** ou **[!UICONTROL View Schemas]**.

   <!--
    * **[!UICONTROL Data Governance]**: ensure you select **[!UICONTROL View User Activity Log]** and **[!UICONTROL View Data Usage Policies]**.
    -->

   <!--![Permissions](assets/permissions-including-privacy.png)-->

   Sélectionner **[!UICONTROL Save]** pour enregistrer les autorisations.

1. Dans **[!UICONTROL Details]** dans **[!UICONTROL Role]**, ajoutez les **[!UICONTROL Users]** ou **[!UICONTROL User groups]** pour permettre aux utilisateurs d’accéder à Mix Modeler.
