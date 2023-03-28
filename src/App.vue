<script >
import axios from 'axios';
import { store } from './store'
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

export default {
    name: 'App',
    components: {
        AppHeader,
        AppMain
    },
    data() {
        return {
            store
        }
    },
    created() {

        axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
            .then((response) => {
                this.store.archetype = response.data;
            })
            .catch((error) => {
                    console.log(error);
                    this.store.archetype = [];
                })


    },
    methods: {
        searchType() {
            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php', {
                params: {
                    archetype: store.searchType
                }
            })
                .then((response) => {
                    this.store.characters = response.data.data;
                    this.store.charactersFound = response.data.data.length;
                })
                .catch((error) => {
                    console.log(error);
                    this.store.characters = [];
                    this.store.charactersFound = 0;
                })
        }
    }
}


</script>

<template>
    <AppHeader></AppHeader>
    <AppMain @prova="searchType"></AppMain>
</template>
