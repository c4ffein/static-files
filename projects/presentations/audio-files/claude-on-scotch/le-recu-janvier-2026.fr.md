En soumettant le rapport incluant le test à François, le bug a pu être corrigé assez rapidement.

C'est-à-dire que là où, normalement, on aurait pu partir sur des analyses assez complexes, en ayant un cas de test minimal, il a finalement été très facile de trouver la correction qui allait régler le problème.

Je la mets en lien, c'était uniquement qu'on ne faisait pas une vérification sur un vertex qui aurait pu être coloré dans une passe précédente.

Ce qui est assez intéressant, c'est qu'on était sur une routine qui est relativement peu utilisée sur des graphes de ce format-là. C'est pour ça qu'il y a eu un bug qui, pendant aussi longtemps, n'a pas été trouvé dans les cas d'utilisation normale du logiciel.
