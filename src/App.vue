<template>
  <div id="app">
    <h1>Przykładowa Strona</h1>
    <Text1 v-bind:textToDisplay1='textToDisplay1'/>
    <Text2 v-bind:textToDisplay2='textToDisplay2'/>
  </div>
</template>

<script>
import Text1 from './components/Text1.vue'
import Text2 from './components/Text2.vue'


export default {
  name: 'app',
  components: {
    Text1,
    Text2
  },
  data() {
    return {
      textToDisplay1 : {
          id : 1,
          text : 'Przykładowy tekst do wyświetlenia'
        },
      textToDisplay2 : {
          id : 2,
          text : 'Inny tekst do wyświetlenia'
        }
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
