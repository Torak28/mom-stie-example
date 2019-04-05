<template>
  <div id="app">
    <h1>Lorem Ipsum</h1>
    <Text1 v-bind:json='json.textToDisplay1'/>
    <Text2 v-bind:json='json.textToDisplay2'/>
  </div>
</template>

<script>
import Text1 from './components/Text1.vue'
import Text2 from './components/Text2.vue'

import json from './json/data.json'

export default {
  name: 'app',
  components: {
    Text1,
    Text2
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
  margin-top: 60px;
}
</style>
