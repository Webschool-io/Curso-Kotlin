
# Aula 04

Olá, esta é nossa quarta aula escrita do curso de Kotlin feito pela Webschool.io para você que deseja aprender sobre esta nova linguagem para desenvolvimento de aplicativos mobile Android adotada pela Google.
Eu sou Anderson Faro e será um prazer fazer esse curso para você. Nessa quarta aula escrita, aprenderemos:

- >**ListView para exibição de uma lista de nomes.**
- >**A criação de botões e mensagem exibida com Toast na tela.**

Boa parte do que é apresentado aqui será mostrado com mais detalhes nas videos aulas. Mostraremos como ficará na prática um app real android. Então não se prendam somente a aula escrita e atentem as vídeos aulas.

# ListView

Responsável pela exibição de itens numa lista, exemplo:

![](https://s26.postimg.org/n3m45w76x/lista.png )


```kotlin
  
package br.com.mylistapp

import android.os.Bundle
import android.support.v7.app.AppCompatActivity
import android.widget.ArrayAdapter
import android.widget.Toast
import kotlinx.android.synthetic.main.activity_main.*

class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val listaApp  = listOf("Fulano", "Beltrano", "Patrão", "João" )

        val arrayAdapter : ArrayAdapter<String> = ArrayAdapter(this, android.R.layout.simple_list_item_1, listaApp)

        //val lista = findViewById(R.id.listview) as ListView <- sem as extensions

        listview.adapter = arrayAdapter //<- com as extensions

        listview.setOnItemClickListener { parent, view, position, id ->

                when (position) {

                    0  -> {
                        Toast.makeText(this, "${position}", Toast.LENGTH_SHORT).show()
                    }

                    1  -> {
                        Toast.makeText(this, "${position}", Toast.LENGTH_SHORT).show()
                    }

                    2  -> {
                        Toast.makeText(this, "${position}", Toast.LENGTH_SHORT).show()
                    }

                    3  -> {
                        Toast.makeText(this, "${position}", Toast.LENGTH_LONG).show()
                    }
                }
        }



    }


}


```

