# Adapter la modélisation pour estimer l’impact d’un nouveau produit
```mermaid
mindmap
root((**Problème initial**
_Question SMART_
_métrique à estimer_))
    Sous-question 1
        Sous-question 2
            (Elément.s de réponse)
        Sous-question 3
            (Elément.s de réponse)
```
Quel est la croissance du CA espérable dans les trois mois après le lancement du produit ?  
Un arbre est dessiner, sauf que les branches correspondent aux sous-éléments de la métrique à estimer.  
```mermaid
mindmap
root((**CA total**))
    CA du produit concerné
        (Le CA de Z correspond à)
        ((Le nb de vente
        x
        le prix))
        ((Le nb de ventes =))
            (Le nb utilisateurs potentiels
            x
            La capacité à les convaincres))
            (Le nombre de ventes par pays)
                (pays 1)
                (pays 2)
                (pays 3, ...)
    CA des autres produits
        (Le CA du nouveau produit peut il impacter les autres pruiduits)
```
Uen fois obtenu les sous-éléments que l’on peut estimer, on s’arrête et remonte la métrique principale en faisant les opération identifiées