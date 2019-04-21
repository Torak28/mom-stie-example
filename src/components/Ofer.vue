<template>
    <b-container id='Ofer'>
        <b-row class='text'>
            <b-col align-self="start">
                <h1>{{json.name}}</h1>
            </b-col>
        </b-row>

        <br>

        <b-card-group deck>
            <b-card :title='json.text1' :img-src="require('../assets/therapy.png')" img-alt="Image" img-top>
            <b-card-text class='text'>
                {{json.text1FollowUp}}
            </b-card-text>
            <div slot="footer"><small class="text-muted">{{json.text1Footer}}</small></div>
            </b-card>

            <b-card :title='json.text2' :img-src="require('../assets/individual.png')" img-alt="Image" img-top>
            <b-card-text  class='text'>
                {{json.text2FollowUp}}
            </b-card-text>
            <div slot="footer"><small class="text-muted">{{json.text2Footer}}</small></div>
            </b-card>

            <b-card :title='json.text3' :img-src="require('../assets/group.png')" img-alt="Image" img-top>
            <b-card-text  class='text'>
                {{json.text3FollowUp}}
            </b-card-text>
            <div slot="footer"><small class="text-muted">{{json.text3Footer}}</small></div>
            </b-card>
        </b-card-group>

    </b-container>
</template>

<script>
export default {
    name: 'Ofer',
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
</style>

