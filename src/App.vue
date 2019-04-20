<template>
  <div id="app">

    <b-container>
      <b-navbar :sticky="true" toggleable="md" type="light" class="nav-background">
          <b-navbar-brand href="#"><img src="./assets/logoNavbar.png" alt="Logo"> Elżbieta Ciołek-Żelechowska, Psycholog</b-navbar-brand>
            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

            <b-collapse id="nav-collapse" is-nav>
            <b-navbar-nav class="ml-auto">
                <b-nav-item href="#About" v-scroll-to="{el: '#About', offset: -170}">{{json.textToDisplay1.name}}</b-nav-item>
                <b-nav-item href="#Help" v-scroll-to="{el: '#Help', offset: -170}">{{json.textToDisplay2.name}}</b-nav-item>
                <b-nav-item href="#Oferta" >Oferta</b-nav-item>
                <b-nav-item href="#Contact" v-scroll-to="{el: '#Contact', offset: -170}">{{json.textToDisplay4.name}}</b-nav-item>
            </b-navbar-nav>
            </b-collapse>
        </b-navbar>

      <br>
      <br>

      <About v-bind:json='json.textToDisplay1'/>

      <br>
      <br>

      <Help v-bind:json='json.textToDisplay2'/>

      <br>
      <br>

      <Contact v-bind:json='json.textToDisplay4'/>
    </b-container>
  </div>
</template>

<script>
import About from './components/About.vue'
import Help from './components/Help.vue'
import Contact from './components/Contact.vue'

import json from './json/data.json'

export default {
  name: 'app',
  components: {
    About,
    Help,
    Contact
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
