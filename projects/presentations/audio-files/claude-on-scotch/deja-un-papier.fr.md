Cette idée, je ne suis clairement pas le seul à l'avoir, sachant qu'il y a déjà un papier qui a été publié le 10 octobre 2025, c'est à dire "Agentic Property Based Testing, Finding Bugs Across the Python Ecosystem".

On peut remarquer dans la liste des auteurs qu'il y a une partie qui vient d'Anthropic, et une partie qui vient directement d'Hypothesis. Et globalement, ils ont un système qui a été construit avec un agent qui lit le code, qui infère les propriétés, qui écrit les tests et rédige le rapport.

C'est à dire que de simples fichiers markdown qui décrivent les procédures permettent à un modèle frontière de l'époque de suivre la recette, d'écrire les tests Hypothesis, de les lancer, d'interpréter les résultats, et de boucler.

L'intérêt, c'est qu'on a 56% des rapports générés qui sont en fait des bugs valides. On peut se poser la question de la rentabilité, mais ici, avoir un rapport positif sur deux offre un très bon RoI sur la relecture des rapports.

Dans un esprit d'analyse des différents événements: ça c'est quelque chose qui a été publié six mois avant la vague Mythos. A mon avis, on pouvait déjà s'attendre à ce que les modèles suivants, étant entrainés sur les sorties des usages courants, soient alors capables de faire de la recherche de bugs même sans être tenus par la main.
