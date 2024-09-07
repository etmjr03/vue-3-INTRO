<template>
  <HeaderComponent v-show="exibirMenu" />
  <img alt="Vue logo" src="./assets/logo.png">
  <div v-if="exibitNome">Quem está logado: {{ nomeUsuario }}</div>
  <div v-if="nivelUsuario == 'Admin'">Admin</div>
  <div v-else-if="nivelUsuario == 'Programador'">Programador</div>
  <div v-else>Comum</div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'

export default {
  name: 'App',
  components: {
    HeaderComponent
  },
  data() {
    return {
      exibirMenu: true,
      nomeUsuario: 'Usuario Admin',
      exibitNome: true,
      nivelUsuario: 'Admin'
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
