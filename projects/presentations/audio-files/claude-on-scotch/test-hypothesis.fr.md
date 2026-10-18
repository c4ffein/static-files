Je vais montrer très rapidement à quoi ressemble un test Hypothesis. On voit ici que ça ressemble globalement à un test qu'on pourrait trouver en Python.
Mais la grosse distinction qu'on va avoir ici, c'est l'utilisation d'un décorateur Given, qui est importé depuis Hypothesis, et qui permet de définir des inputs pour le test en définissant un ensemble de différentes stratégies (ici en utilisant la surcharge des opérateurs).

L'intérêt de faire ça, c'est qu'on va pouvoir rejouer ce test avec différents inputs aléatoires, et donc potentiellement trouver des edge cases que normalement on ne trouverait pas.
Cela va surtout permettre d'accéder à un mécanisme de réduction, c'est-à-dire que si jamais on trouve un test qui échoue, on va pouvoir relancer le même test avec des inputs différents à chaque fois, mais en essayant de se rapprocher d'un cas minimal. C'est ce qu'on appelle le shrinking, on en verra un exemple après.
