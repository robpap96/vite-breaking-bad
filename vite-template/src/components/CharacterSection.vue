<script>
import CharacterCard  from './CharacterCard.vue';
import CharactersCounter  from './CharactersCounter.vue';
import {store} from "../store.js";

export default {
    name: 'CharacterSection',
    components: {
        CharacterCard,
        CharactersCounter,
    },
    defineProps: {
        //msg: String
    },
    data() {
        return {
            store,
        }
    },



}
</script>

<template>
    <div class="p-4">
        <CharactersCounter/>
    </div>
    <div class="row justify-content-between flex-wrap p-5">
        <CharacterCard
            v-for="character in store.Characters"
            class="p-5 mb-5"
        />

    </div>

</template>

<style lang="scss" scoped>

</style>
