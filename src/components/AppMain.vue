<script>
import CharacterList from './CharacterList.vue';
export default{
    name:'Main',
    components:{
        CharacterList
    }
}

</script>


<template>
    <main class="p-5">
        <div class="container p-3">
            <CharacterList></CharacterList>
        </div>
    </main>
</template>


<style lang="scss" scoped>

main{
    background-color: #d48f38;
}

.container{
    height: 600px;
    background-color: white;
}

</style>
