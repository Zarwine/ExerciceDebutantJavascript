# Foreach et Tableau Multidimensionnel

Je te donne un nouvel exercice pour maîtriser les "foreach", les tableau multidimensionnel et les retours de commande

Il faut créer une fonction qui va permettre de ranger les booléens qu'on lui donne.

Dans les paramètres de cette fonction l'utilisateur va lui donner un tableau tout en bordel avec des 0 des 1 et d'autres trucs. 

Par exemple : `[1,0,1,0,0,0,1,'clef à molette', 0, 'chouffleur', 'sandwish', 1]`

L'objectif est de faire en sorte que la fonction retourne un tableau multidimensionnel bien rangé par clés : valeur:
```js
{ '0': [0, 0, 0, 0, 0], '1': [1, 1, 1, 1], 'autres': ['clef à molette','chouffleur','sandwish'] }
```

Voici une doc sur les tableau : https://developer.mozilla.org/fr/docs/Learn/JavaScript/First_steps/Arrays
Et une autre sur les foreach : https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach

Je suppose que ça va être galère alors n'hésite pas m'envoyer une première version et on va la retravailler petit à petit.
Tu peux utiliser http://www.codepen.io pour partager le code :slight_smile:

Good luck !!
