
```table-of-contents
title: 
style: nestedList # TOC style (nestedList|nestedOrderedList|inlineFirstLevel)
minLevel: 0 # Include headings from the specified level
maxLevel: 0 # Include headings up to the specified level
includeLinks: true # Make headings clickable
debugInConsole: false # Print debug info in Obsidian console
```

## la fonction map


La fonction `map()` en JavaScript est une méthode de prototype d'Array qui est utilisée pour transformer les éléments d'un tableau en appliquant une fonction à chaque élément du tableau. Cette méthode renvoie un nouveau tableau contenant les résultats de l'application de la fonction à chaque élément. Elle ne modifie pas le tableau original.

  

### Syntaxe de base

```javascript

let nouveauTableau = tableauOriginal.map(function(element, index, array) {

// Logique de transformation

}, thisArg);

```

  

- **tableauOriginal** : Le tableau sur lequel `map()` est appelé.

- **function(element, index, array)** : La fonction de rappel exécutée sur chaque élément du tableau.

- **element** : L'élément courant du tableau.

- **index** (optionnel) : L'indice de l'élément courant dans le tableau.

- **array** (optionnel) : Le tableau sur lequel `map()` a été appelé.

- **thisArg** (optionnel) : La valeur à utiliser comme `this` lors de l'exécution de la fonction de rappel.

- **nouveauTableau** : Le nouveau tableau résultant, contenant les éléments transformés.

  

### Fonctionnement de `map()`

  

1. **Itération sur le Tableau**

- `map()` passe en revue chaque élément du tableau `tableauOriginal`.

  

2. **Application de la Fonction de Rappel**

- À chaque élément, la fonction de rappel est appelée, recevant l'élément courant, son indice et le tableau lui-même en tant qu'arguments.

  

3. **Transformation des Éléments :**

- La fonction de rappel effectue une opération ou une transformation sur l'élément courant et renvoie un nouveau résultat.

  

4. **Construction d'un Nouveau Tableau**

- Les valeurs renvoyées par la fonction de rappel pour chaque élément sont rassemblées dans un nouveau tableau.

  

5. **Renvoi du Nouveau Tableau**

- Une fois tous les éléments traités, le nouveau tableau transformé est renvoyé.

  

### Exemple d'Utilisation

  

Supposons que nous ayons un tableau de nombres et que nous voulions créer un nouveau tableau avec le carré de chaque nombre :

  

```javascript

let numbers = [1, 2, 3, 4, 5];

let squares = numbers.map(number => number * number);

console.log(squares); // [1, 4, 9, 16, 25]

```

  

Dans cet exemple, `map()` est utilisé pour calculer le carré de chaque élément du tableau `numbers`. Le résultat est un nouveau tableau `squares` contenant ces carrés.

  

### Points Importants

  

- `map()` est souvent utilisé pour transformer des données, notamment en manipulant des tableaux d'objets, en extrayant des sous-ensembles de données ou en convertissant des types de données.

- Contrairement à d'autres méthodes comme `forEach()`, `map()` renvoie toujours un nouveau tableau, ce qui le rend particulièrement utile dans la programmation fonctionnelle.

- `map()` n'affecte pas la taille du tableau original, mais la valeur de chaque élément peut être transformée. Si aucun élément n'est transformé, le tableau résultant aura la même taille que le tableau original.

  

La fonction `map()` en JavaScript est une méthode de l'objet Array qui permet de créer un nouveau tableau en transformant chaque élément du tableau original à l'aide d'une fonction de rappel. L'argument `thisArg` dans `map()` est un paramètre optionnel qui permet de spécifier le contexte (`this`) pour la fonction de rappel.


## Exemples simple

### 1. **Transformation d'Éléments**

- Modifier chaque élément d'un tableau.

- Exemple : Doubler chaque nombre dans un tableau de nombres.

```javascript

let numbers = [1, 2, 3];

let doubled = numbers.map(num => num * 2);

```

  

### 2. **Extraction de Propriétés d'Objets**

- Extraire une propriété spécifique de chaque objet dans un tableau d'objets.

- Exemple : Obtenir un tableau des noms à partir d'un tableau d'utilisateurs.

```javascript

let users = [{name: "Alice", age: 25}, {name: "Bob", age: 30}];

let names = users.map(user => user.name);

```

  

### 3. **Conversion de Types de Données**

- Transformer les types de données des éléments d'un tableau.

