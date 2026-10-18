Ce qui va être intéressant avec nos expérimentations, c'est qu'entre le moment où j'ai commencé à jouer avec Hypothesis et Scotch, et le moment où je trouve ces bugs-là en essayant de faire de l'analyse statique, il y a Hegel qui a été publié.

Hegel, c'est un projet porté en partie par des mainteneurs principaux d'Hypothesis. L'idée, c'est de rendre le moteur d'Hypothesis disponible dans tous les langages, ce qui se fait relativement facilement via un bridge en Rust.

Avant que l'équipe d'Hegel publie son propre binding C, j'avais déjà commencé à m'amuser avec le bridge Rust, et à créer avec Claude ma propre surcouche en C, que j'ai appelée hegel-c. Leur binding officiel, lui, est volontairement minimaliste : il est livré directement dans la lib Rust, sans dépôt séparé. Pour éviter la confusion, je vais dire « le binding officiel » pour le leur, et « mon hegel-c » pour le mien.

Je l'ai mis en pause, mais il m'a permis de simplifier mes interactions avec Scotch : il vise à faciliter la manipulation de structures de données complexes, alors que le binding officiel fournit des primitives minimalistes.

La dernière version de mon hegel-c se base d'ailleurs sur le binding officiel, en ajoutant simplement des outils de plus haut niveau. Je verrai dans les mois qui viennent s'il y a toujours un intérêt à le maintenir, ou si l'approche minimaliste du binding officiel, facile à adapter à chaque projet, suffit pour la très grande majorité des besoins en C.
