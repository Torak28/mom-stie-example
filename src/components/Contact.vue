<template>
    <b-container id='Contact'>
        <b-row class='text'>
            <b-col align-self="start">
                <h1>{{json.name}}</h1>
            </b-col>
        </b-row>

        <br>

        <b-row>
            <b-col>
                <b-form>
                    <b-input id="Imie" placeholder="Imię"></b-input>
                </b-form>
            </b-col>
            <b-col>
                <b-form>
                    <b-input id="Nazwisko" placeholder="Nazwisko"></b-input>
                </b-form>
            </b-col>
        </b-row>

        <br>

        <b-row>
            <b-col>
                <b-form>
                    <b-input id="Telefon" placeholder="Numer Telefonu"></b-input>
                </b-form>
            </b-col>
        </b-row>

        <br>

        <b-row>
            <b-col>
                <b-form>
                    <b-form-textarea id="Wiadomosc" placeholder="Napisz tutaj swoją wiadomość" rows="3" no-resize></b-form-textarea>
                </b-form>
            </b-col>
        </b-row>

        <br>

        <b-row class='text-center'>
            <b-col>
                <b-button block variant="primary">Wyślij</b-button>
            </b-col>
        </b-row>

        <br>
        <br>
        <br>

        <b-row class='text-center'>
            <b-col>
                <h5>{{json.text1}}
                <br>
                <font-awesome-icon icon="envelope" /> <b-link href="mailto:ezelechowska@poczta.onet.pl"> {{json.text3}} </b-link>
                <br>
                <font-awesome-icon icon="phone" /> {{json.text2}}</h5>
            </b-col>
        </b-row>
        <br>
        <br>
        <b-row class='text'>
            <b-col md='8' class='align-self-center'>
                <gmap-map :center= "center" :zoom= "zoom" style="width:100%;  height: 600px;">
                    <gmap-marker :position.sync=markerPos1 :clickable="true"></gmap-marker>
                    <gmap-marker :position.sync=markerPos2 :clickable="true"></gmap-marker>
                    <gmap-marker :position.sync=markerPos3 :clickable="true"></gmap-marker>
                    <gmap-marker :position.sync=markerPos4 :clickable="true"></gmap-marker>
                </gmap-map>
            </b-col>
            <b-col md='4' class='text-center'>
                <br>
                <br>
                <br>
                <h5>{{json.text4}}</h5>
                <b>{{json.text5}}</b>
                <br>
                <font-awesome-icon icon="map-marker-alt" /> {{json.text6}}
                <br>
                <br>
                <b>{{json.text7}}</b>
                <br>
                <font-awesome-icon icon="map-marker-alt" /> {{json.text8}}
                <br>
                <br>
                <b>{{json.text9}}</b>
                <br>
                <font-awesome-icon icon="map-marker-alt" /> {{json.text10}}
                <br>
                <br>
                <b>{{json.text11}}</b>
                <br>
                <font-awesome-icon icon="map-marker-alt" /> {{json.text12}}
            </b-col>
        </b-row>
    </b-container>
</template>

<script>
export default {
    name: 'Contact',
    props: ['json'],
    data() {
        return {
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


<style scope>
    .text {
        text-align: justify;
        text-justify: inter-word;
    }
    h1 {
        background: linear-gradient(180deg, rgba(255,255,255,0) 65%, #FFD0AE 65%);
        display: inline;
    }
    img {
        max-width: 100%;
        height: auto;
    }
</style>

