<template>
  <div id="app">
    <b-container>
      <Navbar v-bind:json='json'/>
      <h1>Żółć ąęźżćś</h1>
      <Text1 v-bind:json='json.textToDisplay1'/>
      <Text2 v-bind:json='json.textToDisplay2'/>
    </b-container>
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
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
  line-height: 1.6;
  color: #222;
  padding: 2rem;
  margin: auto;
  background: #fafafa;
}
</style>
