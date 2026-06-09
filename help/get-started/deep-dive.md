---
title: Exploration approfondie de Mix Modeler
description: Explorez la méthodologie technique sous-jacente à Adobe Mix Modeler, notamment l’attribution multipoint, la modélisation du marketing mix, le transfert d’apprentissage et l’optimisation du budget.
feature: Administration
hide: true
feature_v2:
  - id: a234aebd-3855-4376-a64d-29b38411e0c5
  - id: fe1c9ae8-a908-4ae1-a0b6-fcf35177b134
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
source-git-commit: 4f4fe68694c81ddb258656eb05d62ef057f200cb
workflow-type: tm+mt
source-wordcount: 2747
ht-degree: 0%

---


# Séance d’immersion


Adobe Mix Modeler est une plateforme de mesure unifiée optimisée par l’IA/ML qui combine l’attribution multipoint (MTA) et la modélisation du mix marketing (MMM) afin de fournir des informations marketing précises, évolutives et pérennes. Cet article présente une répartition détaillée de la méthodologie, des choix de conception et des innovations techniques sous-jacentes à Mix Modeler. Il s’appuie également sur [cette session du Summit 2025](https://business.adobe.com/summit/2025/sessions/marketing-mix-modeling-at-adobe-learn-to-predict-s602.html){target="_blank"}, qui présente une répartition détaillée de la méthodologie, des choix de conception et des innovations techniques sous-jacentes à Mix Modeler.

À mesure que la complexité du marketing augmente, les approches de mesure traditionnelles sont insuffisantes. La fragmentation des données, l’évolution des contraintes en matière de confidentialité et le besoin de rapidité et de rigueur obligent à repenser la manière dont la performance marketing est évaluée. La réponse d’Adobe est Mix Modeler : un système intégré qui utilise le machine learning pour synthétiser plusieurs sources de données et paradigmes de modélisation en une stratégie cohérente.


>[!TIP]
>
>L’un des principaux avantages de Mix Modeler est l’accessibilité de la solution pour les professionnels du marketing. L’application simplifie les complexités de la science des données grâce à une interface facile à utiliser qui ne nécessite aucune formation en science des données. Si une exploration approfondie vous intéresse, cet article explore les choix techniques effectués lors du développement de Mix Modeler. L’article suppose une certaine familiarité avec les concepts (avancés) de la science des données.

Cet article explique plus en détail les composants fondamentaux. Ces composants fondamentaux sont les suivants :

* [attribution multipoint](#multi-touch-attribution-mta)
* [modélisation du mix marketing](#marketing-mix-modeling-mmm)
* [transfert de l’apprentissage](#transfer-learning) (l’échange intelligent de résultats entre l’attribution multipoint et la modélisation du mix marketing)



## Attribution multipoint (MTA)


### Vue d’ensemble

Le modèle d’attribution multipoint (MTA) qui alimente Mix Modeler repose sur un modèle de survie en temps discret entraîné sur les données au niveau de l’événement. Les données incluent les recherches, les clics, les consultations de produits, les ajouts aux paniers et les passages en caisse. À l’aide de l’apprentissage supervisé, le modèle estime la probabilité conditionnelle de conversion à chaque étape du parcours client. Le modèle prend en compte les chemins de parcours des clients de conversion et de non-conversion afin de mesurer l’influence des différents points de contact marketing sur le comportement des clients au fil du temps. Le chemin de non-conversion est aussi important que le chemin de conversion. Le contraste entre les deux chemins permet de comprendre si un type particulier de point de contact marketing génère efficacement des conversions. Par exemple, si un type de point de contact apparaît autant sur un chemin de non-conversion que sur un chemin de conversion, ce point de contact n’a pas d’impact sur la conversion. Ce comportement est contraire à un point de contact qui apparaît souvent sur un chemin de conversion et non sur un chemin de non-conversion.

![Données au niveau des événements](/help/assets/event-level-data.png)

### Principaux concepts

Les concepts clés de l’attribution multipoint sont les suivants :

* **Modélisation des intérêts** : la conversion des clients est modélisée comme une accumulation des intérêts au fil du temps.

  ![Augmentation de l’exposition et des intérêts](/help/assets/exposure-increases-interest.jpg)

  Dans cette approche, une série de signaux d’intérêt déterminent la probabilité de conversion, chacun étant influencé par :

   * expositions médiatiques antérieures,
   * impact des médias sur les stocks publicitaires (un modèle de la façon dont les réponses à la publicité se développent et se dégradent dans les marchés de consommation);
   * autres facteurs de référence.



  Ces signaux sont représentés comme *ϴ<sub>BL</sub>* + *ϴ<sub>E,tc-t1</sub>* + *ϴ<sub>E,tc-t2</sub>* et *ϴ<sub>S, tc-t3</sub>*, où :

   * *ϴ* : illustre les paramètres du modèle (ce qui est appris du modèle).
   * *tc* : heure de la conversion.
   * *tc-tx : le temps entre l’exposition et la conversion, qui est pertinent pour le modèle.
   * *BL* : ligne de base.
   * *E* : e-mail.
   * *S* : recherche.

  Dans le cadre de la modélisation, l&#39;objectif est de tenir compte explicitement du temps entre chaque exposition au milieu et le moment de la conversion (*tc-tx*), en reconnaissant que les interactions plus récentes ont plus de poids que les interactions plus anciennes.

* **Correspondance des probabilités** : la probabilité de conversion est dérivée du niveau d’intérêt à l’aide d’une fonction logistique en S.

  ![&#x200B; Probabilité de conversion &#x200B;](/help/assets/probability-of-conversion.jpg)

  Grâce au machine learning supervisé qui utilise un modèle de survie en temps discret, l’illustration ci-dessus visualise le parcours de conversion du client A. Le niveau d’intérêt est affiché sur l’axe X et la probabilité de conversion sur l’axe Y. Ce mappage montre que la deuxième exposition aux e-mails (ϴE, tc-t2 *) a le plus grand impact sur la conversion.* Comme indiqué par un saut significatif de la probabilité de conversion au moment de cette étape.

* **Rendements décroissants** : les points de contact supplémentaires ont un impact incrémentiel moindre à mesure que l’intérêt augmente.

  La courbe en S, illustrée ci-dessus, montre également que l’exposition du client à des points de contact supplémentaires a moins d’impact incrémentiel avec des niveaux d’intérêt croissants.

* **Modèle de survie en temps discret** : l’utilisation d’un modèle de survie en temps discret introduit plus de flexibilité dans le modèle, ce qui permet au modèle de capturer les nuances temporelles du comportement des clients. Le modèle de survie en temps discret assouplit également certaines des hypothèses les plus restrictives requises par les modèles de survie en temps continu.

  ![Modèle de survie en temps discret](/help/assets/discrete-time-survival-model.jpg)

  Une fonction en temps continu modélise l’impact de l’adstock d’e-mails sur le niveau d’intérêt, à tout moment depuis le moment de l’exposition : *ϴ<sub>E</sub>(Δt;⋋)*
Une fonction de temps discret modélise l’impact de l’adstock d’e-mail sur le niveau d’intérêt sous la forme de fenêtres temporelles discrètes à l’aide de paramètres scalaires : *ϴ<sub>E,i</sub> ≥ 0<sub>E,i+1</sub>*


### Avantages

L’approche d’attribution multipoint sélectionnée pour Mix Modeler présente plusieurs avantages majeurs.

* Tenez compte des chemins de conversion et des chemins de non-conversion, ce qui permet d’estimer plus précisément l’impact réel du média.
* Intégrez des stocks et des rendements décroissants qui modélisent le comportement réel des clients clés et évitez les hypothèses trop simplifiées qui se trouvent souvent dans les modèles basés sur des règles.
* Évoluez efficacement vers des jeux de données volumineux grâce à l’optimisation de l’informatique distribuée et du traitement parallèle.
* Prise en charge de l’attribution intuitive des points de contact qui permet une interprétation claire contrairement à d’autres méthodes telles que les modèles Markov cachés.
* Offrez des performances élevées et une précision prédictive élevée par rapport aux autres algorithmes de classification.

Mix Modeler fournit une [interface conviviale pour les professionnels du marketing](/help/models/insights.md#attribution) aux informations résultant de l’attribution multipoint.

![Informations d’attribution du modèle](/help/assets/model-insights-attribution.png)


Bien que l’attribution multipoint offre tous ces avantages, Mix Modeler ne s’appuie pas entièrement sur les informations de conversion des données au niveau de l’événement. La modélisation du marketing mix est un autre composant fondamental pour prendre en compte les données au niveau des agrégats.

## Modélisation du mix marketing (MMM)

La modélisation du marketing mix (MMM) est basée sur des données au niveau agrégé et utilise une structure de modèle multiplicative, plutôt qu’additive, pour refléter les interactions marketing du monde réel.

![Données au niveau agrégé](/help/assets/mmm-aggregate-data.jpg)

L’illustration présente les données au niveau des agrégats sous forme de tableau. Chaque ligne correspond à une période (généralement une semaine, parfois un jour) et chaque colonne représente une variable. Le tableau comprend :

* la colonne de conversion (la variable de résultat du modèle),
* colonnes de média (par exemple : recherche, affichage) et
* des colonnes de facteurs (par exemple, saisonnalité, promotions) pour capturer les influences internes ou externes en dehors des dépenses multimédia qui affectent toujours les performances multimédia.

Le modèle prédit les conversions de la semaine 4 à l’aide des données surlignées en vert clair, y compris les facteurs de cette semaine et les entrées historiques des canaux médias.

### Concepts clés

Les concepts clés derrière la modélisation du marketing mix sont les suivants :

* **Modèle multiplicatif** : les ventes ou les conversions sont le produit d’une ligne de base et de multiplicateurs de médias.

  Ainsi, au lieu d’utiliser un modèle additif :
  *Conversions hebdomadaires = demande de référence **+**&#x200B;Multiplicateur de recherche **+**&#x200B;Multiplicateur d’affichage **+**....*
utiliser un modèle multiplicatif :
  *Conversions hebdomadaires = demande de référence **x**&#x200B;multiplicateur de recherche **x**&#x200B;multiplicateur d’affichage **x**....*

  Ou dans une formule : ** Y = ⨍<sub>BL</sub>(X<sub>facteurs</sub>;θ<sub>facteurs</sub>) x ⨍<sub>S</sub>(X<sub>S</sub>;θ<sub>S</sub>) x ⨍<sub>D</sub>(X<sub>D</sub>;θ<sub>D</sub>)*

  Par exemple :

   * Conversions réelles à la semaine : 1730.
   * Conversions prédites à la semaine : 1 787,5 = 1 100 x 1,25 x 1,3, où :
      * 1100 : demande initiale prédite à la semaine 4, fonction des données des facteurs 1 et 2 à la semaine 4.
      * 1.25 : multiplicateur de recherche prédit à la semaine 4, fonction des données de recherche de la semaine 1 à la semaine 4.
      * 1.3 : multiplicateur d’affichage prédit à la semaine 4, une fonction pour les données d’affichage de la semaine 1 à la semaine 4.

  La différence prévue entre ce que le modèle prédit (1787,5) et les conversions réelles (1730) est le résidu, qui est souvent de petite taille et pas quelque chose à craindre.


* **Capture d’Adstock et rendement décroissant** : Adstock est capturé à l’aide de fonctions de décroissance exponentielle et de puissance.

  ![Capturer les rendements de diminution du stock d’annonces](/help/assets/capturing-adstock-diminishing-return.jpg)


  La décroissance exponentielle d’un stock publicitaire peut être unilatérale ou bilatérale, selon l’endroit où l’impact maximal se produit après l’investissement dans le média.

  Pour prendre en charge les retours décroissants, la fonction de puissance est appliquée : *x<sup>θ</sup>* pour *θ ∈ (0,1*). Cette fonction de puissance permet d&#39;obtenir un graphique de forme concave pour capturer le rendement décroissant. Le rendement décroissant est alors capturé dans la fonction multiplicatrice au sein du modèle MMM.


### Avantages

Les avantages de l’approche de modélisation du marketing mix sont basés sur le fait que le modèle multiplicatif soutient mieux les comportements marketing réels attendus. Par exemple :

* la synergie des médias, où les canaux médiatiques fonctionnent souvent mieux ensemble qu&#39;isolément.
* Un impact qui varie dans le temps : un même niveau d’investissement marketing peut entraîner des rendements différents à différents moments en raison de facteurs externes.
* Les recommandations budgétaires dans le temps lorsque les conditions de marché prévues ou les fluctuations de référence aident à éclairer l&#39;allocation budgétaire au fil du temps.

Mix Modeler fournit une [interface conviviale pour les professionnels du marketing](/help/models/insights.md#attribution) aux différentes informations résultant de la modélisation du marketing mix. Par exemple, une répartition de la contribution des facteurs pour afficher la proportion des conversions de base qui peuvent être attribuées aux différents facteurs inclus dans le modèle.


![Répartition de la contribution des facteurs](/help/assets/factors-example.png)


#### Exemple

Cet exemple simplifié illustre comment une approche de modélisation multiplicative pour une boutique en ligne de baskets fictives permet une meilleure allocation budgétaire que le modèle additif.

![Approche du modèle multiplicatif](/help/assets/benefits-mmm.jpg)

##### Hypothèses

* La demande de baskets est plus élevée en été et plus faible en hiver, comme le montrent les contributions de base totales.

* La stratégie par défaut pour la planification marketing consiste à dépenser un montant fixe de budget marketing (840 $) sur l’ensemble de l’année, où chaque mois obtient le même budget.

* Adstock est ignoré et les médias achetés sont traités comme une unité. Ces hypothèses sont indépendantes du modèle choisi et n&#39;influencent pas la comparaison.

* Un budget constant dans le modèle additif signifie une contribution constante sur chaque mois, qui est reflétée pour le modèle additif sur le graphique supérieur de la colonne centrale.

* Dans le modèle multiplicatif, un budget constant signifie des multiplicateurs constants chaque mois. Afin de fournir un impact variable dans le temps pour les mêmes dépenses mensuelles, le multiplicateur fonctionne avec la demande de base. Cet effet multiplicateur s’affiche sur le graphique du bas dans la colonne du milieu.

##### Déplacer les budgets

Est-il possible de s&#39;éloigner d&#39;un budget fixe, de déplacer le budget, mais de maintenir le budget total à 840 $?

* Dans le modèle additif, il n&#39;y a pas d&#39;incitation, du point de vue de la modélisation, à apporter un changement, car il n&#39;y a pas d&#39;interaction avec la ligne de base. Avoir une dépense fixe est optimal. Si vous déplacez $1 de novembre à mai, le gain de mai est inférieur à la baisse de novembre en raison des rendements décroissants.
* Dans un modèle multiplicatif, il y a de la place pour changer. En fonction de la ligne de base, vous pouvez déplacer les budgets des mois d&#39;hiver vers les mois d&#39;été. Le gain du mois d&#39;été est supérieur à la perte du mois d&#39;hiver en raison de l&#39;effet multiplicateur. L’étendue du changement et le lieu où il doit être effectué sont couverts dans les [algorithmes d’optimisation du budget](#budget-optimization) utilisés dans la modélisation du mix marketing.



## Transfert de l’apprentissage

En plus de l’attribution multipoint et de la modélisation du mix marketing, l’expérimentation est un autre pilier important dans la résolution des problèmes de mesure marketing. Bien que l’expérimentation ne soit pas implémentée dans le cadre de Mix Modeler, vous pouvez l’utiliser, par exemple en désactivant le marketing sur certains marchés, pour comprendre l’impact causal du marketing sur les ventes.

Adobe recommande et utilise le transfert d’apprentissage pour combiner les informations issues de l’attribution multipoint, de la modélisation de la combinaison marketing, de l’expérimentation et d’autres sources de connaissances préalables.  Ce mélange peut être décrit comme une approche par couches. Chaque calque présente des lacunes pour illustrer les limites de la production d’un modèle cohésif. Mais si vous empilez les calques de la bonne manière, vous pouvez compenser les écarts dans le modèle combiné.
Appliquez cette analogie lorsque vous utilisez la combinaison de l’attribution multipoint, de la modélisation du mix marketing, de l’expérimentation et des sources de connaissances antérieures. Mélangez ces composants de manière à ce que la combinaison souffre le moins possible des défauts de chacun d&#39;eux.

Essentiellement, l&#39;apprentissage par transfert est un algorithme d&#39;optimisation numérique à l&#39;œuvre. Dans le cadre de l&#39;entraînement du modèle, une fonction de perte (pour quantifier la différence entre la sortie prévue d&#39;un modèle et la valeur réelle (vérité du sol)) est établie. Et une bonne mesure d’ajustement (pour évaluer dans quelle mesure les prédictions d’un modèle s’alignent sur les données observées) est déterminée. Le transfert d’apprentissage résout ensuite l’optimisation numérique pour obtenir les balises (paramètres du modèle). S’il existe une ou plusieurs sources d’informations, cette fonction d’objectif d’optimisation initiale est augmentée d’un autre terme. Ce terme mesure la distance entre ce que vous avez fourni en tant que connaissance préalable et ce que le modèle produit pour comparer.


### Apprentissage par transfert bidirectionnel

Lorsque vous disposez à la fois de données au niveau de l’événement et de données au niveau agrégé, l’apprentissage par transfert bidirectionnel implique le workflow suivant.

![&#x200B; Apprentissage par transfert bidirectionnel &#x200B;](/help/assets/bi-directional-transfer-learning.jpg)

| Étape | Description |
|:---:|---|
| 1 bis | Le modèle MTA par défaut est entraîné sur les données. En règle générale, un modèle MTA est entraîné sur une fenêtre temporelle plus courte que le modèle MMM. Les données couvrent les données d’événement des canaux en ligne. |
| 1b | Le modèle MTA est entraîné. En règle générale, un modèle MMM est entraîné sur une fenêtre temporelle d’au moins deux ans. Les données couvrent les facteurs, les canaux en ligne et hors ligne. |
| 2 | Le modèle MTA est noté. |
| 3 | Les résultats du modèle MTA noté sont intégrés dans MMM en tant qu&#39;apprentissage par transfert. |
| 4 | Le modèle MMM est mis à jour avec les données d’apprentissage de transfert. Cette mise à jour signifie qu’un nouveau jeu d’estimations de paramètres est utilisé pour obtenir des informations supplémentaires et optimiser le budget. Les canaux et la couverture temporelle ne changent pas. |
| 5 | Le modèle MMM est noté à l’aide des données agrégées hebdomadaires pour les canaux. |
| 6 | Le résultat du modèle MMM noté est intégré au MTA en tant qu’apprentissage par transfert. |
| 7 | Les scores du MTA pour les données au niveau de l’événement sont mis à jour à l’aide des résultats du transfert d’apprentissage et sont utilisés pour obtenir des informations supplémentaires. |

Tenez compte des points suivants :

* Le MTA est limité en ce qui concerne la couverture de canal (uniquement les données au niveau des événements issues des données web et mobiles, par exemple), mais il est avantageux en raison de la grande quantité de données. L’aspect clé du MTA est la performance relative.
* MMM comprend l’image plus holistique avec les facteurs, les canaux en ligne et hors ligne.
* Le transfert de l’apprentissage du MTA vers MMM met à jour le modèle MMM. Les résultats de l’apprentissage par transfert influencent les paramètres qui pilotent le *modèle* multiplicatif. Le transfert de l’apprentissage de MMM vers le MTA met à jour les *scores* du MTA. Il n’est pas nécessaire d’influencer le modèle MTA, les scores initiaux étant déjà statistiquement suffisants.

## Connaissances préalables

Au-delà du MTA, du MMM et de l’expérimentation, il existe donc de nombreuses autres sources de connaissances préalables que vous pouvez éventuellement exploiter pour la planification des mesures marketing. Différentes entreprises ont différentes sources de connaissances préalables. Par exemple, le partage des dépenses, les modèles internes précédents ou l’expérience du secteur.

![Connaissances préalables](/help/assets/prior-knowledge.jpg)

Le processus de création de modèles peut tirer parti de toutes ces sources d’informations par le biais du même processus de transfert d’apprentissage. Ces sources de connaissances préalables sont facultatives. Vous n’avez pas besoin de disposer de sources de connaissances préalables pour que la modélisation du marketing mix fonctionne. Si vous n’avez aucune connaissance préalable, le modèle par défaut est utilisé pour générer des informations sur les scores, puis l’optimisation du budget. Si vous disposez d’une entrée de connaissances préalables, vous pouvez utiliser le transfert d’apprentissage pour mettre à jour le modèle MMM.


## Optimisation du budget

L&#39;optimisation budgétaire est basée sur le modèle MMM multiplicatif expliqué précédemment,

Dans un exemple simple, il existe deux canaux : recherche et affichage. Et vous avez un budget total. L’objectif est de répartir le budget entre les deux canaux afin de maximiser la conversion. L’optimisation numérique est utilisée pour trouver le mix budgétaire optimal qui maximise la conversion sous la contrainte budgétaire totale. Imaginez, par exemple, que votre contrainte budgétaire totale soit de 130 000 $.

La formule d’optimisation du budget est la suivante : *Max ⨍(X<sub>S</sub>, X<sub>D</sub>) = ⨍<sub>BL</sub>(X<sub>facteurs</sub>) x ⨍<sub>S</sub>(X<sub>S</sub>) x ⨍<sub>D</sub>(X<sub>D</sub>)*, *X<sub>S</sub>* et *X<sub>D</sub>* sont des paramètres et *X<sub>factor</sub>* est prévu.

![&#x200B; Contraintes budgétaires &#x200B;](/help/assets/budget-constraints.png)


### Contraintes au niveau du canal

Imaginez que vous ayez d’autres contraintes de niveau de canal :

* $10K - $80K pour la recherche.
* $5K - $70K pour l&#39;affichage.
* 130 000 $ au total.

Par conséquent, le mix budgétaire éligible entraîne la contrainte de la surface d’optimisation. L’algorithme d’optimisation numérique permet ensuite de déterminer l’allocation budgétaire optimale.

### À travers plusieurs conversions

Outre les contraintes au niveau du canal, prévoyez une allocation budgétaire optimale pour plusieurs conversions.

![Optimisation du budget entre les conversions](/help/assets/planning-across-multiple-conversions.jpg)

Pour permettre une allocation budgétaire optimale entre les conversions, une moyenne pondérée de la fonction ci-dessus pour chacune des conversions est utilisée. La formule devient ⨍<sub>new</sub>(X) = w<sub>1</sub>f<sub>1</sub>(X) + w<sub>2</sub>f<sub>2</sub>(X)**

Voici quelques exemples d’optimisation du budget pour plusieurs conversions :

* Vous souhaitez maximiser le chiffre d’affaires total des ventes en ligne et des conversions de ventes en magasin.
* Vous souhaitez optimiser votre succès à long terme en utilisant à la fois les KPI de sensibilisation à la marque et les conversions de ventes.

Dans le deuxième exemple, les unités des deux conversions ne sont pas similaires (KPI de sensibilisation à la marque par rapport aux conversions), mais cela n’a pas d’importance. Les conversions ou les modèles n’ont pas à se référer aux mêmes canaux et peuvent également se chevaucher. L’optimisation numérique trouve la meilleure solution au problème dans les contraintes données.


## Résumé

Adobe Mix Modeler est plus qu’un outil de mesure ; Mix Modeler est un moteur d’aide à la décision et ses points forts sont les suivants :

* La possibilité de modéliser la complexité du monde réel avec une rigueur statistique
* Une intégration unifiée de divers paradigmes de données et de modélisation
* Une architecture durable qui s’adapte aux tendances d’obsolescence des données

Grâce à l’interprétation et aux performances, Mix Modeler est devenu un élément central de la transformation marketing pilotée par les données d’Adobe. Mix Modeler permet aux équipes marketing de prendre des décisions d’investissement plus rapides, plus intelligentes et mieux alignées.
