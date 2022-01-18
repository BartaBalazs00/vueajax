<template>
  <div id="app">
    <button @click="statue = !statue">Statue</button>
    <button @click="painting = !painting">Paintings</button>
    <div v-if="statue"><Statues/></div>
    <div v-if="painting"><Paintings/></div>
  </div>
</template>

<script>

import Statues from './components/Statues.vue'
import Paintings from './components/Paintings.vue'

export default {
  name: 'App',
  components: {
    Statues,
    Paintings
  },
  data(){
    return{
    statue : false,
    painting : false,
    }
  },
  
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
