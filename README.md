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

### public
É onde ficam os arquivos públicos e estáticos, como o index principal do projeto com a div de id app id="app" e o favicon
* index.html - arquivo raiz do projeto

### src
É a pasta que se refere a fonte do projeto, onde ficam as lógicas, é nessa pasta que fica a main.js.
* main.js - é o arquivo de entrada do Vue, é por ele que tudo começa

#### assets
É a pasta que armazena os ativos como imagens, videos, css globais

#### components
É onde fica os componentes

## Como criar um componente

1. Crie seu componente dentro da pasta components com a extensão .vue
2. Seu componente precisa ter <template> <script> <style>

* Como importar um component dentro do outro

1. No <template> chame o componente assim <NomeDoComponente/>
2. No <scrip> importe ele assim import NomeDoComponente from './components/NomeDoComponente.vue'
3. Ainda no <script> no export que representa o objeto de itens do componente exporte ele assim export default { components: { NomeDoComponente } }