- Exemple : Convertir un tableau de chaînes de caractères en nombres.

```javascript

let stringNumbers = ["1", "2", "3"];

let numbers = stringNumbers.map(Number);

```

  

### 4. **Appliquer une Fonction Complexes**

- Appliquer une logique complexe ou une fonction personnalisée à chaque élément.

- Exemple : Ajouter une nouvelle propriété à chaque objet dans un tableau.

```javascript

let items = [{name: "chair"}, {name: "table"}];

let itemsWithPrices = items.map(item => ({ ...item, price: 100 }));

```

  

### 5. **Création de Nouvelles Structures de Données**

- Générer un nouveau format ou une nouvelle structure de données à partir d'un tableau existant.

- Exemple : Créer un tableau de messages à partir d'un tableau d'utilisateurs.

```javascript

let users = [{name: "Alice", age: 25}, {name: "Bob", age: 30}];

let messages = users.map(user => `Bonjour ${user.name}, vous avez ${user.age} ans.`);

```

  

### 6. **Combinaison avec d'autres Méthodes de Tableau**

- Chaîner `map()` avec d'autres méthodes de tableau pour des opérations plus complexes.

- Exemple : Utiliser `map()` et `filter()` ensemble.

```javascript

let numbers = [1, 2, 3, 4, 5];

let doubledEvenNumbers = numbers.filter(num => num % 2 === 0).map(num => num * 2);

```

  

### 7. **Mappage avec Index ou Tableau Complet**

- Utiliser l'indice de l'élément ou le tableau complet pour des opérations plus avancées.

- Exemple : Utiliser l'indice pour modifier les éléments.

```javascript

let items = ["first", "second", "third"];

let indexedItems = items.map((item, index) => `${index}: ${item}`);

console.log(indexedItems)

```

  

### 8. **Opérations Mathématiques ou Algorithmiques**

- Effectuer des calculs complexes ou des algorithmes sur les éléments d'un tableau.

- Exemple : Calculer le carré de chaque nombre d'un tableau.

```javascript

let numbers = [1, 2, 3, 4];

let squares = numbers.map(num => num * num);

console.log(squares)

```

  

`map()` est une méthode de tableau très puissante qui est largement utilisée pour sa capacité à transformer facilement les éléments d'un tableau, tout en gardant le tableau original inchangé.

  
  

<br>

  

<hr>

  

<br>

  

## `thisArg`

  

L'argument `thisArg` est utilisé pour définir le contexte (`this`) dans lequel la fonction de rappel est exécutée. Cela peut être particulièrement utile lorsque vous souhaitez accéder à des propriétés ou des méthodes d'un objet spécifique dans votre fonction de rappel.

  

#### Exemple sans `thisArg`

```javascript

let numbers = [1, 2, 3, 4, 5];

let squares = numbers.map(function(number) {

return number * number;

});

```

  

Dans cet exemple, la fonction de rappel calcule le carré de chaque nombre. `this` dans la fonction de rappel n'est pas défini ou se réfère à l'objet global.

  

#### Exemple avec `thisArg`

```javascript

function multiply(number) {

return number * this.multiplier;

}

  

let numbers = [1, 2, 3, 4, 5];

let multiplierObject = { multiplier: 10 };

let multipliedNumbers = numbers.map(multiply, multiplierObject);

```

  

Ici, la fonction `multiply` utilise `this.multiplier`. Lorsque `map()` est appelé, `multiplierObject` est passé comme `thisArg`, ce qui fait que `this` dans `multiply` se réfère à `multiplierObject`.

  

### Points Importants

  

- Si la fonction de rappel est une fonction fléchée (`arrow function`), `thisArg` est ignoré car les fonctions fléchées n'ont pas leur propre contexte `this` ; elles le captent de leur contexte englobant.

- `map()` est utilisée pour les transformations de données et renvoie un nouveau tableau sans modifier le tableau original.

- `thisArg` est utile pour accéder à des objets ou des fonctions spécifiques dans la fonction de rappel sans avoir à les lier explicitement.

  
  

La fonction `map()` en JavaScript est une méthode très versatile utilisée pour créer un nouveau tableau en transformant chaque élément d'un tableau source. La fonction de rappel utilisée avec `map()` peut prendre jusqu'à trois arguments : l'élément en cours de traitement, son indice dans le tableau et le tableau lui-même. Ces arguments sont souvent notés comme `element`, `index` et `array`.