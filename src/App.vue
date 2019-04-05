<template>
  <div id="app">
    <Navbar v-bind:json='json'/>
    <h1>Lorem Ipsum</h1>
    <Text1 v-bind:json='json.textToDisplay1'/>
    <Text2 v-bind:json='json.textToDisplay2'/>
  </div>
</template>

<script>
import Text1 from './components/Text1.vue'
import Text2 from './components/Text2.vue'
import Navbar from './components/Navbar.vue'

import json from './json/data.json'

export default {
  name: 'app',
  components: {
    Text1,
    Text2,
    Navbar
  },
  data() {
    return {
      json
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
