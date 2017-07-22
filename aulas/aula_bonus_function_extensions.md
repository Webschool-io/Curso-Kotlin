# Extension Function  em Kotlin

"óia eu mais uma vez..."

Uma "Function Extension" é uma função que adiciona comportamento a uma classe, mesmo que não possamos acessar o código-fonte dessa classe. 
É uma maneira de estender as classes adicionando novo comportamentos. 
A vantagem de usar as funções de extensão no Kotlin é que não precisamos passar o objeto como um argumento. Com ela
é possível acessar todas as opções que a API te oferece, ela atua como parte da classe, implementa e cria novas funcionalidades.
A função de extensão atua como parte da classe, e podemos implementá-la usando este e todos os seus métodos públicos.

# Exemplo mais usado quando queremos imprimir uma mensagem na tela:

```kotlin
   Toast.makeText(this, "parabéns, você acertou! ", Toast.LENGTH_SHORT).show()
```

# Exemplo com as Extension Function:

```kotlin
fun Context.toast(message: CharSequence, duration: Int = Toast.LENGTH_SHORT) {
 
    Toast.makeText(this, message, duration).show()
}

```

Entendeu que ele deu uma novo comportamente a classe...

Dá pra imaginar o quanto de opções temos ao nosso dispor com as extensions?


Se interessou por Kotlin, faça nosso curso, participe do grupo no Telegram e se inscreva em nosso curso aqui no Github

## Github
*https://github.com/Webschool-io/Curso-Kotlin*

## Telegram
*https://t.me/webschoolkotlin*
