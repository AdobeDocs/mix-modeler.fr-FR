---
title: Informations sur le modèle
description: Découvrez comment obtenir des détails sur votre modèle, tels qu’une vue d’ensemble historique, des informations sur le modèle et la qualité du modèle dans Mix Modeler.
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
source-git-commit: 0a6ed07585f4e2d324159f649efedf2ec6d1b40b
workflow-type: tm+mt
source-wordcount: '2827'
ht-degree: 3%

---

# Informations sur le modèle

Chaque visualisation d’informations sur le modèle est conçue pour vous aider à :

* Visualisez et quantifiez l’impact des activités marketing de votre organisation.
* Identifiez les canaux les plus performants.
* Identifiez les canaux qui peuvent nécessiter une optimisation.

Ces informations vous aident ensuite à prendre en charge la hiérarchisation et l’affectation des ressources.

Pour afficher des informations sur le modèle, dans l’interface ![&#x200B; &#x200B;](/help/assets/icons/FileData.svg)Modèles **[!UICONTROL Models]** de Mix Modeler :

1. Dans le tableau **[!UICONTROL Models]**, sélectionnez le nom d’un modèle dont le **[!UICONTROL Last run status]** est ![StatusGreen](/help/assets/icons/StatusGreen.svg) **[!UICONTROL Success]**.

1. Dans le menu contextuel, sélectionnez **[!UICONTROL Model Insights]**.



Les onglets suivants sont disponibles :

* [Informations sur le modèle](#model-insights)
* [Synergie des canaux](#channel-synergy)
* [Facteurs](#factors-beta) [!BADGE bêta]
* [Attribution](#attribution) (uniquement pour les modèles compatibles avec le MTA)
* [Diagnostic](#diagnostics)
* [Aperçu de l’historique](#historical-overview).

Vous pouvez modifier la période sur laquelle les visualisations de chacun des onglets sont basées. Saisissez une période ou sélectionnez ![Calendrier](/help/assets/icons/Calendar.svg) pour sélectionner une période.

## Dérive du modèle

{{release-limited-testing-section}}

Si une dérive du modèle est détectée sur le modèle, une boîte de dialogue **[!UICONTROL Model drift detected]** s’affiche avec des options à rappeler ultérieurement ou pour [**[!UICONTROL Retrain]**](overview.md#retrain) immédiatement le modèle. Si vous sélectionnez **[!UICONTROL Remind me later]**, un rappel vous est envoyé le lendemain ou lors de la prochaine connexion.

![&#x200B; Boîte de dialogue Détection de dérive du modèle &#x200B;](/help/assets/model-drift-dialog.png)

## [!UICONTROL Model insights]

L’onglet Informations sur les modèles affiche des visualisations pour [Contribution par date et média de base](#contribution-by-date-and-base-media), [Contribution par canal](#contribution-by-channel), [Résumé des performances marketing](#marketing-performance-summary) et [Courbes de réponse marginales](#marginal-response-curves). L’onglet fournit également un tableau [Répartition des points de contact](#touchppint-breakdown).

![Modèle - Informations sur le modèle](/help/assets/model-insights-insights.png)

* Vous pouvez pointer sur des éléments de graphique individuels dans chaque visualisation pour afficher une fenêtre contextuelle avec plus de détails.

* Pour télécharger un fichier CSV contenant les données de la visualisation, sélectionnez ![&#x200B; Télécharger &#x200B;](/help/assets/icons/Download.svg).

* Pour télécharger des données d’informations de modèle complètes au format Microsoft® Excel, sélectionnez ![Télécharger](/help/assets/icons/Download.svg) **[!UICONTROL Download data]**.


### Contribution par date et média de base

Cette visualisation de graphiques empilés est classée comme suit :

* La base s’affiche dans la partie inférieure.
* Les canaux sans dépenses sont affichés au milieu.
* Les canaux de dépenses s’affichent en haut.

Cette visualisation représente la proportion de contribution réalisée par canal de base, par canal de dépense et par canal de non-dépense, sur une période. Cette visualisation est utile pour présenter l’incrémentalité. La base représente ce qui se serait produit sans marketing, et les canaux sans dépenses plus canaux avec dépenses (en plus de la base) attribuent à l’impact de votre marketing. En résumé, la somme dépenses et non dépenses équivaut à l’impact incrémentiel de vos efforts marketing. La visualisation permet d’obtenir facilement insight quant à la valeur générée par le marketing.

### Contribution par canal

Visualisation en anneau qui présente la répartition de la contribution par différents canaux. Cette visualisation présente l’incrémentalité à travers le prisme des trois canaux les plus performants (à l’exclusion des catégories de base et *Tous les autres*). La visualisation permet de prendre en charge la hiérarchisation et la répartition budgétaire.

### Résumé des performances marketing {#marketing-performance-summary}


>[!CONTEXTUALHELP]
>id="models_insights_marketingperformancesummary"
>title="Canaux non définis"
>abstract="Les canaux non définis sont inclus, mais n’ont aucune conversion attribuée."


Visualisation sous forme de graphique à barres horizontal qui affiche le retour sur investissement ou les performances du CPA pour chacun des canaux. Cette visualisation met en évidence le retour sur investissement/le CPA de vos investissements marketing. Les canaux sont classés par ordre décroissant en fonction du retour sur investissement/CPA. La visualisation permet d’identifier les canaux les plus efficaces et ceux qui peuvent nécessiter une optimisation.

Les canaux non définis sont inclus dans la visualisation mais n’ont pas de conversions attribuées.


### Courbes de réponse marginales

Le graphique en courbes permet de visualiser et de comparer les rendements marginaux générés par l’investissement dans vos canaux marketing.  Il identifie le point de dépense actuel et le seuil de rentabilité marginal (où votre rendement incrémentiel est inférieur à vos dépenses incrémentielles). Par conséquent, cette visualisation vous aide à comprendre à quel moment votre investissement marketing commence à perdre en efficacité.

La courbe, le point de dépense actuel, le seuil de rentabilité marginal et les valeurs correspondantes sont calculés en fonction de la plage de données sélectionnée et du canal sélectionné.

Pour modifier le canal :

* Sélectionnez un canal dans le menu déroulant **[!UICONTROL Channel]** pour mettre à jour la visualisation d’un canal spécifique.


### Répartition des points de contact

Le tableau de répartition des points de contact affiche les répartitions hebdomadaires des points de contact pour tous les canaux ou pour certains canaux, sur une base hebdomadaire, affichant les mesures clés associées à chacun. Le tableau permet une comparaison facile, une identification des tendances et un suivi des performances à un niveau de canal plus granulaire. Ce tableau complète explicitement la visualisation [Contribution par date et média de base](#contribution-by-date-and-base-media) et la visualisation [Contribution par canal](#contribution-by-channel).

![Répartition des points de contact](../assets/touchpoint-breakdown.png)

Les colonnes disponibles sont les suivantes :

| Colonne | Description |
|---|---|
| **[!UICONTROL Date range]** | Semaine du rapport. |
| **[!UICONTROL Touchpoint]** | Canal de point de contact spécifique. |
| **[!UICONTROL ROI]** | Pourcentage de (**[!UICONTROL Revenue]** - **[!UICONTROL Spend]**) / **[!UICONTROL Spend]**. |
| **[!UICONTROL Revenue]** | Chiffre d’affaires de la période. |
| **[!UICONTROL CPA]** | **[!UICONTROL Spend]** / **[!UICONTROL Conversions]**. |
| **[!UICONTROL Conversions]** | Conversions pour la période. |
| **[!UICONTROL Spend]** | Dépenses pour la plage de données. |

Pour sélectionner un canal spécifique ou tous les canaux, sélectionnez dans le menu déroulant **[!UICONTROL View]**.

Pour télécharger le contenu du tableau de répartition des points de contact, sélectionnez ![Télécharger](/help/assets/icons/Download.svg) **[!UICONTROL Download CSV]**.


## Synergie des canaux

Dans l’onglet **[!UICONTROL Channel synergy]** , la visualisation **[!UICONTROL Channel synergies]** vous permet d’identifier comment les canaux marketing interagissent pour créer des effets multiplicatifs, au-delà de leurs contributions individuelles.

La matrice de carte thermique fournit une représentation visuelle des valeurs de synergie entre les paires de canaux de dépenses. Cette matrice permet aux professionnels du marketing de comprendre comment les canaux interagissent pour stimuler les performances. Pour chaque modèle, les valeurs de synergie sont normalisées de 0 à 10. Ces valeurs quantifient la *synergie du prochain dollar*, qui estime l&#39;efficacité de la collaboration entre deux canaux lorsque chacun reçoit un dollar supplémentaire de dépenses aux niveaux actuels.

Ce cadre de plus-value offre une mesure réaliste de la force relative de la synergie, car il tient compte des conditions de dépenses réelles dans les données de formation et permet ainsi de prendre des décisions d’optimisation plus éclairées.

![Planifier les synergies de canaux](/help/assets/model-channel-synergies.png)

Pour télécharger un fichier CSV qui représente la matrice, sélectionnez ![&#x200B; Télécharger &#x200B;](/help/assets/icons/Download.svg) **[!UICONTROL Download]**.

>[!NOTE]
>
>Si l’onglet **[!UICONTROL Channel synergy]** n’est pas visible pour un modèle existant, veillez à entraîner à nouveau le modèle pour activer la fonctionnalité et la visualisation.



## **[!UICONTROL Factors]** [!BADGE version bêta] {#factors}

>[!CONTEXTUALHELP]
>id="models_factors_factorcontributionbreakdown"
>title="Répartition de la contribution des facteurs"
>abstract="La répartition de la contribution des facteurs indique la proportion des conversions de base qui peuvent être attribuées aux différents facteurs inclus dans le modèle.<br/><br/>La base pure représente les conversions sous-jacentes qui se produisent indépendamment des points de contact marketing et des facteurs inclus dans le modèle. Il comprend des conversions axées sur les actions de la marque, les achats répétés, la demande organique, les tendances du marché à long terme et le caractère saisonnier."


L’onglet Facteurs [!BADGE version bêta] affiche des informations externes liées aux facteurs.

![&#x200B; Facteurs &#x200B;](/help/assets/factors.png)

Cette visualisation vous aide à comprendre l’effet incrémentiel que divers facteurs internes et externes ont sur la ligne de base des conversions. Par exemple, conditions économiques ou activités promotionnelles.

Utilisez le menu déroulant **[!UICONTROL Factors]** pour sélectionner les facteurs à afficher.

<!-- need to update the image when we do have a proper example -->

Pour télécharger un fichier CSV contenant les données du tableau, sélectionnez ![Télécharger](/help/assets/icons/Download.svg).

Si aucune donnée n’est disponible, un message ![TableAndChart](/help/assets/icons/TableAndChart.svg) s’**[!UICONTROL No data is available, you may need to retrain your model, or change the date range to view insights]**.

## [!UICONTROL Attribution] {#attribution}


>[!CONTEXTUALHELP]
>id="models_attribution_breakdownbychannel"
>title="Répartition par canal"
>abstract="**[!UICONTROL Breakdown by channel]** est une répartition par type de canal pour les points de contact définis, basée sur le schéma d’événement de l’expérience client. Sélectionnez ![Plus](https://spectrum.adobe.com/static/icons/workflow_18/Smock_MoreSmallList_18_N.svg) et **[!UICONTROL Breakdown by touchpoint]** pour afficher une répartition par point de contact."


>[!CONTEXTUALHELP]
>id="models_attribution_breakdownbytouchpointposition"
>title="Répartition par position du point de contact"
>abstract="Cette visualisation présente une répartition des conversions attribuées par position du point de contact et par point de contact sur tous les chemins de conversion. La visualisation permet de comparer si un point de contact contribue mieux à une position que les positions restantes et les autres points de contact à n’importe quelle position. Notez que la somme des contributions en pourcentage pour un modèle d’attribution sur tous les points de contact et postes serait égale à 100. Les postes de débutant, d&#39;influenceur et de finisseur sont définis comme suit :<ul><li>**Starter** : indique si le point de contact est la première touche d’un chemin de conversion.</li><li>**Lecteur** : indique si le point de contact n’est ni la première ni la dernière touche menant à une conversion.</li><li>**Plus proche** : indique si le point de contact est le dernier contact avant la conversion.</li></ul>"



>[!NOTE]
>
>L’onglet Attribution n’est disponible que pour les modèles compatibles avec le MTA.


Grâce à l’onglet [!UICONTROL Attribution] , vous pouvez comprendre l’efficacité des points de contact et des campagnes marketing qui contiennent des données au niveau de l’événement.  Voir [Créer un modèle](build.md).

Les modèles d’attribution suivants sont pris en charge :

* En fonction du modèle sélectionné dans Mix Modeler :
   * Algorithmique - influencé
   * Algorithmique - incrémentiel
* Basé sur des règles :
   * Unités d’atténuation
   * Première touche
   * Dernière touche
   * Linéaire
   * Ushape

Consultez [Attribution multipoint](../get-started/about.md#multi-touch-attribution) pour une introduction sur la fonctionnalité d’attribution multipoint dans Mix Modeler.

Sélectionnez un ou plusieurs modèles d’attribution dans le menu déroulant **[!UICONTROL Attribution Model]** . Les modèles d’attribution sélectionnés s’appliquent à toutes les visualisations dans l’onglet Attribution.

![Attribution](/help/assets/model-insights-attribution.png)

Les scores d’événement granulaire d’attribution multipoint Mix Modeler s’alignent sur les scores globaux de Mix Modeler et sur les RSI. Ces scores sont également disponibles sous forme de jeux de données dans Experience Platform.

L’onglet Attribution comprend les visualisations suivantes :

### [!UICONTROL Overview]

La visualisation [!UICONTROL Overview] affiche, pour les modèles d’attribution sélectionnés, les totaux et pourcentages des conversions. La sélection d’autres modèles ajoute des cercles supplémentaires à la visualisation, chacun ayant sa propre couleur correspondant à la légende.

Pour afficher une fenêtre contextuelle contenant des détails sur un modèle d’attribution, passez la souris sur l’un des cercles de la visualisation.

### [!UICONTROL Trends]

La visualisation [!UICONTROL Daily trends], [!UICONTROL Weekly trends] ou [!UICONTROL Monthly trends] affiche, pour les modèles d’attribution sélectionnés, les tendances de conversion quotidiennes, hebdomadaires ou mensuelles.

Pour choisir la période, sélectionnez **[!UICONTROL Daily trends]**, **[!UICONTROL Weekly trends]** ou **[!UICONTROL Monthly trends]** dans ![Plus](/help/assets/icons/More.svg).

Pour afficher des détails, pointez sur la ligne de données d’un modèle d’attribution spécifique afin d’afficher une fenêtre contextuelle qui indique le nombre total de conversions de ces données.

### [!UICONTROL Breakdown]

La visualisation [!UICONTROL Breakdown] est une répartition par canal ou point de contact des conversions pour chacun des modèles d’attribution sélectionnés. Cette visualisation peut s’avérer utile pour prendre des décisions sur l’efficacité de chaque canal ou point de contact.

Pour choisir le type de répartition, sélectionnez **[!UICONTROL Breakdown by channel]** ou **[!UICONTROL Breakdown by touchpoint]** dans ![&#x200B; Plus &#x200B;](/help/assets/icons/More.svg).

Pour afficher les détails, pointez sur l’un des éléments du graphique.

### [!UICONTROL Top campaigns]

La visualisation des principales campagnes présente un tableau des principales campagnes avec des colonnes pour le nom de la campagne, le canal, le type de média et les conversions incrémentielles. Cette visualisation peut informer votre équipe de l’efficacité d’une campagne spécifique pour un canal donné et fournir des informations sur les campagnes dans lesquelles vous devriez investir davantage.

Pour trier le tableau par ordre croissant ↑ décroissant ↓ pour les conversions de canal, de type de média ou incrémentielles, sélectionnez l’en-tête de colonne et activez le tri.

Pour développer le tableau dans une boîte de dialogue distincte, sélectionnez **[!UICONTROL Expand]** dans ![Plus](/help/assets/icons/More.svg).

La boîte de dialogue Développée Principales campagnes affiche le même tableau avec des colonnes supplémentaires pour

* Conversions incrémentielles
* Conversions influencées
* Conversions Première touche
* Conversions Dernière touche

  Vous pouvez sélectionner chacun des en-têtes de colonne supplémentaires pour trier le tableau par ordre croissant ou décroissant.

Pour fermer la boîte de dialogue Développée Principales campagnes , sélectionnez **[!UICONTROL Close]**.


### [!UICONTROL Breakdown by touchpoint position]

La visualisation [!UICONTROL Breakdown by touchpoint position] est une répartition des conversions attribuées par position du point de contact et par point de contact sur tous les chemins de conversion. Ce graphique vous permet de comparer si un point de contact contribue mieux à une position que les positions restantes et d’autres points de contact à n’importe quelle position.

>[!NOTE]
>
>La somme des contributions en pourcentage pour un modèle d’attribution à tous les points de contact et postes doit être égale à 100.


Les positions [!UICONTROL Starter], [!UICONTROL Player] et [!UICONTROL Closer] sont définies comme suit :

| Position | Description |
|---|---|
| [!UICONTROL Starter] | Cette position indique si le point de contact est le premier contact d’un chemin de conversion. |
| [!UICONTROL Player] | Cette position indique si le point de contact n’est pas le premier ou le dernier contact menant à une conversion. |
| [!UICONTROL Closer] | Cette position indique si le point de contact est le dernier contact avant la conversion. |


### [!UICONTROL Top conversion paths]

La visualisation [!UICONTROL Top conversion paths] présente les 5 premiers chemins de conversion en fonction des modèles d’attribution sélectionnés.

Pour chaque chemin de conversion, vous voyez :

* le nombre de canaux qui ont un impact,
* le nombre total de chemins attribués,
* le pourcentage de chemins attribués à ce chemin de conversion par rapport au nombre total de chemins attribués,
* pour chaque canal, le pourcentage de contribution du modèle d’attribution, et
* somme de ces pourcentages de contribution du modèle d’attribution de canal.


## [!UICONTROL Diagnostics] {#diagnostics}

>[!CONTEXTUALHELP]
>id="models_diagnostics_modelassessment"
>title="Graphiques d’évaluation des modèles"
>abstract="Les visualisations de l’évaluation des modèles se répartissent entre les conversions réelles, prévues et résiduelles."
>additional-url="https://experienceleague.adobe.com/fr/docs/mix-modeler/using/overview" text="Vue d’ensemble de Mix Modeler"
>additional-url="https://video.tv.adobe.com/v/3440796/?captions=fre_fr&learn=on&enablevpops" text="Démonstration de Mix Modeler"


>[!CONTEXTUALHELP]
>id="models_diagnostics_modeltrainingfitmetrics"
>title="Mesures d’ajustement du modèle"
>abstract="Affiche un aperçu de plusieurs mesures d’ajustement de l’entraînement des modèles."


>[!CONTEXTUALHELP]
>id="models_diagnostics_pathstouched"
>title="Chemins touchés"
>abstract="Les chemins touchés correspondent au pourcentage de chemins générant une conversion et le pourcentage de chemins ne générant pas de conversion pour chaque point de contact."


>[!CONTEXTUALHELP]
>id="models_diagnostics_efficiencymeasure"
>title="Mesure d&#39;efficacité"
>abstract="La mesure d’efficacité générée par le modèle d’attribution algorithmique indique l’importance relative d’un point de contact pour la conversion indépendamment du volume de points de contact. Elle est mesurée sur une échelle de 1 à 5. Notez qu’un volume de points de contact plus élevé ne garantit pas une mesure d’efficacité plus élevée."


>[!CONTEXTUALHELP]
>id="models_diagnostics_totalvolume"
>title="Volume total"
>abstract="Le volume total est le nombre agrégé de fois qu’un point de contact a été touché par un utilisateur et inclut les points de contact qui apparaissent sur un chemin générant une conversion, ainsi que sur les chemins ne générant pas de conversion."


>[!CONTEXTUALHELP]
>id="models_diagnostics_modeldateinfo"
>title="Date du modèle au"
>abstract="Les données de cette table ne sont générées que pour des périodes spécifiques.  La date de **[!UICONTROL As of]** indique la date à laquelle les données ont été générées. Elle est basée sur les données de startDate à endDate."


L’onglet **[!UICONTROL Diagnostics]** affiche les visualisations pour :

* **[!UICONTROL Model Assessment]** visualisations qui consistent en :

  ![Évaluation du modèle](../assets/model-assessment.png)

   * Graphique qui permet de ventiler les conversions réelles par rapport aux conversions prévues ou résiduelles.
Pour ventiler la visualisation, sélectionnez l’une des options suivantes dans la liste **[!UICONTROL Breakdown]**.

      * **[!UICONTROL Actual vs Predicted]** : cette option compare les valeurs réelles aux prédictions du modèle. Idéalement, les valeurs prédites doivent être étroitement alignées sur les valeurs réelles, bien qu’un certain écart soit attendu. Des écarts ou des modèles importants ou systématiques peuvent indiquer des relations manquantes et des données ou des biais potentiels.

      * **[!UICONTROL Residuals]** : cette option affiche la différence entre les valeurs réelles et les valeurs prévues. Un modèle performant a des résidus qui sont distribués de manière aléatoire, sans modèles clairs ni augmentation de la propagation. Les tendances structurées ou l’élargissement des résidus peuvent signaler des relations manquantes et des problèmes de données ou de variance.

   * Un tableau présentant les colonnes suivantes pour chaque mesure de conversion :

      * **[!UICONTROL Actual Conversion]**
      * **[!UICONTROL Predicted Conversion]**
      * **[!UICONTROL Residual Conversion]**
      * **[!UICONTROL R<sup>2</sup>]**, un score qui indique dans quelle mesure les données s’adaptent au modèle de régression (la justesse de l’adaptation).
      * **[!UICONTROL MAPE]** (Erreur de pourcentage absolue moyenne), qui est l’un des indicateurs clés de performance les plus couramment utilisés pour mesurer la précision des prévisions et qui exprime l’erreur de prévision en pourcentage de la valeur réelle.
      * **[!UICONTROL RMSE]** (erreur quadratique moyenne racine) : qui affiche l’erreur moyenne, pondérée en fonction du carré de l’erreur.

  Pour télécharger un fichier CSV contenant les données du tableau, sélectionnez ![Télécharger](/help/assets/icons/Download.svg).

* **[!UICONTROL Model training fit metrics]** tableau qui s’affiche pour chaque mesure de conversion :

  ![Tableau des mesures d’adéquation de l’entraînement du modèle](../assets/model-training-fit-metrics.png)

   * **[!UICONTROL Training R<sup>2</sup>]** : indique la proportion de variance des valeurs réelles expliquées par les prédictions du modèle, allant de 0 à 1.
   * **[!UICONTROL Training sMAPE]** (erreur en pourcentage absolu moyen symétrique) : mesure l’erreur en pourcentage moyen sur les données d’identification. Des valeurs plus faibles indiquent une meilleure précision.
   * **[!UICONTROL Training RMSE]** (erreur quadratique moyenne racine) : mesure l’erreur moyenne en pourcentage sur les données d’identification. Pénalise les erreurs plus importantes que la MAPE. Une RMSE plus faible suggère une meilleure précision prédictive, mais est sensible aux valeurs aberrantes.
   * **[!UICONTROL Out-of-sample sMAPE]** : évalue l’erreur en pourcentage sur les données non vues, en équilibrant les sur-et-sous-prédictions. Permet d’évaluer la généralisation. Actuellement, Mix Modeler évalue le pourcentage d’erreur en utilisant le dernier trimestre des données d’identification comme ensemble d’exclusions.
   * **[!UICONTROL Out-of-sample RMSE]** : évalue l’erreur en pourcentage sur les données non vues, en équilibrant les sur-et-sous-prédictions. Permet d’évaluer la généralisation. Actuellement, Mix Modeler évalue le pourcentage d’erreur en utilisant le dernier trimestre des données d’identification comme ensemble d’exclusions. Le RMSE pénalise plus les erreurs plus importantes que le MAPE.


* **[!UICONTROL Touchpoint effectiveness]** tableau, représentant le résultat du modèle algorithmique de l’IA dédiée à l’attribution.

  ![Tableau d’efficacité des points de contact](../assets/touchpoint-effectiveness.png)

  Les données de cette table ne sont générées que pour des périodes spécifiques. Sélectionnez **[!UICONTROL As of *xx/xx/xx, xx:xx TZ *]**![Info](/help/assets/icons/InfoOutline.svg) pour plus d’informations.

  La visualisation affiche, par ordre décroissant de [!UICONTROL Efficiency measure] ![ordre décroissant](/help/assets/icons/SortOrderDown.svg), pour chaque point de contact :

   * **[!UICONTROL Paths touched]** : permet de visualiser le pourcentage de chemins générant une conversion et le pourcentage de chemins ne générant pas de conversion. Pour un point de contact, vous voyez plus de conversions attribuées lorsque le taux de conversion d’attribution est élevé. Ce rapport compare le pourcentage de chemins qui mènent à la conversion par rapport au pourcentage de chemins qui ne mènent *pas* à la conversion.
   * **[!UICONTROL Efficiency measure]** : générée par le modèle d’attribution algorithmique, la mesure d’efficacité indique l’importance relative d’un point de contact pour la conversion, indépendamment du volume de points de contact. L&#39;efficacité est mesurée sur une échelle de 1 à 5. Notez qu’un volume de points de contact plus élevé ne garantit pas une mesure d’efficacité plus élevée.
   * **[!UICONTROL Total volume]** : nombre agrégé de fois qu’un utilisateur touche un point de contact. Le nombre inclut les points de contact qui apparaissent sur un chemin générant une conversion, ainsi que sur les chemins *non* générant une conversion.


### Détection de dérive de modèle

>[!AVAILABILITY]
>
>La fonctionnalité décrite dans cette section se trouve dans la phase de test limité de la publication et peut ne pas encore être disponible dans votre environnement. Cette note est supprimée lorsque la fonctionnalité est disponible. Pour plus d’informations sur le processus de publication de Mix Modeler, consultez [Versions des fonctionnalités de Mix Modeler](/help/releases/latest.md).
>

Si une dérive du modèle est détectée, une notification **[!UICONTROL Model drift detected]** s’affiche en haut de l’écran.

![Notification de dérive du modèle](/help/assets/model-drift-notification.png)

Sélectionnez **[!UICONTROL Hide]** pour masquer la notification. La notification réapparaîtra le lendemain ou lors de la prochaine connexion.


## [!UICONTROL Historical overview]

L’onglet Aperçu de l’historique affiche des visualisations pour :

![Modèle - Aperçu de l’historique](/help/assets/model-insights-historical-overview.png)


### Conversion et dépenses par trimestre fiscal et produit

Cette visualisation représente la distribution des conversions et des dépenses sur différents trimestres au cours de la période donnée. La visualisation permet d’identifier les trimestres très performants où les dépenses génèrent des conversions.


### Dépenses par canal

Cette visualisation représente la distribution des dépenses sur divers canaux au cours de la période donnée. La visualisation permet d’identifier rapidement les canaux qui reçoivent le plus de dépenses.


### Dépenses du point de contact

Cette visualisation représente la répartition des dépenses entre les points de contact payés pour chaque trimestre de la période donnée. La visualisation permet de comprendre quels points de contact sont prioritaires au sein de canaux et de trimestres spécifiques. La visualisation permet d’identifier les modèles et les tendances des dépenses des canaux, en particulier les canaux avec des dépenses faibles et peu fréquentes au fil du temps.

Pour sélectionner un autre canal basé sur les dépenses à afficher pour cette visualisation :

* Sélectionnez un canal dans **[!UICONTROL Channels]**.


### Volume de points de contact

Cette visualisation représente la distribution du volume sur tous les points de contact pour chaque trimestre dans la période donnée.

Pour sélectionner un autre canal basé sur le volume à afficher pour cette visualisation :

* Sélectionnez un canal dans **[!UICONTROL Channels]**.


## **[!UICONTROL Edit]**

Vous pouvez modifier le nom, la description, la planification de l’entraînement et la notation du modèle.

1. Sélectionnez ![&#x200B; Modifier &#x200B;](/help/assets/icons/Edit.svg) Modifier .

1. Dans la boîte de dialogue **[!UICONTROL Edit model]** :

   * Saisissez un nouveau **[!UICONTROL Name]** et une nouvelle **[!UICONTROL Description]**.

   * Pour activer la planification, activez **[!UICONTROL Status]**. Vous pouvez uniquement activer la planification pour les modèles entraînés et notés.

      1. Sélectionner un **[!UICONTROL Scoring frequency]** :

         * **[!UICONTROL Daily]** : saisissez une heure valide (par exemple, `05:22 pm`) ou utilisez ![Horloge](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Weekly]** : sélectionnez un jour de la semaine et saisissez une heure valide (par exemple, `05:22 pm`) ou utilisez ![Horloge](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Monthly]** : sélectionnez un jour du mois dans le menu déroulant Exécuter sur chaque et saisissez une heure valide (par exemple `05:22 pm`) ou utilisez ![Horloge](/help/assets/icons/Clock.svg).

      1. Sélectionnez un **[!UICONTROL Training frequency]** dans le menu déroulant : **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** ou **[!UICONTROL None]**.

     ![Modifier un modèle](../assets/model-edit.png)

1. Sélectionnez **[!UICONTROL Save]**.
