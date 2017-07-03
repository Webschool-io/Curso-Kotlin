# Aula 01 (Uma introdução a linguagem)

Olá, esta é nossa primeira aula escrita do curso de Kotlin feito pela Webschool.io para você que deseja aprender sobre esta nova linguagem para desenvolvimento de aplicativos mobile Android adotada pela Google.
Eu sou Anderson Faro e será um prazer fazer esse curso para você. Nessa primeira aula escrita, aprenderemos:

- >**Variáveis(mutáveis e imutáveis), constantes e funções.**
- >**Loops, for in, ranger, if, else, when.**

 Boa parte do que é apresentado aqui será mostrado com mais detalhes nas videos aulas. Mostraremos como ficará na prática um app real android. Então não se prendam somente a aula escrita e atentem as vídeos aulas.

# Na prática
 
- >**Variáveis, constantes e funções.**
 
Para declarar uma variável em Kotlin usa-se a palavra-chave var podendo declarar seu tipo ou omitindo.
 
<b>Exemplo:</b>
 
 ```kotlin
var pergunta = “ Quantas séries de TV americana tem o cara mais rápido do mundo?” //Omitindo seu tipo
 ```
```kotlin
var resposta = 1 //Omitindo seu tipo
``` 
Nesse exemplo foi omitido o tipo das variáveis mas você pode especificar explicitamente seu tipo se quiser:

```kotlin
var pergunta: String = “Quantas séries de TV americana tem o cara mais rápido de toda a galáxia?” 
 
var resposta :Int = 1
```

<b>Caso sua variável não inicialize com algum valor você precisa especificar seu tipo explícito:</b>
 
Exemplo:

```kotlin
var x: Int //Uma variável inteira com tipo declarado
x = 25
``` 
<b>Mesmo var permitindo que seu valor seja alterado seu tipo precisa continuar sendo do mesmo tipo.</b>

```kotlin 
var color = “red”
color = 10 //Esse código não compila
``` 
 <b> Digamos que eu queira converter uma string em um int, como eu faria?</b>
 
 Usaria o metódo toInt() para convertê-lo em inteiro
 
 Exemplo:
 
 ```kotlin 
 var numberFour : String = "4"
 numberFour.toInt() // e voilá... aparece na tela 4
 ```
 
 <b> Se eu quiser converter um Double?</b>
 
 ```kotlin 
 var numberDouble : String = "4000"
 numberFour.toDouble() // e voilá... aparece na tela 4000.0
 ```
 
Existem duas formas de declarar uma variável em kotlin:
 
val - referência imutável. Quando declarado desta forma a variável depois de inicializar seu valor, não pode ser alterado.
 
var - referência mutável. Seu valor pode ser alterado.
 
 
É aconselhável que você declare sempre suas variáveis em kotlin usando o val. Declare var se for extremamente necessário evitando efeitos colaterais futuros.
Isso torna seu código mais legível e mais próximo do paradigma de programação funcional o que deixa sua programação menos mutável.
 
<b>Obs: Mesmo que sua variável seja imutável o objeto que ela aponta pode ser alterado.</b>
 
Exemplo: 
 
```kotlin 
val x = arrayListOf ( “Java”)
x.add(“Kotlin”) //Muda o objeto apontado pela referência
```

Formatação de Strings no Kotlin é mais fácil e divertido, não acha?
 
 ```kotlin 
fun main (args:Array<String>) {
	val gato_pidao = 10
	print(“Quantos gatos pedem? ${gato_pidao}”)
}
 ```
 
- >**For in, ranger, if, else, when.**
 
Vamos iterar com o for in?
 
Exemplo: 
 
```kotlin

//Mais simples possível
```
 
```kotlin 
for (x in 1..5) {
	print(x)
}
```

```kotlin 
//Ou assim 
```

```kotlin
for (x in 1..5) print(x)
```

Mas e se quisermos mostrar os números em ordem reversa?
 
Exemplo:
 
```kotlin
for (x in 4 downTo 1) print(x) // 4321
```
 
Com array:
 
```kotlin

val lista = setOf(1,3,4,5)
 
for( array in lista) {
	print(array)
}
 ```
 
If e else.
 
```kotlin

var max = a 
if (a < b ) max = b
 ```
 
Com o else:
 
```kotlin
if (a > b) {
	//faça algo
}
 
else {
	//faça outra coisa
}
 ```
 
Como uma expressão:
 
```kotlin
val x = if (a > b) print (a)  else b
```
 
Uso do When em Kotlin:
 
Exemplo: 

 ```kotlin 
fun showWhen (x: Int) {
  
   when (x) {
          
         0  -> {
            print("zero")
         }
              
         1  -> {
            print("Um")
         }
      
        10 -> {
           print("Dez")
        }
  
       else -> {
           print("errado")
       }
   }
  
}
 ```
 
When com range:
 
  ```kotlin
fun whenRange(xx:Int) {
   when (xx) {
      
       in 1..10 -> print("teste")
       else -> { print("erro")}
      
   }
  }
 
  ```
 
 
Ranges em kotlin
 
Da forma mais básica:
 
 ```kotlin
val x  = 1..10
val t = “a” .. “z”
  ```
  
Ranges com if:
 
  ```kotlin
if (i in 1..10) { // equivalent of 1 <= i && i <= 10
    println(i)
}
  ```
  
com o for
  
  ```kotlin
for (i in 1..4) print(i)
  ```
 
Funções em Kotlin da forma mais simples:
 
Exemplo: 
 
 ```kotlin
 fun showText(String: text) = text
  ```
  
Funções com argumentos:
 
 ```kotlin 
 fun sum (pegasus: Int, jaspion: Int):Int = (pegasus + jaspion)
  ```
  
com corpo:

 ```kotlin 
fun text () {
 
	print(“texto...”)
}
 ``` 
 
 A Chamada da função

  ```kotlin
  val result = text() 
 ```
 
Funções com argumentos, retorno e chaves:

```kotlin
fun calc (numberOne:Int, numberTwo: Int): Int { return numberOne + numberTwo }
```

Funções Locais e um exemplo básico de seu uso:

//TODO |^


E agora, vamos aprender um pouco de Android?
calma,  e aguardem os videos...


 
 
 
 


