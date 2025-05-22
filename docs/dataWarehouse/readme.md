# **Data Warehouse** <a href="../"> <img src="../../assets/atomicBi.png" alt="Business intelligence" align="right" height="64px"> </a>
L’entrepôt des données est un grand référentiel central.  

Un Data Warehouse est une base de données relationnelle hébergée sur un serveur dans un [Data Center](../dataCenter) ou dans le [Cloud](../cloud). Il recueille des données de sources variées et hétérogènes dans le but principal de soutenir l’analyse et faciliter la prise de décision. Concernant l’intégration dans le système de données existant, le fonctionnement du Data Warehouse est basé sur le processus [ETL (Extract, Tranform, Load)](../etl) permettant de charger les données issues des différentes applications.
D’un point de vue plus technique, un Data Warehouse est défini comme un ensemble de données orientées sujet, intégrées, variables dans le temps et non volatiles.
* Orienté sur le sujet  
  Organisé par thème, le Data Warehouse est utilisable pour analyser n’importe quel secteur particulier de l’entreprise.
* Intégré  
  Avant toute utilisation, les données récupérées de sources hétérogènes internes ou externes sont intégrées au Data Warehouse. En conséquence, il est obligatoire de les mettre en forme et les unifier afin de garantir une certaine cohérence. Les données proviennent principalement de traitement transactionnel en ligne (OLTP).
* Variante temporelle  
  Les données passées sont également conservées dans le Data Warehouse, contrairement à certains des systèmes transactionnels traditionnels où seules les données les plus récentes sont stockées. Afin de visualiser l’évolution des données dans le temps.
* Non volatile  
  Une fois stockées dans l’entrepôt de données ne peuvent jamais être modifiées.
## **Les opérations**
* Drill-down  
  L’opération drill-down permet la conversion des données moins détaillées en données plus détaillées par l’une des deux méthodes :  
    * Descendre dans la hiérarchie conceptuelle ou alors, ajouter une nouvelle dimension au cube. Par exemple, en affichant les données de vente pour le calendrier civil ou le trimestre fiscal d’une organisation
    * Ou bien, effectuer un drill-down pour voir les ventes de chaque mois, en descendant dans la hiérarchie conceptuelle de la dimension « temps ».
* Roll-up  
  C’est le contraire.  
  Agrège les données d’un cube OLAP en remontant dans la hiérarchie conceptuelle sinon, en réduisant le nombre de dimensions. E.g., monter dans la hiérarchie conceptuelle de la dimension « l’emplacement » en affichant les données de chaque pays plutôt que de chaque ville.
* Slice and dice (trancher et découper)  
  L’opération « slice » crée un sous-cube en sélectionnant une seule dimension dans le cube OLAP principal. (effectuer un slice en mettant en évidence toutes les données du premier trimestre fiscal ou civil de l’organisation (dimension temporelle)).  
  L’opération « slice » crée un sous-cube en sélectionnant plusieurs dimensions dans le cube OLAP principal. Par exemple, vous pouvez effectuer une opération « dice » en mettant en évidence toutes les données par calendrier ou trimestre fiscal d’une organisation (dimension temporelle) et aux États-Unis et au Canada (dimension géographique).
  Dice restreint un cube de données en appliquant des conditions sur plusieurs dimensions simultanément.
```diff
Avant Dice : 
Cube complet avec toutes les dimensions et mesures.
Dimensions: 
- Temps (Année, Trimestre, Mois)
- Produit (Catégorie, Type, Nom)
- Région (Pays, État, Ville)

Après Dice :
Cube réduit avec les filtres.
Dimensions: 
- Temps (Trimestre 1 et 2 de 2023)
- Produit (Électronique, Meubles)
- Région (France, Allemagne)
```
* Pivot
  La fonction « pivot » fait pivoter la vue cubique actuelle pour afficher une nouvelle représentation des données, permettant ainsi des vues multidimensionnelles dynamiques des données. Cette fonction de l’OLAP est comparable à la fonctionnalité « tableau croisé dynamique » de tableurs, mais si les tableaux croisés dynamiques d’Excel peuvent présenter des difficultés, les pivots OLAP sont relativement simples à utiliser car moins d’expertise est requise et offrent un temps de réponse et des performances de requête plus rapides.
