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
    <div class="p-4">
        <CharacterCard
            v-for="character in store.Characters"
        />
    </div>

</template>

<style lang="scss" scoped>

</style>
