# Foreach et Tableaux Multidimensionnels

Je te propose un nouvel exercice pour maîtriser les "foreach", les tableaux multidimensionnels et les retours de fonction.

Il faut créer une fonction qui va permettre de classer les booléens qu'on lui donne.

Dans les paramètres de cette fonction, l'utilisateur va lui fournir un tableau désordonné contenant des 0, des 1, et d'autres éléments.

Par exemple : `[1, 0, 1, 0, 0, 0, 1, 'clé à molette', 0, 'chou-fleur', 'sandwich', 1]`

L'objectif est de faire en sorte que la fonction retourne un tableau multidimensionnel bien organisé par clés : valeur :
```js
{ '0': [0, 0, 0, 0, 0], '1': [1, 1, 1, 1], 'autres': ['clé à molette','chouffleur','sandwish'] }
```
- Les tableaux : https://developer.mozilla.org/fr/docs/Learn/JavaScript/First_steps/Arrays
- Les foreach : https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach

Je suppose que ça va être compliqué, alors n'hésite pas à m'envoyer une première version et nous la retravaillerons petit à petit.
Tu peux utiliser http://www.codepen.io pour partager le code. 🤖

Good luck !!

# Cas Concret

Cette fonction peut servir à organiser proprement du contenu. Imaginons que nous voulons créer des fiches pour des films avec le titre, le casting, et le synopsis, et que notre partenaire nous envoie une TONNE d'informations incluant toutes les séances en France, l'âge des acteurs, le réalisateur, des photos, etc. Cette fonction nous permettrait d'ordonner correctement le contenu reçu et de le formater selon nos besoins pour le réutiliser ensuite.
