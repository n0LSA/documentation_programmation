**Analyse du prompt et intentions**

1. Clarifier la différence entre la **notation dynamique** pour le nom de la propriété (i.e. `[key]`) et l’utilisation d’une variable directement comme valeur.
2. Illustrer ce qui se passe quand on veut une propriété dont le nom est défini dynamiquement par une variable.
3. Confirmer qu’on n’a pas besoin de crochets pour la **valeur** de la propriété si on veut simplement y insérer une variable.

---

## 1. Rappel sur la “notation dynamique” pour le nom d’une propriété

La notation entre crochets `[variable]` (ou `[expression]`) est ce que l’on appelle la **Computed Property Name** en JavaScript. Elle permet de **calculer** le nom d’une propriété à partir d’une variable ou d’une expression. Par exemple :

```js
const cle = 'username';
const obj = {
  [cle]: 'Alice'
};
```

Dans cet exemple, la propriété de l’objet aura pour nom la valeur contenue dans la variable `cle` (soit `username`), et non littéralement `cle`.

---

## 2. Pas besoin de notation dynamique pour la valeur

Pour la **valeur**, on peut directement utiliser une variable sans la mettre entre crochets : il suffit de l’écrire comme on écrirait n’importe quelle valeur.

Exemple :

```js
const nomPropriete = 'identifiant';
const valeurPropriete = 42;

const monObjet = {
  [nomPropriete]: valeurPropriete
};

console.log(monObjet);
// Résultat : { identifiant: 42 }
```

- **`[nomPropriete]`** : notation dynamique → on utilise la valeur de la variable `nomPropriete` comme nom de la propriété, ici `'identifiant'`.
- **`valeurPropriete`** : aucun crochet → c’est simplement la valeur qu’on assigne à la propriété `'identifiant'`, ici 42.

---

## 3. Exemple pas à pas

Supposons les variables suivantes :

```js
const propName = 'score';
const propValue = 10;
```

### a) Notation dynamique pour le nom

```js
const result1 = {
  [propName]: propValue
};
// Résultat : { score: 10 }
```

Le nom `'score'` (valeur de `propName`) est utilisé comme clé, et la valeur 10 (contenue dans `propValue`) est assignée à cette clé.

### b) Nom littéral, valeur dynamique

```js
const result2 = {
  propName: propValue
};
// Résultat : { propName: 10 }
```

Cette fois, la clé est littéralement `'propName'` (et non `'score'`), et sa valeur est 10.

---

## 4. Conclusion

- Pour **nommer dynamiquement** une propriété d’objet avec une variable ou une expression, vous **devez** utiliser la syntaxe `[variable]`.
- Pour la **valeur** d’une propriété, vous pouvez directement affecter la variable sans utiliser de crochets.

En d’autres termes, si vous voulez que le **nom** de la propriété change en fonction d’une variable, il est nécessaire d’employer la notation dynamique `[key]`. Par contre, la **valeur** peut être assignée simplement :

```js
const myKey = 'someKey';
const myValue = 'someValue';

const obj = {
  [myKey]: myValue // nom dynamique, valeur directe
};
```