On a ici un replay de l'installation, enregistré sur une machine sur laquelle il n'y a aucun Scotch.
On crée un venv avec uv, on installe pyscotch avec l'extra parallel, et ce qu'on voit, c'est que tout arrive depuis PyPI : pyscotch en version 7.0.4, mpi4py en wheel binaire, il n'y a rien à compiler.

Ensuite, cinq lignes de Python suffisent pour charger un petit graphe et le partitionner, et on obtient directement les parties, avec le Scotch 7.0.13 qui est embarqué dans la wheel. Le tout prend 1,4 seconde.

Pour moi, c'est important, puisque c'est une des choses qui manquait à scotchpy : pouvoir tester la dernière version de Scotch sans rien installer à la main.
