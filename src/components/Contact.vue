<template>
    <b-container id='Contact'>
        <b-row class='text'>
            <b-col align-self="start">
                <h1>{{json.name}}</h1>
            </b-col>
        </b-row>
        <br>
        <b-row>
            <b-col align-self="center" md='3' order='1' order-md='3'> 
            </b-col>
            <b-col align-self="center" md='6' order='2' order-md='2'>
                <br>
                <a id="zl-url" class="zl-url" href="https://www.znanylekarz.pl/elzbieta-ciolek-zelechowska/psycholog/katowice" rel="nofollow" data-zlw-doctor="elzbieta-ciolek-zelechowska" data-zlw-type="big_with_calendar" data-zlw-opinion="false" data-zlw-hide-branding="true">
                    Elżbieta Ciołek-Żelechowska - ZnanyLekarz.pl
                </a>
                <br>
                <h5>
                    <center><font-awesome-icon icon="phone" /> {{json.text2}}</center>
                </h5>
            </b-col>
            <b-col align-self="center" md='3' order='3' order-md='1'> 
            </b-col>
        </b-row>
        <br>
        <br>
        <br>
        <b-row class='text'>
            <b-col md='8' class='align-self-center'>
                <gmap-map :center= "center" :zoom= "zoom" style="width:100%;  height: 600px;">
                    <!-- <gmap-marker :position.sync=markerPos1 :clickable="true"></gmap-marker> -->
                    <gmap-marker :position.sync=markerPos2 :clickable="true"></gmap-marker>
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
                <!-- <br>
                <br>
                <b>{{json.text9}}</b>
                <br>
                <font-awesome-icon icon="map-marker-alt" /> {{json.text10}} -->
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
            // markerPos1: { lat: 50.274189, lng: 18.861862 },
            markerPos2: { lat: 50.252806, lng: 19.012073 },
            name: '',
            surname: '',
            phone: '',
            msg: '',
            validateForm: false
        }
    },
    created: function () {
        !function($_x,_s,id){
            var js,fjs=$_x.getElementsByTagName(_s)[0];
            if(!$_x.getElementById(id)){
                js = $_x.createElement(_s);
                js.id = id;
                js.src = "//platform.docplanner.com/js/widget.js";
                fjs.parentNode.insertBefore(js,fjs);
            }
        }(document,"script","zl-widget-s");
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

