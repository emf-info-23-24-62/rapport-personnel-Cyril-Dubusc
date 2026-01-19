<h1>🤔 RP - 323 - Programmation fonctionnelle</h1>

> [!TIP] >**Référence Javascript:** <https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference>  
> **Tester du code JS** : <https://runjs.app/play>  
> **Convertir en PDF** : <https://marketplace.visualstudio.com/items?itemName=manuth.markdown-converter>

<h1>Table des matières</h1>

-   [Introduction](#introduction)
-   [Opérateurs javascript super-cooool 😎](#opérateurs-javascript-super-cooool-)
    -   [opérateur `?:`](#opérateur-)
    -   [opérateur `??`](#opérateur--1)
    -   [opérateur `??=`](#opérateur--2)
    -   [opérateur de décomposition 'spread' `...`](#opérateur-de-décomposition-spread-)
    -   [Déstructuration](#déstructuration)
-   [Date et Heure](#date-et-heure)
    -   [Obtenir la date et/ou heure actuelle](#obtenir-la-date-etou-heure-actuelle)
-   [Math](#math)
    -   [`Math.PI` - la constante π](#mathpi---la-constante-π)
    -   [`Math.abs()` - la |valeur absolue| d'un nombre](#mathabs---la-valeur-absolue-dun-nombre)
    -   [`Math.pow()` - élever à une puissance](#mathpow---élever-à-une-puissance)
    -   [`Math.min()` - plus petite valeur](#mathmin---plus-petite-valeur)
    -   [`Math.max()` - plus grande valeur](#mathmax---plus-grande-valeur)
    -   [`Math.ceil()` - arrondir à la prochaine valeur entière la plus proche](#mathceil---arrondir-à-la-prochaine-valeur-entière-la-plus-proche)
    -   [`Math.floor()` - arrondir à la précédente valeur entière la plus proche](#mathfloor---arrondir-à-la-précédente-valeur-entière-la-plus-proche)
    -   [`Math.round()` - arrondir à la valeur entière la plus proche](#mathround---arrondir-à-la-valeur-entière-la-plus-proche)
    -   [`Math.trunc()` - supprime la virgule et retourne la partie entière d'un nombre](#mathtrunc---supprime-la-virgule-et-retourne-la-partie-entière-dun-nombre)
    -   [`Math.sqrt()` - la raçine carrée d'un nombre](#mathsqrt---la-raçine-carrée-dun-nombre)
    -   [`Math.random()` - générer un nombre aléatoire entre 0.0 (compris) et 1.0 (non compris)](#mathrandom---générer-un-nombre-aléatoire-entre-00-compris-et-10-non-compris)
-   [JSON](#json)
    -   [`JSON.stringify()` - transformer un objet Javascript en JSON](#jsonstringify---transformer-un-objet-javascript-en-json)
    -   [`JSON.parse()` - transformer du JSON en objet Javascript](#jsonparse---transformer-du-json-en-objet-javascript)
-   [Chaînes de caractères](#chaînes-de-caractères)
    -   [`split()` - un ciseau qui coupe une chaîne là où un caractère apparaît et produit un tableau](#split---un-ciseau-qui-coupe-une-chaîne-là-où-un-caractère-apparaît-et-produit-un-tableau)
    -   [`trim()`, `trimStart()` et `trimEnd()` - épuration des espaces en trop dans une chaîne (trimming)](#trim-trimstart-et-trimend---épuration-des-espaces-en-trop-dans-une-chaîne-trimming)
    -   [`padStart()` et `padEnd()` - aligner le contenu dans une chaîne de caractères](#padstart-et-padend---aligner-le-contenu-dans-une-chaîne-de-caractères)
-   [Console](#console)
    -   [`console.log()` - Afficher un message sur la console](#consolelog---afficher-un-message-sur-la-console)
    -   [`console.info()`, `warn()` et `error()` - Afficher un message sur la console (filtrables)](#consoleinfo-warn-et-error---afficher-un-message-sur-la-console-filtrables)
    -   [`console.table()` - Afficher tout un tableau ou un objet sur la console](#consoletable---afficher-tout-un-tableau-ou-un-objet-sur-la-console)
    -   [`console.time()`, `timeLog()` et `timeEnd()` - Chronométrer une durée d'exécution](#consoletime-timelog-et-timeend---chronométrer-une-durée-dexécution)
-   [Tableaux](#tableaux)
    -   [`forEach` - parcourir les éléments d'un tableau](#foreach---parcourir-les-éléments-dun-tableau)
    -   [`entries()` - parcourir les couples index/valeurs d'un tableau](#entries---parcourir-les-couples-indexvaleurs-dun-tableau)
    -   [`in` - parcourir les clés d'un tableau](#in---parcourir-les-clés-dun-tableau)
    -   [`of` - parcourir les valeurs d'un tableau](#of---parcourir-les-valeurs-dun-tableau)
    -   [`find()` - premier élément qui satisfait une condition](#find---premier-élément-qui-satisfait-une-condition)
    -   [`findIndex()` - premier index qui satisfait une condition](#findindex---premier-index-qui-satisfait-une-condition)
    -   [`indexOf()` et `lastIndexOf()` - premier/dernier élément qui correspond](#indexof-et-lastindexof---premierdernier-élément-qui-correspond)
    -   [`push()`, `pop()`, `shift()` et `unshift()` - ajouter/supprime au début/fin dans un tableau](#push-pop-shift-et-unshift---ajoutersupprime-au-débutfin-dans-un-tableau)
    -   [`slice()` - ne conserver que certaines lignes d'un tableau](#slice---ne-conserver-que-certaines-lignes-dun-tableau)
    -   [`splice()` - supprimer/insérer/remplacer des valeurs dans un tableau](#splice---supprimerinsérerremplacer-des-valeurs-dans-un-tableau)
    -   [`concat()` - joindre deux tableaux](#concat---joindre-deux-tableaux)
    -   [`join()` - joindre des chaînes de caractères](#join---joindre-des-chaînes-de-caractères)
    -   [`keys()` et `values()` - les clés/valeurs d'un objet](#keys-et-values---les-clésvaleurs-dun-objet)
    -   [`includes()` - vérifier si une valeur est présente dans un tableau](#includes---vérifier-si-une-valeur-est-présente-dans-un-tableau)
    -   [`every()` et `some()` - vérifier si plusieurs valeurs sont toutes/quelques présentes dans un tableau](#every-et-some---vérifier-si-plusieurs-valeurs-sont-toutesquelques-présentes-dans-un-tableau)
    -   [`fill()` - remplir un tableau avec des valeurs](#fill---remplir-un-tableau-avec-des-valeurs)
    -   [`flat()` - aplatir un tableau](#flat---aplatir-un-tableau)
    -   [`sort()` - pour trier un tableau](#sort---pour-trier-un-tableau)
    -   [`map()` - tableau avec les résultats d'une fonction](#map---tableau-avec-les-résultats-dune-fonction)
    -   [`filter()` - tableau avec les éléments passant un test](#filter---tableau-avec-les-éléments-passant-un-test)
    -   [`groupBy()` - regroupe les éléments d'un tableau selon un règle](#groupby---regroupe-les-éléments-dun-tableau-selon-un-règle)
    -   [`flatMap()` - chaînage de map() et flat()](#flatmap---chaînage-de-map-et-flat)
    -   [`reduce()` et `reduceRight()` - réduire un tableau à une seule valeur](#reduce-et-reduceright---réduire-un-tableau-à-une-seule-valeur)
    -   [`reverse()` - inverser l'ordre du tableau](#reverse---inverser-lordre-du-tableau)
-   [Techniques](#techniques)
    -   [\`\`(backticks) - pour des expressions intelligentes](#backticks---pour-des-expressions-intelligentes)
    -   [`new Set()` - pour supprimer les doublons](#new-set---pour-supprimer-les-doublons)
-   [Fonctions](#fonctions)
    -   [Déclaration de fonction](#déclaration-de-fonction)
    -   [Fonctions immédiatement invoquées (IIFE)](#fonctions-immédiatement-invoquées-iife)
-   [Conclusion](#conclusion)

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Introduction

> Votre introduction avec notamment les objectifs opérationnels du module.

### Contenu du module

#### Introduction à la programmation fonctionnelle

-   Paradigmes de programmation
-   Fonctions fléchées
-   Définition et utilité de la programmation fonctionnelle

#### Fonctions fondamentales

-   `map()`
-   `filter()`
-   `reduce()`

#### Concepts de programmation fonctionnelle

-   **First-class citizen**
-   **Fonctions lambda**
-   **Immuabilité**
-   **Fonctions pures**
-   **Composition de fonctions :**
    -   Fonctions unaires
    -   Currying
    -   Closure
    -   Fonction _pipe_
-   **Récursion**
-   **Builder pattern**
-   **Refactorisation**

# Opérateurs javascript super-cooool 😎

## opérateur `?:`

> L'expression `question?valeur1:valeur2` retournera `valeur1` si `question` vaut `true` sinon elle retournera `valeur2`.

```javascript
const age = 15;
const resultat = age >= 18 ? 'majeur' : 'mineur'; // 'mineur'
```

## opérateur `??`

Cet opérateur logique se nomme l'opérateur de "coalescence des nuls".

> Renvoie son opérande de droite lorsque son opérande de gauche vaut `null` ou `undefined` et qui renvoie son opérande de gauche sinon.

```javascript
const foo1 = null ?? 'default'; // "default"
const foo2 = 0 ?? 42; // 0
```

> [!CAUTION]
> Contrairement à l'opérateur logique OU (`||`), l'opérande de gauche sera également renvoyé s'il s'agit d'une valeur équivalente à `false` et pas seulement `null` et `undefined`.
>
> ⚠️ En d'autres termes **ATTENTION** ‼️ lors de l'utilisation de `||` pour fournir une valeur par défaut à une variable, car on peut rencontrer des comportements inattendus lorsqu'on considère certaines valeurs comme correctes et utilisables (par exemple une chaine vide `''` ou `0`) ‼️

```javascript
const foo3 = 0 || 42; // 42 => ATTENTION !
const foo4 = 1 || 42; // 1
const foo5 = null || 'salut !'; // 'salut !'
const foo6 = '' || 'salut !'; // 'salut !' => ATTENTION !
```

## opérateur `??=`

Cet opérateur logique se nomme l'opérateur d'affectation de "coalescence des nuls", également connu sous le nom d'opérateur affectation logique nulle.

> Évalue l'opérande de droite et l'attribue à gauche **UNIQUEMENT si l'opérande de gauche est nulle** (`null` ou `undefined`).

```javascript
const a = { duration: 50 };
a.duration ??= 10; // pas fait
a.speed ??= 25; // fait => { duration: 50, speed: 25 }
```

## opérateur de décomposition 'spread' `...`

L'opérateur de décomposition spread `...` permet de décomposer un itérable (comme un tableau) en en ses éléments distincts. Cela permet de rapidement copier tout ou une partie d'un tableau existant dans un autre tableau ou d'en extraire facilement des parties.

```javascript
// Combiner des valeurs existantes dans un nouveau tableau
const numbersOne = [1, 2, 3];
const numbersTwo = [4, 5, 6];
const numbersCombined = [...numbersOne, ...numbersTwo];

// Extraire uniquement ce qui est utile d'un tableau
const numbers = [1, 2, 3, 4, 5, 6];
const [one, two, ...rest] = numbers;

// Mariage d'objets avec mise à jour :-)
const myVehicle = {
    brand: 'Ford',
    model: 'Mustang',
    color: 'red',
};
const updateMyVehicle = {
    type: 'car',
    year: 2021,
    color: 'yellow',
};
const myUpdatedVehicle = { ...myVehicle, ...updateMyVehicle };
```

## Déstructuration

L'opérateur de décomposition spread `...` sert aussi à isoler certains éléments afin de les utiliser ensuite, et de **mettre le reste** d'un coup ailleurs.

```javascript
const valeurs = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
const [a, b, ...c] = valeurs;
console.log(a); // 1
console.log(b); // 2
console.log(c); // [3, 4, 5, 6, 7, 8, 9, 10]
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Date et Heure

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Date](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Date)

## Obtenir la date et/ou heure actuelle

```javascript
const maintenant = new Date(); // Obtenir l'un comme l'autre

console.log(maintenant.toLocaleDateString()); // ex: "06.06.2025"
console.log(maintenant.toLocaleTimeString()); // ex: "15:23:42"

const jour = maintenant.getDate();
const mois = maintenant.getMonth() + 1; // Attention : janvier = 0
const annee = maintenant.getFullYear();
const heure = maintenant.getHours();
const minute = maintenant.getMinutes();
const seconde = maintenant.getSeconds();
console.log(`${jour}/${mois}/${annee} - ${heure}h${minute}`);

// Au format ISO (standard international)
console.log(maintenant.toISOString()); // ex: "2025-06-06T13:23:42.123Z"
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Math

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Math](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Math)

## `Math.PI` - la constante π

Description

Math.PI fournit la valeur numérique de π (approximativement 3.14159). Utile pour tout calcul géométrique impliquant des cercles (périmètre, surface, volumes de révolution).

Exemple : calculer la circonférence et l'aire d'un cercle.

```javascript
const r = 3; // rayon
const circonference = 2 * Math.PI * r; // P = 2πr
const aire = Math.PI * Math.pow(r, 2); // A = πr²
console.log({ circonference, aire });
```

## `Math.abs()` - la \|valeur absolue\| d'un nombre

Description

Renvoie la valeur absolue (distance à zéro) d'un nombre. Pratique pour normaliser des différences, calculer des écarts ou éviter des signes indésirables.

```javascript
Math.abs(-5); // 5
Math.abs(3 - 10); // 7
```

## `Math.pow()` - élever à une puissance

Description

Élève un nombre à la puissance donnée. Depuis ES2016 on peut aussi utiliser l'opérateur ** (ex: x ** y).

```javascript
Math.pow(2, 3); // 8
2 ** 3; // 8
```

## `Math.min()` - plus petite valeur

Description

Retourne la plus petite valeur parmi les arguments fournis. Utile pour bornes, validations et comparaisons rapides.

```javascript
Math.min(3, 7, -1, 0); // -1
Math.min(...[10, 2, 8]); // 2
```

## `Math.max()` - plus grande valeur

Description

Retourne la plus grande valeur parmi les arguments fournis.

```javascript
Math.max(3, 7, -1, 0); // 7
Math.max(...[10, 2, 8]); // 10
```

## `Math.ceil()` - arrondir à la prochaine valeur entière la plus proche

Description

Renvoie le plus petit entier supérieur ou égal au nombre — arrondi « vers le haut ».

```javascript
Math.ceil(3.14); // 4
Math.ceil(-1.2); // -1
```

## `Math.floor()` - arrondir à la précédente valeur entière la plus proche

Description

Renvoie le plus grand entier inférieur ou égal au nombre — arrondi « vers le bas ».

```javascript
Math.floor(3.9); // 3
Math.floor(-1.2); // -2
```

## `Math.round()` - arrondir à la valeur entière la plus proche

Description

Arrondit au nombre entier le plus proche. Les valeurs .5 sont arrondies vers l'entier pair suivant l'implémentation JS courante (arrondit vers +∞ pour .5 dans la plupart des moteurs).

```javascript
Math.round(3.2); // 3
Math.round(3.5); // 4
```

## `Math.trunc()` - supprime la virgule et retourne la partie entière d'un nombre

Description

Renvoie la partie entière en supprimant la fraction (troncature). Contrairement à floor, trunc ne dépend pas du signe.

```javascript
Math.trunc(3.9); // 3
Math.trunc(-1.9); // -1
```

## `Math.sqrt()` - la raçine carrée d'un nombre

Description

Renvoie la racine carrée d'un nombre. Utile pour calculs géométriques, distances, normalisations.

```javascript
Math.sqrt(9); // 3
Math.sqrt(2); // ~1.4142
```

## `Math.random()` - générer un nombre aléatoire entre 0.0 (compris) et 1.0 (non compris)

Description

Retourne un flottant pseudo-aléatoire dans [0, 1]. Pour obtenir un entier dans un intervalle, combiner avec Math.floor/ceil.

```javascript
// entier aléatoire entre min (inclus) et max (inclus)
function randint(min, max) {
    return Math.floor(Math.random() * (max - min + 1)) + min;
}

randint(1, 6); // 1..6
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# JSON

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/JSON](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/JSON)

## `JSON.stringify()` - transformer un objet Javascript en JSON

Description

Transforme un objet JS en une chaîne JSON. Pratique pour stocker ou envoyer des données sur le réseau (API, stockage local).

```javascript
const obj = { nom: 'Cyril', age: 20, lang: ['JS', 'Python'] };
const json = JSON.stringify(obj);
console.log(json); // '{"nom":"Cyril","age":21,"lang":["JS","Python"]}'
```

## `JSON.parse()` - transformer du JSON en objet Javascript

Description

Transforme une chaîne JSON en objet Javascript. Attention aux données non fiables : valider ou utiliser un parseur sécurisé si nécessaire.

```javascript
const json = '{"nom":"Cyril","age":21}';
const obj = JSON.parse(json);
console.log(obj.nom); // 'Cyril'
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Chaînes de caractères

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/String](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/String)

## `split()` - un ciseau qui coupe une chaîne là où un caractère apparaît et produit un tableau

Description

Découpe une chaîne en un tableau selon un séparateur (caractère, expression régulière). Très utile pour parser des CSV simples ou des entrées utilisateurs.

```javascript
'a,b,c'.split(','); // ['a','b','c']
'2025-10-28'.split('-'); // ['2025','10','28']
```

## `trim()`, `trimStart()` et `trimEnd()` - épuration des espaces en trop dans une chaîne (trimming)

Description

Suppriment les espaces superflus en début/fin de chaîne. Indispensable pour normaliser des saisies utilisateur.

```javascript
'  hello  '.trim(); // 'hello'
'  hello  '.trimStart(); // 'hello  '
'  hello  '.trimEnd(); // '  hello'
```

## `padStart()` et `padEnd()` - aligner le contenu dans une chaîne de caractères

Description

Ajoutent des caractères au début ou à la fin pour atteindre une longueur donnée (utile pour formatage, tableaux, affichage en console).

```javascript
'5'.padStart(3, '0'); // '005'
'42'.padEnd(4, ' ').replace(/ /g, '\u00B7'); // '42··'
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Console

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/API/console](https://developer.mozilla.org/fr/docs/Web/API/console)

## `console.log()` - Afficher un message sur la console

```javascript
console.log('Coucou !'); // Coucou !
```

## `console.info()`, `warn()` et `error()` - Afficher un message sur la console (filtrables)

Description

Ces variantes de console permettent de catégoriser les messages (info, warning, error). En dev on s'en sert pour signaler états, avertissements et erreurs sans polluer la sortie principale.

```javascript
console.info('Chargement OK');
console.warn('Temps de réponse élevé');
console.error("Impossible de se connecter à l'API");
```

## `console.table()` - Afficher tout un tableau ou un objet sur la console

Description

Affiche un tableau structuré en colonnes — très pratique pour inspecter des tableaux d'objets en dev.

```javascript
console.table([
    { nom: 'Alice', age: 23 },
    { nom: 'Bob', age: 25 },
]);
```

## `console.time()`, `timeLog()` et `timeEnd()` - Chronométrer une durée d'exécution

Description

Permettent de mesurer des durées côté client/serveur pour repérer des goulets d'étranglement.

```javascript
console.time('boucle');
for (let i = 0; i < 1e6; i++); // travail
console.timeEnd('boucle'); // 'boucle: XXms'
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Tableaux

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Array](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Array)

## `forEach` - parcourir les éléments d'un tableau

Description

Parcourt chaque élément du tableau et exécute une fonction. Ne renvoie rien (utiliser map/filter/reduce si on veut transformer/reduire).

```javascript
[1, 2, 3].forEach((x) => console.log(x));
```

## `entries()` - parcourir les couples index/valeurs d'un tableau

Description

Renvoie un itérateur de paires [index, valeur], utile avec for..of pour parcourir les indices et valeurs.

```javascript
for (const [i, v] of ['a', 'b', 'c'].entries()) {
    console.log(i, v);
}
```

## `in` - parcourir les clés d'un tableau

Description

L'opérateur `in` teste si une clé existe dans un objet/array. Pour parcourir les indices d'un tableau on peut l'utiliser dans une boucle for.

```javascript
console.log(2 in ['a', 'b', 'c']); // true
for (const i in ['a', 'b', 'c']) console.log(i); // '0','1','2'
```

## `of` - parcourir les valeurs d'un tableau

Description

`for..of` itère sur les valeurs d'un itérable (tableaux, strings, maps...). Pratique et lisible.

```javascript
for (const v of ['a', 'b', 'c']) console.log(v);
```

## `find()` - premier élément qui satisfait une condition

Description

Retourne le premier élément qui satisfait la fonction de test ou undefined.

```javascript
[{ id: 1 }, { id: 2 }].find((x) => x.id === 2); // {id:2}
```

## `findIndex()` - premier index qui satisfait une condition

Description

Retourne l'index du premier élément qui passe la condition, ou -1 si aucun.

```javascript
[10, 20, 30].findIndex((x) => x > 15); // 1
```

## `indexOf()` et `lastIndexOf()` - premier/dernier élément qui correspond

Description

indexOf renvoie le premier index correspondant; lastIndexOf le dernier. Pour arrays d'objets, utiliser findIndex.

```javascript
[1, 2, 3, 2].indexOf(2); // 1
[1, 2, 3, 2].lastIndexOf(2); // 3
```

## `push()`, `pop()`, `shift()` et `unshift()` - ajouter/supprime au début/fin dans un tableau

Description

push ajoute à la fin, pop retire à la fin; unshift ajoute au début, shift retire au début. Mutent le tableau.

```javascript
const t = [1, 2];
t.push(3); // [1,2,3]
t.pop(); // 3, t => [1,2]
t.unshift(0); // [0,1,2]
t.shift(); // 0, t => [1,2]
```

## `slice()` - ne conserver que certaines lignes d'un tableau

Description

slice renvoie une copie superficielle d'une portion du tableau — non destructive.

```javascript
[1, 2, 3, 4].slice(1, 3); // [2,3]
```

## `splice()` - supprimer/insérer/remplacer des valeurs dans un tableau

Description

splice modifie le tableau en place: suppression, insertion ou remplacement selon les arguments.

```javascript
const a = [1, 2, 3, 4];
a.splice(1, 2, 9, 9); // supprime 2 éléments à l'index 1, insère 9,9 => a = [1,9,9,4]
```

## `concat()` - joindre deux tableaux

Description

Retourne un nouveau tableau résultat de la concaténation (non destructif).

```javascript
[1, 2].concat([3, 4]); // [1,2,3,4]
[...a, ...b]; // équivalent moderne
```

## `join()` - joindre des chaînes de caractères

Description

Rejoint les éléments d'un tableau en une seule chaîne séparée par le séparateur fourni.

```javascript
['a', 'b', 'c'].join('-'); // 'a-b-c'
```

## `keys()` et `values()` - les clés/valeurs d'un objet

Description

Sur un tableau, keys() renvoie un itérateur d'indices, values() d'éléments. Sur Map, ces méthodes sont aussi utiles pour itérer.

```javascript
for (const k of ['a', 'b'].keys()) console.log(k); // 0,1
for (const v of ['a', 'b'].values()) console.log(v); // 'a','b'
```

## `includes()` - vérifier si une valeur est présente dans un tableau

Description

Retourne true si la valeur est présente, false sinon. Pour objets, comparer par référence.

```javascript
[1, 2, 3].includes(2); // true
```

## `every()` et `some()` - vérifier si plusieurs valeurs sont toutes/quelques présentes dans un tableau

Description

every renvoie true si tous les éléments satisfont le test; some renvoie true si au moins un satisfait.

```javascript
[2, 4, 6].every((x) => x % 2 === 0); // true
[1, 2, 3].some((x) => x > 2); // true
```

## `fill()` - remplir un tableau avec des valeurs

Description

Remplit un tableau existant avec la valeur fournie (mutation). Utile pour initialiser des buffers ou tests.

```javascript
new Array(3).fill(0); // [0,0,0]
```

## `flat()` - aplatir un tableau

Description

Applatis les tableaux imbriqués jusqu'à une profondeur donnée (par défaut 1).

```javascript
[1, [2, 3], [4, [5]]].flat(); // [1,2,3,4,[5]]
[1, [2, [3]]].flat(2); // [1,2,3]
```

## `sort()` - pour trier un tableau

Description

Trie un tableau en place. Par défaut trie les éléments comme des strings; pour nombres fournir une fonction de comparaison.

```javascript
[3, 1, 2].sort((a, b) => a - b); // [1,2,3]
['b', 'a'].sort(); // ['a','b']
```

## `map()` - tableau avec les résultats d'une fonction

Description

Crée un nouveau tableau contenant le résultat de l'appel d'une fonction sur chaque élément. Pur et non mutatif.

```javascript
[1, 2, 3].map((x) => x * 2); // [2,4,6]
```

## `filter()` - tableau avec les éléments passant un test

Description

Renvoie un nouveau tableau avec les éléments qui satisfont la condition donnée.

```javascript
[1, 2, 3, 4].filter((x) => x % 2 === 0); // [2,4]
```

## `groupBy()` - regroupe les éléments d'un tableau selon un règle

Description

Cette méthode (selon l'environnement) regroupe les éléments selon une clé. En pratique on utilise reduce pour compatibilité.

```javascript
const animaux = [
  { type: "mammifère", nom: "chien" },
  { type: "oiseau", nom: "moineau" },
  { type: "mammifère", nom: "chat" },
  { type: "poisson", nom: "saumon" },
];

// On regroupe les animaux par type
const groupes = Object.groupBy(animaux, (a) => a.type);

console.log(groupes);
//Résultat
{
  mammifère: [
    { type: "mammifère", nom: "chien" },
    { type: "mammifère", nom: "chat" }
  ],
  oiseau: [
    { type: "oiseau", nom: "moineau" }
  ],
  poisson: [
    { type: "poisson", nom: "saumon" }
  ]
}

```

## `flatMap()` - chaînage de map() et flat()

Description

Applique une fonction à chaque élément et aplatit le résultat d'un niveau. Pratique pour transformer et aplatir en un seul passage.

```javascript
[1, 2].flatMap((x) => [x, x * 2]); // [1,2,2,4]
```

## `reduce()` et `reduceRight()` - réduire un tableau à une seule valeur

Description

Réduit un tableau à une seule valeur en appliquant une fonction accumulateur. Très puissant : sommes, groupements, transformations complexes.
Exemple 1 :

```javascript
[1, 2, 3].reduce((acc, x) => acc + x, 0); // 6
```

Exemple 2 :

```javascript
const produits = [
    { categorie: 'fruit', nom: 'pomme' },
    { categorie: 'légume', nom: 'carotte' },
    { categorie: 'fruit', nom: 'banane' },
];

const groupés = produits.reduce((acc, p) => {
    // Si la catégorie n'existe pas encore, on la crée
    if (!acc[p.categorie]) {
        acc[p.categorie] = [];
    }
    // On ajoute le produit dans la bonne catégorie
    acc[p.categorie].push(p.nom);
    return acc;
}, {});

console.log(groupés);
// → { fruit: ["pomme", "banane"], légume: ["carotte"] }
```

## `reverse()` - inverser l'ordre du tableau

Description

Inverse le tableau en place. Attention : mutation.

```javascript
const a = [1, 2, 3];
a.reverse(); // a => [3,2,1]
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Techniques

## ``(backticks) - pour des expressions intelligentes

Description

Les backticks (template literals) permettent d\'insérer des expressions et d\'écrire des strings multi-lignes facilement. Très pratiques pour construire des messages ou des templates.

```javascript
const nom = 'Cyril';
const msg = `Bonjour ${nom}, aujourd\'hui nous sommes ${new Date().toLocaleDateString()}`;
```

## `new Set()` - pour supprimer les doublons

Description

Set est une structure qui stocke des valeurs uniques. Utile pour dédupliquer rapidement un tableau.

```javascript
const arr = [1, 2, 2, 3];
const dedup = [...new Set(arr)]; // [1,2,3]
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Fonctions

## Déclaration de fonction

**Standard**

```javascript
function doStuff(a, b, c) {
    return a + b + c;
}
```

**Sous forme d'expression de fonction**

```javascript
const doStuff = function (a, b, c) {
    return a + b + c;
};
```

**Sous forme d'expression de fonction anonyme**

```javascript
const doStuff = (a, b, c) => {
    return a + b + c;
};
```

**Sous forme raccourcie**

S'il n'y a qu'un seul argument et que son corps n'a qu'une seule expression, on peut omettre le return et le corps de la fonction :

```javascript
const doStuff = (a) => `Salut ${a} !`;
```

## Fonctions immédiatement invoquées (IIFE)

IIFE = Immediately Invoked Function Expressions.

Ces fonctions sont définies et **exécutées immédiatement**. Elles sont souvent utilisées pour créer un **contexte isolé** ou encapsuler du code sans polluer l’espace global.

```javascript
(function(){ ... })()
```

ou

```javascript
(() => { ... })()
```

# Exemple de code fonctionnel et commenté

```js
// ===========================================================================
// Gestion des événements et affichage des résultats
// ===========================================================================

// Quand la page est complètement chargée, on ajoute les événements sur les boutons
window.addEventListener('load', (event) => {
    // Chaque bouton déclenche une action correspondant à un rapport spécifique
    document.querySelector('#idActionA1').addEventListener('click', actionA1);
    document.querySelector('#idActionA2').addEventListener('click', actionA2);
    document.querySelector('#idActionA3').addEventListener('click', actionA3);
    document.querySelector('#idActionA4').addEventListener('click', actionA4);
    document.querySelector('#idActionA5').addEventListener('click', actionA5);
    document.querySelector('#idActionA6').addEventListener('click', actionA6);
    document.querySelector('#idActionA7').addEventListener('click', actionA7);
    document.querySelector('#idActionA8').addEventListener('click', actionA8);
    document.querySelector('#idActionA9').addEventListener('click', actionA9);
    document.querySelector('#idActionA10').addEventListener('click', actionA10);
    document.querySelector('#idActionA11').addEventListener('click', actionA11);
    document.querySelector('#idActionA12').addEventListener('click', actionA12);
});

// ---------------------------------------------------------------------------
// Fonction d'affichage dans la page
// ---------------------------------------------------------------------------
function afficherObjet(resultat) {
    // Récupère le conteneur HTML avec l'id "output"
    const container = document.getElementById('output');
    // Affiche l'objet passé en argument sous forme JSON avec indentation
    container.innerHTML = JSON.stringify(resultat, null, 3);
}

// ===========================================================================
// RAPPORTS
// ===========================================================================

// ---------------------------------------------------------------------------
// A1 : Somme des km parcourus pour les véhicules de type "Moyenne"
// ---------------------------------------------------------------------------
function actionA1() {
    // Filtre les locations pour ne garder que les véhicules de type "Moyenne"
    const vMyenne = jsonData.locations.filter(location => location.vehicule.vehicule_type === "Moyenne");

    // Additionne tous les km parcourus pour ces véhicules
    const resultat = vMyenne.reduce((acc, location) => {
        acc += location.location.location_km;
        return acc;
    }, 0);

    // Affiche le résultat
    afficherObjet(resultat);
}

// ---------------------------------------------------------------------------
// A2 : Les types de véhicules de Mobilus, sans doublons et triés par nom
// ---------------------------------------------------------------------------
function actionA2() {
    // On récupère tous les types de véhicules
    const vType = [...new Set(
        jsonData.locations.map(location => location.vehicule.vehicule_type)
    )].sort(); // Supprime les doublons et trie par ordre alphabétique

    afficherObjet(vType);
}

// ---------------------------------------------------------------------------
// A3 : Les véhicules de Mobilus regroupés par type et triés
// ---------------------------------------------------------------------------
function actionA3() {
    // Reduce permet de créer un objet où chaque clé est un type de véhicule
    const resultat = jsonData.locations.reduce((acc, location) => {
        const veh = location.vehicule;
        // Si le type n'existe pas encore, on crée un tableau vide
        if (!acc[veh.vehicule_type]) {
            acc[veh.vehicule_type] = [];
        }

        // Crée une description unique du véhicule
        const description = `${veh.vehicule_nom} [${veh.vehicule_id}], à ${veh.vehicule_prix_par_jour} Frs/jour et ${veh.vehicule_prix_par_km} Frs/km`;

        // Ajoute le véhicule si il n'est pas déjà présent
        if (!acc[veh.vehicule_type].includes(description)) {
            acc[veh.vehicule_type].push(description);
        }

        return acc;
    }, {});

    // Tri les véhicules de chaque type par ordre alphabétique
    Object.keys(resultat).forEach(key => {
        resultat[key].sort();
    });

    afficherObjet(resultat);
}

// ---------------------------------------------------------------------------
// A4 : Liste des clients du plus jeune au plus ancien, puis par nom_prenom
// ---------------------------------------------------------------------------
function actionA4() {
    // On crée un tableau de clients avec leur nom complet et date de naissance
    const client = jsonData.locations.flatMap(location => {
        const fullName = location.client.client_nom.toUpperCase() + " " + location.client.client_prenom;
        return {
            nom_prenom: fullName,
            date_naissance: location.client.client_date_naissance
        }
    })
    // Trie les clients par date de naissance (du plus jeune au plus ancien)
    .sort((a, b) => {
        const dateA = new Date(a.date_naissance.split('.').reverse().join('-'));
        const dateB = new Date(b.date_naissance.split('.').reverse().join('-'));
        if (dateA < dateB) return -1;
        if (dateA > dateB) return 1;
        if (dateA === dateB) return a.nom_prenom.localeCompare(b.nom_prenom);
    });

    // Supprime les doublons
    const uniqueClients = client.filter((client, index, self) =>
        index === self.findIndex((c) => (
            c.nom_prenom === client.nom_prenom && c.date_naissance === client.date_naissance
        ))
    );

    afficherObjet(uniqueClients);
}

// ---------------------------------------------------------------------------
// A5 : Résultat global sur la période (CA total, jours, km, nbre locations)
// ---------------------------------------------------------------------------
function actionA5() {
    // Reduce pour calculer cumulativement CA, nombre de locations, jours et km
    const resultat = jsonData.locations.reduce((acc, location) => {
        const loc = location.location;
        const veh = location.vehicule;

        return {
            ca : acc.ca + (loc.location_jours * veh.vehicule_prix_par_jour) + (loc.location_km * veh.vehicule_prix_par_km),
            location : acc.location + 1,
            jour : acc.jour + loc.location_jours,
            km : acc.km + loc.location_km
        };
    }, {
        ca: 0,
        location: 0,
        jour: 0,
        km: 0
    });

    afficherObjet(resultat);
}

// ---------------------------------------------------------------------------
// A6 : Résultat des véhicules sur la période, triés par CA
// ---------------------------------------------------------------------------
function actionA6() {
    // On groupe les locations par véhicule avec un objet accumulatif
    const acc = jsonData.locations.reduce((acc, location) => {
        const loc = location.location;
        const veh = location.vehicule;

        // Si véhicule non présent dans l'objet, on l'initialise
        if (!acc[veh.vehicule_id]) {
            acc[veh.vehicule_id] = {
                vehicule_id: veh.vehicule_id,
                vehicule_type: veh.vehicule_type,
                vehicule_nom: veh.vehicule_nom,
                vehicule_prix_par_jour: veh.vehicule_prix_par_jour,
                vehicule_prix_par_km: veh.vehicule_prix_par_km,
                ca: 0,
                locations: 0,
                jours: 0,
                km: 0
            };
        }

        // Ajouter les valeurs de la location au véhicule
        acc[veh.vehicule_id].ca += (loc.location_jours * veh.vehicule_prix_par_jour) + (loc.location_km * veh.vehicule_prix_par_km);
        acc[veh.vehicule_id].locations += 1;
        acc[veh.vehicule_id].jours += loc.location_jours;
        acc[veh.vehicule_id].km += loc.location_km;

        return acc;
    }, {});

    // Transformer l'objet en tableau et trier par CA décroissant
    const resultat = Object.values(acc).sort((a, b) => b.ca - a.ca);

    afficherObjet(resultat);
}

// ---------------------------------------------------------------------------
// A7 : Locations d'un client spécifique >12 jours, triées par date
// ---------------------------------------------------------------------------
function actionA7() {
    const idClient = "IDC-32CE80"; // ID du client à filtrer
    const maxDay = 12;             // Durée minimale des locations

    const resultat = jsonData.locations
        // Filtre les locations du client spécifique
        .filter(location => location.client.client_id === idClient)
        // Transforme en objet simplifié
        .map(location => ({
            date: location.location.location_date,
            jours: location.location.location_jours,
            km: location.location.location_km,
            vehicule_id: location.vehicule.vehicule_id,
            vehicule_nom: location.vehicule.vehicule_nom
        }))
        // Filtre les locations supérieures à maxDay
        .filter(location => location.jours > maxDay)
        // Trie par date croissante
        .sort((a, b) => {
            const dateA = new Date(a.date.split('.').reverse().join('-'));
            const dateB = new Date(b.date.split('.').reverse().join('-'));
            return dateA - dateB;
        });

    afficherObjet(resultat);
}

// ---------------------------------------------------------------------------
// A8 : Liste des incidents, triés par date
// ---------------------------------------------------------------------------
function actionA8() {
    const resultat = jsonData.locations
        .map(location => ({
            date: location.location.location_date,
            incident: location.location.incident_details,
            vehicule: `${location.vehicule.vehicule_nom} [${location.vehicule.vehicule_id}]`,
            client: location.client.client_nom.toUpperCase() + " " + location.client.client_prenom
        }))
        // Garde uniquement les locations avec incidents
        .filter(location => location.incident !== null)
        // Trie par date croissante
        .sort((a, b) => {
            const dateA = new Date(a.date.split('.').reverse().join('-'));
            const dateB = new Date(b.date.split('.').reverse().join('-'));
            return dateA - dateB;
        });

    afficherObjet(resultat);
}

// ---------------------------------------------------------------------------
// A9 : TOP 5 des meilleurs clients
// ---------------------------------------------------------------------------
function actionA9() {
    const top = 5; // Nombre de clients à retourner

    // On regroupe les locations par client et calcule leurs statistiques
    const resultat = jsonData.locations.reduce((acc, location) => {
        const client = location.client;
        const nomPrenom = client.client_nom.toUpperCase() + " " + client.client_prenom;

        if (!acc[nomPrenom]) {
            acc[nomPrenom] = {
                nom_prenom: nomPrenom,
                date_naissance: client.client_date_naissance,
                age_str: client.client_age_str,
                locations_nbre: 0,
                locations_jours: 0,
                locations_km: 0,
                locations_ca: 0
            };
        }

        acc[nomPrenom].locations_nbre += 1;
        acc[nomPrenom].locations_jours += location.location.location_jours;
        acc[nomPrenom].locations_km += location.location.location_km;
        acc[nomPrenom].locations_ca += (location.location.location_jours * location.vehicule.vehicule_prix_par_jour)
                                      + (location.location.location_km * location.vehicule.vehicule_prix_par_km);

        return acc;
    }, {});

    // Transforme en tableau, trie par CA décroissant et garde le top 5
    const resultatArray = Object.values(resultat)
        .sort((a, b) => b.locations_ca - a.locations_ca)
        .slice(0, top);

    afficherObjet(resultatArray);
}

// ---------------------------------------------------------------------------
// A10 : Âge moyen des conducteurs des véhicules accidentés
// ---------------------------------------------------------------------------
function actionA10() {
    const resultat = jsonData.locations.reduce((acc, location) => {
        const veh = location.vehicule;
        const cli = location.client;

        // Initialisation du véhicule si nécessaire
        if (!acc[veh.vehicule_nom]) {
            acc[veh.vehicule_nom] = {
                vehicule_nom: veh.vehicule_nom,
                vehicule_id: veh.vehicule_id,
                total_age: 0,
                total_clients: 0
            };
        }

        // Ajouter l'âge du client si incident présent
        if (location.location.has_incident) {
            acc[veh.vehicule_nom].total_age += cli.client_age_ans;
            acc[veh.vehicule_nom].total_clients += 1;
        }

        return acc;
    }, {});

    // Calcul de la moyenne et tri décroissant
    const resultatFinal = Object.values(resultat).map(veh => ({
        vehicule: `${veh.vehicule_nom} [${veh.vehicule_id}]`,
        moyenne_age: veh.total_clients > 0 ? veh.total_age / veh.total_clients : 0
    }))
    .filter(veh => veh.moyenne_age > 0)
    .sort((a, b) => b.moyenne_age - a.moyenne_age);

    afficherObjet(resultatFinal);
}

// ---------------------------------------------------------------------------
// A11 : CA réalisé mois par mois
// ---------------------------------------------------------------------------
function actionA11() {
    const resultat = jsonData.locations.reduce((acc, location) => {
        const loc = location.location;
        const veh = location.vehicule;

        // Convertit le mois en index (0 = janvier)
        const mois = parseInt(loc.location_date.split(".")[1], 10) - 1;

        // Ajoute le CA de la location au mois correspondant
        acc[mois] += loc.location_jours * veh.vehicule_prix_par_jour + loc.location_km * veh.vehicule_prix_par_km;
        return acc;
    }, Array(12).fill(0)) // Initialise un tableau de 12 mois
      .map(x => x.toFixed(2)); // Arrondit chaque valeur à 2 décimales

    afficherObjet(resultat);
}

// ---------------------------------------------------------------------------
// A12 : Statistiques km pour "Kia Picanto" type "Petite citadine"
// ---------------------------------------------------------------------------
function actionA12() {
    const name = "Kia Picanto";
    const typeV = "Petite citadine";

    // Filtre les locations pour ce type et nom de véhicule
    const locationsFiltrees = jsonData.locations.filter(location => location.vehicule.vehicule_nom === name && location.vehicule.vehicule_type === typeV);

    // Groupe les km par ID de véhicule
    const groupe = locationsFiltrees.reduce((acc, location) => {
        const id = location.vehicule.vehicule_id;
        if (!acc[id]) acc[id] = [];
        acc[id].push(location.location.location_km);
        return acc;
    }, {});

    // Calcul min, max et moyenne
    const resultat = Object.keys(groupe).map(id => {
        const km_min = Math.min(...groupe[id]);
        const km_max = Math.max(...groupe[id]);
        const km_avg = groupe[id].reduce((sum, km) => sum + km, 0) / groupe[id].length;
        return {
            vehicule_id: id,
            km_min: km_min,
            km_max: km_max,
            km_moy: parseFloat(km_avg.toFixed(2))
        };
    });

    afficherObjet(resultat);
}

```


# Conclusion

Ce module 323 m’a vraiment appris une nouvelle façon de penser le code : la programmation fonctionnelle. Au début, ce n’était pas facile de changer mes habitudes, car j’avais tendance à coder de manière plus « classique », avec des boucles et des conditions. Mais petit à petit, en pratiquant, j’ai commencé à comprendre l’intérêt d’utiliser des fonctions comme map(), filter() ou reduce().

Ces outils m’ont permis d’écrire du code plus simple, plus propre et souvent plus efficace. J’ai aussi compris que la programmation fonctionnelle, ce n’est pas juste une autre manière de faire la même chose, mais une façon différente de structurer sa logique pour que le code soit plus clair.

Certaines notions, comme reduce(), m’ont pris un peu plus de temps à comprendre, mais avec les exercices et les exemples du cours, ça a fini par faire sens. Maintenant, j’arrive mieux à transformer ou regrouper des données sans forcément passer par des boucles compliquées.

En résumé, ce module m’a vraiment fait progresser. Il m’a appris à réfléchir autrement, à mieux utiliser les outils de JavaScript et à écrire du code plus réfléchi. Je sais que j’ai encore des choses à améliorer, mais je sens déjà une vraie évolution dans ma façon de coder.

> Votre conclusion avec les éléments usuels
