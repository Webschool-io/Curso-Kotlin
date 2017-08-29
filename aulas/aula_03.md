
# Aula 03 

Olá, esta é nossa terceira aula escrita do curso de Kotlin feito pela Webschool.io para você que deseja aprender sobre esta nova linguagem para desenvolvimento de aplicativos mobile Android adotada pela Google.
Eu sou Anderson Faro e será um prazer fazer esse curso para você. Nessa terceira aula escrita, aprenderemos:

- >**Nullable types, Non-Null Types
lambdas(map, filter, etc).**



 Boa parte do que é apresentado aqui será mostrado com mais detalhes nas videos aulas. Mostraremos como ficará na prática um app real android. Então não se prendam somente a aula escrita e atentem as vídeos aulas.
 
 # Nullable types
 
 O perigo de uma referência nula resulta em uma exceção de referência nula e para eliminar esta possibilidade, kotlin usa dois operadores importantes, o operador ? e operador !! e acaba de vez com o <b>NullPointerException's</b>, como ocorre no Java por exemplo.

# Na prática
 
- >**Nullable types, Non-Null Types.**
 
 Imagine que tenhamos algo como isso:

<b>Exemplo:</b>
 
 ```kotlin
   var a: String = "abc"
   a = null // compila com erro
 ```
Mas o porquê disso?

### Entenda que a variável foi definida com um valor que coloquei, até aí tudo ok... logo depois pedi para compilar e executar com um valor null e ela me retorna um erro, isso porque a tentei torna-lá nula e isso não funciona no kotlin, é uma forma insegura e sujeita a alterações perigosas.

# Como deve ser

<b>Exemplo:</b>
 
 ```kotlin
   var a: String? = "abc" // veja o uso da interrogação (?)
   a = null // compila com sucesso
 ```
 
 ### Isso quer dizer que eu tenho uma opção a mais para trabalhar com minha variável. Ainda sim não funcionaria,veja isso abaixo:
 
 ```kotlin
 
   var a: String? = "abc" // veja o uso da interrogação (?)
   a = null // compila com sucesso
   a.length // não funciona como deveria, porque ela só pode ser nula
 
 ```
 
 # Da forma correta 
 
 ```kotlin
 
   var a: String? = "abc" // veja o uso da interrogação (?)
   a = null // compila com sucesso
   a?.length // funciona como deveria, vejam o uso da interroção, nesse caso, ainda te dou uma opção para exibir o que quero
 
 ```
 
 ### "Às vezes,queremos dispensar as verificações do compilador e forçar um tipo nulo em um tipo não anulável. Para isso usamos o operador !!
 
 <b>Exemplo:</b>
 
 ```kotlin
   var a: String? = "abc" 
   val f: String = a!! // compila com sucesso
 ```
### O uso do operador !! também é uma opção a usar...ainda sim não é uma opção segura pois a ideia de forçar já nos dá uma impressão insegura por si só

### Sempre que possível use o operador ?


- >**lambdas(map, filter, entre outros)**

Vimos em nossas aulas bônus *https://github.com/Webschool-io/Curso-Kotlin/blob/master/aulas/aula_bonus.md* o uso de lambdas e seus benefícios.

Um exemplo básico e para fácil entendimento, é o exemplo da média de notas de um aluno.
Vejam como o código ficará mais elegante do que este abaixo:

<b>Exemplo sem lambdas:</b>
 
 ```kotlin
  
 val nota_um = 1
 val nota_dois:Int = 0
 val nota_tres:Int = 2
 val media: Double = (nota_um + nota_dois + nota_tres)/ 3.toDouble()
 val max = if (media >= 7) print("Parabéns garoto!") else print("Ops... precisa melhorar")
    
 ```
<b>Exemplo com lambdas:</b>

 Com os caras map e filter
 
 ```kotlin
 
    val notas = listOf<Int>(7, 6, 10)
    
    //O método get() Pega  a posição do array
    
   val media  : Double = (notas.get(0) + notas.get(1) + notas.get(2) ) / 3.toDouble()
   notas.map { media }.filter { it > 6 }
 
    
 ```
 <b>Mais elegante:</b>
 
 ```kotlin
   val notas = listOf<Int>(1,2,3)
   val media  : Double = (soma.sumBy { it  }) / 3.toDouble()// o metodo sumBy soma cada um das posições e depois divide.
 ```
  
 ### Quando usamos lambdas, estamos falando diretamente das funcões de alta ordem, ou seja as funções bacanas e de alto poder. A programação funcional nos presenteia com a possibilidade de programar mais elegantemente. 
 
 ### Mais um exemplo:
 
 ```kotlin
 val numbers = listOf(1,21,33,67)
 numbers.maxBy{it}
 ```
 
 ### Neste exemplo eu quero imprimir o maior numero entre esses que estão em nosso array.
 
 #### Entendam que o uso de lambdas nos permite que usemos da própria api, funcões e metódos nativos que resolvem problemas frequentes em que precisamos resolver... imagina uma função cheio de if e else deixando o código ilegivel... ficaria horrível.. então é bom que conheça essas funções nativas da própria lang que nos evita gastar tempo desnecessário.
 
 
 #### Até a proxima com nossa video aula
 
 
 
 
 
 
 
