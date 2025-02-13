---
title: Informations sur le modèle
description: Découvrez comment obtenir des détails sur votre modèle, tels qu’une vue d’ensemble historique, des informations sur le modèle et la qualité du modèle dans Mix Modeler.
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
source-git-commit: 0ee212a626986e4c721d0e58f2528d0ca1a9fdbf
workflow-type: tm+mt
source-wordcount: '1549'
ht-degree: 0%

---

# Informations sur le modèle

Pour afficher des informations sur le modèle, dans l’interface **[!UICONTROL Models]** ![Modèles](/help/assets/icons/FileData.svg) de Mix Modeler :

1. Dans le tableau **[!UICONTROL Models]**, sélectionnez le nom d’un modèle dont le **[!UICONTROL Last run status]** est <span style="color:green">●</span> **[!UICONTROL Success]**.

1. Dans le menu contextuel, sélectionnez **[!UICONTROL Model Insights]**.

![Barre d’onglets Model Insights](/help/assets/model-insights-tabbar.png)

Vous pouvez voir quand le modèle spécifié est actualisé pour la dernière fois et les visualisations s’affichent à l’aide de quatre onglets : [Informations sur le modèle](#model-insights), [Attribution](#attribution), [Facteurs](#factors), [Diagnostics](#diagnostics) et [Aperçu de l’historique](#historical-overview).

Vous pouvez modifier la période sur laquelle les visualisations de chacun des onglets sont basées. Saisissez une période ou sélectionnez ![Calendrier](/help/assets/icons/Calendar.svg) pour sélectionner une période.

## [!UICONTROL Model insights]

L’onglet Model insights affiche des visualisations pour [Contribution par date et média](#contribution-by-date-and-base-media) de base, [Contribution par canal](#contribution-by-channel), [Résumé](#marketing-performance-summary) des performances marketing et [Courbes de réponse marginale](#marginal-response-curves). L’onglet présente également un tableau de ventilation](#touchppint-breakdown) des points de [contact.

![Modèle - Aperçu du modèle](/help/assets/model-insights-insights.png)

* Vous pouvez survoler des éléments de graphique individuels dans chaque visualisation pour afficher une fenêtre contextuelle avec plus de détails.

* Pour télécharger un fichier CSV contenant les données de la visualisation, sélectionnez ![Télécharger](/help/assets/icons/Download.svg).

* Pour télécharger des données d’informations de modèle complètes au format Microsoft® Excel, sélectionnez ![Télécharger](/help/assets/icons/Download.svg) **[!UICONTROL Download data]**.


### Contribution par date et média de base.

Le graphique empilé est trié en fonction des valeurs suivantes : Base en bas, Canaux sans dépenses en milieu et Canaux Dépenses en haut.

### Contribution par canal

La visualisation en anneau montre la répartition de la contribution par canal.

### Résumé des performances marketing.

Graphique à barres horizontal affichant les performances du retour sur investissement par canal.

### Courbes de réponse marginales.

Le graphique en courbes permet de visualiser et de comparer les rendements marginaux générés par l’investissement dans vos canaux marketing.  et identifie le point d’équilibre où votre rendement incrémentiel est inférieur à vos dépenses incrémentielles. Par conséquent, cette visualisation vous aide à comprendre à quel moment votre investissement marketing commence à perdre en efficacité.

La courbe, le point mort et les valeurs correspondantes sont calculés en fonction de la plage de données sélectionnée et du canal sélectionné.

Pour modifier le canal :

* Sélectionnez un canal dans le menu déroulant **[!UICONTROL Channel]** pour mettre à jour la visualisation d’un canal spécifique.


### Répartition des points de contact

Le tableau de répartition des points de contact affiche les répartitions des points de contact pour tous les canaux ou pour certains canaux sur une base hebdomadaire.

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

## **[!UICONTROL Factors]** [!BADGE version bêta]

L’onglet Facteurs [!BADGE version bêta] affiche des informations externes liées aux facteurs.

![ Facteurs ](/help/assets/factors.png)

Cette visualisation vous aide à comprendre l’effet incrémentiel que divers facteurs internes et externes ont sur la ligne de base des conversions. Par exemple, conditions économiques ou activités promotionnelles.

Utilisez le menu déroulant **[!UICONTROL Factors]** pour sélectionner les facteurs à afficher.

<!-- need to update the image when we do have a proper example -->

Pour télécharger un fichier CSV contenant les données du tableau, sélectionnez ![Télécharger](/help/assets/icons/Download.svg).

Si aucune donnée n’est disponible, un message ![TableAndChart](/help/assets/icons/TableAndChart.svg) s’**[!UICONTROL No data is available, you may need to retrain your model, or change the date range to view insights]**.

## [!UICONTROL Attribution]

>[!NOTE]
>
L’onglet Attribution n’est disponible que pour les modèles compatibles avec le MTA.


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

Pour afficher une fenêtre contextuelle avec des détails sur un modèle d’attribution, passez la souris sur l’un des cercles de la visualisation.

### [!UICONTROL Trends]

La [!UICONTROL Daily trends]visualisation , [!UICONTROL Weekly trends]ou [!UICONTROL Monthly trends] affiche, pour les modèles d’attribution sélectionnés, les tendances de conversion quotidiennes, hebdomadaires ou mensuelles.

Pour choisir la période, sélectionnez **[!UICONTROL Daily trends]** ou **[!UICONTROL Weekly trends]** **[!UICONTROL Monthly trends]** de plus![](/help/assets/icons/More.svg).

Pour afficher les détails, passez la souris sur la ligne de données d’un modèle d’attribution spécifique pour afficher une fenêtre contextuelle indiquant le nombre total de conversions pour ces données.

### [!UICONTROL Breakdown]

La visualisation [!UICONTROL Breakdown] est une répartition par canal ou point de contact des conversions pour chacun des modèles d’attribution sélectionnés. Cette visualisation peut s’avérer utile pour prendre des décisions sur l’efficacité de chaque canal ou point de contact.

Pour choisir le type de répartition : select **[!UICONTROL Breakdown by channel]** ou **[!UICONTROL Breakdown by touchpoint]** de ![Plus](/help/assets/icons/More.svg).

Pour afficher les détails, survolez l’un des éléments du graphique.

### [!UICONTROL Top campaigns]

La visualisation Principales campagnes affiche un tableau des principales campagnes avec des colonnes pour Campaign nom, canal ou type de média. and Conversions incrémentielles. Cette visualisation peut aider à informer votre équipe de l’efficacité d’une campagne spécifique pour un canal donné et fournir des informations sur les campagnes dans lesquelles vous devriez investir davantage.

Pour trier le tableau par ↑ croissant ou par ordre décroissant ↓ canal, saisissez Média . or Conversions incrémentielles : sélectionnez l’en-tête de colonne et activez le tri.

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
La somme des contributions en pourcentage pour un modèle d’attribution à tous les points de contact et postes doit être égale à 100.


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


## [!UICONTROL Diagnostics]

L’onglet Diagnostics affiche des visualisations pour :

* [!UICONTROL Model Assessment] la visualisation, que vous pouvez ventiler selon les conversions réelles, prévues ou résiduelles.

Pour ventiler la visualisation, sélectionnez **[!UICONTROL Actual vs. Predicted]** ou **[!UICONTROL Residuals]** dans la liste **[!UICONTROL Breakdown]**.

* [!UICONTROL Model fitting metrics] tableau, présentant les colonnes suivantes pour chaque mesure de conversion :

   * Conversion réelle

   * Conversion Modélisée

   * Conversion résiduelle (différence entre la conversion réelle et la conversion modélisée)

   * Valeurs du score de qualité du modèle :

      * R2 (carré R), qui indique dans quelle mesure les données correspondent au modèle de régression (la validité de l’ajustement).

      * Le MAPE (Mean Absolute Percentage Error), qui est l’un des indicateurs clés les plus couramment utilisés pour mesurer la précision des prévisions. Il exprime l’erreur de prévision sous la forme d’un pourcentage de la valeur réelle.

      * RMSE (Root Mean Square Error) : indique l’erreur moyenne, pondérée en fonction du carré de l’erreur.

Pour télécharger un fichier CSV contenant les données du tableau, sélectionnez ![Télécharger](/help/assets/icons/Download.svg).

* [!UICONTROL Touchpoint effectiveness] tableau, représentant le résultat du modèle algorithmique de l’IA dédiée à l’attribution. Les données de ce tableau ne sont générées que pour des périodes spécifiques. Sélectionnez **[!UICONTROL As of *xx/xx/xx, xx:xx TZ *]**![Info](/help/assets/icons/InfoOutline.svg) pour plus d’informations.

La visualisation affiche, par ordre décroissant de [!UICONTROL Efficiency measure] ![ordre décroissant](/help/assets/icons/SortOrderDown.svg), pour chaque point de contact :

   * [!UICONTROL Paths touched] : permet de visualiser le pourcentage de chemins générant une conversion et le pourcentage de chemins ne générant pas de conversion. Pour un point de contact, vous voyez plus de conversions attribuées lorsque le taux de conversion d’attribution est élevé. Ce rapport compare le pourcentage de chemins qui mènent à la conversion par rapport au pourcentage de chemins qui ne mènent *pas* à la conversion.
   * [!UICONTROL Efficiency measure] : générée par le modèle d’attribution algorithmique, la mesure d’efficacité indique l’importance relative d’un point de contact pour la conversion, indépendamment du volume de points de contact. L&#39;efficacité est mesurée sur une échelle de 1 à 5. Notez qu’un volume de points de contact plus élevé ne garantit pas une mesure d’efficacité plus élevée.
   * [!UICONTROL Total volume] : nombre agrégé de fois qu’un utilisateur touche un point de contact. Le nombre inclut les points de contact qui apparaissent sur un chemin générant une conversion, ainsi que sur les chemins *non* générant une conversion.

![ Diagnostics ](/help/assets/model-insights-diagnostics.png)


## [!UICONTROL Historical overview]

L’onglet Aperçu de l’historique affiche des visualisations pour :

* Conversion et dépenses par trimestre fiscal et produit.

* Dépenses par canal.

* Dépenses liées au point de contact.

Vous pouvez sélectionner un autre canal basé sur les dépenses à afficher pour cette visualisation. Sélectionnez un canal dans **[!UICONTROL Channels]** le fichier .

* Volume du point de contact.

Vous pouvez sélectionner un autre canal basé sur le volume à afficher pour cette visualisation. Sélectionnez un canal dans **[!UICONTROL Channels]**.

![Modèle - Aperçu de l’historique](/help/assets/model-insights-historical-overview.png)

## **[!UICONTROL Edit]**

Vous pouvez modifier le nom, la description et la planification de la formation et de la notation du modèle.

1. Sélectionnez ![Modifier](/help/assets/icons/Edit.svg) , Modifier

1. Dans la boîte de **[!UICONTROL Edit model]** dialogue :

   * Entrez un nouveau **[!UICONTROL Name]** et **[!UICONTROL Description]**.

   * Pour activer la planification, activez **[!UICONTROL Status]**. Vous pouvez uniquement activer la planification pour les modèles entraînés et notés.

      1. Sélectionner un **[!UICONTROL Scoring frequency]** :

         * **[!UICONTROL Daily]** : saisissez une heure valide (par exemple, `05:22 pm`) ou utilisez ![Horloge](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Weekly]** : sélectionnez un jour de la semaine et saisissez une heure valide (par exemple, `05:22 pm`) ou utilisez ![Horloge](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Monthly]** : sélectionnez un jour du mois dans le menu déroulant Exécuter sur chaque et saisissez une heure valide (par exemple `05:22 pm`) ou utilisez ![Horloge](/help/assets/icons/Clock.svg).

      1. Sélectionnez un **[!UICONTROL Training frequency]** dans le menu déroulant : **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** ou **[!UICONTROL None]**.

     ![Modifier un modèle](../assets/model-edit.png)

1. Sélectionnez **[!UICONTROL Save]**.
