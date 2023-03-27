<script>
    export default {
        name: 'CharacterCard',
        props: {
            img: String,
            name: String,
            type: String,
        }
    }
</script>


<template>
    <article class="text-center">   
        <div class="img"><img class="img-fluid" :src="img"></div>
        <h3>{{  name }}</h3>
        <div>{{ type}}</div>
    </article>
</template>


<style lang="scss" scoped>
</style>