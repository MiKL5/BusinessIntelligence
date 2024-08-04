# **Permutations et Arrangements**
## **La permutation**
C’est une disposition des objets dans un certain ordre.  
Cela perle de réarangement d’objets. Avec ‘A, B, C’, il y a six permutations possibles.  
Pour calculer le nombre de permutations possible, il faut prendre (“factorielle n”).  
IL y a trois éléments ‘abc’, fixés à ‘n’.  
n!=3!=3xéX1=6 permutations. <!-- abc est égales à factorielle 3, soit 3x2x1 = - permutations --> 
## **L’arrangement**
Si l’on prend un sous-ensemble d’éléments dans une permutation est un arangeemnt.  
Le nombre de permutations possible de ’_k_’ objet dans un ensemble de ’_n_’ objets est donné par la formule :  
![arrangement](../../../assets/arrangement.png)  
’_K_’ est le nombre d’objets, ’_n_’ est le nombre de lettres (26) et ’_k_’ (3) car je veux le nombre de permutations possible par ensemble de lettres. La formule est factorielle, divisée par (n-k), puis prndre la factorielle de ça.
### Permutation sans répétition
##### Exemple :
Le site nécessite un ensemble de 4 caractères (des muniscules et chiffres de 0 à 9).  
Il est interdit de répéter une lettre ou un chiffre.  
<!-- Les factorielles au numérateur et dénominateur sont très courants -->
```json
Combien peut-il y en avoir ?  
À quoi est égale ‘N’, puis à quoi est égale ‘K’ ?  

N=26(letttres)+10(chiffres)=36  
K=4(objets séléctionnés)  

36-4=32 donc factorielle 32 qui est inclu dans la factorielle 36, il suffit de barré 32 et inférieur au numérateur ce qui annule le dénominateur. 

36x35x34x33=1'413'720 arrangeemnts.
```
Mais avec la répétition ?
### Permutation avec répétiton
Combien d’arrangemnt de ‘k’ objets dans un ensemble de ‘n’ objets aurais-je ?  
![répétition](../../../assets/repetition.png)  
Combien de plaques d’immatriculation à 4 chiffres (0 à 9) sont fabricables, la répétition est permise ?  
```json
n^K=10^4=10'000 arrangements possibles
```