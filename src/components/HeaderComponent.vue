<template>
  <h1 :class="{'titulo': true, 'tituloMaior': isHome}">Título da página</h1>
  <br>
  <span v-if="exibitNome">Quem está logado: {{ nomeUsuario }} - perfil: </span>
  <span v-if="nivelUsuario == 'Admin'">Admin</span>
  <span v-else-if="nivelUsuario == 'Programador'">Programador</span>
  <span v-else>Comum</span>
  <br>
</template>

<script>
  export default {
    name: 'App',
    data() {
      return {
        isHome: true,
        classeTitulo: 'titulo',
        nomeUsuario: 'Usuario Admin',
        exibitNome: true,
        nivelUsuario: 'Admin',
        todos: [
            {
                "userId": 1,
                "id": 1,
                "title": "delectus aut autem",
                "completed": false,
                "url": "https://via.placeholder.com/150/d32776",
            },
            {
                "userId": 1,
                "id": 2,
                "title": "quis ut nam facilis et officia qui",
                "completed": false,
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
    }
  }
</script>

<style>
  .menu{
    width: 100%;
    background: #1a1919;
    position: fixed;
    top: 0;
  }
  .titulo{
    color: #1a1919;
    font-size: 24px;
  }
  .tituloMaior{
    font-size: 30px;
  }
</style>