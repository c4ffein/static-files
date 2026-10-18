Pour revenir à pyscotch, je vais montrer rapidement où en est le projet aujourd'hui, puisqu'on est passé d'un wrapper minimaliste, vibé en quelques jours pour pouvoir lancer Hypothesis, à quelque chose qui est maintenant réellement utilisable.

Aujourd'hui, ça s'installe en une ligne avec uv pip install pyscotch, avec un Scotch séquentiel embarqué dans la wheel.

Il y a une commande doctor qui vérifie l'installation, et une commande scotch build qui compile Scotch depuis les sources, y compris la version MPI. Les stratégies qu'on passe aux routines sont validées par le parseur de Scotch lui-même.

Et surtout, les sorties sont identiques à celles de gpart, gord et gmap, c'est-à-dire les outils en ligne de commande de Scotch. C'est ce qui va me servir d'oracle, on va y revenir.
