# Vérifier les chiffres
Il est indispensable de vérifier les chiffres au long de l’analyse ; il y a des très nombreuses sources d’erreur entre ce que l’on veut et le résultat.  
Il peut y avoir :
* Des données incorrectes (mauvais choix de la source) ;
* L’extraction des données (partielle ou duplication) ;
* Lors du nettoyage (l’altération) ;
* Le traitement des données (formule.s incorrecte.s).

Différentes méthodes évitent de vérifier plusieurs fois chaque méthodes afin de savoir s’il y a une erreur et la chercher. Elles consistent à prendre du recul en prendre au global les valeurs obtenues.  

## La vérification en amont
Dans la population : combien de personnes dans les données extraites ? Ceci doit être cohérent en amont de l’extraction (pas de perte de population). Une autre info donne le total de cette population ou au moins l’ordre de grandeur (en réfléchissant autres sources contenant ce nombre [outils d’Analytics, ficher comptable, outils d’e-mailing, 3450 est aussi rassurant que les 3500 avec lesquels je travail, pas 5000] ou en se servant d’ordre de grandeur [connaissances personnelles grâce aux souvenirs d’évènements, rapports d’activités, discussions, …]).  

Cette vérification vaut autant pour les autres indicateurs que l’on manipule, CA, nombre de ventes, et cætera.  
Si l’on utilise des chiffres tels que le nombre d’articles par personnes, la panier moyen, l’écart moyen entre deux achats, on peut aussi faire une pause et s’interroger de la plausibilité des chiffres. Et de la même manière observer les taux obtenus (5% de paniers validés sont des données probablement fausses).  
Une erreur lors de l’extraction des données a généralement un impact important et est détectable grâce aux ordres de grandeur. 

## La vérification en aval
Le total doit rester à 3500 ; l’exactitude est primordiale, des données ne doivent ni apparaitre ni disparaitre.  
Ce processus est valable avec les formules, graphes, tableaux croisés dynamiques ; il peut arriver que le tableau Excel ne couvre pas toutes les données.

Le long de l’analyse, il faut s’assurer que les chiffres somment. La somme des percentages doit rester égales à 199%. 