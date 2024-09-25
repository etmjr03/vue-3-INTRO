<script>
import SlotExempleComponent from './SlotExempleComponent.vue';

export default {
  components: {
    SlotExempleComponent
  }
}
</script>

<template>
  <SlotExempleComponent>
    <template v-slot:titulo>Título aplicado pelo slot</template>
  </SlotExempleComponent>
</template>

<style>

</style>