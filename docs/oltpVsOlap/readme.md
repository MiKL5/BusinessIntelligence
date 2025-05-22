# **La différence entre OLTP et OLAP** <a href="../"><img src="../../assets/atomicBi.png" alt="Business intelligence" align="right" height="64px"></a>
Apparemment analogues ces concepts constituent deux systèmes de traitement de données en ligne et divergent considérablement.

OLTP permet l’exécution en temps réel d’un grand nombre de transactions par un grand nombre de personnes, contrairement au traitement analytique en ligne (OLAP) consistant généralement à interroger ces transactions (appelées enregistrements) dans une base de données à des fins analytiques. L’OLAP aide les sociétés à extraire des informations à partir de leurs données de transaction afin de les exploiter pour prendre des décisions plus éclairées.

OLTP | OLAP
:-:|:-:
Permet l’exécution en temps réel d’un nombre élevé de transactions de base de données par de nombreux utilisateurs | Interroge généralement de nombreux enregistrements (voire tous) dans une base de données à des fins analytiques
La latence extrêmement courte | Exige largement plus de latence que l’OLTP
Modifie fréquemment de petites quantités de données et nécessite généralement un équilibre entre opération de lecture et d’écriture | Ne modifie pas du tout les données ; les [workloads](workload) consomment généralement beaucoup de ressources en lecture
Les données sont indexées pour réduire la latence | Stocke les données en colonnes facilitant l’accès à un grand nombre d’enregistrements
Requiert des sauvegardes fréquentes ou simultanées de la base de données | Nécessite beaucoup moins fréquement les sauvegardes de base de données
Besoin de relativement peu d’espace de stockage | Requiert généralement d’importants espaces de stockage pour les grands volumes de données historiques
Exécute généralement des requêtes simples impliquant un ou plusieurs enregistrements | Impliquant un grand nombre d’enregistrements, il exécute des requêtes complexes

L’OLTP est un système de modification de données en ligne, alors qu’OLAP est un système de banque de données multidimensionnelle historique en ligne utilisé pour extraire des données volumineuses à des fins d’analyse. L’OLAP fournit généralement des analyses sur les données capturées par un voire quelques OLTP.
___
>>> Source  
[Oracle](https://www.oracle.com/fr/database/what-is-oltp/)