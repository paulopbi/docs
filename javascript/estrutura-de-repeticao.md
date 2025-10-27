## Introdução

**As estruturas de repetição são mecanismos utilizados na programação para executar um bloco de instruções mais de uma vez, com base em uma condição específica, elas permitem que um algoritmo repita um conjunto de ações enquanto uma condição de controle**, expressa por uma expressão lógica, for verdadeira.

As estruturas de repetições também podem ser chamadas de _loops_ ou _laços_, existem diferentes tipos de estruturas ou laços de repetição, os mais comuns são _for_, _while_ ou _do while_ ao qual iremos ver mais abaixo.

## For

O laço `for` normalmente é utilizada quando o número de repetições já é conhecido, ele consiste em 3 expressões e 1 sequencia de instruções!

```js
for (inicialização; condição; expressão final) {
  //instruções que serão executadas repetidamente até o valor virar false
}
```

- **Inicialização:** **Esta expressão é executada antes da execução do primeiro laço**, aqui definimos uma variável para servir de contador, a variável criada aqui fica no escopo do laço, quando o laço se encerrar, ela é destruída.

- **Condição:** **Esta expressão é verificada a cada iteração antes da execução do laço**, se ela for `true`, as instruções ou o código do laço é executado, se ela for `false`, o laço é interrompido, se essa expressão for omitida, será sempre `true`.

- **Expressão Final:** **Esta expressão é executada após cada iteração do laço**, ela é usada normalmente para incrementar um contador usando `i++`, mas também pode ser usada para decrementá-lo com `i--`, sendo a variável `i` o index atual do loop.

- **Instruções:** **O código dentro do bloco a ser repetido no laço**. Pode ser uma única ou várias linhas de código.

### Exemplo

Podemos fazer um loop para contar números de 0 até 5, para isso basta criar o laço `for`, e na parte da condição colocar que o index é menor ou igual a 5.

```js
for (let i = 0; i <= 3; i++) {
  console.log(i)
}

// resultado:
// 0
// 1
// 2
// 3
```

## For In

O `for in` itera sobre as propriedades enumeráveis de um objeto, como índices de um array ou chaves de um objeto.

```js
//em objetos
const pessoa = { nome: 'Ana', idade: 25 }
for (let chave in pessoa) {
  console.log(chave) // "nome", "idade"
}

//em array
const numeros = [10, 20, 30]
for (let indice in numeros) {
  console.log(indice) // "0", "1", "2"
}
```

## For Of

O `for of` itera diretamente sobre os valores de estruturas iteráveis, como arrays, strings, maps, sets, etc.

```js
//em strings
for (let letra of 'Oi') {
  console.log(letra) // "O", "i"
}

//em arrays
const numeros = [10, 20, 30]
for (let valor of numeros) {
  console.log(valor) // 10, 20, 30
}
```

## While

O laço `while` normalmente é utilizado quando não sabemos a quantidade de repetições que serão necessárias.

```js
while (expressao) {
  //instruções que serão executadas repetidamente até o valor virar false
}
```

O laço `while` começa avaliando a condição se a condição for `true`, o código dentro do bloco será executado. Se a condição for `false`, o código dentro do bloco não será executado e o laço se encerra.

### Exemplo

Criando um contador de 1 até 5, e exibirá o valor atual da iteração no console.

```js
let i = 1

while (i < 5) {
  console.log(i)
  i++ //não pode esquecer de incrementar se não dará loop infinito
}

// resultado:
// 1
// 2
// 3
// 4
```

## Do...While

O `do...while` **é uma estrutura de repetição que executa um bloco de código pelo menos uma vez e continua repetindo enquanto a condição especificada for verdadeira**. Diferentemente do `while`, a condição é verificada após a execução do bloco, ele é muito utilizado para fazer menu, pois ele sempre executará 1 vez, independente da condição.

```js
let i = 0
do {
  console.log(i)
  i++
} while (i < 3)

// resultado:
// 0
// 1
// 2
```
