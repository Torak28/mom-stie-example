<template>
    <b-container id='Help'>
        <b-row class='justify-content-end'>
            <b-col md='8'>
                <h1>{{json.name}}</h1>
            </b-col>
        </b-row>
        <b-row>
            <b-col md='4' class='align-self-center'>
                <img src="../assets/Przykład1.png" alt="Logo">
            </b-col>
            <b-col md='8' class='text'>
                 {{json.text1}}
                <br>
                <br>
                {{json.text2}}
                <br>
                <br>
                {{json.text3}}
                <br>
                <br>
                {{json.text4}}
            </b-col>
        </b-row>
    </b-container>
</template>

<script>
export default {
    name: 'Help',
    props: ['json']
}
</script>


<style scope>
    .text {
        text-align: justify;
        text-justify: inter-word;
    }
</style>

