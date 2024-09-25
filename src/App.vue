<template>
  <SlotComponent />
</template>

<script>
import SlotComponent from './components/SlotComponent.vue';

//import HeaderComponent from './components/HeaderComponent.vue';
//import LifeCycleComponent from './components/LifeCycleComponent.vue';
//import NewsletterComponent from './components/NewsletterComponent.vue';

export default {
  name: 'App',
  components: {
    SlotComponent
    //HeaderComponent,
    //NewsletterComponent,
    //LifeCycleComponent
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
