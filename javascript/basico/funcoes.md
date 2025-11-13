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

Uma **function declaration** é uma forma tradicional de criar funções em JavaScript, usando a palavra-chave `function` seguida pelo nome da função.

A grande vantagem é que **elas são içadas (hoisted)**, ou seja, podem ser chamadas **antes** de serem declaradas no código.

```js
//chamando a função 'areaQuadrado' antes da sua definição
areaQuadrado(4) //retorno: 16

//cria a definição da function declaration
function areaQuadrado(lado) {
  return lado * lado
}
```

## Arrow Function

A **arrow function** (função de seta) é uma forma mais moderna e curta de escrever funções, ela é definida usando o operador `=>` e geralmente atribuída a uma variável.

```js
//a mesma função mas utilizando arrow function
const areaQuadrado = (lado) => {
  return lado * lado
}

areaQuadrado(4) //retorno: 16
```

> [!IMPORTANT]
> Diferente das _function declarations_, as _arrow functions_ não são içadas (hoisted), portanto, a chamada da função deve sempre vir abaixo da sua definição, ou ocorrerá um erro.

## Execução de uma função

Definir uma função não é o mesmo que executá-la, **nada dentro dela será executado até que ela seja chamada**, ou seja, até que tenha parênteses após o nome.

```js
const exibirNome = (nome) => {
  console.log(nome)
}

/*
A função 'exibirNome' está sendo executada porque
possui parênteses após o nome.
*/
exibirNome('Paulo')
```

## Argumentos e Parâmetros

- **Argumentos:** Ao executar uma função, você pode passar argumentos, `somar(5, 3)`, `5` e `3` são os argumentos.
- **Parâmetros:** Ao criar uma função podemos definir os parâmetros `function somar(a, b)`, `a` e `b` são parâmetros.

## Retorno de Valores

Se uma função não tiver `return`, ela retornará automaticamente `undefined`.
Mesmo assim, o código dentro dela será executado normalmente.

Quando usamos `return`, o valor pode ser armazenado em uma variável ou exibido no console.

```js
const semRetorno = () => {
  console.log('Não retorna nenhum dado')
}

semRetorno() // retorno: undefined

const comRetorno = () => {
  return 'Retorna essa string'
}

comRetorno() // retorno: 'Retorna essa string'
```

## Métodos e Atributos de Funções

Podemos ver alguns métodos e atributos disponíveis no construtor de uma função [clicando aqui](./metodos-de-funcoes.md)
