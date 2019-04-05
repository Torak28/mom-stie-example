<template>
  <div id="app">
    <div>
      <b-navbar toggleable="lg" type="dark" variant="info">
        <b-navbar-brand href="#">NavBar</b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <b-nav-item href="#Text1">Link1</b-nav-item>
            <b-nav-item href="#Text2">Link2</b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
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
}
</style>
