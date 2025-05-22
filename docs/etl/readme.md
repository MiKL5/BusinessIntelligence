# **Qu’est ce que l’ETL (Extract, Transform, Load)** <a href="../"><img src="../../assets/atomicBi.png" alt="Business intelligence" align="right" height="64px"></a>
L’ETL (extract, transform, load), est un processus automatisé combinant les données brutes de plusieurs sources, extrait l’information nécessaire à l’analyse, la transforme par un ensemble de règles opérationnelles visant à nettoyer et organiser en un format répondant aux besoins opérationnels et la charge dans un [Data Warehouse](docs/dataWarehouse).Elle pourront être utilisées pour l’[analytique des données](docs/dataAnalytics) et le [machine learning]( https://github.com/MiKL5/artificialIntelligence/blob/master/docs/machineLearning/definition). L’ETL résume généralement les données afin de réduire leur taille et d’améliorer leur performance pour des types d’analyse spécifiques.

Il faut régulièrement charger le data warehouse afin de faciliter l’analyse commerciale. Les données d’un ou plusieurs systèmes opérationnels sont extraites et copiées dans ce dernier. Le défi dans les environnements de data warehouse est d’intégrer, réorganiser et consolider de grands volumes de données sur de nombreux systèmes, fournissant ainsi une nouvelle base d’information unifiée pour la [Business Intelligence](https://github.com/MiKL5/artificialIntelligence/blob/master/docs/other/bi).  
Le processus d’extraction des données des systèmes sources et de leur transfert dans l’entrepôt de données est communément appelé ETL. Il est à noter que l’ETL fait référence à un processus général et non à trois étapes bien définies. L’acronyme ETL est peut-être trop simpliste, car il omet la phase de transport et implique que chacune des autres phases du processus est distincte.  
Que se passe-t-il pendant le processus ETL ? Quelles sont les principales actions du processus ?
## **L’extraction des données**
La première étape est l’extraction. Les données sont spécifiquement identifiées et ensuite prélevées à de nombreux endroits différent. Ces données peuvent émanées d’une variété d’éléments (fichiers, feuilles de calcul, systèmes de bases de données, applications, etc.). Il n’est généralement pas possible d’identifier le sous-ensemble exact d’intérêt, de sorte que l’on extrait plus de données que nécessaire pour s’assurer de couvrir tous les besoins.  
Selon les capacités du système source (e.g. les ressources du système d’exploitation), certaines transformations peuvent avoir lieu pendant ce processus d’extraction. La taille des données extraites varie de quelques centaines de kilo-octets à plusieurs giga-octets, selon le système source et la situation commerciale. C’est aussi le cas pour la période entre deux extractions ; certaines peuvent varier de jours ou d’heures à presque en temps réel.
## **Le transport des données**
Une fois les données extraites, elles doivent être physiquement transportées vers le système cible ou intermédiaire pour un traitement ultérieur. Selon le mode de transport choisi, certaines transformations peuvent également être effectuées au cours de ce processus.
## **La transformation des données**
On sait qu’une fois les données extraites, elles doivent être physiquement transportées vers la destination cible, mais aussi converties dans le format approprié. Cette transformation de données peut inclure des opérations telles que le nettoyage, l’assemblage et la validation des données.
## **Le chargement des données**
La dernière étape du processus consiste à téléverser les données transformées dans la cible de destination, soit une BDD, soit un data warehouse. Il existe deux principales méthodes pour envoyer les données dans un entrepôt :
Chargement complet | Chargement incrémentale
---|---
Cette méthode implique un déchargement complet des données qui a lieu la première fois que la source est chargée dans l’entrepôt. | En revanche, cette méthode a lieu à intervalles réguliers. Ces intervalles peuvent être des incréments de flux (meilleurs pour de plus petits volumes de données) ou des incréments de lots (meilleurs pour de plus grands volumes de données).

Les équipes de BI lancent ensuite des requêtes sur ces données, ensuite présentées aux utilisateurs finaux ou aux personnes chargées de prendre des décisions commerciales, ou utilisées comme entrées pour des algorithmes de ML. Un problème courant rencontré ici est que si les résumés [OLAP](docs/olap) ne peuvent pas supporter le type d’analyse que l’équipe BI veut faire, alors tout le processus doit être relancé, cette fois avec différentes transformations.

⟹ Les technologies émergentes et l’automatisation imprègnent tous les aspects de notre travail et de notre vie d’aujourd’hui.  
La véritable opportunité de ces technologies, qui incluent l’intelligence artificielle (IA), le machine learning, l’Internet des Objets (IoT) et les interfacent humaines, est de nous permettre d’adopter l’innovation à une échelle jamais vue auparavant.  
Ces technologies nous aident à réimaginer ce qu’il est possible de faire au travail et dans la vie : des voitures à la médecine personnalisée à l’agriculture de précision et aux villes intelligentes qui changent notre façon de vivre notre monde.

___
>>> Cf.  
[Qu’est-ce que le processus ETL](https://www.oracle.com/fr/database/processus-etl-definition/)