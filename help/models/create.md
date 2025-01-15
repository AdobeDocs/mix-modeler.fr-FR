---
title: Création d’un modèle
description: Découvrez comment créer un modèle dans Mix Modeler.
feature: Models
exl-id: e1093c09-1e23-460b-92de-cfb0061112fd
source-git-commit: 16aec67b3e0562ff766f81b8036c724fa03bba17
workflow-type: tm+mt
source-wordcount: '900'
ht-degree: 0%

---

# Création d’un modèle

Pour créer un modèle, dans l’interface **[!UICONTROL Models]** ![Modèles](/help/assets/icons/FileData.svg) de Mix Modeler, sélectionnez **[!UICONTROL Open model canvas]**.

Pour créer vos modèles personnalisés optimisés par l’IA, l’interface fournit un flux de configuration guidé du modèle étape par étape.

## Configuration

Définissez le nom et la description à l’étape **[!UICONTROL Setup]** :

1. Saisissez votre **[!UICONTROL Name]** de modèle, par exemple `Demo model`. Saisissez un **[!UICONTROL Description]**, par exemple `Demo model to explore AI featues of Mix Modeler`.

   ![ Nom et description du modèle ](/help/assets/model-name-description.png)

1. Sélectionnez **[!UICONTROL Next]** pour passer à l’étape suivante. Sélectionnez **[!UICONTROL Cancel]** pour annuler la configuration du modèle.

## Configuration

Configurez votre modèle à l’étape **[!UICONTROL Configure]**. La configuration implique la définition d’objectifs de conversion, de points de contact marketing, de la population de données éligibles, de facteurs externes et internes, etc.

1. Dans la section **[!UICONTROL Conversion goal]** :

   ![Modèle - étape de conversion](/help/assets/model-conversion-step.png)

   1. Sélectionnez une conversion dans le menu déroulant **[!UICONTROL Conversion]** . Les conversions disponibles correspondent à celles que vous avez définies dans le cadre de l’[!UICONTROL Harmonized datasets] [Conversions](../harmonize-data/conversions.md). Par exemple : **[!UICONTROL Online Conversion]**.

   1. Vous pouvez sélectionner l’**[!UICONTROL Create a conversion]** ![LinkOutLight](/help/assets/icons/LinkOutLight.svg) pour créer une conversion directement à partir de la configuration du modèle.



1. Dans la section **[!UICONTROL Marketing touchpoints]** , vous pouvez sélectionner un ou plusieurs points de contact marketing, correspondant aux points de contact marketing que vous avez définis dans le cadre de l’[points de contact marketing](../harmonize-data/marketing-touchpoints.md) dans [!UICONTROL Harmonized datasets].


   ![Modèle - étape du point de contact marketing](/help/assets/model-marketing-touchpoint-step.png)

   1. Sélectionnez un ou plusieurs points de contact marketing dans le menu déroulant **[!UICONTROL Touchpoint include]** .

      * Vous pouvez utiliser ![CrossSize75](/help/assets/icons/CrossSize75.svg) pour supprimer un point de contact.
      * Vous pouvez utiliser **[!UICONTROL Clear all]** pour supprimer tous les points de contact.

   1. Vous pouvez sélectionner l’**[!UICONTROL Create a touchpoint]** ![LinkOutLight](/help/assets/icons/LinkOutLight.svg) pour créer un point de contact marketing directement à partir de la configuration du modèle.

   >[!NOTE]
   >
   >Vous ne pouvez pas configurer le modèle avec des points de contact dont les données se chevauchent et qui doivent comporter au moins un point de contact avec des dépenses.

