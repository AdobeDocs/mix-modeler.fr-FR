---
title: Création d’un modèle
description: Découvrez comment créer un modèle en Mix Modeler.
feature: Models
exl-id: e1093c09-1e23-460b-92de-cfb0061112fd
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 0%

---

# Création d’un modèle

Pour créer un modèle, dans l&#39;interface ![Modèles](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** de Mix Modeler, sélectionnez **[!UICONTROL Open model canvas]**.

Pour créer vos modèles personnalisés optimisés par l’IA, l’interface fournit un flux de configuration de modèle guidé étape par étape.

1. À l’étape **[!UICONTROL Setup]** :

   1. Saisissez votre modèle **[!UICONTROL Name]**, par exemple `Demo model`. Saisissez un **[!UICONTROL Description]**, par exemple `Demo model to explore AI featues of Mix Modeler`.

      ![Nom et description du modèle](/help/assets/model-name-description.png)

   1. Sélectionnez **[!UICONTROL Next]** pour passer à l’étape suivante. Sélectionnez **[!UICONTROL Cancel]** pour annuler la configuration du modèle.

1. À l’étape **[!UICONTROL Configure]** :

   1. Dans la section **[!UICONTROL Conversion goal]**, dans le conteneur :

      1. Saisissez un **[!UICONTROL Conversion name]** pour la conversion, par exemple `Conversion`

      1. Sélectionnez une conversion à partir de **[!UICONTROL *Sélectionner un champ harmonisé&#x200B;*]**, contenant les conversions disponibles que vous avez définies dans le cadre de [Conversions](../harmonize-data/conversions.md) dans [!UICONTROL Harmonized datasets]. Par exemple :**[!UICONTROL Online Conversion]**.

      1. Vous pouvez sélectionner ![Répondre](/help/assets/icons/Reply.svg) **[!UICONTROL Create new conversion]** pour créer une conversion directement depuis la configuration du modèle.

         ![Modèle - étape de conversion](/help/assets/model-conversion-step.png)

   1. Dans la section **[!UICONTROL Marketing touchpoints]**, vous voyez plusieurs conteneurs de points de contact marketing, correspondant aux points de contact marketing que vous avez définis dans [Points de contact marketing](../harmonize-data/marketing-touchpoints.md) dans [!UICONTROL Harmonized datasets].

      * Pour chaque conteneur :

         1. Vous pouvez modifier le **[!UICONTROL Marketing touchpoint name]**.

         1. Sélectionnez un point de contact marketing à partir de **[!UICONTROL _Sélectionner un point de contact marketing_]**.

         1. Vous pouvez sélectionner ![Répondre](/help/assets/icons/Reply.svg) **[!UICONTROL Create new marketing touchpoint]** pour créer un point de contact marketing directement dans la configuration du modèle.

      * Pour ajouter un conteneur de point de contact marketing, sélectionnez ![Ajouter](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add marketing touchpoint]**.

      * Pour supprimer un conteneur de point de contact marketing, dans le conteneur, sélectionnez ![Plus](/help/assets/icons/More.svg), puis **[!UICONTROL Remove container]** dans le menu contextuel.

        ![Modèle - marketing touchpoints-step](/help/assets/model-marketing-touchpoint-step.png)

   1. Par défaut, un score est généré pour toutes les données de la vue harmonisée. Pour ne noter qu’un sous-ensemble de la population, définissez un ou plusieurs filtres à l’aide de conteneurs dans la section **[!UICONTROL Eligible data population]** .

      * Pour chaque conteneur, définissez un ou plusieurs événements.

         1. Pour chaque événement :

            1. Sélectionnez une mesure ou une dimension dans **[!UICONTROL _Sélectionner un champ harmonisé_]**.

            1. Sélectionnez l’opérateur approprié : **[!UICONTROL equals]**, **[!UICONTROL not equals]**, **[!UICONTROL less than]**, **[!UICONTROL greater than]**, **[!UICONTROL starts with]**, **[!UICONTROL doesn't start with]**, **[!UICONTROL ends with]**, **[!UICONTROL doesn't end with]**, **[!UICONTROL contains]**, **[!UICONTROL doesn't contain]**, **[!UICONTROL is in]** ou **[!UICONTROL is not in]**.

            1. Saisissez ou sélectionnez une valeur à l’emplacement **[!UICONTROL _Entrez ou sélectionnez la valeur_]**.

         1. Pour ajouter un événement supplémentaire dans le conteneur, sélectionnez ![Ajouter](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add event]**.

         1. Pour supprimer un événement du conteneur, sélectionnez ![Fermer](/help/assets/icons/Close.svg).

         1. Pour filtrer à l’aide de l’ensemble ou de l’un des événements multiples définis dans le conteneur, sélectionnez **[!UICONTROL Any of]** ou **[!UICONTROL All of]**. L’étiquette passe en conséquence de **[!UICONTROL Include ... Or ...]** à **[!UICONTROL Include ... And ...]**.

      * Pour ajouter un conteneur de population de données éligible, sélectionnez ![Ajouter](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add eligible population]**.

      * Pour supprimer un conteneur de population de données éligible, dans le conteneur, sélectionnez ![Plus](/help/assets/icons/More.svg), puis **[!UICONTROL Remove marketing touchpoint]** dans le menu contextuel.

        ![Modèle - Population de données éligible](/help/assets/model-eligible-data-population-step.png)

   1. Pour ajouter des jeux de données contenant des facteurs externes à votre modèle, utilisez un ou plusieurs conteneurs dans la section **[!UICONTROL External factors dataset]** .

      * Pour chaque conteneur :

         1. Saisissez un **[!UICONTROL Factor name]** à **[!UICONTROL _Saisir le facteur_]**.

         1. Sélectionnez un jeu de données dans **[!UICONTROL _Sélectionner un jeu de données_]**. Vous pouvez sélectionner ![Data](/help/assets/icons/Data.svg) pour gérer les jeux de données. Voir [Jeux de données](../ingest-data/datasets.md) pour plus d’informations.

      * Pour ajouter un autre conteneur de jeux de données de facteurs externes, sélectionnez ![Ajouter](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add external factor]**.

      * Pour supprimer un conteneur de jeux de données de facteurs externes, dans le conteneur, sélectionnez ![Plus](/help/assets/icons/More.svg), puis **[!UICONTROL Remove external factor]** dans le menu contextuel.

        ![Modèle - Jeu de données de facteurs externes](/help/assets/model-external-factors-dataset-step.png)


   1. Pour ajouter des jeux de données contenant des facteurs internes à votre modèle, utilisez un ou plusieurs conteneurs dans la section **[!UICONTROL Internal factors dataset]**.

      * Pour chaque conteneur :

         1. Saisissez un **[!UICONTROL Factor name]** à **[!UICONTROL _Saisir le facteur_]**.

         1. Sélectionnez un jeu de données dans **[!UICONTROL _Sélectionner un jeu de données_]**. Vous pouvez sélectionner ![Data](/help/assets/icons/Data.svg) pour gérer les jeux de données. Voir [Jeux de données](../ingest-data/datasets.md) pour plus d’informations.

      * Pour ajouter un conteneur de jeux de données de facteurs internes supplémentaire, sélectionnez ![Ajouter](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add internal factor]**.

      * Pour supprimer un conteneur de jeux de données de facteurs internes supplémentaire, dans le conteneur, sélectionnez ![Plus](/help/assets/icons/More.svg) et **[!UICONTROL Remove internal factor]** dans le menu contextuel.

        ![Modèle - Jeu de données de facteurs internes](/help/assets/model-internal-factors-dataset-step.png)

   1. Pour définir l’intervalle de recherche en amont du modèle, saisissez une valeur comprise entre `1` et `52` dans **[!UICONTROL Give contribution credit to touchpoints occurring within]** ... **[!UICONTROL weeks prior to the conversion]**.

   1. Sélectionnez **[!UICONTROL Next]** pour passer à l’étape suivante. Si davantage de configuration est nécessaire, un contour rouge et un texte expliquent la configuration supplémentaire requise. <br/>Sélectionnez **[!UICONTROL Back]** pour revenir à l’étape précédente. <br/>Sélectionnez **[!UICONTROL Cancel]** pour annuler la configuration du modèle.

1. À l’étape **[!UICONTROL Advanced]** :

   1. Dans la section **[!UICONTROL Define training window]**, sélectionnez entre

      * **[!UICONTROL Have Mix Modeler select a helpful training window]** et

      * **[!UICONTROL Manually input a training window]**. Lorsqu’elle est sélectionnée, définissez le nombre d’années dans **[!UICONTROL Include events the following years prior to a conversion]**.

        ![Modèle - Définir la fenêtre de formation](/help/assets/model-define-training-window.png)

   1. Dans la section **[!UICONTROL Spend share]** :

      * Pour utiliser les ratios d’investissement marketing historiques afin d’informer le modèle lorsque les données marketing sont éparses, activez **[!UICONTROL Allow spend share]**.

   1. Dans la section **[!UICONTROL Prior knowledge]** :

      1. Sélectionnez le **[!UICONTROL Rule type]**.

      1. Spécifiez des pourcentages de contribution pour l’un des canaux répertoriés sous **[!UICONTROL Name]**, à l’aide de la colonne **[!UICONTROL Contribution proportion]**.

      1. Le cas échéant, vous pouvez ajouter pour chaque canal un pourcentage **[!UICONTROL Level of confidence]**.

      1. Si nécessaire, utilisez **[!UICONTROL Clear all]** pour effacer toutes les valeurs d’entrée pour les colonnes **[!UICONTROL Contribution proportion]** et **[!UICONTROL Level of confidence]**.

         ![Modèle - Connaissances préalables](/help/assets/model-prior-knowledge-step.png)

1. Sélectionnez **[!UICONTROL Finish]** pour terminer la configuration du modèle.

   * Dans la boîte de dialogue **[!UICONTROL Create instance?]**, sélectionnez **[!UICONTROL Ok]** pour déclencher immédiatement le premier ensemble d’exécutions de formation et de notation. Votre modèle est répertorié avec l’état <span style="color:orange">●</span> **[!UICONTROL Awaiting training]**.

     Sélectionnez **[!UICONTROL Cancel]** pour annuler.

   * Si davantage de configuration est nécessaire, un contour rouge et un texte expliquent la configuration supplémentaire requise.

   Sélectionnez **[!UICONTROL Back]** pour revenir à l’étape précédente.

   Sélectionnez **[!UICONTROL Cancel]** pour annuler la configuration du modèle.
