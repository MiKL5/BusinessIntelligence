# **La mesure des quartiles**
Les _quartiles_ et les _interquartiles (EI)_ sont une autre manière d’écrire les données.  
Ils ont l’avantages de considéré chauqe point de données ; ne pas agréger les points.  
```sql
9 10 10 11 13 15 16 19 19 21 23 28 30 33 34 36 44 45 47 60
```
* La première étapa consiste à diviser la série en deux afin de trouver sa veleur médiane ;
* Puis diviser les sous-divisions en deux. Il y a alors trois lignes. Une est divisée en deux. Les deux autres à l’extérieur, sont aussi divisées en deux.
* Ces trois lignes sont les quartiles.

Pour découpé en quart, il faut trois lignes. Il y a le premier quartile, le second est la médiane, puis le troisième.  
Cela divise les données en compartiments de même taille.  
Le premier quartile est 14. Le second (la médiane) est 22. Et le dernier est 35.

Si la série est désordonnée, il est indispensable de la trier.  
Et si une valeur tombe pile sur la médiane, il y a deux possibilités :
* La supprimer ;
* L’ajouter à gauche et à droite de la médiane.
## **Le vocabulaire**
Le premier quartile est nommé le `vingt-cinquième percentile`.  
Et le troisième quartiles : le `soixante-quinzième percentile`.
## **Le diagramme en boîte (boîte à moustache/box-plot)**
La boîte informe de la distribution réelle des données.  
La boîte est à l’intérieur, et les moustaches de part et d’autre.  

Les écarts des quartiles sont rarement de la même taille.  
Pour comprendre la distribution réelle de l’ensemble centrale, une ligne verticale est tracée varticalement au milieu de la boîte.

L’écart interquartile est la distance entre le premier quartile et le troisième (la longueure de la boîte).
## **Les clotures et valeur aberrantees (outliers) et comment les traiter**
### Qu’est-ce qu’une ”`outlier`” ?
Très courament, il est fixer une ”`clôture`” 1,5 fois plus grande que l’écart intercartile.  
Tout ce qui y est en dehors est une ”`outlier`”.  
Ces valeurs aberrantes sont determinées par les données ; pas par un pourcentage arbitraire. C’est la distribution de l’ensemble de données qui défini ce qu’est une valeur aberrante.  
La longueur réelle de la boîte est multipliée par 1,5 et essentiellement ce qui est en dehors est aberrant. Si 60 n’est pas aberrant 70 l’est car il est aprés les 1,5 fois.

Celon le contexte, il peut être utile de conserver ces ’`outliers`’ et les examinées ou de les rejetées.

Les moustâche sont ramenées aux valeurs vers l’intérieur jusqu’aux valeurs les plus extérieures dans de la clôture. Au delà de la clôture, ce sont les ’`outliers`’.  
Et pour tracer les moustaches jusqu’aux valeurs min et max, il faut les placé à ces valeurs.