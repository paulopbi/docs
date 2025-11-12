## Introdução

Uma **função em JavaScript é um bloco de código que executa uma tarefa específica e pode ser chamado (executado) sempre que necessário**, elas são usadas para organizar o código, evitar repetições e torná-lo mais eficiente, as funções podem receber dados (argumentos) como entrada e retornar um valor de saída.

### Principais características das funções

- **Blocos de construção fundamentais**: Funções são blocos de código reutilizáveis que são a base da programação em JavaScript.

- **Reutilização**: Uma função é definida uma vez e pode ser chamada várias vezes, o que ajuda a evitar a repetição de código.

- **Entrada e saída**: Elas podem receber dados de entrada (argumentos) e, opcionalmente, retornar um valor de saída.

- **Organização**: Funções ajudam a dividir um programa em partes menores e mais gerenciáveis, tornando o código mais claro e organizado.

- **Objetos de primeira classe**: Em JavaScript, as funções são tratadas como objetos, o que significa que podem ter propriedades, métodos e ser atribuídas a variáveis.

- **Construtor Function**: Toda função é criada com o construtor `Function` e por isso herda as suas propriedades e métodos.

## Function Declaration

Uma function declaration no JavaScript é uma maneira de criar uma função usando a palavra-chave `function`, seguida por um nome de função, uma grande vantagem é que elas são elevadas (hoisted), o que significa que podem ser chamadas antes de sua definição no código.

```js
//cria a function declaration
function areaQuadrado(lado) {
  return lado * lado
}
```

## Arrow Function

A arrow function (função de seta) é um jeito mais moderno e curto de escrever uma função, podemos atribuir o retorno da função em uma variável, e para utilizar basta remover a palavra chave `function` e adicionar a fat arrow `=>` após os argumentos.

```js
const areaQuadrado = (lado) => {
  return lado * lado
}
```

## Argumentos e Parâmetros

- **Argumentos:** Ao executar uma função, você pode passar argumentos, `somar(5, 3)`, `5` e `3` são os argumentos.
- **Parâmetros:** Ao criar uma função podemos definir os parâmetros `function somar(a, b)`, `a` e `b` são parâmetros.

## Function.length

`Function.length` retorna o total de argumentos da função. Function.name retorna uma string com o nome da função.

```js
function somar(n1, n2) {
  return n1 + n2
}

somar.length // 2
somar.name // 'somar'
```

## Function.call()

`function.call(this, arg1, arg2, ...)` executa a função, sendo possível passarmos uma nova referência ao this da mesma, mas é importante lembrar que se a função for uma arrow function não irá funcionar, ela precisa ser uma function declaration.

```js
const person = {
  name: 'Paulo Victor',
  age: 26,
}

function showInformation() {
  console.log(`O nome é ${this.name} e tem ${this.age} anos.`)
}

showInformation.call(person)
```

## Function.apply()

O `apply(this, [arg1, arg2, ...])` funciona como o call, a única diferença é que os argumentos da função são passados através de uma array.

```js
const numeros = [3, 4, 6, 1, 34, 44, 32]
Math.max.apply(null, numeros)
Math.max.call(null, 3, 4, 5, 6, 7, 20)

// Podemos passar null para o valor
// de this, caso a função não utilize
// o objeto principal para funcionar
```
