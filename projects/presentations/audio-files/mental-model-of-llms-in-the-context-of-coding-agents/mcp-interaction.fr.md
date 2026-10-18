À partir de là, la bibliothèque qu'on utilise pour faire du MCP va être capable de transformer les fonctions en schémas qui vont pouvoir être injectés dans le contexte.

Là, j'ai mis à gauche ce que le modèle reçoit dans son contexte. Pour la fonction traduite en schéma, on voit bien qu'il y a le nom de la fonction, une description, ce qui va permettre au modèle de savoir quand est-ce qu'il veut appeler cette fonction. Et également, un schéma d'input va permettre au modèle de savoir comment formuler ses appels.

Et là, ce qu'on voit aussi à droite, c'est l'appel par le modèle et le résultat. Donc l'appel par le modèle va se faire en décrivant le tool use, l'id, le nom, les inputs. Et le code de cette fonction va alors s'exécuter, et le retour de cette fonction va repartir dans le contexte. Et le modèle va continuer à générer à partir de ce retour, potentiellement en offrant lui-même après ce résultat une génération beaucoup plus intéressante que s'il avait dû deviner tout seul.
