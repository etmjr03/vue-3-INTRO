<template>
  <div class="menu">
    <div 
      v-for="obj in todos"
      :key="obj.id"
    >
    <div v-if="obj.url">
      <span>{{ obj.title }}</span>
      <img 
        v-if="obj.url"
        :src="obj.url" 
        :alt="obj.title"
      >
    </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'App',
    data() {
      return {
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
</style>