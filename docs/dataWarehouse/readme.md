# **Data Warehouse** <a href="../../"> <img src="../../assets/bi.svg" alt="Business intelligence" align="right" height="64px"> </a>
L’entrepôt des données est un grand référentiel central.  

Un Data Warehouse est une base de données relationnelle hébergée sur un serveur dans un [Data Center](docs/dataCenter) ou dans le [Cloud](docs/cloud). Il recueille des données de sources variées et hétérogènes dans le but principal de soutenir l’analyse et faciliter la prise de décision. Concernant l’intégration dans le système de données existant, le fonctionnement du Data Warehouse est basé sur le processus [ETL (Extract, Tranform, Load)](docs/etl) permettant de charger les données issues des différentes applications.
D’un point de vue plus technique, un Data Warehouse est défini comme un ensemble de données orientées sujet, intégrées, variables dans le temps et non volatiles.
* Orienté sur le sujet  
  Organisé par thème, le Data Warehouse est utilisable pour analyser n’importe quel secteur particulier de l’entreprise.
* Intégré  
  Avant toute utilisation, les données récupérées de sources hétérogènes internes ou externes sont intégrées au Data Warehouse. En conséquence, il est obligatoire de les mettre en forme et les unifier afin de garantir une certaine cohérence. Les données proviennent principalement de traitement transactionnel en ligne (OLTP).
* Variante temporelle  
  Les données passées sont également conservées dans le Data Warehouse, contrairement à certains des systèmes transactionnels traditionnels où seules les données les plus récentes sont stockées. Afin de visualiser l’évolution des données dans le temps.
* Non volatile  
  Une fois stockées dans l’entrepôt de données ne peuvent jamais être modifiées.

* Drill-down  
  L’opération drill-down permet la conversion des données moins détaillées en données plus détaillées par l’une des deux méthodes :  
    * Descendre dans la hiérarchie conceptuelle ou alors, ajouter une nouvelle dimension au cube. Par exemple, en affichant les données de vente pour le calendrier civil ou le trimestre fiscal d’une organisation ou bien, effectuer un drill-down pour voir les ventes de chaque mois, en descendant dans la hiérarchie conceptuelle de la dimension « temps ».


___
>>> Sources  
[IBM](https://www.ibm.com/fr-fr/topics/olap#:~:text=IBM-,Qu'est%2Dce%20que%20l'OLAP%20%3F,un%20autre%20r%C3%A9f%C3%A9rentiel%20de%20donn%C3%A9es.)  
[Oracle](https://www.oracle.com/fr/database/data-warehouse-definition/#:~:text=Un%20Data%20Warehouse%20est%20une,pour%20une%20meilleure%20business%20intelligence.)  