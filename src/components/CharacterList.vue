<script>
import { store } from '../store';
import CharacterCard from './CharacterCard.vue';

    export default {
        name:'CharacterList',
        components: {
            CharacterCard
        },
        data() {
            return {
                store
            }
        },
        
    }
</script>

<template>
    <div class="container">
       <div class="row row-cols-sm-1 row-cols-lg-5 g-3">
            <div class="col" v-for="character in store.characters.slice(0,100)">
                <CharacterCard :img="character.card_images[0].image_url" :name="character.name.toUpperCase()" :type="character.archetype"  />
            </div>
       </div>
    </div>
</template>



<style lang="scss" scoped>
</style>