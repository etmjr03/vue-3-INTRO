<template>
  <div>
    <p>Digite seu nome</p>
    <input 
      v-model="nome"
      type="text"
    >
    <p>Nome digitado: {{ nome }}</p>
    <label for="">Jogos</label>
    <select v-model="produto">
      <option value="">selecione</option>
      <option value="tênis">Tênis</option>
      <option value="short">Short</option>
    </select>
    <p>Jogo selecionado: {{ produto }}</p>

    <br>

    <label for="">Assinar newsletter</label>
    <input v-model="newsletter" type="radio" value="sim">
    <input v-model="newsletter" type="radio" value="nao">
    <p>{{ newsletter }}</p>

    <br>

    <label for="">Assinar contrato</label>
    <input v-model="contrato" type="checkbox">Aceita nossos contratos
    <p>Aceito: {{ contrato }}</p>

    <br>

    <label for="">Selecione suas marcas preferidas</label>
    <input type="checkbox" v-model="marcas" value="Nike">Nike
    <input type="checkbox" v-model="marcas" value="Adidas">Adidas
    <input type="checkbox" v-model="marcas" value="Vans">Vans
    <input type="checkbox" v-model="marcas" value="Gucci">Gucci
    <p>Marcas selecionadas: {{ marcas }}</p>
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
    }
  }
</script>

<style>

</style>