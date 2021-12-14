<template>
  <div id="app" class="small-container">
    <simulator/>
  </div>
</template>

<script>
  import Simulator from '@/components/simulator.vue'

  export default {
    name: 'app',
    components: {
      Simulator,
    },
  }
</script>

<style>
  button {
    background: #009435;
    border: 1px solid #009435;
  }

  .small-container {
    max-width: 680px;
  }
</style>