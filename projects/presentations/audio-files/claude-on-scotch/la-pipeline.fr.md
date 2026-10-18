Tout ça est tenu par une pipeline, qui est pour moi la vraie valeur du projet.

C'est à ce moment huit workflows GitHub Actions, qui tournent à chaque push, sur chaque tag, et pour certains toutes les six heures.

À chaque push, on teste pyscotch de Python 3.9 à 3.12, sur les quatre variantes de Scotch, 32 et 64 bits, séquentiel et parallèle, avec Hypothesis.
Et surtout, on fait des tests différentiels : les sorties de pyscotch sont comparées à celles de gpart, gord, gmap et de leurs versions distribuées.

Il y a aussi un golden master, c'est-à-dire que le parcours utilisateur complet, incluant l'installation, doctor, le build, le partitionnement, et mpirun, est donc rejoué dans un venv vide, en 14 étapes, et comparé à des sorties de référence.

On construit aussi Scotch depuis les sources pour trois versions, avec les sha256 pinnés, et on vérifie que le quickfix de la 7.0.12 est bien nécessaire, puisque sans lui, le build doit échouer.

Les wheels sont construites pour x86_64 et ARM, publiées sur PyPI par Trusted Publishing, puis réinstallées depuis PyPI, sans aucun checkout, pour certifier le paquet publié.
Et toutes les six heures, un job planifié dans GitHub Actions vérifie que la tarball upstream n'a pas bougé, et compare le dernier tag de Scotch sur le GitLab de l'Inria à la version embarquée : dès qu'une nouvelle version sort, je reçois un mail.
Le lundi matin, la matrice complète est reconstruite, et on vérifie aussi que le Scotch de Debian et celui de conda-forge n'ont pas changé.

Je n'ai fait que décrire et relire ces fichiers.
L'écriture de pipeline étant occasionnelle pour un ingénieur qui n'est pas spécialisé DevOps, elle était généralement fastidieuse, même si facile dans l'absolu.
C'est maintenant très rapide d'ajouter toute cette plus-value de qualité.
