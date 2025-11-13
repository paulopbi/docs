## Function.length

`Function.length` retorna o total de argumentos da função.

```js
function somar(n1, n2) {
  return n1 + n2
}

somar.length // 2
somar.name // 'somar'
```

## Function.name

`Function.name` retorna uma string com o nome da função.

```js
const sayHello = () => {
  console.log('Hello World')
}

sayHello.name //retorna: 'sayHello'
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
