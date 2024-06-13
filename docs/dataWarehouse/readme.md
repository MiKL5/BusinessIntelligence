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
## **Que stocke-t-on dans un Data Warehouse ?**


___
>>> Sources  
[IBM](https://www.ibm.com/fr-fr/topics/olap#:~:text=IBM-,Qu'est%2Dce%20que%20l'OLAP%20%3F,un%20autre%20r%C3%A9f%C3%A9rentiel%20de%20donn%C3%A9es.)  
[Oracle](https://www.oracle.com/fr/database/data-warehouse-definition/#:~:text=Un%20Data%20Warehouse%20est%20une,pour%20une%20meilleure%20business%20intelligence.)  
[DataScientest](https://datascientest.com/data-warehouse)  
[YouTube](https://youtu.be/AHR_7jFCMeY)  