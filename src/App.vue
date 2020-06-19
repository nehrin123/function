<template>
  <div id="app">
    <buttons/>
    <cascade/>
    <Checkbox/>
  </div>
</template>

<script>

import buttons from './components/buttons.vue'
import cascade from './components/cascade.vue'
import Checkbox from './components/Checkbox.vue'
export default {
  name: 'App',
  components: {
    buttons,
    cascade,
    Checkbox
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
