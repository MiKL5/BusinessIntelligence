# **Les mesures de dispersion**
Il y a trois principales manières, l’_étendue_, la _variance_ et l’_écart-type_.  
```sql
9 10 11 12 15 16 19 19 21 23 28 30 33 34 36 39
-- La moyenne est 22,25
```
La moyenne n’informe pas à propos de la dispersion des données. 
## Décrire la répartition de l’échantillon
### **L’étendue**
L’_étendue_ est définie par la valeur maximale et minimale en faisant la différence.
```sql
39 - 9 = 30
```
L’étendue est 30.
* Elle ne considère que deux valeurs d’une série (max - min).
* Est influençable par des ”_valeurs aberrantes_” (_outliser_).

**L’étendue décrit-elle vraiment les données ?**
###  **La variance**
La variance considère chaque point de données.  
Elle est calculée comme la somme des distances au carré entre chaque point et la moyenne de l’ensemble de données. Globalement, la distance moyenne de chaque point par rapport à la moyenne ou par rapport au centre.  
Il y a une différence entre la variance de l’_`échantillon`_ et la façon de calculer la variance de la _`population`_.  
La principale différence est soumise à la `correction de Bessel` 
Échantillon | Population
---|---
(n-1). | (n)

_La correction de Bessel vise à réduire le biais dus à une sorte de taille d’échantillon finie et qu’elle va essentiellement corriger le biais lorsque l’on essaye d’estimer la variance de la population parce que l’on ne peut pas réellement considérer chaque points de données._  
_La division par `n-1` rend la variance globale plus importante. Car on peut supposer que plus le numérateur est grand, plus la variance est petite et on utilise la correction de Bessel. Puisque que l’on prend que quelques points de données de toute la population, il n’y aura pas une très bonne estimation de la variance réelle de toute la population. Donc, pour être correcte utiliser `n-1` comme dénominateur._

* Pour l’échantillon, il faut utiliser
```
x et x-barre minuscule et n-minuscule pour le nombre d'éléments
```
* Pour la variance de la population
```
X majuscule, la lettre mew pour la moyenne et N majuscule pour le nombre d'éléments total.
```
6,7 ans au carré étant difficile à interpréter, il est possible d’utiliser l’écart-type.
### **L’écart-type**
C’est essentiellement la racine carrée de la variance.  
Il a l’avantage de posséder les mêmes unités que l’échantillon. Avec la racine carrée des années, on récupère l’unité avec laquelle on travaille originellement, soit les années.  
Il est significatif de parler de _“valeurs situées dans l’écart-type de la moyenne ou deux écarts-types de la moyenne”_.  

Ici le calcul est le même pour la population et l’échantillon. 