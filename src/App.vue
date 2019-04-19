<template>
  <div id="app">

    <b-container>
      <b-navbar :sticky="true" toggleable="md" type="light" class="nav-background">
          <b-navbar-brand href="#"><img src="./assets/logoNavbar.png" alt="Logo"> Elżbieta Ciołek-Żelechowska, Psycholog</b-navbar-brand>
            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

            <b-collapse id="nav-collapse" is-nav>
            <b-navbar-nav class="ml-auto">
                <b-nav-item href="#Text1" v-scroll-to="{el: '#Text1', offset: -170}">{{json.textToDisplay1.name}}</b-nav-item>
                <b-nav-item href="#Text2" v-scroll-to="{el: '#Text2', offset: -170}">{{json.textToDisplay2.name}}</b-nav-item>
                <b-nav-item href="#Text2" >Oferta</b-nav-item>
                <b-nav-item href="#Text2" >Kontakt</b-nav-item>
            </b-navbar-nav>
            </b-collapse>
        </b-navbar>

      <br>
      <br>

      <Text1 v-bind:json='json.textToDisplay1'/>

      <br>
      <br>

      <Text2 v-bind:json='json.textToDisplay2'/>
    </b-container>
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
  body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif !important;
    background: #fafafa !important; 
    color: #222;
    padding: 2rem;
    margin: auto;
  }

  .nav-background {
    background: #fafafa;
    min-height: 50px;
    margin: auto;
  }



</style>
