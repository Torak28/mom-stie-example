<template>
  <div id="app">
    <test v-bind:textToDisplay='textToDisplay'/>
  </div>
</template>

<script>
import test from './components/test.vue'

export default {
  name: 'app',
  components: {
    test
  },
  data() {
    return {
      textToDisplay  : [
        {
          id : 1,
          text : 'Przykładowy tekst do wyświetlenia'
        },
        {
          id : 2,
          text : 'Dalszy tekst do wyświetlenia'
        }
      ]
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
