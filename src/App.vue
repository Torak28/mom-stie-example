<template>
  <div id="app">

    <b-container>
        <b-navbar :sticky="true" toggleable="md" type="light" class="nav-background">
          <b-navbar-brand href="#">
            <img src="./assets/logoNavbar.png" alt="Logo">
          </b-navbar-brand>
          <h4 class='d-md-none d-sm-none d-none d-lg-block'>Elżbieta Ciołek-Żelechowska, Psycholog</h4>
          <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
          
          <b-collapse id="nav-collapse" is-nav>
            <b-navbar-nav class="ml-auto">
              <b-nav-item href="#About" v-scroll-to="{el: '#About', offset: -210}">{{json.textToDisplay1.name}}</b-nav-item>
              <b-nav-item href="#Help" v-scroll-to="{el: '#Help', offset: -210}">{{json.textToDisplay2.name}}</b-nav-item>
              <b-nav-item href="#Oferta" v-scroll-to="{el: '#Ofer', offset: -210}">{{json.textToDisplay3.name}}</b-nav-item>
              <b-nav-item href="#Contact" v-scroll-to="{el: '#Contact', offset: -210}">{{json.textToDisplay4.name}}</b-nav-item>
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

    <Ofer v-bind:json='json.textToDisplay3'/>

    <br>
    <br>

    <Contact v-bind:json='json.textToDisplay4'/>

    <br>

    <b-row class='text-center'>
      <b-col>
        <small class="text-muted">© 2019, Jarek Ciołek-Żelechowski</small>
      </b-col>
    </b-row>

    </b-container>
    <footer>
      <cookie-law :buttonText=json.cookieButton :message=json.cookieMessage theme="base"></cookie-law>
    </footer>
  </div>
</template>

<script>
import About from './components/About.vue'
import Help from './components/Help.vue'
import Ofer from './components/Ofer.vue'
import Contact from './components/Contact.vue'

import json from './json/data.json'

import CookieLaw from 'vue-cookie-law'

export default {
  name: 'app',
  components: {
    About,
    Help,
    Ofer,
    Contact,
    CookieLaw
  },
  data() {
    return {
      json,
      center: { lat: 50.2226782, lng: 18.9739298 },
      zoom: 10,
      markerPos1: { lat: 50.231156, lng: 18.997150 },
      markerPos2: { lat: 50.294132, lng: 18.654360 },
      markerPos3: { lat: 50.254317, lng: 19.033358 },
      markerPos4: { lat: 50.274189, lng: 18.861862 }
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
