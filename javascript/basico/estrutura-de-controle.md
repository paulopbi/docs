## Introdução

Estrutura de controles são fundamentais na programação, estrutura de controle (ou fluxo de controle) refere-se à ordem em que instruções, expressões e chamadas de funções são executadas, com elas podemos _"desviar"_ o código para seguir outro caminho.

## If e Else

O `if` verifica se uma expressão é verdadeira, caso contrário o `else` será ativado.

```js
const maiorDeDezoito = true;

if(maiorDeDezoito) {
 // o console abaixo será executado
  console.log('O usuário é maior de dezoito anos');
} else {
  console.log('O usuário não é maior de dezoito anos');
}
```

No exemplo a cima, o valor retornado é _"O usuário é maior de dezoito anos"_ pois a variável possui o valor `true`.

> [!NOTE]
> 
> O valor dentro dos parênteses sempre será avaliado como um `boolean`, possuindo `true` ou `false`.

## Else If

Caso o valor do `if` seja falso e o mesmo não é executado, podemos colocar outra expressão para comparação utilizando o `else if`, e se o `else if` for verdadeiro, ele será executado.

```js
const possuiGraduacao = true;
const possuiDoutorado = false;

if(possuiDoutorado) {
  console.log('Possui graduação e doutorado');
} else if(possuiGraduacao) {
  console.log('Possui graduação, mas não possui doutorado');
} else {
  console.log('Não possui graduação');
}
// retorna Possui Graduação, mas não possui doutorado
```

## Switch Case

O `switch case` é uma estrutura condicional que verifica o valor de uma variável e executa um código diferente dependendo do valor, é parecido com o `if/else` porém ele é mais conciso e fácil de ler.

```js
const console = 'Xbox'

switch (console) {
  case 'PlayStation':
    console.log('Seu console é um Playstation.')
    break
  case 'Xbox':
    console.log('Seu console é um Xbox.')
    break
  case 'Nintendo':
    console.log('Seu console é um Nintendo.')
    break
  default:
    //valor padrão caso não satisfaça as condição
    console.log('Console não reconhecido.')
}
```

Como o valor acima é `Xbox` ele irá entrar no `case "Xbox"` e executará o `console.log("Seu console é um Xbox.")`.

## Ternário

Serve como uma abreviação das condicionais `if` e `else`, geralmente é utilizado quando precisamos atribuir um valor para uma variável dependendo de uma condição.

```js
var idade = 19;
// condição ? true : false
var podeBeber = (idade >= 18) ? 'Pode beber' : 'Não pode beber';
console.log(podeBeber) // Pode beber
```

A sintaxe do ternário é simples, passamos a condição e caso for `true`, irá retornar o primeiro valor, caso seja `false` irá retornar o segundo valor `idade >= 18 ? true : false`.
