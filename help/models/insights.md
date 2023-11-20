---
title: Informations sur les modèles
description: Découvrez comment obtenir des détails sur votre modèle, tels qu’une présentation historique, des informations sur les modèles et la qualité des modèles en Mix Modeler.
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
source-git-commit: 73534d1aecb6d1513f6f3b5f1801b497ad73278f
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Informations sur les modèles

Pour afficher les insights du modèle, dans la variable ![Modèles](../assets/icons/FileData.svg) **[!UICONTROL Models]** dans Mix Modeler :

1. Sélectionnez le nom d’un modèle avec une **[!UICONTROL Last run status]** de <span style="color:green">●</span> **[!UICONTROL Success]** de la **[!UICONTROL Models]** table.

1. Dans le menu contextuel, sélectionnez **[!UICONTROL Model Insights]**.

Le moment où le modèle spécifié est actualisé pour la dernière fois et les widgets s’affichent à l’aide de trois onglets : Aperçu historique, Informations sur le modèle et Qualité du modèle.

Vous pouvez modifier la période sur laquelle reposent les widgets sur chacun des onglets. Entrez une période ou sélectionnez ![Calendrier](../assets/icons/Calendar.svg) pour sélectionner une période.


## Présentation historique

L’onglet Aperçu historique affiche des widgets pour :

* Conversion et dépense par trimestre fiscal et par produit.

* Dépensé par canal.

* Point de contact - Dépense.

  Vous pouvez sélectionner un canal alternatif basé sur les dépenses à afficher pour ce widget. Sélection d’un canal depuis **[!UICONTROL Channels]**.

* Volume des points de contact.

  Vous pouvez sélectionner un autre canal en fonction du volume à afficher pour ce widget. Sélection d’un canal depuis **[!UICONTROL Channels]**.

![Modèle - Aperçu historique](../assets/model-historical-overview.png)

## Informations sur les modèles

L’onglet Informations sur les modèles affiche des widgets pour :

* Contribution par date et support de base. Le graphique empilé est trié : d’après le bas, les canaux qui ne dépensent pas au milieu et les canaux qui dépensent au haut.

* Contribution par canal.

* Synthèse des performances marketing.

![Modèle - Informations sur les modèles](../assets/model-model-insights.png)

Vous pouvez placer le pointeur de la souris sur des éléments de graphique individuels dans chaque widget pour afficher une fenêtre contextuelle contenant plus de détails.

Pour télécharger un fichier CSV contenant les données du widget, sélectionnez ![Télécharger](../assets/icons/Download.svg).




## Qualité du modèle

L’onglet Qualité du modèle affiche des widgets permettant de mesurer :

* R2 (au carré R), qui indique dans quelle mesure les données correspondent au modèle de régression (la qualité de l’ajustement).

* MAPE (Erreur en pourcentage absolue moyenne), qui est l’un des IPC les plus couramment utilisés pour mesurer la précision des prévisions et exprime l’erreur de prévision en pourcentage de la valeur réelle.

* RMSE (Root Mean Square Error) : qui affiche la moyenne de &quot;l’erreur&quot;, pondérée en fonction du carré de l’erreur.

![Qualité du modèle](../assets/model-quality.png)

Pour télécharger un fichier CSV contenant les données du widget, sélectionnez ![Plus](../assets/icons/More.svg) dans le widget et, dans le menu contextuel, sélectionnez ![Télécharger](../assets/icons/Download.svg) **[!UICONTROL Download as CSV]**.
