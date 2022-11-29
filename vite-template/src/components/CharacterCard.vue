<script>
//import AppName  from './....AppName.vue'
import {store} from "../store.js";

export default {
    name: 'CharacterCard',
    components: {

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
        counter(index){
            

        }
    }

}
</script>

<template>  

    <div class="card mb-5" v-for="character in store.Characters">
        <img :src="`${character.img}`" class="card-img-top" :alt="`${character.name}`">
        <div class="card-body">
            <h5 class="card-title">{{character.name}}</h5>
            <h4 class="card-title">{{character.category}}</h4>
            <h3 class="card-title">{{character.status}}</h3>
        </div>


</div>

</template>

<style lang="scss" scoped>
    .card{
        width: calc(100% / 5 - 30px);
        img{
            width: 100%;
            height: 250px;
        }
    }
</style>
