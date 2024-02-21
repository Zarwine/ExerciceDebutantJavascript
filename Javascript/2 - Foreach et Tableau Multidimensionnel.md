# Foreach et Tableau Multidimensionnel

Je te donne un nouvel exercice pour maîtriser les "foreach", les tableau multidimensionnel et les retours de commande

Il faut créer une fonction qui va permettre de ranger les booléens qu'on lui donne.

Dans les paramètres de cette fonction l'utilisateur va lui donner un tableau tout en bordel avec des 0 des 1 et d'autres trucs. 

Par exemple : `[1,0,1,0,0,0,1,'clef à molette', 0, 'chouffleur', 'sandwish', 1]`

L'objectif est de faire en sorte que la fonction retourne un tableau multidimensionnel bien rangé par clés : valeur:
```js
{ '0': [0, 0, 0, 0, 0], '1': [1, 1, 1, 1], 'autres': ['clef à molette','chouffleur','sandwish'] }
```
- Les tableaux : https://developer.mozilla.org/fr/docs/Learn/JavaScript/First_steps/Arrays
- Les foreach : https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach

Je suppose que ça va être galère alors n'hésite pas m'envoyer une première version et on va la retravailler petit à petit.
Tu peux utiliser http://www.codepen.io pour partager le code 🤖

Good luck !!

# Cas Concret

Cette fonction peut servir à ranger proprement du contenu. Imaginons que nous voulons faire des fiches pour des film avec le Titre, le casting et synopsis et que notre partenaire nous envoie une TONNE d'information avec toutes les séances en france au cinéma, l'age des acteurs, le réalisateur, des photo etc.. Cette fonction nous permettrait d'ordonner correctement le contenu reçu et de le formater selon nos besoin pour le réutiliser ensuite. 
