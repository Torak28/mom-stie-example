<template>
    <div class="container" id='About'>
        <div class='text row'>
            <div class='col'>
                <h1>{{json.name}}</h1>
            </div>
        </div>
        <div class='text row'>
            <div class='col-8'>
                {{json.text1}}
                <br>
                <br>
                {{json.text2}}
            </div>
            <div class='col-4 align-self-center'>
                <img src="../assets/Mama.png" alt="Logo">
            </div>
        </div>
    </div>
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

