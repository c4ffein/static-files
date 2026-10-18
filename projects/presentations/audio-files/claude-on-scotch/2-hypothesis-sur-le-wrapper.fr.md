Une fois que j'ai pu obtenir un proof of concept pour mon wrapper, j'ai enfin pu lancer Hypothesis dessus.

L'intérêt va être d'ajouter facilement différents helpers qui permettront de créer des graphes scotch, on voit ici le simple_graph dans le décorateur, qui spécifie un nombre minimum et maximum de vertices.

A partir de là, je peux vérifier simplement un invariant de coloriage, que le coloring a été effectué correctement.

En résumé: J'ai ma propriété très simple et je vais chercher à vérifier qu'elle soit valide sur différents types de graphes.
