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

* itération 1 : m = 544, n = 119.
  * étape 1 : m/n = 4 reste 68 -> r = 68.
  * étape 2 : r non nul -> l'algorithme n'est pas terminé.
  * étape 3 : m = n = 119, n = r = 68.
* itération 2 : m = 119, n = 68.
  * étape 1 : m/n = 1 reste 51 -> r = 51.
  * étape 2 : r non nul -> l'algorithme n'est pas terminé.
  * étape 3 : m = n = 68, n = r = 51.
* itération 3 : m = 68, n = 51.
  * étape 1 : m/n = 1 reste 17 -> r = 17.
  * étape 2 : r non nul -> l'algorithme n'est pas terminé.
  * étape 3 : m = n = 51, n = r = 17.
* itération 4 : m = 51, n = 17.
  * étape 1 : m/n = 3 reste 0 -> r = 0.
  * étape 2 : r = 0 -> l'algorithme est terminé, la réponse est n = 17.

2. Oublier les règles, et calculer le PGCD pour *m* = 119 et *n* = 544. Optimiser l'algorithme en rajoutant une **étape 0**.

* itération 1 : m = 119, n = 544.
  * étape 1 : m/n = 0 reste 119 -> r = 119.
  * étape 2 : r non nul -> l'algorithme n'est pas terminé.
  * étape 3 : m = n = 544, n = r = 119.
* itération 2 : m = 544, n = 119.

-> quand m < n, la première itération échange *m* et *n*.

**étape 0**. [Garantir m > n.] Si *m* < *n*, échanger *m* et *n*.
