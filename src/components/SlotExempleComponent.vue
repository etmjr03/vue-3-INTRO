<script>
export default {
  mounted() {
    console.log(this.$slots);
  }
}
</script>

<template>
  <div class="slot">
    <h1 class="title">
      <slot name="titulo" />
    </h1>
    <p class="default" v-if="$slots.default">
      <slot />
    </p>
  </div>
</template>

<style>
.slot{
  width: 100%;
  background: #562694;
  color: #FFF;
}
</style>