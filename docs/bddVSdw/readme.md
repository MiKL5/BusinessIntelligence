# **Quelle est la différence entre base de données et entrepôt de données ?** <a href="../"> <img src="../../assets/atomicBi.png" alt="Business intelligence" align="right" height="64px"> </a>
Bien que les deux stocks des données, il ont des fins défférentes.
La base de données stocke, gère de manière structurée les données <!-- les transactions courantes --> pour les applications opérationnelles quotidiennes d’une organisation, elle et permet un accès rapide à des transactions spécifiques notamment grâce aux technologies d’indexation. Elle est conçue pour les transactions en temps réel, les mises à jour fréquentes et les requêtes transactionnelles.  
Une BDD est généralement normalisée, ce qui signifie qu’il existe une copie unique de chaque donnée.  
Elle est généralement optimisée pour les opérations de lecture/écriture

Le data warehouse, collectionne, consolide, organise et analyse d’immenses quantités de données émanant de différentes sources. Il est conçu pour l’analyse et les rapports, permettant aux utilisateurs de prendre des décisions basées sur des insights (connaissances) métier à partir de données historiques à l’aide de technologies comme l’[OLAP](../olap) et ses dérivés voire In-memory, l’[OLTP](../oltp), et cætera.
Le Data Warehouse, stock couramment différentes versions des mêmes données.
À l’instar de la BDD, il est optimisé pour traiter les requêtes agrégées ainsi que les opérations de lecture/récupération.
Une base de données est principalement utilisée pour les opérations quotidiennes et en temps réel, alors qu’un data warehouse a un rôle analytique sur le long-terme.
___
>>> Source  
[Oracle](https://www.oracle.com/fr/database/data-warehouse-definition/#:~:text=Un%20Data%20Warehouse%20est%20une,pour%20une%20meilleure%20business%20intelligence.)  