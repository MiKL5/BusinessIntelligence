# **Le Data Lake** <a href="../../"><img src="../../assets/bi.svg" alt="Business intelligence" align="right" height="64px"></a>
L’ancien directeur technique de Pentaho en est l’inventeur. Un data lake est un environnement de stockage à faible coût, qui héberge généralement des pétaoctets de données brutes. Contrairement à un entrepôt de données (DW), un data lake peut stocker à la fois des données structurées et non structurées, et ne nécessite pas de schéma défini pour les stocker. C’est une caractéristique connue sous le nom de « schéma en lecture ». Cette flexibilité en matière de stockage est particulièrement essentielle pour les data scientists, les ingénieurs en traitement de données ainsi que les développeurs ; elle leur permet d’accéder aux données pour des exercices de découverte de données et des projets de machine learning.

Alors que les utilisateurs trouvent de la valeur dans les data lakes, certains peuvent être victimes de devenir des marécages de données ou des puits de données.  
Un marécage de données est le résultat d’un data lake mal géré, c’est-à-dire qu’il manque de pratiques appropriées en matière de qualité et de gouvernance des données pour fournir des informations pertinentes. En l’absence d’une surveillance correcte, les données contenues dans ces référentiels seront inutilisables.  
Les puits de données, quant à eux, sont similaires aux marécages de données ; ils n’apportent qu’une faible valeur ajoutée à l’entreprise, et la source du problème de données n’est pas claire dans ces cas-là.

La participation des équipes chargées de la gouvernance et de la science des données peut contribuer à éviter ces écueils.
## **Data lake ou data lakehouse ?**
L’adoption des data lakes et des entrepôts de données augmente avec la croissance des nouvelles sources de données, les limites de ces deux référentiels de données conduisent à une convergence de ces technologies.  
Un data lakehouse associe les avantages en termes de coûts d’un data lake aux capacités de structure et de gestion des données d’un entrepôt de données.
## **L’architecture du data lake**
Un data lake est souvent associé à _Apache Hadoop_, un logiciel open source permettant un traitement distribué fiable et peu coûteux pour le stockage de données volumineuses.  
Les utilisateurs adoptent rapidement des environnements cloud car ils offrent une plus grande flexibilité aux utilisateurs finaux. Contrairement aux déploiements sur site, les fournisseurs de stockage dans le cloud permettent aux utilisateurs de créer de larges clusters en fonction de leurs besoins, en ne payant que pour le stockage spécifié. Cela signifie que si vous avez besoin d’une puissance de calcul supplémentaire pour exécuter un travail en quelques heures et pas en quelques jours, il est possible de le faire facilement sur une plateforme cloud en achetant des nœuds de calcul supplémentaires.  
Au sein d’Hadoop, le système de fichiers distribués (HDFS) stocke et réplique les données sur plusieurs serveurs, tandis que le système YARN (Yet Another Resource Negotiator) détermine la façon d’allouer les ressources sur ces serveurs. Il est ensuite possible d’utiliser Apache Spark pour créer un grand espace mémoire pour le traitement des données, ce qui permet aux utilisateurs plus avancés d’accéder aux données via des interfaces utilisant Python, R et Spark SQL.  
Le volume de données augmentant à un rythme exponentiel, les data lakes constituent un composant essentiel du pipeline de données.
## **Les avantages d’un data lake**
* **Plus flexible**   
  Il ingére à la fois des ensembles de données structurés, semi-structurés et non structurés, les rendant idéaux pour les projets d’analyse avancée et de machine learning.  
* **Le coût**  
  Ne nécessitant pas autant de planification initiale pour l’ingestion des données (schéma et définition de la transformation), moins d’argent doit être investi dans les ressources humaines. En outre, les coûts de stockage réels des data lakes sont inférieurs à ceux d’autres référentiels de stockage, comme les DW. Cela permet aux entreprises d’optimiser leurs budgets et leurs ressources de manière plus efficace dans le cadre de leurs initiatives de gestion des données.
* **L’évolutivité**  
  Les data lakes peuvent aider les entreprises à évoluer de plusieurs façons. La fonctionnalité en libre-service et la capacité de stockage globale rendent les data lakes plus évolutifs que les autres services de stockage. En outre, les data lakes offrent aux travailleurs un bac à sable pour développer des [POC](../poc) réussis. Une fois qu’un projet a démontré sa valeur à petite échelle, il est plus facile d’étendre ce workflow à plus grande échelle grâce à l’automatisation.
* **La réduction des silos de données**   
  Des soins de santé à la chaîne d’approvisionnement, les entreprises de divers secteurs sont confrontées à des [silos de données](../dataSilo) au sein de leur organisation. Étant donné que les data lakes ingèrent des données brutes dans différentes fonctions, ces dépendances commencent à s’éliminer car il n’y a plus un seul propriétaire à un jeu de données donné.
* **L’amélioration de l’expérience client**  
  Cet avantage n’est pas immédiatement perceptible, cependant une démonstration de faisabilité réussie peut améliorer l’expérience globale de l’utilisateur, en permettant aux équipes de mieux comprendre et de personnaliser le parcours du client grâce à des analyses nouvelles et perspicaces.
## **Ses défis**
Malgré les avantages, ils posent des problèmes.
* Les performances  
  À mesure que le volume de données injecté augmente, les performances baisses, originellement plus lentes qu’aux autres systèmes alternatifs. 
* La gouvernance  
  La capacité d’un data lake à ingérer diverses sources de données offre aux entreprises un avantage dans leurs pratiques de gestion des données. Nonobstant, une gouvernance solide est indispensable pour le gérer de manière appropriée. Les données doivent être étiquetées et classées avec des métadonnées pertinentes afin d’éviter les marécages de données, et ces informations doivent être facilement accessibles par le biais d’un catalogue de données, permettant une fonctionnalité en libre-service pour le personnel moins technique, comme les analystes d’entreprise.  
  Enfin, des mesures doivent être mis en place pour respecter les normes réglementaires et de protection de la vie privée ; il peut s’agir de contrôles d’accès, de chiffrement des données, etc.
___
>>> Source  
[IBM](https://www.ibm.com/fr-fr/topics/data-lake)