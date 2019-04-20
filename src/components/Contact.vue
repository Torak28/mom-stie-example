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
                    <b-input id="Mail" placeholder="Mail"></b-input>
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
                <font-awesome-icon icon="envelope" /> {{json.text3}}
                <br>
                <font-awesome-icon icon="phone" /> {{json.text2}}
                <br>
                <br>
                <br>
                {{json.text4}}
                <br>
                <font-awesome-icon icon="map-marker-alt" /> {{json.text5}}</h5>
            </b-col>
        </b-row>
    </b-container>
</template>

<script>
export default {
    name: 'Contact',
    props: ['json']
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
    .test{
        background: #ff0000 !important; 
    }
    .test2{
        background: #002fff !important; 
    }
</style>

