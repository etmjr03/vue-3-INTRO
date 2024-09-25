<script>
import TestLifeCycleComponent from './TestLifeCycleComponent.vue';

export default {
  data() {
    return {
      nome: "juninho",
      showTest: false
    }
  },
  components: {
    TestLifeCycleComponent
  },
  beforeUpdate() {
    console.log('beforeUpdate');
    console.log('estado: ',this.nome);
    console.log('DOM: ',this.$el);
    console.log('-----------------');
  },
  updated() {
    console.log('updated');
    console.log('estado: ',this.nome);
    console.log('DOM: ',this.$el);
    console.log('-----------------');
  }
  // beforeCreate(){
  //   console.log('beforeCreate');
  //   console.log('estado: ',this.nome);
  //   console.log('DOM: ',this.$el);
  //   console.log('-----------------');
  // },
  // created(){
  //   console.log('created');
  //   console.log('estado: ',this.nome);
  //   console.log('DOM: ',this.$el);
  //   console.log('-----------------');
  // },
  // beforeMount(){
  //   console.log('beforeMount');
  //   console.log('estado: ',this.nome);
  //   console.log('DOM: ',this.$el);
  //   console.log('-----------------');
  // },
  // mounted(){
  //   console.log('mounted');
  //   console.log('estado: ',this.nome);
  //   console.log('DOM: ',this.$el);
  //   console.log('-----------------');
  // }
}
</script>

<template>
  <div>
    <TestLifeCycleComponent v-if="showTest"/>
    <h1>Aplicando o conceito de life Cycle</h1>
    <input type="text" v-model="nome" value="{{ nome }}">
    {{ nome }}
    <br>
    <br>
    <button @click="showTest = !showTest">Ativar e desativar o Test</button>
  </div>
</template>

<style>

</style>