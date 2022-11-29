<script>
//import AppName  from './....AppName.vue'
import {store} from "../store.js";

export default {
    name: 'ApiSelector',
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
        print(a){
            console.log(a);
        }
    },
    computed: {
        filteredList() {

        }
    }

}
</script>

<template>
    <div class="category">
        <select v-model="store.category" class="form-select" aria-label="Default select example">
            <option selected>Category</option>
            <option value="Breaking Bad">Breaking Bad</option>
            <option value="Better Call Saul">Better Call Saul</option>
            
        </select>
    </div>

</template>

<style lang="scss" scoped>
    .category{
        width: 200px;
    }
</style>
