<template>
    <div>
        <h1>Przykładowa Strona</h1>
        <div v-bind:key='textToDisplay.id' v-for='example in textToDisplay'>
            <h3>{{example.text}}</h3>
        </div>
    </div>
</template>

<script>
export default {
    name: 'test',
    props: ['textToDisplay']
}
</script>


<style scope>

</style>

