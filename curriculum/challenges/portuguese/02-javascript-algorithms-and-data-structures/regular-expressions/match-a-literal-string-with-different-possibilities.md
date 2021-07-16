---
id: 587d7db4367417b2b2512b90
title: Busque uma String Literal com Diferentes Possibilidades
challengeType: 1
forumTopicId: 301345
dashedName: match-a-literal-string-with-different-possibilities
---

# --description--

Ao usar regexes como `/coding/`, você pode procurar pelo padrão `coding` em strings.

Isso funciona com strings únicas, mas é limitado a apenas um padrão. Você pode procurar por múltiplos padrões usando o operador de `alternação`, ou `OU`: `|`.

Este operador funciona para buscar padrões à esquerda e à direita dele. Por exemplo, se você quiser encontrar as strings `yes` ou `no`, a regex que você quer é `/yes|no/`.

Você pode também procurar por mais de dois padrões com este operador. É possível fazer isso ao adicionar mais instâncias do operador seguido do padrão desejado: `/yes|no|maybe/`.

# --instructions--

Complete a regex `petRegex` para encontrar os pets `dog`, `cat`, `bird`, ou `fish`.

# --hints--

Sua regex `petRegex` deve retornar `true` para a string `John has a pet dog.`

```js
assert(petRegex.test('John has a pet dog.'));
```

Sua regex `petRegex` deve retornar `false` para a string `Emma has a pet rock.`

```js
assert(!petRegex.test('Emma has a pet rock.'));
```

Sua regex `petRegex` deve retornar `true` para a string `Emma has a pet bird.`

```js
assert(petRegex.test('Emma has a pet bird.'));
```

Sua regex `petRegex` deve retornar `true` para a string `Liz has a pet cat.`

```js
assert(petRegex.test('Liz has a pet cat.'));
```

Sua regex `petRegex` deve retornar `false` para a string `Kara has a pet dolphin.`

```js
assert(!petRegex.test('Kara has a pet dolphin.'));
```

Sua regex `petRegex` deve retornar `true` para a string `Alice has a pet fish.`

```js
assert(petRegex.test('Alice has a pet fish.'));
```

Sua regex `petRegex` deve retornar `false` para a string `Jimmy has a pet computer.`

```js
assert(!petRegex.test('Jimmy has a pet computer.'));
```

# --seed--

## --seed-contents--

```js
let petString = "James has a pet cat.";
let petRegex = /change/; // Change this line
let result = petRegex.test(petString);
```

# --solutions--

```js
let petString = "James has a pet cat.";
let petRegex = /dog|cat|bird|fish/; // Change this line
let result = petRegex.test(petString);
```