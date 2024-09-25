<script>
export default {
  beforeUnmount(){
    console.log('beforeUnmount');
    console.log('estado: ',this.nome);
    console.log('DOM: ',this.$el);
    console.log('-----------------');
    window.removeEventListener('resize', this.resize);
  },
  unmounted(){
    console.log('unmounted');
    console.log('estado: ',this.nome);
    console.log('DOM: ',this.$el);
    console.log('-----------------');
  },
  mounted(){
    alert('O component foi montado :)')
    window.addEventListener('resize', this.resize);
  },
  methods: {
    resize(){
      console.log(`width: ${window.innerWidth} - height: ${window.innerHeight}`);
    }
  }
}
</script>

<template>
  <div>
    <h1>Teste de life Cycle</h1>
  </div>
</template>

<style>

</style>