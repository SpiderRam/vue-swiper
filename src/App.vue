<template>
  <div id="app">
    <app-grid></app-grid>
  </div>
</template>

<script>
import GridVue from './components/Grid.vue';
export default {
  data() {
    return {

    }
  },
  components: {
    appGrid: GridVue
  },
  props: {
    
  }
}
</script>

<style scoped>
  #app {
    background-image: linear-gradient(#cfe2cf, #609f60);
    min-height: 100vh;
  }
</style>