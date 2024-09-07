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
    <hr>
  </div>
</template>

<script>
  export default {
    data(){
      return {
        nome: 'Juninho',
        produto: '',
        newsletter: 'sim',
        contrato: false,
        marcas: []
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