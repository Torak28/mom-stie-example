<template>
    <div id='Text2'>
        <div class='text'>
            <h2>{{json.name}}</h2>
            <h3>{{json.text}}</h3>
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