## L’histoire des Data Warehouses ?
Au cours des années 1960 et 1970, les entreprises ont été séduites par les systèmes informatiques pour gérer leurs opérations. Cependant, ces systèmes étaient souvent isolés les uns des autres, ce qui rendait difficile la consolidation des données pour obtenir une vue globale de l’entreprise.
Le volume de données à disposition des entreprises a considérablement augmenté rendant les Data Warehouses indispensables.  

En 1970, pour la première fois, Nielsen et IRI introduisent le concept de Data Mart dimensionnels pour les commerces de détail. En 1983, Teradata lance un système de gestion de base de données spécifiquement conçu pour l’aide à la décision.  

Dans les années 1980, les bases de données relationnelles ont été popularisés, permettant le stockage des données dans un format plus standardisé et de faciliter l’accès aux données par différents systèmes, ouvrant la voie au Data Warehouse.  

Dans les années 1980, les bases de données relationnelles ont été popularisés, permettant le stockage des données dans un format plus standardisé et de faciliter l’accès aux données par différents systèmes, ouvrant la voie au Data Warehouse.  

À la fin des années 1980 l’émergence du premier Data Warehouse d’entreprise, est développé par Paul Murphy et Barry Devlin d’IBM.  

Dans les années 1990, les Data Warehouse ont été popularisés par essentiellement par IBM et Oracle. L’introduction de systèmes de gestion de bases de données relationnelles (SGBDR) a permis de stocker les données efficacement et de les interroger de rapidement et flexiblement. Les outils de Business Intelligence, permettant la visualisation et l’analyse des données stockées dans un Data Warehouse, commencèrent à émerger.
## **Quels sont les objectifs du Data Warehouse ?**
Habituellement, les Data Warehouse se stuent à la frontière entre les données brutes d’un système d’information, telles qu’elles ont été récoltées, et avec les outils d’analyse de données, de dashboarding et d’aide à la prise de décisions.  

Une entreprise peut en avoir besoin pour ces raisons :
1. **La consolidation des données**  
   Les données sont souvent dispersées dans différents systèmes et formats. Le Data Warehouse consolide toutes ces données dans un endroit centralisé ; facilitant l’accès et l’analyse.
2. **L’analys des données**  
   Le Data Warehouse permet de stocker des données historiques et actuelles, permettant de faire des analyses sur des périodes plus longues. Les outils de Business Intelligence peuvent être utilisés pour interroger le Data Warehouse et obtenir des informations précieuses sur les activités de l’entreprise.
3. **L’amélioration de la prise de décision**  
   Ayant accès à des données fiables et cohérentes, il est possible de prendre des décisions plus éclairées. Les données historiques stockées dans le Data Warehouse permettent également d’identifier les tendances et les modèles, aidant à la prédiction des futurs résultats ou tendances.
4. **La réduction des coûts**  
   Le Data Warehouse pour stockant toutes les données, les entreprises peuvent réduire les coûts liés au stockage et à la gestion des données. Les outils de Business Intelligence permettent également de réduire les coûts liés à la création de rapports personnalisés.
5. **Améliorer la collaboration entre les équipes**  
   Les données peuvent être utilisées par différentes équipes, favorisant la collaboration et la prise de décision en équipe.
## **De quoi est composer un DW ?**
* **Les sources de données**  
  Les sources d’où les données sont extraites et chargées dans le Data Warehouse. Ces sources peuvent inclure des systèmes opérationnels, des fichiers plats, des bases de données, des applications, des services web, et cætera.
* Le processus **ETL**  
  Permettant l’extraction des données, de les transformer en un format standardisé et de les charger dans le Data Warehouse. Ce processus implique souvent la suppression des doublons, la normalisation des données et la vérification de leur qualité.
* **Le stockage de données**  
  Elles y sont stockées de manière à faciliter leur analyse. Les données peuvent être dans des tables, des vues, des cubes ou des fichiers.
* **Le modèle de données**  
  C’est la structure définissant la manière dont les données sont organisées dans le DW. Ce modèle peut être en étoile, en flocon ou en constellation.
