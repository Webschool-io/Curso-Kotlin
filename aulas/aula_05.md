# Aula 05

Olá, esta é nossa quinta aula escrita do curso de Kotlin feito pela Webschool.io para você que deseja aprender sobre esta nova linguagem para desenvolvimento de aplicativos mobile Android adotada pela Google.
Eu sou Anderson Faro e será um prazer fazer esse curso para você. Nesta aula escrita, aprenderemos:

- >**A criação de um menu com opções para diferentes activitys.**
- >**Criação de abas no aplicativo.**


# Um menu prático com algumas opções


```kotlin

package br.com.mylistapp

import android.content.Intent
import android.os.Bundle
import android.support.v7.app.AppCompatActivity
import android.view.Menu
import android.view.MenuItem

class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
    }

    override fun onCreateOptionsMenu(menu: Menu?): Boolean {
        menuInflater.inflate(R.menu.menu, menu)
        return true
    }

    override fun onOptionsItemSelected(item: MenuItem) : Boolean {

        when (item.itemId) {

            R.id.pagina_um -> {

                val intent = Intent(this@MainActivity, PaginaUm::class.java)

                startActivity(intent)
                return true
            }

            R.id.pagina_dois -> {

                val intent = Intent(this@MainActivity, PaginaDois::class.java)

                startActivity(intent)
                return true
            }

            else -> return super.onOptionsItemSelected(item)
        }

    }

}

```


![](https://s26.postimg.org/6c2og6f6x/menu.png)


# As opções para o menu ficam no xml de nome menu.xml dentro da pasta menu

```xml
<?xml version="1.0" encoding="utf-8"?>
<menu xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent">
    <item
        android:id="@+id/pagina_um"

        android:title="Página Um"
        />

    <item
        android:id="@+id/pagina_dois"

        android:title="Página Dois"
        />


</menu>


```
