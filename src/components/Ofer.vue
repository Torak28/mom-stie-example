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
            <b-card-text class ='text-center'>
                <br>
                <br>
                <br>
                <font-awesome-icon icon="question-circle" v-b-toggle.collapse-1 class="m-1"></font-awesome-icon>
            </b-card-text>
            <b-card-text class='text-left'>
                <b-collapse id="collapse-1">
                    <b>{{json.text1CollPart}}</b> 
                    <li v-for="item in json.text1FollowDown" :key='item.text'>
                        {{item.text}}
                    </li>
                </b-collapse>
            </b-card-text>
            <div slot="footer"><small class="text-muted">{{json.text1Footer}}</small></div>
            </b-card>

            <b-card :title='json.text2' :img-src="require('../assets/individual.png')" img-alt="Image" img-top>
            <b-card-text class='text'>
                {{json.text2FollowUp}}
            </b-card-text>
            <b-card-text class ='text-center'>
                <br>
                <font-awesome-icon icon="question-circle" v-b-toggle.collapse-1 class="m-1"></font-awesome-icon>
            </b-card-text>
            <b-card-text class='text-left'>
                <b-collapse id="collapse-1">
                    <b>{{json.text2CollPart}}</b> 
                    <li v-for="item in json.text2FollowDown" :key='item.text'>
                        {{item.text}}
                    </li>
                </b-collapse>
            </b-card-text>
            <div slot="footer"><small class="text-muted">{{json.text2Footer}}</small></div>
            </b-card>

            <b-card :title='json.text3' :img-src="require('../assets/group.png')" img-alt="Image" img-top>
            <b-card-text class='text'>
                {{json.text3FollowUp}}
            </b-card-text>
            <b-card-text class ='text-center'>
                <font-awesome-icon icon="question-circle" v-b-toggle.collapse-1 class="m-1"></font-awesome-icon>
            </b-card-text>
            <b-card-text class='text-left'>
                <b-collapse id="collapse-1">
                    <b>{{json.text3CollPart}}</b> 
                    <li v-for="item in json.text3FollowDown" :key='item.text'>
                        {{item.text}}
                    </li>
                </b-collapse>
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

