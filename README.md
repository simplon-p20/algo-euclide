un algorithme est comme une recette de cuisine, c'est-à-dire un ensemble d'instructions permettant d'aboutir à un résultat, avec les caractéristiques suivantes :

* Il se termine en un nombre fini d'étape.
* Il est composé d'instructions non ambigües.
* Il a des entrées (ou pas...).
* Il a des sorties (ou pas...).
* Il peut en principe être appliqué par une personne avec un papier et un crayon.

---

**Algorithme d'Euclide**. Soit 2 entiers positifs *m* et *n* avec *m* > *n*, trouver leur PGCD (plus grand diviseur commun), c'est-à-dire l'entier positif le plus grand dont *m* et *n* sont tous les 2 des multiples.

**étape 1**. [Trouver le reste.] Diviser *m* par *n* et associer à le reste de la division à *r*. (Cela donne 0 <= *r* < *n*.)

**étape 2**. [Est-il nul ?] Si *r* = 0, l'algorithme est terminé ; la réponse est *n*.

**étape 3**. [Réduire.] Associer *n* à *m*, *r* à *n* et repartir à l'étape 1.

1. Calculer le PGCD pour *m* = 544 et *n* = 119.
2. Oublier les règles, et calculer le PGCD pour *m* = 119 et *n* = 544. Optimiser l'algorithme en rajoutant une **étape 0**.
