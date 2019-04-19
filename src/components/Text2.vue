<template>
    <div class="container" id='Text2'>
        <div class='text row justify-content-end'>
            <div class='col-8'>
                <h1>{{json.name}}</h1>
            </div>
        </div>
        <div class='text row'>
            <div class='col-4 align-self-center'>
                <img src="../assets/Przykład1.png" alt="Logo">
            </div>
             <div class='col-8'>
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
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Text2',
    props: ['json']
}
</script>


<style scope>
    .text {
        text-align: justify;
        text-justify: inter-word;
    }
</style>

