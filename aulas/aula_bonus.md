# Aula bônus

Conversando com meu amigo Suissa, tive a ideia de pegar emprestado alguns dos exercícios do seu curso de refatoração em Js 
e mostrar como fica esse mesmo código em kotlin. Esses exercícios terão uma abordagem matemática, e um bom passeio pela programação funcional, já que considero que esse é o mais importante paradigma que existe no Kotlin. Acreditamos que todo programador deve ter uma bom entendimento de matemática e o uso da programação funcional pode ser de grande utilidade para o entendimento do conceito de imutabilidade que existe no kotlin. Nesse primeiro momento vou utilizar o exemplo dos números primos e um pouco do que pode ser feito com o uso das lambdas em Kotlin. A principio como vocês devem ver no github do Suissa, nós queremos saber se o 10002,10003 são primos.

Aqui neste link você pode ter acesso as aulas do Suissa e ao exemplo dos números primos:

*https://github.com/suissa/Curso-refatoracao-para-js-funcional/blob/master/aulas/aula01%20-%20Como%20solucionar%20um%20problema/readme.md*


Para quem não se lembra, os números primos tem apenas dois divisores naturais, o número  1 e ele mesmo. Sendo que o número  2 é o único número par que é primo pois é divisivel por um e por ele mesmo.

# Exemplo em Js imperativo do curso do Suissa:

```js
function isPrime(num) { 
  // se for par E não for 2
  if ((num % 2) === 0 && num !== 2)
  for (let i = num - 1; i >= 2; i--) {
    if(num % i === 0) {
      console.log('\n')
      console.log(num + ' é divisível por: ', i)
      return false;
    }
  }
  return true;
}

```
# Exemplo em Kotlin imperativo:

```kotlin

fun isPrime(num:Int) :Boolean {
    
    if ((num % 2) == 0 && num !== 2 || num == 1) {
         print("Não é primo")
        
        return false
    } else {
        print("Primo")
        return true
    }
 }

```

Gostou, e como ficaria esse mesmo exemplo com o uso das lambdas?

A grande sacada das lambdas é que ao invés de implementar algo genérico para solucionar um problema( o que custaria talvez algumas linhas de código ), eu posso me beneficiar de funções poderosas da API nativa da própria linguagem, tornando o código mais légivel e profissional. O uso de metódos map, filter(funções usadas para Colections) são exemplos de como resolver facilmente certos problemas de programação.


Significado de lambdas, segundo o Wikipedia:
*https://pt.wikipedia.org/wiki/C%C3%A1lculo_lambda*


# O mesmo exemplo com o uso de lambdas:


## Com vocês no palco principal, o cara mais importante da galera: o main, onde tudo pode acontecer

```kotlin

fun main(args: Array<String>) { //Aqui é onde tudo acontece
    
    val numbersPrimes = arrayOf(10_002,10_003) //Pegamos o 10002 10003, como tinhamos falado
    
    //a mágica das lambdas
    val isPrime = { numbersPrimes  :Int -> (numbersPrimes % 2 == 0 && numbersPrimes !== 2 || numbersPrimes == 1) }
    
    numbersPrimes.map(isPrime) // O uso do método map
    print(numbersPrimes)
    
}

```
Muito mais légivel, não? ficou dahora!

Vamos citar um exemplo, que não está nos exemplos do Suissa?
O que me vem a cabeça neste momento é o exemplo clássico da média das 03 notas dos alunos.

## Da forma mais escrachada possível.

```kotlin
   val notas = listOf<Int>(7, 6, 10)
    
    //O método get() Pega  a posição do array
    
   val media  : Double = (notass.get(0) + notass.get(1) + notass.get(2) ) / 3.toDouble()
   notas.map { media }.filter { it > 6 }
  
```
Funciona mas não é légivel e nem elegante.

## Um exemplo elegante e com o uso do método sumBy()

```kotlin
  
    //O método sumBy() soma cada um das suas posições e mostra seu resultado
    
    val notas = listOf<Int>(1,2,3)
    
    val media  : Double = (soma.sumBy { it  }) / 3.toDouble()// toDouble converte para que o resultado seja double no final
```


Não é bonito de ver?

Se interessou por Kotlin, faça nosso curso, participe do grupo no Telegram e se inscreva em nosso curso aqui no Github

## Github
*https://github.com/Webschool-io/Curso-Kotlin*

## Telegram
*https://t.me/webschoolkotlin*