* **Les outils d’analyse**  
  Ils interrogent le DW afin de fournir des informations précieuses sur les activités de l’entreprise. Ces outils peuvent inclure des rapports, des tableaux de bord, des graphiques, des diagrammes, des analyses statistiques…
## **Que stocke-t-on dans un DW ?**
Un entrepôt de données peut stocker des informations très diversifiées en fonction des besoins de l’entreprise. Voici un petit aperçu.
* **Données transactionnelles**  
  Ce sont des données détaillées des transactions quotidiennes de l’entreprise, (ventes, commandes, activités clients…).
* **Données clients**  
  Cela inclut (les noms, adresses, coordonnées et l’historique des achats des clients).
* **Données produit**  
  Cela comprend des informations sur les produits ou services de l’entreprise (les descriptions, prix, niveaux de stock…).
* **Données financières**  
  Les revenus, les dépenses et les bénéfices de l’entreprise…
* Données marketing  
  Cela comprend des infos de campagnes marketing, les performances des canaux et le retour sur investissement (ROI).
## **Les avantages et inconvénients**
Avantages | Inconvénients
---|---
Très utiles pour permettre aux entreprises d’accéder rapidement et facilement aux données provenant de multiples sources de manière centralisée. | Cette solution optimisée pour les données non structurées.
La possibilité d’accéder à des informations cohérentes et à jour sur toutes les activités de l’entreprise, d’où la possibilité de générer des rapports et d’effectuer des requêtes pour interroger les données. | La création et l’implémentation d’un entrepôt de données prennent du temps et requièrent souvent beaucoup de travail. 
Généralement, un DW réduit le temps d’analyse de données et la production de rapports et facilite ces tâches. | Paradoxalement, un Warehouse peut rapidement devenir obsolète.
Grâce aux vastes volumes de données historiques, les utilisateurs peuvent analyser les tendances sur différentes périodes temporelles afin de réaliser des prédictions pour le futur. | Il est difficile de réaliser des changements dans les types de données, les schémas de sources de données, les index et les requêtes.
| | L’utilisation d’une telle plateforme peut se révéler trop complexe pour l’utilisateur moyen.
| | Les organisations doivent déployer de nombreuses ressources pour former les employés et pour implémenter le Warehouse. C’est important de peser les pours et contres avant de décider d’utiliser ce type de solution.
## **Les acteurs du marché du Data Warehousing**
**Les solutions propriétaires** | **Les solutions open source**
:-:|:-:
_Ces solutions incombent de payer et sont souvent liée à un Cloud. Néanmoins, elles ont le gros avantage de disposer d’une documentation enrichie, de fonctionnalités d’intégration avancées et d’une utilisation relativement simple contrairement aux alternatives gratuites et open source._ | _Bien que moins représentées, Apache et très présente dans la communauté Data._
**Amazon Redshift** est un Data Warehouse cloud d’Amazon Web Services (AWS). Connu pour ses performances élevées, sa facilité d’utilisation et son intégration avec d’autres services AWS. | Grâce à **Apache Hive** les systèmes d’information utilisant déjà l’écosystème Hadoop peuvent se greffer dessus afin de profiter de la capacité de stockage et de mise à l’échelle pour créer un Data Warehouse compatible SQL.
**Google BigQuery** est l’équivalent d’Amazon proposé par Google Cloud Platform. Il est également connu pour ses performances élevées, sa facilité d’utilisation et sa tarification flexible basée sur l’utilisation. | **Apache Cassandra** est une base de données NoSQL distribuée conçue pour stocker de grandes quantités de données. Elle est connue pour sa haute disponibilité et sa capacité à gérer des données en temps réel.
**Microsoft Azure Synapse Analytics** un autre équivalent, de Microsoft Azure, offrant une intégration étroite avec les outils Microsoft existants comme Power BI, ainsi qu’une tarification basée sur l’utilisation. | **ClickHouse** est une base de données en colonnes open source conçue pour le traitement de données en temps réel à grande échelle. Souvent utilisé pour les analyses de données à haute performance et les tableaux de bord interactifs.
Snowflake a gagné en popularité ces dernières années, en partie grâce à sa facilité d’utilisation, sa compatibilité multi-cloud et sa capacité à tenir des charges de travail à grande échelle. | 
## **Qui utilise en utilise un ?**
Toutes les entreprises ayant de vastes volumes de données à traiter, et/ou collectant des données à partir de sources variées. Ainsi que celles souhaitant accéder plus facilement aux données. Ils sont pertinents pour toute entreprise voulant profiter d’une aide à la décision. C’est également le cas des utilisateurs cherchant à gérer des rapports, des graphiques ou des diagrammes à partir des données.  
Les Data Warehouses ont leur place dans tous les secteurs d’activité. Selon l’industrie, l’utilisation diffère.  
Les compagnies aériennes analysent la rentabilité des trajets, proposent des promotions personnalisées.  
Les banques l’exploitent pour gérer les ressources, effectuer des études de marché, ou analyser les performances de leurs différents produits.  
Les assurances, pour analyser les tendances du marché ou le comportement des clients.  
Dans le domaine de la santé, ils permettent de prédire les résultats d’un traitement, de produire des rapports sur les patients ou partager les données avec les compagnies d’assurance.  
Le secteur public y collecte des données, ou pour analyser les rapports sur les taxes ou la politique de santé. Les assurances, pour analyser les tendances du marché ou le comportement des clients.  
Les chaînes de magasins l’exploitent pour la distribution et le marketing, l’inventaire, la logistique, pour comprendre les consommateurs et pour optimiser les prix ou lancer des campagnes de promotion personnalisées.  
Le secteur de la télécommunication ou les décisions de vente et de distributions sont basées en rapport aux données, au même titre que les campagnes promotionnelles.  
Enfin, le tourisme et de l’hôtellerie, les campagnes publicitaires et promotionnelles peuvent être basées sur les préférences et les habitudes des voyageurs.
## **Son avenir**
En même temps qu’elles migrent leurs activités vers le cloud les entreprises ont tendance à migrer leurs bases de données et leurs outils de data warehousing vers le cloud. Ce dernier a de nombreux avantages, flexibilité, collaboration et accessibilité universelle. Des outils très répandus tels que Amazon Redshift, Microsoft Azure SQL Data Warehouse, Snowflake et Google BigQuery permettent de disposer de solutions simples et efficaces pour d’y stocker et analyser les données.  
Le modèle de cloud réduit les barrières à l’entrée – en particulier le coût, la complexité et les temps de valorisation – ayant tendance jusqu’à présent à restreindre l’adoption et l’utilisation efficace. Avec le cloud, l’entreprise peut augmenter ou réduire la capacité de son DW selon ses réels besoins. De plus, les premiers pas d’une initiative de DW dans le cloud sont très faciles et très rapides : l’investissement initial est réduit et le processus de déploiement est beaucoup moins long (et beaucoup moins coûteux !) qu’un déploiement sur site.  
Le DW en cloud élimine en grande partie les risques incontournables du DW sur site. Pas besoin de prévoir un budget ni de sourcer du matériel et des logiciels. Nul besoin de prévoir un poste budgétaire annuel pour la maintenance et le support technique. Dans le cloud, les considérations de coût qui ont traditionnellement préoccupé les équipes chargées du data warehousing –la budgétisation des mises à niveau planifiées et non planifiées – n’ont plus cours.
___
>>> Sources  
[IBM](https://www.ibm.com/fr-fr/topics/olap#:~:text=IBM-,Qu'est%2Dce%20que%20l'OLAP%20%3F,un%20autre%20r%C3%A9f%C3%A9rentiel%20de%20donn%C3%A9es.)  
[Oracle](https://www.oracle.com/fr/database/data-warehouse-definition/#:~:text=Un%20Data%20Warehouse%20est%20une,pour%20une%20meilleure%20business%20intelligence.)  
[DataScientest](https://datascientest.com/data-warehouse)  
[YouTube, chaîne de 365 Data Science](https://youtu.be/AHR_7jFCMeY)  
[Blent](https://blent.ai/blog/a/data-warehouse-definitions-exemples)  
[Youtube, chaîne de SAP](https://youtu.be/I67vax-FATo)  
[Talend](https://www.talend.com/fr/resources/guide-entrepot-donnees/)