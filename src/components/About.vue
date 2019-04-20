<template>
    <b-container id='About'>
        <b-row class='text'>
            <b-col>
                <h1>{{json.name}}</h1>
            </b-col>
        </b-row>
        <b-row class='text'>
            <b-col md='8' order='2' order-md='1'>
                {{json.text1}}
                <br>
                <br>
                {{json.text2}}
            </b-col>
            <b-col md='4' class='align-self-center' order='1' order-md='2'>
                <img src='../assets/Mama.png' alt='Logo'>
            </b-col>
        </b-row>
    </b-container>
</template>

<script>
export default {
    name: 'About',
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

