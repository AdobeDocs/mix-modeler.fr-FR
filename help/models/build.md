---
title: Création de modèles dans Mix Modeler
description: Découvrez comment créer des modèles dans Mix Modeler, notamment comment configurer et spécifier des options avancées pour le modèle.
feature: Models
solution: Mix Modeler
exl-id: e1093c09-1e23-460b-92de-cfb0061112fd
source-git-commit: 011b9b83569925ca9ff4f1ee472288473fbe8502
workflow-type: tm+mt
source-wordcount: '1276'
ht-degree: 2%

---

# Créer des modèles

Pour créer vos modèles personnalisés optimisés par l’IA, l’interface fournit un flux de configuration guidé du modèle étape par étape.

Dans l’interface ![&#x200B; &#x200B;](/help/assets/icons/FileData.svg)Modèles **[!UICONTROL Models]** de Mix Modeler, sélectionnez **[!UICONTROL Open model canvas]**.

## Configuration

Vous définissez un nom et une description à l’étape **[!UICONTROL Setup]** :

1. Saisissez votre **[!UICONTROL Name]** de modèle, par exemple `Demo model`. Saisissez un **[!UICONTROL Description]**, par exemple `Demo model to explore AI features of Mix Modeler`.

   ![&#x200B; Nom et description du modèle &#x200B;](/help/assets/model-name-description.png)

1. Sélectionnez **[!UICONTROL Next]** pour passer à l’étape suivante. Sélectionnez **[!UICONTROL Cancel]** pour annuler la configuration du modèle.

## Configuration{#configure}

>[!CONTEXTUALHELP]
>id="model_marketingtouchpoints_select"
>title="Points de contact marketing"
>abstract="Les points de contact marketing sont des événements marketing au niveau de la personne destinataire, de l’individu ou du cookie utilisés pour évaluer l’impact des investissements marketing sur les conversions numériques ou basées sur les revenus.<br/><br/>Vous ne pouvez pas configurer le modèle avec des points de contact dont les données se chevauchent et qui doivent comporter au moins un point de contact avec des dépenses."

Configurez votre modèle à l’étape **[!UICONTROL Configure]**. La configuration implique la définition d’objectifs de conversion, de points de contact marketing, de la population de données éligibles, de facteurs externes et internes, etc.

1. Dans la section **[!UICONTROL Conversion goal]** :

   ![Modèle - étape de conversion](/help/assets/model-conversion-step.png)

   1. Sélectionnez une conversion dans le menu déroulant **[!UICONTROL Conversion]** . Les conversions disponibles correspondent à celles que vous avez définies dans le cadre de l’[&#x200B; &#x200B;](../harmonize-data/conversions.md)Conversions[!UICONTROL Harmonized datasets]. Par exemple : **[!UICONTROL Online Conversion]**.

   1. Vous pouvez sélectionner l’![&#x200B; &#x200B;](/help/assets/icons/LinkOutLight.svg)LinkOutLight **[!UICONTROL Create a conversion]** pour créer une conversion directement à partir de la configuration du modèle.



1. Dans la section **[!UICONTROL Marketing touchpoints]** , vous pouvez sélectionner un ou plusieurs points de contact marketing, correspondant aux points de contact marketing que vous avez définis dans le cadre de l’[points de contact marketing](../harmonize-data/marketing-touchpoints.md) dans [!UICONTROL Harmonized datasets].


   ![Modèle - étape du point de contact marketing](/help/assets/model-marketing-touchpoint-step.png)

   1. Sélectionnez un ou plusieurs points de contact marketing dans le menu déroulant **[!UICONTROL Touchpoint include]** .

      * Vous pouvez utiliser ![CrossSize75](/help/assets/icons/CrossSize75.svg) pour supprimer un point de contact.
      * Vous pouvez utiliser **[!UICONTROL Clear all]** pour supprimer tous les points de contact.

   1. Vous pouvez sélectionner l’![&#x200B; &#x200B;](/help/assets/icons/LinkOutLight.svg)LinkOutLight **[!UICONTROL Create a touchpoint]** pour créer un point de contact marketing directement à partir de la configuration du modèle.

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

      1. Pour ajouter un événement supplémentaire dans le conteneur, sélectionnez ![&#x200B; Ajouter &#x200B;](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add event]**.

      1. Pour supprimer un événement du conteneur, sélectionnez ![&#x200B; Fermer &#x200B;](/help/assets/icons/CrossSize75.svg).

      1. Pour filtrer à l’aide de l’ensemble ou de l’un des multiples événements définis dans le conteneur, sélectionnez **[!UICONTROL Any of]** ou **[!UICONTROL All of]**. Le libellé passe donc de **[!UICONTROL Include ... Or ...]** à **[!UICONTROL Include ... And ...]**.

   * Pour ajouter un conteneur de population de données éligible, sélectionnez ![&#x200B; Ajouter &#x200B;](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add eligible population]**.

   * Pour supprimer un conteneur de population de données éligible dans le conteneur, sélectionnez ![Plus](/help/assets/icons/More.svg), puis **[!UICONTROL Remove container]** dans le menu contextuel.

   * Sélectionnez **Et** et **Ou** entre les conteneurs pour créer des définitions plus complexes pour votre population de données éligible.


1. Pour ajouter des jeux de données contenant des facteurs externes à votre modèle, utilisez un ou plusieurs conteneurs dans la section **[!UICONTROL External factors dataset]** . Les indices S&amp;P sont un exemple de facteurs externes.

   ![Modèle - Jeu de données de facteurs externes](/help/assets/model-external-factors-dataset-step.png)

   * Pour chaque conteneur :

      1. Saisissez un **[!UICONTROL External factor name]**, par exemple `External Factors`.

      1. Sélectionnez un jeu de données dans le menu déroulant **[!UICONTROL Dataset]** . Vous pouvez sélectionner ![Données](/help/assets/icons/Data.svg) pour gérer les jeux de données. Voir [Jeux de données](../ingest-data/datasets.md) pour plus d’informations.

      1. Sélectionnez une option dans le menu déroulant **[!UICONTROL Impact on conversion]** : **[!UICONTROL Auto select]**, **[!UICONTROL Positive]** ou **[!UICONTROL Negative]**. L’option par défaut est **[!UICONTROL Auto select]**, ce qui permet au modèle de déterminer l’impact. Vous pouvez remplacer la valeur par défaut.

   * Pour ajouter un conteneur de jeu de données de facteurs externes supplémentaires, sélectionnez ![Ajouter](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add external factor]**.

   * Pour supprimer un conteneur de jeu de données de facteurs externes, sélectionnez ![RemoveCircle](/help/assets/icons/RemoveCircle.svg).




1. Pour ajouter des jeux de données contenant des facteurs internes à votre modèle, utilisez un ou plusieurs conteneurs dans la section **[!UICONTROL Internal factors dataset]** . Les données de marketing par e-mail sont un exemple de facteurs internes.

   ![&#x200B; Modèle - Jeu de données de facteurs internes &#x200B;](/help/assets/model-internal-factors-dataset-step.png)

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

   * Pour utiliser les ratios d’investissement marketing historiques afin d’informer le modèle lorsque les données marketing sont rares, activez **[!UICONTROL Allow spend share]**. Ce paramètre est recommandé, en particulier dans les scénarios suivants :
      * Un canal ne contient pas suffisamment d’observations (par exemple, une faible fréquence de dépenses, d’impressions ou de clics).
      * Vous modélisez des médias sophistiqués mais réguliers, et potentiellement coûteux (comme la télévision pour certaines marques), où les données peuvent être éparses.

     >[!NOTE]
     >
     >Pour les investissements ponctuels (par exemple une publicité pour le Super Bowl), pensez à incorporer ces données en tant que facteur plutôt que de compter sur la part de dépenses.
     >


1. Dans la section **[!UICONTROL MTA enabled]** :

   * Pour activer les fonctionnalités MTA pour le modèle, activez **[!UICONTROL MTA enabled]**. Si vous avez activé le MTA, les informations d’attribution multipoint sont disponibles après avoir formé et noté votre modèle. Voir l’onglet [Attribution](insights.md#attribution) dans [Model Insights](insights.md).

1. Dans la section **[!UICONTROL Prior knowledge]** :

   ![Modèle - Connaissances préalables](/help/assets/model-prior-knowledge-step.png)

   1. Sélectionnez l’**[!UICONTROL Rule type]**, qui est **[!UICONTROL Absolute values]** par défaut.

   1. Indiquez les pourcentages de contribution pour l’un des canaux répertoriés sous **[!UICONTROL Name]**, à l’aide de la colonne **[!UICONTROL Contribution proportion]** .

   1. Le cas échéant, vous pouvez ajouter pour chaque canal un pourcentage **[!UICONTROL Level of confidence]**.

   1. Si nécessaire, utilisez **[!UICONTROL Clear all]** pour effacer toutes les valeurs d’entrée des colonnes **[!UICONTROL Contribution proportion]** et **[!UICONTROL Level of confidence]**.


## Définir les options

Vous pouvez [planifier la formation et la notation](#schedule), [définir la fenêtre de formation](#training-window) et spécifier [des champs de rapport d’informations granulaires](#granular-insights-reporting-fields) pour votre modèle à l’étape **[!UICONTROL Set options]**.


### Planning

Dans la section **[!UICONTROL Schedule]** , vous pouvez planifier l’entraînement et la notation des modèles.

![Modèle de planification](../assets/model-schedule.png)

Pour planifier la notation et la formation des modèles :

1. Activez **[!UICONTROL Enable scheduled model scoring and training]**.
1. Sélectionner un **[!UICONTROL Scoring frequency]** :

   * **[!UICONTROL Daily]** : saisissez une heure valide (par exemple, `05:22 pm`) ou utilisez ![Horloge](/help/assets/icons/Clock.svg).
   * **[!UICONTROL Weekly]** : sélectionnez un jour de la semaine et saisissez une heure valide (par exemple, `05:22 pm`) ou utilisez ![Horloge](/help/assets/icons/Clock.svg).
   * **[!UICONTROL Monthly]** : sélectionnez un jour du mois dans le menu déroulant Exécuter sur chaque et saisissez une heure valide (par exemple `05:22 pm`) ou utilisez ![Horloge](/help/assets/icons/Clock.svg).

1. Sélectionnez un **[!UICONTROL Training frequency]** dans le menu déroulant : **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** ou **[!UICONTROL None]**.


### Période de formation

Dans la section **[!UICONTROL Define training window]**, sélectionnez entre :

![Modèle - Définir la fenêtre de formation](/help/assets/model-define-training-window.png)

* **[!UICONTROL Have Mix Modeler select a helpful training window]** et

* **[!UICONTROL Manually input a training window]**. Lorsque cette option est sélectionnée, définissez le nombre d’années dans **[!UICONTROL Include events the following years prior to a conversion]**.


### Champs de création de rapports d’informations granulaires

La section **[!UICONTROL Granular insights reporting fields]** utilise la fonctionnalité de création de rapports d’incrémentalité granulaire. Cette fonctionnalité vous permet de sélectionner des champs harmonisés pour répartir les scores de conversion et d’incrémentalité de point de contact.

![Définir des champs de rapport d’informations granulaires](/help/assets/granular-insights-reporting-fields.png)

Vous définissez ces champs harmonisés afin de pouvoir analyser en profondeur les rapports de votre modèle à l’aide de colonnes de rapports granulaires au lieu d’avoir à créer des modèles distincts.

Par exemple, vous créez un modèle axé sur le chiffre d’affaires, mais vous êtes également intéressé par les performances des campagnes, des types de médias, des régions et des sources de trafic. Sans la fonctionnalité de création de rapports d’incrémentalité granulaire, vous devriez créer quatre modèles distincts. Grâce à la fonctionnalité de création de rapports d’incrémentalité granulaire, vous pouvez ventiler votre modèle de chiffre d’affaires sur les campagnes, les types de médias, les régions et les sources de trafic.

1. Sélectionnez un ou plusieurs champs harmonisés à partir des **[!UICONTROL _Sélectionner les champs harmonisés_]** sous **[!UICONTROL Includes]**. Les champs harmonisés sélectionnés sont ajoutés au panneau.
1. Sélectionnez **[!UICONTROL *Champ harmonisé&#x200B;*]**![CrossSize100](/help/assets/icons/CrossSize100.svg) pour supprimer un champ harmonisé du conteneur avec les champs harmonisés sélectionnés.
1. Sélectionnez **[!UICONTROL Clear all]** pour supprimer tous les champs harmonisés sélectionnés.

Les champs harmonisés sélectionnés pour les rapports d’incrémentalité granulaires sont disponibles dans le cadre des [schéma](/help/ingest-data/schemas.md) et [jeu de données](/help/ingest-data/datasets.md) d’Experience Platform qui résultent de la notation du modèle. Les champs de rapport d’informations granulaires se trouvent dans les objets **[!UICONTROL conversionPassthrough]** et **[!UICONTROL touchpointPassthrough]**.

![Copie d’écran des objets conversionPassthrough et touchpointPassthrough dans un schéma pour un modèle activé pour le compte rendu des performances d’incrémentalité granulaire](/help/assets/schema-granular-insights-reporting.png)


## Terminer

* Sélectionnez **[!UICONTROL Finish]** pour terminer la configuration du modèle.

   * Dans la boîte de dialogue **[!UICONTROL Create instance?]**, sélectionnez **[!UICONTROL Ok]** pour déclencher immédiatement le premier jeu d’exécutions d’entraînement et de notation. Votre modèle est répertorié avec le statut ![StatusOrange](/help/assets/icons/StatusOrange.svg) **[!UICONTROL Awaiting training]**.

     Sélectionnez **[!UICONTROL Cancel]** pour annuler.

   * Si une configuration supplémentaire est nécessaire, un contour et un texte rouges expliquent quelle configuration supplémentaire est requise.

* Sélectionnez **[!UICONTROL Back]** pour revenir à l’étape précédente.

* Sélectionnez **[!UICONTROL Cancel]** pour annuler la configuration du modèle.

