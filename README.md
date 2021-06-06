Ce projet est réalisé dans le cadre de Valorisation des Données de la formation Mathématiques appliquées et Modélisation de Polytech Nice Sophia. Il fut réalisé dans son intégralité avec le langage R.
***
## Détection de fraudes de cartes bancaires
***
L'objectif de ce projet était  dans un premier temps d'analyser en profondeur et de faire des études statistiques concernant notre base de données.
La base de données sur laquelle nous allons travailler est constituée de 284807 transactions bancaires. Celles-ci  sont représentées par 30 informations concernant ces transactions telles que le montant. La plupart des noms de ces informations sont cryptées pour des raisons de sécurité. Parmi toutes ces données,  492 transactions sont classées comme étant frauduleuses et les 284315 autres sont validées comme étant non-frauduleuses. Le but final de ce projet est de pouvoir détecter en fonction des caractéristques des transactions si celles-ci sont frauduleuses. Il s'agira ici d'une classification désequilibrée.
La classification est une famille d'algorithmes de machine learning supervisés qui identifient à quelle catégorie appartient un objet (par exemple si une transaction est une fraude ou non), sur la base d'exemples étiquetés d'objets connus (par exemple des transactions connues pour être des fraudes ou non). La classification prend un ensemble de données avec des étiquettes connues et des caractéristiques prédéterminées et apprend à étiqueter de nouveaux enregistrements sur la base de ces informations.

Dans notre cas, la classification déséquilibrée est un problème de classification dans lequel une classe est sous-représentée par rapport aux autres. Le cas classique est un problème à deux classes, une majoritaire à 99% et une minoritaire à 1%.
![alt text](https://github.com/JessicaGourdon/Fraudes-de-Cartes-Bancaires/blob/main/Capture%20d%E2%80%99%C3%A9cran%20(217).png)

Lors de l'étape d'analyse et d'études statistiques, nous avons observé la densité des transactions au cours d'une journée (pour voir les heures favorables à la survenue de transactions frauduleuses),  la distribution des montants des transactions par classe etc

![alt text](https://github.com/JessicaGourdon/Fraudes-de-Cartes-Bancaires/blob/main/Capture%20d%E2%80%99%C3%A9cran%20(216).png)
![alt text](https://github.com/JessicaGourdon/Fraudes-de-Cartes-Bancaires/blob/main/Capture%20d%E2%80%99%C3%A9cran%20(218).png)

Pour la suite, nous allons utiliser la réegression logistique dans le but de pouvoir classifier nos données.
Etant donné que notre base de données est déséquilibrée (grande proportion de données non-frauduleuses et petite de frauduleuses), l'algorithme aura naturellement tendance à classifier les données comme étant non-frauduleuses même si elles sont véritablement frauduleuses. Dans notre étude, on va donc s'intéresser à minimiser le taux de faux négatifs (lorsque l'algorithme prédit la donnée comme étant non-frauduleuse alors qu'elle est frauduleuse).
![alt text](https://github.com/JessicaGourdon/Fraudes-de-Cartes-Bancaires/blob/main/Capture%20d%E2%80%99%C3%A9cran%20(219).png)
Nous avons par la suite fait de nombreux test pour appliquer notre régression logistique. 
Nous avons d'abord pris l'intégralité du dataset :
![alt texte](https://github.com/JessicaGourdon/Fraudes-de-Cartes-Bancaires/blob/main/Capture%20d%E2%80%99%C3%A9cran%20(220).png)
