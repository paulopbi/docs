## `Array.map()`

A função `map()` do JavaScript é um método de arrays que **cria um novo array** aplicando uma função de callback a cada elemento do array original.

Ele percorre todos os itens do array, transforma-os de acordo com a lógica da função fornecida e retorna um novo array com os resultados, sem modificar o array original.

###### Sintaxe

`array.map(callback(item, index, array), thisArgs)`

###### Caso De Uso

Um exemplo do map seria para criar um gerador de _slugs_, podemos utilizar o map para transformar os valores e adicionar o hifen `-` a cada item do array.

```js
const persons = [
  'Paulo Muzy',
  'Pitagores',
  'Neymar JR',
  'Ricardo Sales',
  'Napoleão O Grande',
]

const generateSlug = (values) => {
  if (values) {
    return values.map((person) =>
      person.trim().toLowerCase().replaceAll(' ', '-')
    )
  }

  return undefined
}

generateSlug(persons)

//retorno: ["paulo-muzy", "pitagores", "neymar-jr", "ricardo-sales", "napoleão-o-grande"]
```
