# **Comment fonctionne l’analytique du big data ?** <a href="../"> <img src="../../../assets/atomicBi.png" alt="Business intelligence" align="right" height="64px"> </a>
L’analytique du big data suit cinq étapes pour analyser de grands jeux de données : 
* Collecter les données
* Le stockage
* Le traitement
* Le nettoyage
* L’analyse
* La collecte
Permettant l’identification de sources de données et la collecte de données à partir de ces dernières. La collecte de données suit des processus ETL ou ELT.

#### **ETL : extraction, transformation, chargement**  
Les données générées sont d’abord converties dans un format standard puis chargées dans le stockage.  
#### **ELT : extraction, chargement, transformation**  
inversement, d’abord chargées dans le stockage puis converties au format requis.
## **Le stockage de données**
Selon leurs complexité, celles-ci peuvent être transférées dans des stockages tels que les entrepôts des données cloud ou les lacs de données. Les outils d’informatique décisionnelle peuvent y accéder au besoin.
## **Le traitement de données**
Lorsqu’elles sont mises en place, elles doivent être converties et organisées afin que les requêtes analytiques génèrent des résultats corrects. Pour ce faire, il existe différentes options de traitement de données. Le choix d’une approche dépend des ressources de calcul et d’analytique disponibles pour le traitement des données.
## **Le traitement centralisé** 
L’ensemble à lieu dans un serveur central dédié qui héberge toutes les données.
## **Le traitement distribué** 
Elles sont distribuées puis stockées sur différents serveurs.
## **Le traitement par lots** 
Les morceaux de données s’accumulent dans le temps et sont traités par lots.
# **Le traitement en temps réel**
Traitées de manière continue et les tâches de calcul effectuées en quelques secondes. 
## **Le nettoyage de données**
Implique la recherche d’erreurs, (les duplications, les incohérences, les redondances ou les formats erronés), consistant aussi à filtrer les données indésirables pour l’analytique.
## **L’analyse de données**
Les données brutes sont converties en informations exploitables. En voici quatre types  
1. Analytique descriptive
Les scientifiques des données analysent les données afin de comprendre ce qu’il s’est passé ou ce qu’il se passe au sein de l’environnement de données. Elle se caractérise par des visualisations de données, telles que des diagrammes à secteurs, des histogrammes, des graphiques linéaires, des tableaux ou des récits générés.
2. Analytique diagnostique
L’analytique diagnostique est un processus d’analytique des données détaillé ou approfondi, visant à comprendre pourquoi un événement s’est produit. Elle se caractérise par des techniques telles que l’analyse détaillée, la découverte de données, l’exploration de données et les corrélations. Dans chacune de ces techniques, les différentes opérations et transformations de données sont utilisées pour analyser les données brutes.
3. Analytiques prédictives
L’analytique prédictive utilise des données historiques pour établir des prédictions précises concernant des tendances futures. Elle se caractérise par des techniques telles que le machine learning, la prédiction, la comparaison de modèles et la modélisation prédictive. Dans chacune de ces techniques, les ordinateurs sont entraînés à étudier par ingénierie inverse les liens de causalité des données.
4. Analytique prescriptive
L’analytique prescriptive permet de faire passer les données prédictives au niveau supérieur. Elle ne se contente pas de prédire ce qui risque de se produire, mais elle propose aussi une réponse optimale à ce résultat. Elle peut analyser les implications potentielles de différents choix et recommander la meilleure ligne de conduite. Elle se caractérise par l’utilisation d’analyses graphiques, de la simulation, du traitement des événements complexes, des réseaux neuronaux et des moteurs de recommandation.
___
>>> Source  
[AWS](https://aws.amazon.com/fr/what-is/data-analytics/)