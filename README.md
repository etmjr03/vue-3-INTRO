# vue3

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).



## Estrutura de pastas Vue 3

## public
É onde ficam os arquivos públicos e estáticos, como o index principal do projeto com a div de id app id="app" e o favicon
* index.html - arquivo raiz do projeto

## src
É a pasta que se refere a fonte do projeto, onde ficam as lógicas, é nessa pasta que fica a main.js.
* main.js - é o arquivo de entrada do Vue, é por ele que tudo começa

## assets
É a pasta que armazena os ativos como imagens, videos, css globais

## components
É onde fica os componentes

## Como criar um componente

* Crie seu componente dentro da pasta components com a extensão .vue
* Seu componente precisa ter template script style

<br>

## Como importar um component dentro do outro

* No <template> chame o componente assim <NomeDoComponente/>
* No <scrip> importe ele assim import NomeDoComponente from './components/NomeDoComponente.vue'
* Ainda no <script> no export que representa o objeto de itens do componente exporte ele assim export default { components: { NomeDoComponente } }

```js
    <template>
        <NomeDoComponente/>
    </template>

    <script>
        import NomeDoComponente from './components/NomeDoComponente.vue';

        export default { 
            components: { 
                NomeDoComponente 
            } 
        }
    </script>
```

## Diretivas

* As diretivas são as instruções que o vue da para os elementos HTML e os componentes e elas começam com v-

## Diretivas condicionais

* v-show - é para exibição, se for false o elemento vai existir, mas ele vai adicionar display none

* v-if - também é para exibição, se for false ele vai remover o elemento da DOM

* v-else-if - quando a condição dele for verdadeira ele irá exibir

* v-else - quando não for nenhuma das condições do if ou else if ele irá exibir

## Diretiva bind

* É utilizado para acessar itens do objeto dinamicamente, por exemplo para adicionar uma url de imagem que será retornado pela api v-bind:src="obj.url", mas você pode utilizar somente : no lugar o v-bind

## Diretiva v-model

* É utilizado para alterar o valor da variável pelos 2 atuadores, como uma via de mão dupla

## Diretiva de evento v-on

* É utilizado para chamar funções em um elemento HTML, vc pode substituir a diretiva v-on:click="nomeDaFuncao()" por @click="nomeDaFuncao()"
* Para identificar um evento você pode utilizar no parâmetro da função a variável $evt funcao($evt)
* Você pode modificar o comportamento do envento, como o de submit por exemplo, segue o <a href="https://vuejs.org/guide/essentials/event-handling.html" target="_blank">Link</a>
* Para adicionar eventos de mouse use @mouseover="passouMouse"
* Para utilizar eventos de click use @keyup.enter="apertouEnter", segue o <a href="https://vuejs.org/guide/essentials/event-handling.html#key-modifiers" target="_blank">Link</a>

## Variáveis

* Para criar uma variável você vai adicionar o objeto de conteúdo do componente a função 

```js
export default {
    data(){ 
        return { 
            variavel: 'valor da variavel' 
        } 
    }
}
```

## Computed

* É possível computar valores dentro da instancia do vue e utiliza-los a medida do necessário, como por exemplo ao invés de chamar duas propriedades de nome e sobrenome para formar o nome completo, você pode criar uma função no computed, concatena-las e retornar

```js
export default {
    computed: { 
        nomeCompleto(){ 
            return `${this.usuario.nome} $this.usuario.sobrenome`; 
        }
    }
}
```

* Para pendurar o vue.js é necessário adicionar window.app = antes do create do vue createApp(App).mount('#app')

## Whatch

* É possível escutar alguma alteração em uma variável, para isso declare uma função com o mesmo nome da variável, assim:

```js
export default {
    whatch: { 
        nomeDaVariavel(){
            console.log('teste');
        } 
    }
}
```

* Para poder observar alterações em um objeto você deve usar o seguinte padrão: 

```js
usuario: {
      handler(usuario){
        console.log('Usuario alterado: ' + usuario.primeiroNome + ' ' + usuario.sobrenome);
      },
      deep: true
    }
```
