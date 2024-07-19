---
title: Informations sur les modèles
description: Découvrez comment obtenir des détails sur votre modèle, tels qu’une présentation historique, des informations sur les modèles et la qualité des modèles en Mix Modeler.
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '1159'
ht-degree: 0%

---

# Informations sur les modèles

Pour afficher les informations sur les modèles, dans l’interface ![Modèles](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** en Mix Modeler :

1. Dans la table **[!UICONTROL Models]**, sélectionnez le nom d&#39;un modèle dont le **[!UICONTROL Last run status]** de <span style="color:green">●</span> **[!UICONTROL Success]**.

1. Dans le menu contextuel, sélectionnez **[!UICONTROL Model Insights]**.

![Barre d’onglets d’informations sur les modèles](/help/assets//model-insights-tabbar.png)

Vous voyez le moment où le modèle spécifié est actualisé pour la dernière fois et où les widgets s’affichent à l’aide de quatre onglets : [Model insights](#model-insights), [Attribution](#attribution), [Diagnostics](#diagnostics) et [Présentation historique](#historical-overview).

Vous pouvez modifier la période sur laquelle reposent les widgets sur chacun des onglets. Entrez une période ou sélectionnez ![Calendrier](/help/assets//icons/Calendar.svg) pour sélectionner une période.

## [!UICONTROL Model insights]

L’onglet Informations sur les modèles affiche des widgets pour :

* Contribution par date et support de base. Le graphique empilé est ordonné : d’après le bas, les canaux qui ne dépensent pas au milieu et les canaux qui dépensent au haut.

* Contribution par canal.

* Synthèse des performances marketing.

* Courbes de réponse marginales.
  <br/>Sélectionnez un canal dans la liste déroulante **[!UICONTROL Channel]** pour mettre à jour le widget d’un canal spécifique.

![Modèle - insights du modèle](/help/assets//model-insights-insights.png)

Vous pouvez placer le pointeur de la souris sur des éléments de graphique individuels dans chaque widget pour afficher une fenêtre contextuelle contenant plus de détails.

Pour télécharger un fichier CSV contenant les données du widget, sélectionnez ![Télécharger](/help/assets//icons/Download.svg).

Pour télécharger des données complètes d’informations sur les modèles au format Microsoft® Excel, sélectionnez ![Télécharger](/help/assets//icons/Download.svg) **[!UICONTROL Download data]**.

## [!UICONTROL Attribution]

À l’aide de l’onglet [!UICONTROL Attribution], vous pouvez comprendre l’efficacité des points de contact et des campagnes marketing qui contiennent des données au niveau de l’événement. Les modèles d’attribution suivants sont pris en charge :

* Selon le modèle sélectionné en Mix Modeler :
   * Algorithmique - Influencé
   * Algorithmique - Incrémentiel
* Règle basée sur :
   * Unités de décomposition
   * Première touche
   * Dernière touche
   * Linéaire
   * Ushape

Voir [Attribution multi-touch](../get-started/about.md#multi-touch-attribution) pour une présentation de la fonctionnalité d’attribution multi-touch en Mix Modeler.

Sélectionnez un ou plusieurs modèles d’attribution dans la liste déroulante **[!UICONTROL Attribution Model]**. Les modèles d’attribution sélectionnés s’appliquent à tous les widgets de l’onglet Attribution .

![Attribution](/help/assets//model-insights-attribution.png)

Les scores d’événement granulaires de l’attribution multi-touch Mix Modeler s’alignent sur les scores de Mix Modeler globaux et les ROI. Ces scores sont également rendus disponibles en tant que jeux de données dans Experience Platform.

L’onglet Attribution se compose des widgets suivants :

### [!UICONTROL Overview]

Le widget [!UICONTROL Overview] affiche, pour les modèles d’attribution sélectionnés, les totaux et les pourcentages de conversion. La sélection d’autres modèles ajoute des cercles supplémentaires à la visualisation, dont chacun a sa propre couleur correspondant à la légende.

Pour afficher une fenêtre contextuelle contenant des détails sur un modèle d’attribution, passez la souris sur l’un des cercles de la visualisation.

### [!UICONTROL Trends]

Le widget [!UICONTROL Daily trends], [!UICONTROL Weekly trends] ou [!UICONTROL Monthly trends] affiche, pour les modèles d’attribution sélectionnés, les tendances de conversion quotidiennes, hebdomadaires ou mensuelles.

Pour choisir la période, sélectionnez **[!UICONTROL Daily trends]**, **[!UICONTROL Weekly trends]** ou **[!UICONTROL Monthly trends]** dans ![Plus](/help/assets//icons/More.svg).

Pour afficher des détails, passez la souris sur la ligne de données d’un modèle d’attribution spécifique afin d’afficher une fenêtre contextuelle qui affiche le nombre total de conversions pour ces données.

### [!UICONTROL Breakdown]

Le widget [!UICONTROL Breakdown] est une ventilation par canal ou point de contact des conversions pour chacun des modèles d’attribution sélectionnés. Ce widget peut s’avérer utile pour prendre des décisions sur l’efficacité de chaque canal ou point de contact.

Pour choisir le type de ventilation, sélectionnez **[!UICONTROL Breakdown by channel]** ou **[!UICONTROL Breakdown by touchpoint]** dans ![Plus](/help/assets//icons/More.svg).

Pour afficher les détails, passez la souris sur l’un des éléments du graphique.

### [!UICONTROL Top campaigns]

Le widget Campagnes principales affiche un tableau des principales campagnes avec des colonnes pour le nom de la campagne, le canal, le type de média et les conversions incrémentielles. Ce widget peut vous aider à informer votre équipe de l’efficacité d’une campagne spécifique pour un canal donné et fournir des informations sur les campagnes dans lesquelles vous devriez investir davantage.

Pour trier le tableau par ordre croissant ↑ ou décroissant ↓ pour les conversions de type Canal, Média ou Incrémentiel, sélectionnez l’en-tête de colonne et faites basculer le tri.

Pour développer le tableau dans une boîte de dialogue distincte, sélectionnez **[!UICONTROL Expand]** dans ![Plus](/help/assets//icons/More.svg).

La boîte de dialogue Campagnes principales développée affiche le même tableau avec des colonnes supplémentaires pour

* Conversions incrémentielles
* Conversions influencées
* Conversions Première touche
* Conversions Dernière touche

  Vous pouvez sélectionner chacun des en-têtes de colonne supplémentaires pour trier le tableau par ordre croissant ou décroissant.

Pour fermer la boîte de dialogue Campagnes principales développée, sélectionnez **[!UICONTROL Close]**.


### [!UICONTROL Breakdown by touchpoint position]

La visualisation [!UICONTROL Breakdown by touchpoint position] est une ventilation des conversions attribuées par position du point de contact et du point de contact sur tous les chemins de conversion. Ce graphique vous permet de comparer si un point de contact contribue mieux à une position qu’à d’autres positions et à d’autres points de contact à n’importe quelle position.

>[!NOTE]
>
>La somme des pourcentages de contribution pour un modèle d’attribution sur tous les points de contact et toutes les positions doit être égale à 100.


Les positions [!UICONTROL Starter], [!UICONTROL Player] et [!UICONTROL Closer] sont définies comme suit :

| Position | Description |
|---|---|
| [!UICONTROL Starter] | Cette position indique si le point de contact est la première touche d’un chemin de conversion. |
| [!UICONTROL Player] | Cette position indique si le point de contact n’est pas la première ou la dernière touche menant à la conversion. |
| [!UICONTROL Closer] | Cette position indique si le point de contact est la dernière touche avant la conversion. |


### [!UICONTROL Top conversion paths]

La visualisation [!UICONTROL Top conversion paths] présente les 5 premiers chemins de conversion en fonction des modèles d’attribution sélectionnés.

Pour chaque chemin de conversion, vous voyez :

* le nombre de canaux qui ont un impact,
* le total des chemins attribués,
* le pourcentage des chemins attribués pour ce chemin de conversion par rapport au total des chemins attribués,
* pour chaque canal, le pourcentage de contribution du modèle d’attribution et
* la somme de ces pourcentages de contribution du modèle d’attribution de canal.


## [!UICONTROL Diagnostics]

L’onglet Diagnostics affiche des widgets pour :

* Visualisation [!UICONTROL Model Assessment], que vous pouvez ventiler en fonction des conversions réelles ou prévues ou résiduelles.

  Pour ventiler la visualisation, sélectionnez **[!UICONTROL Actual vs. Predicted]** ou **[!UICONTROL Residuals]** dans la liste **[!UICONTROL Breakdown]**.

* tableau [!UICONTROL Model fitting metrics], présentant les colonnes suivantes pour chaque mesure de conversion :

   * Conversion réelle

   * Conversion modélisée

   * Conversion résiduelle (différence entre conversion réelle et conversion modélisée)

   * Valeurs de score de qualité du modèle :

      * R2 (au carré R), qui indique dans quelle mesure les données correspondent au modèle de régression (la qualité de l’ajustement).

      * MAPE (Erreur en pourcentage absolue moyenne), qui est l’un des IPC les plus couramment utilisés pour mesurer la précision des prévisions et exprime l’erreur de prévision en pourcentage de la valeur réelle.

      * RMSE (Root Mean Square Error) : indique l’erreur moyenne, pondérée en fonction du carré de l’erreur.

  Pour télécharger un fichier CSV contenant les données de la table, sélectionnez ![Télécharger](/help/assets//icons/Download.svg).

* [!UICONTROL Touchpoint effectiveness], représentant le résultat du modèle algorithmique Attribution AI. Les données de ce tableau ne sont générées que pour des périodes spécifiques. Sélectionnez **[!UICONTROL As of *xx/xx/xx, xx:xx TZ *]**![Info](/help/assets//icons/InfoOutline.svg) pour plus de détails.

  La visualisation s’affiche, dans l’ordre décroissant de [!UICONTROL Efficiency measure] ![Ordre décroissant](/help/assets//icons/SortOrderDown.svg), pour chaque point de contact :

   * [!UICONTROL Paths touched] : visualise le pourcentage de chemins qui effectuent une conversion et le pourcentage de chemins qui n’atteignent pas la conversion. Pour un point de contact, vous voyez davantage de conversions attribuées lorsque le taux de conversion d’attribution est élevé. Ce rapport compare le pourcentage des chemins menant à la conversion par rapport au pourcentage des chemins qui ne mènent pas à la conversion *pas*.
   * [!UICONTROL Efficiency measure] : généré par le modèle d’attribution algorithmique, la mesure d’efficacité indique l’importance relative d’un point de contact pour la conversion, indépendamment du volume du point de contact. L&#39;efficacité est mesurée sur une échelle de 1 à 5. Notez qu’un volume de point de contact plus élevé ne garantit pas une mesure d’efficacité plus élevée.
   * [!UICONTROL Total volume] : nombre de fois où un utilisateur touche un point de contact. Le nombre comprend les points de contact qui apparaissent sur un chemin pour effectuer une conversion, ainsi que les chemins *et non* résultant en une conversion.

![Diagnostics](/help/assets//model-insights-diagnostics.png)


## [!UICONTROL Historical overview]

L’onglet Aperçu historique affiche des widgets pour :

* Conversion et dépense par trimestre fiscal et par produit.

* Dépensé par canal.

* Point de contact - Dépense.

  Vous pouvez sélectionner un canal alternatif basé sur les dépenses à afficher pour ce widget. Sélectionnez un canal à partir de **[!UICONTROL Channels]**.

* Volume des points de contact.

  Vous pouvez sélectionner un autre canal en fonction du volume à afficher pour ce widget. Sélectionnez un canal à partir de **[!UICONTROL Channels]**.

![Modèle - Aperçu historique](/help/assets//model-insights-historical-overview.png)
