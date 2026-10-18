Par contre, dans mon cas, ça m'amène à chercher un moyen de bridger Scotch et Hypothesis.

Il y a déjà un wrapper pour Scotch qui s'appelle ScotchPy, mais le problème, pour moi, c'est qu'il est en retard sur les mises à jour : si je fais de la recherche de bugs, je veux toujours avoir la dernière version disponible.

Aussi également, il y a le fait que je n'ai pas l'ownership sur ScotchPy, et que, si jamais je veux faire des modifications, je vais être obligé de forker, en tout cas si jamais ça devient un projet long terme... Pour plusieurs raisons, ça peut être compliqué de demander des évolutions sur ScotchPy.

Moi, tout ce que je veux initialement, c'est un bridge, le moins coûteux possible. Et générer des wrappers, c'est très facile quand on a la bonne méthode, même avec les modèles disponibles à ce moment : on n'est pas nous en train de faire l'ingénierie complexe, on ne s'occupe que de la petite couche au-dessus qui permet de faire le pont entre un langage et un autre.

Je me retrouve donc à essayer de créer un système automatisé qui écrit du code Scotch en C, génère l'équivalent Python, et vérifie l'équivalence. Et à partir de ça, en fait, je me retrouve avec une boucle qui permet de créer un wrapper vraiment minimaliste, mais qui me permet déjà de commencer à faire des tests.

Le bonus pour moi, c'est que des bugs ont été trouvés avant même de lancer Hypothesis et d'avoir mes premiers tests en Python, uniquement en essayant de travailler avec le code source en C.
