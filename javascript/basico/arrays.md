## Introdução

**Arrays são estruturas de dados que armazenam uma coleção de elementos, geralmente do mesmo tipo**, organizados de forma sequencial e acessíveis por meio de índices numéricos, **cada elemento no array é identificado por uma posição específica**, começando do índice `0`, o que significa que o primeiro elemento está na posição `0`, o segundo na posição `1`, e assim por diante.

Em linguagens como _Java_, _C_ e _JavaScript_, os arrays podem ser:

- **Unidimensionais (vetores)** – uma lista simples de valores.
- **Bidimensionais (matrizes)** – um conjunto de listas.
- **Multidimensionais** – estruturas mais complexas com vários níveis.

A criação de um array é feita usando colchetes `[]`.

## Criando um Array

Os dados podem ser de vários tipos como: `string`, `number`, `objects` entre outros.

```js
//array de strings
let brands = ['BMW', 'Rockstar Games', 'LG', 'Samsung']
//array de numbers
let numbers = [40, 20, 10, 5, 0]
//array de objetos
let persons = [
  { name: 'Paulo', age: 25 },
  { name: 'Mia', age: 22 },
]
```

> [!NOTE]
> Uma boa pratica de array é colocar o nome de referência das variáveis no plural.

## Modificando Valores

Podemos alterar os valores dentro de um array, o jeito mais direto mas não recomendado em grandes projetos é modificar o valor diretamente pelo índice.

```js
// Cria o array de strings
let newArray = ['Zero', 'Um', 'Dois', 'Três']

/*
Substitui o valor 'Um' (posição 1) pela string 'Modificado'
*/
newArray[1] = 'Modificado'
```

> [!WARNING]
> O array precisa ser declarado com `let` para permitir modificações, se for declarado com `const`, o JavaScript impedirá a reatribuição de valores.

## Métodos de Array

Aprender a manipular arrays é algo muito importante, e o JavaScript oferece diversos métodos nativos para isso.
Você pode conferir mais sobre esses métodos [clicando aqui](./metodos-arrays.md).
