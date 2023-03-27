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
       <div class="row g-3">
            <div class="col-12 col-sm-3" v-for="character in store.characters">
                <CharacterCard :img="character.card_images[0].image_url" :name="character.name" :type="character.type"  />
            </div>
       </div>
    </div>
</template>



<style lang="scss" scoped>
</style>