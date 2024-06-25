# Choisir la méthode de mesure
## Comparaison
_Valeurs initiale_ et _valeur passée_ sont analogues car elles sont assez faciles à mettre en place, notamment à posteriori.  

Valeurs initiales et valeurs passées | Méthodes statistiques comme A/B  test
---|---
Approximatives | Fiables, même avec des fluctuations hebdomadaires ou saisonnières
_**Avantages**_ |
Faciles à mettre en place |
Utilisables à posteriori |
_**Inconvénients**_ |
Statistiquement moins fiables | Impossible à mettre en place à postériori
… | Ne concerne que les actions répétables
… | Incombe de diviser aléatoirement la population en deux
… | La définition de “ne rien faire” au groupe B n’est pas nécessairement évidente
_**Biais possibles**_ | _**Biais possibles pour l’AB test**_
**Bcp d’événements peuvent avoir affecté l’indicateur à peu près au même moment que l’action** | **Évolution différente de l’impact à long terme**
Autres actions dans l’entreprise | résistance au changement
événements extérieurs à l’entreprise | résistance au changement
Variation aléatoires de l’indicateur | attrait de la nouveauté
… | effet de saisonnalité
Avec les méthodes simples, si l’indicateur est plus élevé, il est impossible de savoir si les variations sont dues à l’action où a ces autres évènements. Ce peut être une variation normale.  
Seules les méthodes statistiques permettent d’être sûr. Nonobstant, les biais la rende parfois non représentative à log terme, la plupart des entreprises étant impactés par des variation saisonnières ou économiques.  
## Choix
1. L’action à t-elle eu lieu ? Si oui, l’AB test est exclu.  
    1.1 Y a t-il des données avant l’action  
        1.1.1 Non, alors la valeur initiale permettra une estimation  
        1.1.2 Oui, alors l’indicateur a-t-il des fluctuations saisonnières ?  
            1.1.2.1 Oui, alors la valeur passée est utile  
            1.1.2.2 Non, alors la valeur initiale  
2. L’action n’a pas encore eu lieu  
    2.1 Les conditions pour l’A/B test sont-elles là ?  
        2.1.1 Non  
        2.1.2 Oui, y a t-il besoin de la fiabilité d’un A/B test ?  
            2.1.2.1 Non  
            2.1.2.2 Oui, alors A/B test  

L’A/B test est plus difficile à mettre en place dont, d’autre méthodes plus simples peuvent être choisies.  
Ce qui renvoie à la question des indicateurs, pour choisir la méthode.  

Dès que l’on sait quel indicateur va quantifier le résultat de l’action et comment mesurer le résultat, il faut déterminer ce qui fait un succès. Ça peut être :
* Tout résultat supérieur à la valeur de référence ;
* Augmentation de la valeur de 10%, 20%, …

C’est une étape généralement instinctive qui mértite de l’attention car elle permet de comprendre ce que l’on vise et si l’impact voulu est important ou non.