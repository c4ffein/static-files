L'intérêt a donc été de pouvoir trouver des bugs dans Scotch assez rapidement. Le bug le plus simple a déjà été trouvé le septième jour, sachant que je n'ai pas passé plus d'une heure ou 2 par jour sur ce projet. Le 4 novembre 2025, premier commit, depuis des sessions cloud de Claude Code, depuis la version web.

Ce que je cherchais simplement à faire, c'était charger à la fois la version 32 et 64 bits, parce que je me dis que ça va être intéressant de pouvoir faire des tests sur les deux architectures et vérifier si ça correspond. Pareil, je veux à la fois tester sur la version séquentielle et la version MPI. Je veux faire tout ça dans un même process.

Ce que ça veut dire, c'est que je dois build avec des suffixes, ce qui semble initialement bien parti. Mais rien que quand j'essaie de charger la version 32 bits et 64 bits en même temps, dans un même process, il y a des incohérences au niveau de la table de symboles, il y a des collisions.

Effectivement, il y a des symboles qui n'étaient pas suffixés. C'est dû à quelques macros manquantes, ce qui a pu être découvert même sans démarrer spécifiquement la recherche de bugs, même si c'était effectivement mineur.
