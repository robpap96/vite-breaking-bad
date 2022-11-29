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
            <h3 class="card-title">{{character.name}}</h3>
            <h4 class="card-title">{{character.category}}</h4>
            <h5 class="card-title">{{character.status}}</h5>
        </div>


</div>

</template>

<style lang="scss" scoped>
    .card{
        width: calc(100% / 5 - 30px);
        background-color: #2e3a46;
        border-radius: 0px;
        img{
            width: 100%;
            height: 250px;
            margin-top: 10px;
            border-radius: 0px;
        }
    }
    .card-body{
        h3{
            font-size: 20px;
            color: rgb(225, 234, 242);
        }
        h4{
            font-size: 18px;
            color: rgb(107, 107, 107);
        }
        h5{
            font-size: 17px;
            color: rgb(107, 107, 107);
        }
    }
</style>
