---
title: Journaux d’audit
description: Découvrez comment accéder aux journaux d’audit à partir de Mix Modeler.
feature: Administration
exl-id: aa65aac5-bea4-43ff-b0d0-9e8a6a97d3ca
source-git-commit: 77a338ae568c854b99069b849a18661d413c501c
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 12%

---

# Journaux d’audit

Pour accroître la transparence et la visibilité des activités exécutées dans le système, l’activité de l’utilisateur dans le workflow du Mix Modeler est capturée dans les journaux d’audit de l’Experience Platform afin de comprendre toute modification apportée par l’utilisateur aux catégories du Mix Modeler. Ces journaux constituent un journal d’audit qui peut vous aider à résoudre les problèmes et à vous aider à respecter efficacement les politiques de gestion des données de l’entreprise et les exigences réglementaires.

<!-- DO WE HAVE TO ADD THIS
If you are subject to the Health Insurance Portability and Accountability Act (HIPAA) and create, receive, maintain, or transmit permitted sensitive personal data through Mix Modeler, you are responsible for executing a BAA with Adobe and licensing Healthcare Shield.
-->

Un journal d’audit indique qui a exécuté quelle action et quand. Chaque action enregistrée dans un journal contient des métadonnées qui indiquent le type d’action, la date et l’heure, l’ID d’e-mail de l’utilisateur ou de l’utilisatrice qui a exécuté l’action et des attributs supplémentaires liés au type d’action. Il effectue le suivi des actions de création, de mise à jour et de suppression entreprises par les utilisateurs dans Mix Modeler.

Pour examiner le journal d’audit, dans l’interface du Mix Modeler :

1. Sélectionnez ![Liste de tâches](/help/assets/icons/TaskList.svg) **[!UICONTROL Audits]** dans **[!UICONTROL PRIVACY]**.

1. Dans **[!UICONTROL Audits]**, vous pouvez trouver le **[!UICONTROL Activity log]**. Le journal des activités affiche les entrées pour les catégories de Mix Modeler, les actions et l’état suivants.

   | Catégorie | Action | Statut |
   |---|---|---|
   | Règle de jeu de données Mix Modeler | Créer | Autoriser ou refuser |
   | Règle de jeu de données Mix Modeler | Mise à jour  | Autoriser ou refuser |
   | Règle de jeu de données Mix Modeler | Supprimer | Autoriser ou refuser |
   | Champ Mix Modeler | Créer | Autoriser ou refuser |
   | Champ Mix Modeler | Mise à jour  | Autoriser ou refuser |
   | Champ Mix Modeler | Supprimer | Autoriser ou refuser |
   | Point de contact marketing Mix Modeler | Créer | Autoriser ou refuser |
   | Point de contact marketing Mix Modeler | Mise à jour  | Autoriser ou refuser |
   | Point de contact marketing Mix Modeler | Supprimer | Autoriser ou refuser |
   | Conversion de Mix Modeler | Créer | Autoriser ou refuser |
   | Conversion de Mix Modeler | Mise à jour  | Autoriser ou refuser |
   | Conversion de Mix Modeler | Supprimer | Autoriser ou refuser |
   | Modèle Mix Modeler | Créer | Autoriser ou refuser |
   | Modèle Mix Modeler | Mise à jour  | Autoriser ou refuser |
   | Modèle Mix Modeler | Supprimer | Autoriser ou refuser |
   | Modèle Mix Modeler | Re-score | Autoriser ou refuser |
   | Modèle Mix Modeler | Cloner | Autoriser ou refuser |
   | Modèle Mix Modeler | Train / Réentraînement | Autoriser ou refuser |
   | Modèle Mix Modeler | Téléchargement/enregistrement de métadonnées | Autoriser ou refuser |
   | Formule Mix Modeler | Créer | Autoriser ou refuser |
   | Formule Mix Modeler | Mise à jour  | Autoriser ou refuser |
   | Formule Mix Modeler | Modifier le modèle associé | Autoriser ou refuser |
   | Harmonisation des données Mix Modeler | Déclencher la synchronisation | Autoriser ou refuser |


1. Pour plus d’informations, sélectionnez une entrée dans le journal des activités afin d’ouvrir un panneau.

   ![Audit Mix Modeler](/help/assets/mix-modeler-audit.png)

1. Pour filtrer selon la plage **[!UICONTROL Category]**, **[!UICONTROL Action]**, **[!UICONTROL Request ID]**, **[!UICONTROL User]**, **[!UICONTROL Status]** ou **[!UICONTROL Date]**, sélectionnez ![Filtre](/help/assets/icons/Filter.svg).

1. Pour modifier les colonnes affichées dans le journal des activités, sélectionnez ![Colonnes](/help/assets/icons/ColumnSetting.svg) et, dans la boîte de dialogue **[!UICONTROL Customize table]**, sélectionnez les colonnes à afficher. Sélectionnez **[!UICONTROL Apply]** pour appliquer la sélection, **[!UICONTROL Cancel]** pour annuler la sélection.

1. Pour télécharger le journal d’audit, sélectionnez ![Télécharger](/help/assets/icons/Download.svg) **[!UICONTROL Download log]**. Dans la boîte de dialogue **[!UICONTROL Download log]**, sélectionnez **[!UICONTROL CSV]** ou **[!UICONTROL JSON]** comme format et sélectionnez **[!UICONTROL Download]**.

## Accès aux journaux d’audit

Lorsque la fonction est activée pour votre organisation, les journaux d’audit sont automatiquement collectés au fur et à mesure de l’activité. Vous n’avez pas besoin d’activer la collecte manuelle des journaux d’audit.

Pour afficher et exporter les journaux d’audit, vous devez disposer de l’autorisation de contrôle d’accès Logs d’audit . Pour savoir comment gérer les autorisations individuelles pour les fonctionnalités de Mix Modeler, consultez la [documentation sur le contrôle d’accès](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home).
