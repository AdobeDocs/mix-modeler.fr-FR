---
title: Administration
description: Découvrez comment administrer un Adobe Mix Modeler.
source-git-commit: 4a6cbda1ff0a779ebf8a38a4de3f797ed9e54b00
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 8%

---


# Administration

Utilisez la variable [Adobe Admin Console](https://helpx.adobe.com/fr/enterprise/using/admin-console.html) pour gérer les produits et les utilisateurs Adobe Mix Modeler.

Pour que l’Adobe Mix Modeler fonctionne correctement, vous devez définir les autorisations appropriées.

Dans l’interface utilisateur de Adobe Experience Cloud,

1. Sélectionner **[!UICONTROL Permissions]** depuis le rail de gauche, sous **[!UICONTROL ADMINISTRATION]**.

1. Sélectionner ![Personne](assets/icons/User.svg) **[!UICONTROL Roles]** dans le panneau de gauche.

1. Sélectionnez un rôle existant ou créez-en un en utilisant **[!UICONTROL Create role]**. Si vous sélectionnez un rôle existant, sélectionnez ![Modifier](assets/icons/Edit.svg) **[!UICONTROL Edit]** pour modifier les autorisations du rôle. Voir [Gestion des rôles](https://helpx.adobe.com/fr/enterprise/using/admin-console.html) pour plus d’informations.

1. Veillez à sélectionner les autorisations suivantes pour le rôle :

   * **[!UICONTROL Sandboxes]**: sélectionnez au moins un environnement de test.

   * **[!UICONTROL Data Management]**: assurez-vous de sélectionner les options **[!UICONTROL View Datasets]** et **[!UICONTROL Manage Datasets]**.

   * **[!UICONTROL Data Modeling]**: assurez-vous de sélectionner les options **[!UICONTROL Manage Schemas]** et **[!UICONTROL View Schemas]**.

   * **[!UICONTROL Destinations]**: assurez-vous que vous sélectionnez **[!UICONTROL Manage and Activate Dataset Destination]**, **[!UICONTROL Destination Authoring]**, **[!UICONTROL Activate Destinations]** et **[!UICONTROL View Destinations]**.

   * **[!UICONTROL Data Ingestion]**: assurez-vous que vous sélectionnez **[!UICONTROL View Sources]** et **[!UICONTROL Manage Sources]**.

   Les autorisations configurées pour le rôle doivent se présenter comme suit :

   ![Autorisations](assets/permissions.png)

   Sélectionner **[!UICONTROL Save]** pour enregistrer les autorisations.

1. Dans **[!UICONTROL Details]** dans **[!UICONTROL Role]**, ajoutez les **[!UICONTROL Users]** et/ou **[!UICONTROL User groups]** pour permettre aux utilisateurs d’accéder à Adobe Mix Modeler.
