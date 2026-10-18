Et enfin, le replay de la commande que doctor venait de nous donner, pyscotch scotch build, avec le flag parallel.

Il y a d'abord un preflight qui vérifie ce qui est disponible sur la machine, puis les sources de Scotch 7.0.13 sont téléchargées depuis le GitLab de l'Inria, avec leur sha256 vérifié.
Pour cette version-là, aucun quickfix n'est nécessaire, on verra dans la pipeline que ce n'est pas le cas de toutes.

Ensuite, c'est un make classique de libscotch et de libptscotch, et la version construite est sélectionnée pour pyscotch. Le tout prend une minute sur huit cœurs, et surtout, sans root.

À la fin, on relance doctor, cette fois en mode parallèle, et pour vérifier que tout fonctionne, un graphe distribué de 8 par 8 par 8 est partitionné en 4 sous mpirun avec deux rangs.