1. Par défaut, un score est généré pour toutes les données de la vue harmonisée. Pour noter uniquement un sous-ensemble de la population, définissez un ou plusieurs filtres à l’aide de conteneurs dans la section **[!UICONTROL Eligible data population]** .

   ![Modèle - Population de données éligible](/help/assets/model-eligible-data-population-step.png)

   * Pour chaque conteneur, définissez un ou plusieurs événements.

      1. Pour chaque événement :

         1. Sélectionnez une mesure ou une dimension dans **[!UICONTROL _Sélectionner le champ harmonisé_]**.

         1. Sélectionnez l’opérateur approprié : **[!UICONTROL equals]**, **[!UICONTROL not equals]**, **[!UICONTROL less than]**, **[!UICONTROL greater than]**, **[!UICONTROL starts with]**, **[!UICONTROL doesn't start with]**, **[!UICONTROL ends with]**, **[!UICONTROL doesn't end with]**, **[!UICONTROL contains]**, **[!UICONTROL doesn't contain]**, **[!UICONTROL is in]** ou **[!UICONTROL is not in]**.

         1. Saisissez ou sélectionnez une valeur sur **[!UICONTROL _Saisissez ou sélectionnez une valeur_]**.

      1. Pour ajouter un événement supplémentaire dans le conteneur, sélectionnez ![ Ajouter ](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add event]**.

      1. Pour supprimer un événement du conteneur, sélectionnez ![ Fermer ](/help/assets/icons/CrossSize75.svg).

      1. Pour filtrer à l’aide de l’ensemble ou de l’un des multiples événements définis dans le conteneur, sélectionnez **[!UICONTROL Any of]** ou **[!UICONTROL All of]**. Le libellé passe donc de **[!UICONTROL Include ... Or ...]** à **[!UICONTROL Include ... And ...]**.

   * Pour ajouter un conteneur de population de données éligible, sélectionnez ![ Ajouter ](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add eligible population]**.

   * Pour supprimer un conteneur de population de données éligible dans le conteneur, sélectionnez ![Plus](/help/assets/icons/More.svg), puis **[!UICONTROL Remove marketing touchpoint]** dans le menu contextuel.

   * Sélectionnez **Et** et **Ou** entre les conteneurs pour créer des définitions plus complexes pour votre population de données éligible.


1. Pour ajouter des jeux de données contenant des facteurs externes à votre modèle, utilisez un ou plusieurs conteneurs dans la section **[!UICONTROL External factors dataset]** . Les indices S&amp;P sont un exemple de facteurs externes.

   ![Modèle - Jeu de données de facteurs externes](/help/assets/model-external-factors-dataset-step.png)

   * Pour chaque conteneur :

      1. Saisissez un **[!UICONTROL External factor name]**, par exemple `External Factors`.

      1. Sélectionnez un jeu de données dans le menu déroulant **[!UICONTROL Dataset]** . Vous pouvez sélectionner ![Données](/help/assets/icons/Data.svg) pour gérer les jeux de données. Voir [Jeux de données](../ingest-data/datasets.md) pour plus d’informations.

      1. Sélectionnez une option dans le menu déroulant **[!UICONTROL Impact on conversion]** : **[!UICONTROL Auto select]**, **[!UICONTROL Positive]** ou **[!UICONTROL Negative]**.

   * Pour ajouter un conteneur de jeu de données de facteurs externes supplémentaires, sélectionnez ![Ajouter](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add external factor]**.

   * Pour supprimer un conteneur de jeu de données de facteurs externes, sélectionnez ![RemoveCircle](/help/assets/icons/RemoveCircle.svg).




1. Pour ajouter des jeux de données contenant des facteurs internes à votre modèle, utilisez un ou plusieurs conteneurs dans la section **[!UICONTROL Internal factors dataset]** . Les données de marketing par e-mail sont un exemple de facteurs internes.

   ![ Modèle - Jeu de données de facteurs internes ](/help/assets/model-internal-factors-dataset-step.png)

   * Pour chaque conteneur :

      1. Saisissez un **[!UICONTROL Internal factor name]**, par exemple `Email Marketing Data`.

      1. Sélectionnez un jeu de données dans **[!UICONTROL _Sélectionnez un jeu de données_]**. Vous pouvez sélectionner ![Données](/help/assets/icons/Data.svg) pour gérer les jeux de données. Voir [Jeux de données](../ingest-data/datasets.md) pour plus d’informations.

      1. Sélectionnez une option dans le menu déroulant **[!UICONTROL Impact on conversion]** : **[!UICONTROL Auto select]**, **[!UICONTROL Positive]** ou **[!UICONTROL Negative]**.

   * Pour ajouter un conteneur de jeu de données de facteurs internes supplémentaires, sélectionnez ![Ajouter](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add internal factor]**.

   * Pour supprimer un conteneur de jeux de données de facteurs internes, sélectionnez ![RemoveCircle](/help/assets/icons/RemoveCircle.svg).



1. Pour définir l’intervalle de recherche en amont du modèle, saisissez une valeur comprise entre `1` et `52` dans **[!UICONTROL Give contribution credit to touchpoints occurring within]** ... **[!UICONTROL weeks prior to the conversion]**.

1. Sélectionnez **[!UICONTROL Next]** pour passer à l’étape suivante. Si une configuration supplémentaire est nécessaire, un contour et un texte rouges expliquent quelle configuration supplémentaire est requise. <br/>Sélectionnez **[!UICONTROL Back]** pour revenir à l’étape précédente. <br/>Sélectionnez **[!UICONTROL Cancel]** pour annuler la configuration du modèle.


## Advanced

Vous pouvez spécifier des paramètres avancés à l’étape **[!UICONTROL Advanced]**. Au cours de cette étape, vous pouvez activer votre modèle pour l’attribution multipoint (MTA).

1. Dans la section **[!UICONTROL Spend share]** :

   * Pour utiliser les ratios d’investissement marketing historiques afin d’informer le modèle lorsque les données marketing sont rares, activez **[!UICONTROL Allow spend share]**.

1. Dans la section **[!UICONTROL MTA enabled]** :

   * Pour activer les fonctionnalités MTA pour le modèle, activez **[!UICONTROL MTA enabled]**. Si vous avez activé le MTA, les informations d’attribution multipoint sont disponibles après avoir formé et noté votre modèle. Voir l’onglet [Attribution](insights.md#attribution) dans [Model Insights](insights.md).

1. Dans la section **[!UICONTROL Prior knowledge]** :

   ![Modèle - Connaissances préalables](/help/assets/model-prior-knowledge-step.png)

   1. Sélectionnez l’**[!UICONTROL Rule type]**, qui est **[!UICONTROL Absolute values]** par défaut.

   1. Indiquez les pourcentages de contribution pour l’un des canaux répertoriés sous **[!UICONTROL Name]**, à l’aide de la colonne **[!UICONTROL Contribution proportion]** .

   1. Le cas échéant, vous pouvez ajouter pour chaque canal un pourcentage **[!UICONTROL Level of confidence]**.

   1. Si nécessaire, utilisez **[!UICONTROL Clear all]** pour effacer toutes les valeurs d’entrée des colonnes **[!UICONTROL Contribution proportion]** et **[!UICONTROL Level of confidence]**.


## Planning

Vous pouvez planifier l’entraînement et l’enregistrement de votre modèle à l’étape **[!UICONTROL Schedule]**.

1. Dans la section **[!UICONTROL Schedule]** , vous pouvez planifier l’entraînement et la notation des modèles.

   ![Modèle de planification](../assets/model-schedule.png)

   Pour planifier la notation et la formation des modèles :

   1. Activez **[!UICONTROL Enable scheduled model scoring and training]**.
   1. Sélectionner un **[!UICONTROL Scoring frequency]** :

      * **[!UICONTROL Daily]** : saisissez une heure valide (par exemple, `05:22 pm`) ou utilisez ![Horloge](/help/assets/icons/Clock.svg).
      * **[!UICONTROL Weekly]** : sélectionnez un jour de la semaine et saisissez une heure valide (par exemple, `05:22 pm`) ou utilisez ![Horloge](/help/assets/icons/Clock.svg).
      * **[!UICONTROL Monthly]** : sélectionnez un jour du mois dans le menu déroulant Exécuter sur chaque et saisissez une heure valide (par exemple `05:22 pm`) ou utilisez ![Horloge](/help/assets/icons/Clock.svg).

   1. Sélectionnez un **[!UICONTROL Training frequency]** dans le menu déroulant : **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** ou **[!UICONTROL None]**.

1. Dans la section **[!UICONTROL Define training window]**, sélectionnez entre :

   ![Modèle - Définir la fenêtre de formation](/help/assets/model-define-training-window.png)

   * **[!UICONTROL Have Mix Modeler select a helpful training window]** et

   * **[!UICONTROL Manually input a training window]**. Lorsque cette option est sélectionnée, définissez le nombre d’années dans **[!UICONTROL Include events the following years prior to a conversion]**.


1. Sélectionnez **[!UICONTROL Finish]** pour terminer la configuration du modèle.

   * Dans la boîte de dialogue **[!UICONTROL Create instance?]**, sélectionnez **[!UICONTROL Ok]** pour déclencher immédiatement le premier jeu d’exécutions d’entraînement et de notation. Votre modèle est répertorié avec le statut ![StatusOrange](/help/assets/icons/StatusOrange.svg) **[!UICONTROL Awaiting training]**.

     Sélectionnez **[!UICONTROL Cancel]** pour annuler.

   * Si une configuration supplémentaire est nécessaire, un contour et un texte rouges expliquent quelle configuration supplémentaire est requise.

   Sélectionnez **[!UICONTROL Back]** pour revenir à l’étape précédente.

   Sélectionnez **[!UICONTROL Cancel]** pour annuler la configuration du modèle.
