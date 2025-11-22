## Introdução

**Tipos primitivos são os tipos de dados básicos** e mais simples em uma linguagem de programação, tipos de dados são imutáveis, ou seja, seus valores não podem ser alterados após sua criação.

## Tipos primitivos

- `string:` Representa valores de texto, como "Olá, mundo", precisam ser passado entre aspas.

- `number:` Usado para valores numéricos, incluindo inteiros e de ponto flutuante (números com virgula) no JavaScript, `number` cobre todos os tipos de números (não existe int, float).
  
- `boolean:` Um valor binário podendo ser `true` ou `false`.

- `null:` Representa um valor nulo intencional.

- `undefined:` Indica que a variável foi criada, mas ainda não recebeu nenhum valor.

- `symbol:` Um tipo de dado cujos valores são únicos e imutáveis, introduzido no ECMAScript 6, é útil quando você precisa de identificadores que nunca entrem em conflito.

```js
//string
let nome = "Harry Potter"
let frase = 'Olá, mundo!'
let template = `Texto com template literal`

//number
let idade = 25
let altura = 1.75

//boolean
let logado = true
let maiorDeIdade = false

//null
let resposta = null

//symbols
const id = Symbol('id')
```