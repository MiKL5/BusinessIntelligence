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
