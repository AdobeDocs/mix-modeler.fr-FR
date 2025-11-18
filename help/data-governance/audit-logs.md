---
title: Journaux d’audit
description: Découvrez comment accéder aux journaux d’audit de Mix Modeler.
feature: Administration
exl-id: aa65aac5-bea4-43ff-b0d0-9e8a6a97d3ca
source-git-commit: 1a9df9f9819d9e0031e58443ec6a9e755a151ba0
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 12%

---

# Journaux d’audit

Pour accroître la transparence et la visibilité des activités exécutées dans le système, l’activité des utilisateurs et utilisatrices dans le workflow Mix Modeler est capturée dans les journaux d’audit Experience Platform afin de comprendre toute modification apportée aux catégories Mix Modeler par les utilisateurs et utilisatrices. Ces journaux constituent un journal d’audit qui peut vous aider à résoudre les problèmes et à vous conformer efficacement aux politiques de gestion des données d’entreprise et aux exigences réglementaires.

<!-- DO WE HAVE TO ADD THIS
If you are subject to the Health Insurance Portability and Accountability Act (HIPAA) and create, receive, maintain, or transmit permitted sensitive personal data through Mix Modeler, you are responsible for executing a BAA with Adobe and licensing Healthcare Shield.
-->

Un journal d’audit indique qui a effectué quelle action et quand. Chaque action enregistrée dans un journal contient des métadonnées qui indiquent le type d’action, la date et l’heure, l’ID d’e-mail de l’utilisateur ou de l’utilisatrice qui a exécuté l’action et des attributs supplémentaires liés au type d’action. Il effectue le suivi des actions de création, de mise à jour et de suppression entreprises par les utilisateurs dans Mix Modeler.

Pour examiner le journal d’audit, dans l’interface de Mix Modeler :

1. Sélectionnez ![Liste des tâches](/help/assets/icons/TaskList.svg) **[!UICONTROL Audits]** dans **[!UICONTROL PRIVACY]**.

1. En **[!UICONTROL Audits]**, vous pouvez trouver le **[!UICONTROL Activity log]**. Le journal des activités affiche les entrées des catégories, actions et statuts Mix Modeler ci-après.

   | Catégorie | Action | Statut |
   |---|---|---|
   | Règle du jeu de données Mix Modeler | Créer | Autoriser ou refuser |
   | Règle du jeu de données Mix Modeler | Mise à jour  | Autoriser ou refuser |
   | Règle du jeu de données Mix Modeler | Supprimer | Autoriser ou refuser |
   | Champ Mix Modeler | Créer | Autoriser ou refuser |
   | Champ Mix Modeler | Mise à jour  | Autoriser ou refuser |
   | Champ Mix Modeler | Supprimer | Autoriser ou refuser |
   | Point de contact marketing Mix Modeler | Créer | Autoriser ou refuser |
   | Point de contact marketing Mix Modeler | Mise à jour  | Autoriser ou refuser |
   | Point de contact marketing Mix Modeler | Supprimer | Autoriser ou refuser |
   | Conversion Mix Modeler | Créer | Autoriser ou refuser |
   | Conversion Mix Modeler | Mise à jour  | Autoriser ou refuser |
   | Conversion Mix Modeler | Supprimer | Autoriser ou refuser |
   | Modèle Mix Modeler | Créer | Autoriser ou refuser |
   | Modèle Mix Modeler | Mise à jour  | Autoriser ou refuser |
   | Modèle Mix Modeler | Supprimer | Autoriser ou refuser |
   | Modèle Mix Modeler | Score | Autoriser ou refuser |
   | Modèle Mix Modeler | Cloner | Autoriser ou refuser |
   | Modèle Mix Modeler | Former / Recycler | Autoriser ou refuser |
   | Modèle Mix Modeler | Télécharger/enregistrer des métadonnées | Autoriser ou refuser |
   | Plan Mix Modeler | Créer | Autoriser ou refuser |
   | Plan Mix Modeler | Mise à jour  | Autoriser ou refuser |
   | Plan Mix Modeler | Modifier le modèle associé | Autoriser ou refuser |
   | Harmonisation des données Mix Modeler | Synchronisation du déclencheur | Autoriser ou refuser |


1. Sélectionnez une entrée dans le journal des activités pour ouvrir un panneau pour plus d’informations.

   ![Audit Mix Modeler](/help/assets/mix-modeler-audit.png)

1. Pour filtrer par plage de **[!UICONTROL Category]**, **[!UICONTROL Action]**, **[!UICONTROL Request ID]**, **[!UICONTROL User]**, **[!UICONTROL Status]** ou **[!UICONTROL Date]**, sélectionnez ![Filtrer](/help/assets/icons/Filter.svg).

1. Pour modifier les colonnes affichées dans le journal d’activité, sélectionnez ![Colonnes](/help/assets/icons/ColumnSetting.svg) et dans la boîte de dialogue **[!UICONTROL Customize table]**, sélectionnez les colonnes à afficher. Sélectionnez **[!UICONTROL Apply]** pour appliquer la sélection, **[!UICONTROL Cancel]** pour l’annuler.

1. Pour télécharger le journal d’audit, sélectionnez ![Télécharger](/help/assets/icons/Download.svg) **[!UICONTROL Download log]**. Dans la boîte de dialogue **[!UICONTROL Download log]**, sélectionnez **[!UICONTROL CSV]** ou **[!UICONTROL JSON]** comme format, puis sélectionnez **[!UICONTROL Download]**.

## Accès aux journaux d’audit

Lorsque la fonctionnalité est activée pour votre organisation, les journaux d’audit sont automatiquement collectés au fur et à mesure de l’activité. Vous n’avez pas besoin d’activer manuellement la collecte des journaux d’audit.

Pour afficher et exporter les journaux d’audit, l’autorisation de contrôle d’accès Accès aux journaux d’audit doit avoir été accordée. Pour savoir comment gérer les autorisations individuelles pour les fonctionnalités Mix Modeler, consultez la [documentation sur le contrôle d’accès](https://experienceleague.adobe.com/fr/docs/experience-platform/access-control/home).
