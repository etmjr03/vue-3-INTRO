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

1. Crie seu componente dentro da pasta components com a extensão .vue
2. Seu componente precisa ter <template> <script> <style>

## Como importar um component dentro do outro

1. No <template> chame o componente assim <NomeDoComponente/>
2. No <scrip> importe ele assim import NomeDoComponente from './components/NomeDoComponente.vue'
3. Ainda no <script> no export que representa o objeto de itens do componente exporte ele assim export default { components: { NomeDoComponente } }

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

## Variáveis

* Para criar uma variável você vai adicionar o objeto de conteúdo do componente a função data(){ return { variavel: 'valor da variavel' } }
