<template>
    <div>
        <div class='text'>
            <h3>{{json.text}}</h3>
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

