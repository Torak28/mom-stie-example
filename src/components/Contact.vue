<template>
    <b-container id='Contact'>
        <b-row class='text'>
            <b-col align-self="start">
                <h1>{{json.name}}</h1>
            </b-col>
        </b-row>
        <b-row class='text'>
            <b-col align-self="start">
            </b-col>
            <b-col align-self="center">
                {{json.text1}}
                <br>
                {{json.text2}}
                <br>
                {{json.text3}}
            </b-col>
            <b-col align-self="end">
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
</style>

