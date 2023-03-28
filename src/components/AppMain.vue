<script>
import { store } from '../store';
import CharacterList from './CharacterList.vue';
export default {
    name: 'Main',
    components: {
        CharacterList
    },
    data() {
        return {
            store
        }
    }
}

</script>


<template>
    <main class="p-5">
        <div class="mb-3 col-12 col-sm-auto">
            <label for="search-status" class="form-label d-none">Select Status</label>
            <select style="width: auto" class="form-select" id="search-status">
                <option selected>Select Status</option>
                <option value="1">One</option>
                <option value="2">Two</option>
                <option value="3">Three</option>
            </select>
        </div>
        <div class="container p-3">
            <section class="p-3">
                <h2>Found {{ store.charactersFound }} cards</h2>
            </section>
            <CharacterList></CharacterList>
        </div>
    </main>
</template>


<style lang="scss" scoped>
main {
    background-color: #d48f38;
}

.container {
    background-color: white;

    section {
        background-color: #212529;

        h2 {
            color: white;
        }
    }
}
</style>
