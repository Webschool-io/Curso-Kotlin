
# Function Type em Kotlin

Na última aula bônus vimos exemplos de como as lambdas facilitam a vida do programador.
Hoje veremos o uso da <b> functions types </b> em Kotlin evidênciando ainda mais o poder da programação funcional em Kotlin.


## Exemplo:

```kotlin

val sum: (Int, Int) -> Int = { x, y -> x + y } // função com dois parâmetros inteiros e retorno de valor inteiro

```

Como vocês podem ver, o compilador infere que há variáveis com tipos de função.

<b>Para declarar uma "Function Types", você deve colocar os tipos de parâmetros da função entre os parênteses, seguido de uma seta e o seu tipo de retorno</b> 

## Exemplo:

```kotlin

fun sumTwoNumbers(operation:(Int,Int)-> Int) {
    val result = operation(2,2)
    print(result)
}

```
```kotlin

//Chamando no main
fun main(args: Array<String>) {
 
    sumTwoNumbers { numberOne, numberTwo -> numberOne + numberTwo }
    //sumTwoNumbers { numberOne, numberTwo -> numberOne * numberTwo }
  
 }


```
A sintaxe para chamar a função passada como um argumento é a mesma que usamos para chamar uma função normal: você coloca os parênteses depos do nome da função e  os parâmetros ficam dentro dos parênteses.


Se interessou por Kotlin, faça nosso curso, participe do grupo no Telegram e se inscreva em nosso curso aqui no Github.

## Github
*https://github.com/Webschool-io/Curso-Kotlin*

## Telegram
*https://t.me/webschoolkotlin*

