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
                <b-button
                :class="showCollapseA ? 'collapsed' : null"
                :aria-expanded="showCollapseA ? 'true' : 'false'"
                @click="showCollapseA = !showCollapseA"
                >
                    <font-awesome-icon :icon="appIcon1" v-b-toggle.collapse-2 class="m-1" /> 
                </b-button>
            </b-card-text>
            <b-card-text class='text-left'>
                <b-collapse id="A" v-model="showCollapseA" class='m-1'>
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
                <b-button
                :class="showCollapseB ? 'collapsed' : null"
                :aria-expanded="showCollapseB ? 'true' : 'false'"
                @click="showCollapseB = !showCollapseB"
                >
                    <font-awesome-icon :icon="appIcon2" v-b-toggle.collapse-2 class="m-1" /> 
                </b-button>
            </b-card-text>
            <b-card-text class='text-left'>
                <b-collapse id="B" v-model="showCollapseB" class='m-1'>
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
                <b-button
                :class="showCollapseC ? 'collapsed' : null"
                :aria-expanded="showCollapseC ? 'true' : 'false'"
                @click="showCollapseC = !showCollapseC"
                >
                    <font-awesome-icon :icon="appIcon3" v-b-toggle.collapse-2 class="m-1" /> 
                </b-button>
            </b-card-text>
            <b-card-text class='text-left'>
                <b-collapse id="C" v-model="showCollapseC" class='m-1'>
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
import { faChevronRight } from '@fortawesome/free-solid-svg-icons'
import { faChevronDown } from '@fortawesome/free-solid-svg-icons'

export default {
    name: 'Ofer',
    props: ['json'],
    data() {
        return {
            showCollapseA : false,
            showCollapseB : false,
            showCollapseC : false
        }
    },
    computed: {
        appIcon1() {
            return this.showCollapseA ? faChevronRight : faChevronDown
        },
        appIcon2() {
            return this.showCollapseB ? faChevronRight : faChevronDown
        },
        appIcon3() {
            return this.showCollapseC ? faChevronRight : faChevronDown
        },
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

