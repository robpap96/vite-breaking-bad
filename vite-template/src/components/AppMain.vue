<script>
import ApiSelector  from './ApiSelector.vue';
import CharacterSection  from './CharacterSection.vue';
import {store} from "../store.js";
import axios from "axios";

export default {
    name: 'AppMain',
    components: {
        ApiSelector,
        CharacterSection,
    },
    defineProps :{
        //msg: String
    },
    data(){
        return {
            store,
        }
    },  
    methods: {
    
    },
    created(){
        axios.get("https://www.breakingbadapi.com/api/characters")
        .then((resp) => {
            this.store.Characters = resp.data;
        });
    },



}
</script>

<template>
    <div class="container p-3">
        <ApiSelector/>
        <div class="character-section mt-5">
            <CharacterSection/>

        </div>
    </div>
</template>

<style lang="scss" scoped>
    .character-section {
        background-color: #f8f9fa;
    }
</style>
