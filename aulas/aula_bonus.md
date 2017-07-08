# Aula bônus

Conversando com meu amigo Suissa, tive a ideia de pegar emprestado alguns dos exercícios do seu curso de refatoração em Js.
e mostrar como fica esse mesmo código em kotlin. Esses exercícios terão uma abordagem matemática, e um bom passeio pela programação funcional, já que considero que esse é o mais importante paradigma que existe no Kotlin; a programação funcional. Acreditamos que todo programador deve ter uma bom entendimento de matemática e o uso da programação funcional pode ser de grande utilidade para o entendimento do conceito de imutabilidade que existe no kotlin. Nesse primeiro momento vou utilizar o exemplo dos números primos e um pouco do que pode ser feito com o uso das lambdas em Kotlin.

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

Gostou?
Então como ficaria esse mesmo exemplo com o uso das lambdas?

A grande sacada das lambdas é que ao invés de implementar algo genérico para solucionar um problema( o que custaria talvez algumas linhas ), eu posso me beneficiar de funções poderosas da API nativa da própria linguagem, tornando o código mais légivel e profissional. O uso de metódos map, filter são exemplos de como resolver facilmente certos problemas de programação.


Significado de lambdas, segundo o Wikipedia:
*https://pt.wikipedia.org/wiki/C%C3%A1lculo_lambda*


Continuo amanhã...

