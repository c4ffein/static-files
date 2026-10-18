Là, ce que je mets ici, c'est un replay de mon hegel-c. Avec le scotch d'avant le fix, on voit qu'effectivement, j'arrive à trouver des cas de test qui échouent, et je peux itérer pour trouver le cas minimal.

L'intérêt aussi, c'est que je fais du fork à chaque fois que je veux exécuter mon cas de test. Comme on est sur un langage beaucoup plus bas niveau que Python, par exemple, on peut avoir des segfaults, et on veut pouvoir les considérer comme une erreur et continuer le shrinking.

Ce que ça veut dire, c'est que le bridge peut fork, potentiellement observer un segfault dans l'enfant, et passer au cas de test suivant, on n'a donc pas de problème à écrire des tests qui peuvent corrompre la mémoire.
