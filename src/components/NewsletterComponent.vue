<template>
  <div class="div-principal">
    <h2 class="texto-titulo">Utilizando v-model</h2>

    <br>

    <h4>Alterar valor de input</h4>
    <p>Digite seu nome</p>
    <input 
      v-model="nome"
      type="text"
    >
    <p>Nome digitado: {{ nome }}</p>
    <hr>

    <h4>Selecionar opções</h4>
    <p>Jogos</p>
    <select v-model="produto">
      <option value="">selecione</option>
      <option value="tênis">Tênis</option>
      <option value="short">Short</option>
    </select>
    <p>Jogo selecionado: {{ produto }}</p>
    <hr>

    <h4>Selecionar uma opção</h4>
    <p>Assinar newsletter</p>
    <input v-model="newsletter" type="radio" value="sim">
    <input v-model="newsletter" type="radio" value="nao">
    <p>{{ newsletter }}</p>
    <hr>

    <h4>Selecionar uma checkbox</h4>
    <p>Assinar contrato</p>
    <input v-model="contrato" type="checkbox">Aceita nossos contratos
    <p>Aceito: {{ contrato }}</p>
    <hr>

    <h4>Selecionar varias opções</h4>
    <p>Selecione suas marcas preferidas</p>
    <input type="checkbox" v-model="marcas" value="Nike">Nike
    <input type="checkbox" v-model="marcas" value="Adidas">Adidas
    <input type="checkbox" v-model="marcas" value="Vans">Vans
    <input type="checkbox" v-model="marcas" value="Gucci">Gucci
    <p>Marcas selecionadas: {{ marcas }}</p>
    <hr>

    <h2 class="texto-titulo">Utilizando eventos</h2>

    <br>

    <h4>Evento de click</h4>
    <button @click="onClick()">Enviar</button>
    <hr>

    <h4>Evento de mouse</h4>
    <span @mouseover="passouMouse" class="mouse">Seu mouse passou aqui</span>
    <hr>

    <h4>Evento de envio de Formulário</h4>
    <form 
      @submit.prevent="enviouFormulario"
      action="https://google.com"
      >
      <button type="submit">Enviar formulário</button>
    </form>
    <hr>

    <h4>Evento de tecla específica</h4>
    <p>Digite algo e aperte enter para confirmar</p>
    <input @keyup.enter="apertouEnter">
    <button @click="instanciaVue">Clica aqui</button>
    <hr>

    <h2 class="texto-titulo">Utilizando computed</h2>
    <br>

    <h4>Concatenando nome completo</h4>
    <p>Nome completo: {{ nomeCompleto }}</p>
    <hr>

    <h4>Todo list</h4>

    <p class="text-todos">Completadas</p>
    <div 
      v-for="todo in todosCompletadas"
      :key="todo.id"
    >
      {{ todo.title }} - concluídas: {{ todo.completed }}
    </div>

    <p class="text-todos">Não completadas</p>
    <div 
      v-for="todo in todosNaoCompletadas"
      :key="todo.id"
    >
      {{ todo.title }} - concluída: {{ todo.completed }}
    </div>

    <p class="text-todos">Lista de Todos</p>
    <div
      v-for="todo in todos"
      :key="todo.id"
    >
      <input 
        v-model="todo.completed"
        type="checkbox"
      >{{ todo.title }}
    </div>
    <hr>
  </div>
</template>

<script>
  export default {
    data(){
      return {
        nome: 'Juninho',
        usuario: {
          primeiroNome: 'Juninho',
          sobrenome: 'dev'
        },
        produto: '',
        newsletter: 'sim',
        contrato: false,
        marcas: [],
        todos: [
          {
            "userId": 1,
            "id": 1,
            "title": "delectus aut autem",
            "completed": true,
            "url": "https://via.placeholder.com/150/d32776",
          },
          {
            "userId": 1,
            "id": 2,
            "title": "quis ut nam facilis et officia qui",
            "completed": true,
            "url": "https://via.placeholder.com/150/d32776",
          },
          {
            "userId": 1,
            "id": 3,
            "title": "fugiat veniam minus",
            "completed": false,
            "url": "https://via.placeholder.com/150/d32776",
          },
          {
            "userId": 1,
            "id": 4,
            "title": "et porro tempora",
            "completed": true
          },
          {
            "userId": 1,
            "id": 5,
            "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
            "completed": false
          }
        ]
      }
    },
    methods: {
      onClick(){
        alert('Enviou :)')
      },
      passouMouse($evt){
        alert('Mouse passou aqui :)')
        console.log($evt);
      },
      enviouFormulario(){
        alert('Enviou o formulário :)')
      },
      apertouEnter(){
        alert('Enviado :)')
      },
      instanciaVue(){
        console.log(this.usuario);
      }
    },
    computed: {
      nomeCompleto(){
        return `${this.usuario.primeiroNome} ${this.usuario.sobrenome}`
      },
      todosCompletadas(){
        return this.todos.filter(todo => todo.completed)
      },
      todosNaoCompletadas(){
        return this.todos.filter(todo => !todo.completed)
      }
    }
  }
</script>

<style>
  hr{
    width: 500px;
  }
  .div-principal{
    margin-bottom: 20px;
  }
  .texto-titulo{
    color: #13a360;
  }
  .text-todos{
    font-weight: 700;
    color: #f87e2c;
  }
  .mouse{
    display: flex;
    margin: 20px auto;
    padding: 10px;
    width: 200px;
    color: #FFF;
    background: #13a360;
    justify-content: center;
    border-radius: 15px;
  }
</style>