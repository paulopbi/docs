## Introdução

Uma variável representa um contêiner ou espaço na memória (física ou virtual) de um computador, onde diferentes tipos de dados (valores) são armazenados durante a execução de um programa.

Cada variável recebe um nome descritivo (identificador) que faz referência ao valor salvo, os dados armazenados podem mudar ou podem ser constantes dependendo do tipo de variável utilizada.

## Var

Antes da atualização **ES6+**, as variáveis declaradas com `var` eram o padrão no JavaScript, o problema é que `var` possui **escopo global e de função**, o que pode gerar comportamentos inesperados, como:

- permitir modificar a variável em qualquer lugar do código;
- sobrescrever variáveis sem avisar quando usamos o mesmo nome;
- sofrer _hoisting_ (é “içada” para cima do código de forma confusa).

```js
var nome = 'Paulo'
```

> [!WARNING]
> No JavaScript moderno, não é recomendado usar var, ainda funciona, mas não é seguro e raramente faz sentido usar hoje em dia.

## Const

Variáveis declaradas com const são constantes, ou seja, o valor não pode ser reatribuído depois da declaração.

```js
const nome = 'Paulo'
```

> [!NOTE]
> O valor é constante, mas **objetos** e **arrays** podem ser modificados internamente, **apenas a referência que não pode mudar**.

## Let

Variáveis declaradas com `let` podem ter seus valores modificados ao longo da execução, `let` é a forma recomendada quando você precisa alterar o valor da variável.

```js
let nome = "Paulo
```

## Boas Práticas

- Os nomes podem iniciar com $, \_, ou letras.
- Os nomes podem conter números mas não iniciar com eles.
- O padrão mais usado no JavaScript é o _camelCase_ `nomeCompleto`, `idadeDoUsuario`, `totalDePontos`.
- Variáveis são case sensitive, _nome_ é diferente de _Nome_ e também diferente de _NOME_.

## Leitura Complementar

- [Escopo](./escopo.md)
- [Hoisting](./hoisting.md)
