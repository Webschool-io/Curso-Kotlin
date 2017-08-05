# Aula 02 (Um pouco mais  da linguagem kotlin com mais um pouco com Android)

Olá, esta é a segunda aula escrita do curso de Kotlin feito pela Webschool.io para você que deseja aprender sobre Kotlin.
Eu sou Anderson Faro e será um prazer fazer esse curso para você. Nessa segunda aula escrita, aprenderemos:

- >**Classes, enums,interface, propriedades e Smart casts.**
- >**Arrays, list e extensions.**

 Boa parte do que é apresentado aqui será mostrado com mais detalhes nas videos aulas.
 Mostraremos como ficará na prática um app real android.
 
# Na prática
 
- >**Classes, enums,interface, propriedades e Smart casts.**

Como declarar uma classe?

# Exemplo:

```kotlin
  
  class MyActivity { //Não é diferente do que ocorre em outras linguagens
    
  }
  
```
## Herança em Kotlin

Por padrão qualquer classe em Kotlin herda de Any, são fechadas por padrão(final) e para extender-se de uma classe é preciso declarar como open ou abstract.

# Exemplo:

```kotlin
  
  open class Animal (name: String) { }
  
```

```kotlin

  class Dog(firstName: String, lastName: String) : Animal(name)
  
```

- >**Enum.**

Em Kotlin criamos um Enum desta forma:

# Exemplo: 

```kotlin
  
  
enum class Color {
    vermelho, amarelo
}

```

### Implementando sua enum class

```kotlin
  
    fun showColor(color:Color) {

        when (color) {

            Color.amarelo -> "Amarelo"
            Color.vermelho -> "Vermelho"
        }
    }
```

- >**Interface**

Em kotlin, interface é similar ao que ocorre em outras linguagens de programação, podem ter metódos abstratos e propriedades.
O que as diferencia das classes abstratas é que uma interface não pode armazenar estado.


#### Exemplo:

```kotlin

interface MyInterface {
    fun somar()
    
    fun dividir() {
        //corpo da função opcional
    }
}
```

**Isso mesmo, interface em kotlin pode usar funções com corpo, diferentes da maioria das linguagens de programação.**


Implementando uma interface:

```kotlin

class MyClass : MyInterface {

    override fun somar() {
    
    }
    
    override fun dividir() {
       
    }
}
```
Propriedades na interface:


```kotlin

  interface MyInterface {
    val propriedadeOne: Int // abstrato

    val propriedadeComImplementacao: String
    
        get() = "foo"

    fun foo() {
        print(propriedadeOne)
    }
}

class Class : MyInterface {
    override val propriedadeOne: Int = 29
}
```
Você pode declarar propriedades em interfaces e ou fornecer implementações para acessores. Entenda que logo ai em cima
"propriedadeComImplementacao" implementa sua constante com o acessor get.



- >**Smart Cast em Kotlin**

Podemos verificar se um objeto está em conformidade com um tipo específico em tempo de execução usando o operador "is" ou "!is" a forma negada e também o operador "as"

#### Exemplo:


```kotlin

  if (obj is String) {
     print(obj.length) // verifica se o objeto é String
}

```

```kotlin

  if (obj !is String) {
     print(obj.length) // negando que o objeto é string, ou seja, se não for String ele imprime o tamanho de sua string
}

```

Com o uso do operador "as"

#### Exemplo:

Desta forma é uma forma insegura de usar o cast e retorna um erro de TypeCastException

```kotlin

  val x: String = y as String  

```

Da form certa e segura

```kotlin

  val x: String? = y as String?  

```
Ou desta forma também.

```kotlin
  
  val x: String? = y as? String

```
# Na prática
 
- >**Arrays, list e extensions.**


Arrays em Kotlin são representadas pela classe Array e possue listas e indices assim como ocorre em outras linguagens de programação.

### Exemplo:

```kotlin

  val x: IntArray = intArrayOf(1, 2, 3)

```

```kotlin

  //Com o uso do metodo get
  
  val x: IntArray = intArrayOf(1, 2, 3)
  x.get(1) //pego a posição 1 do array

```


```kotlin

  //Com o uso de lambdas
  
  val x: IntArray = intArrayOf(1, 2, 3,4,5,6,7)
  
  x.filter{it > 2}// filtrando um numero maior que 2

```

## Extensions functions

É uma função que adiciona um novo comportamento a uma classe, estende as classes adicionando novo comportamentos.

### Exemplo:

```kotlin
  
  //Imprime uma mensagem na tela
  
  Toast.makeText(this, "parabéns, você acertou! ", Toast.LENGTH_SHORT).show()

```


```kotlin
  
  //O mesmo efeito mas com as functions extensions (assim eu poderia chamar essa função onde desejar)
  
  ```kotlin
  
    fun Context.toast(message: CharSequence, duration: Int = Toast.LENGTH_SHORT) {
      
      Toast.makeText(this, message, duration).show()
      
    }

  ```

Com isso finalizamos esta segunda aula. Não esqueça, que além desse contéudo, teremos muito nos videos aulas.


