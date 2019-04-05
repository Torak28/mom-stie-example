<template>
    <div id='Text1'>
        <div class='text'>
            <h2>{{json.name}}</h2>
            {{json.text}}
        </div>
    </div>
</template>

<script>
export default {
    name: 'Text1',
    props: ['json']
}
</script>


<style scope>
    .text {
        text-align: justify;
        text-justify: inter-word;
    }
</style>

