<template>
  <HeaderComponent v-show="exibirMenu" />
  <NewsletterComponent />
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import NewsletterComponent from './components/NewsletterComponent.vue';

export default {
  name: 'App',
  components: {
    HeaderComponent,
    NewsletterComponent
  },
  data() {
    return {
      exibirMenu: true,
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
  color: #000;
  margin-top: 60px;
}
</style>
