On peut donc facilement obtenir des cas minimaux. Ici, on est vraiment sur le cas optimal, c'est-à-dire un graphe à trois sommets qui a permis de déclencher le bug sur cette routine de Scotch : un sommet isolé, et deux autres sommets reliés par une arête.

Et ce qui est intéressant, c'est que dans mon rapport initial du 5 avril, il y avait un reproducteur à 14 sommets, écrit avec Claude, sans outil de réduction. Et dans le test qu'il a ajouté le 15, François avait lui aussi cherché à réduire, et était arrivé à un cas à six sommets : trois sommets isolés, et un triangle.

En utilisant mon hegel-c, on a pu découvrir un cas minimal à trois sommets. Ce qui est intéressant aussi, c'est que sur mes quelques runs, seuls deux sur cinq atteignent le minimum théorique. Les autres s'arrêtent à quatre sommets ou deux arêtes.

Je dis ça pour illustrer que quand on utilise le mécanisme du shrinking, on aura généralement un cas qui sera intéressant pour nous pour débugger, mais on n'a pas de garantie que ce soit le cas minimal.
