## Introdução

A entrada e saída de dados, também conhecidas como **E/S ou I/O (Input/Output), referem-se ao processo de transferência de informações entre um sistema computacional e o mundo externo, seja um usuário ou outro sistema**.

**A entrada de dados envolve a recepção de informações do usuário ou de fontes externas**, como teclados, mouse, microfones, scanners ou arquivos, esses dados são capturados pelo sistema para serem processados.

**A saída de dados consiste na comunicação dos resultados processados de volta ao usuário ou a um sistema externo**, por meio de dispositivos como monitores, impressoras, alto-falantes ou arquivos, na programação, a entrada é representada por qualquer dado que o programa recebe durante a execução, proveniente de fontes como o teclado, arquivos ou redes.

## Entrada de dados

A função `input()` recebe como parâmetro uma **string** que será mostrada como auxílio ao usuário, geralmente o informando que tipo de dado o programa está aguardando receber, podemos armazenar o valor que é digitado em uma variável, assim podemos utilizar mais tarde.

```py
# irá exibir a mensagem
input('Escreva sua idade: ')

# irá armazenar o retorno do input na variável name
name = input("Escreva o seu nome: ")
```

Quando executarmos esse código no terminal, irá acontecer o seguinte:

1. Mostrar o texto `"Escreva sua idade: "` na tela.
2. E aguardar até que o usuário digite alguma informação.

## Saída de dados

A função `print()` é a responsável por imprimir os dados na tela, podemos utilizar ela como `print()` ou no modo formatado que é `print(f'')` nesse modo formatado podemos adicionar valores de variáveis ou outros formatos de texto.

```py
# função print normal
print("Olá mundo!")

# função print formatada
idade = 26
print(f"Você tem {idade} anos!") #exibe "Você tem 26 anos!"
```
