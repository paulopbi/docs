## Introdução

Escopo é o contexto que determina **onde uma variável, função ou objeto pode ser acessado no código**.  

Ele organiza o programa e evita conflitos como sobrescrita de valores ou o uso indevido de variáveis fora do lugar correto.

## Tipos de escopo

No JavaScript, os principais tipos de escopo são:

- **Escopo Global:** Variáveis declaradas fora de qualquer função ou bloco podem ser acessadas de qualquer lugar do código, é importante usar com cautela, pois pode levar a problemas de colisão de nomes e bugs difíceis de consertar.

- **Escopo Local:** Variáveis declaradas dentro de uma função são acessíveis apenas dentro daquele escopo, com o `var`, esse escopo era de função. Isso significa que a variável era visível em todo o corpo da função, mesmo antes de sua declaração.

- **Escopo de Bloco:** Introduzido com `let` e `const` no _ES2015_, este escopo restringe a variável a um bloco específico de código (como um if, for ou while). Uma variável declarada com `let` ou `const` dentro de um bloco não é acessível fora dele.

## Exemplo

```js
let nomeGlobal = 'Alice'; // Variável de escopo global

function minhaFuncao() {
  let nomeLocal = 'Bob'; // Variável de escopo de função
  console.log(nomeGlobal); // Acessa a variável global
  console.log(nomeLocal); // Acessa a variável local
}

minhaFuncao();

console.log(nomeGlobal); // Acessa a variável global
console.log(nomeLocal); // Isto daria erro, pois nomeLocal não é acessível fora da função
```