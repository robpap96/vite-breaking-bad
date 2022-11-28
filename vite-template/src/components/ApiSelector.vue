<script>
//import AppName  from './....AppName.vue'

export default {
    name: 'ApiSelector',
    components: {

    },
    defineProps :{
        //msg: String
    },
    data(){
        return {
            //
        }
    },


}
</script>

<template>
    <div class="category">
        <select class="form-select" aria-label="Default select example">
            <option selected>Select Category</option>
            <option value="1">One</option>
            <option value="2">Two</option>
            <option value="3">Three</option>
        </select>
    </div>

</template>

<style scoped>
    .category{
        width: 200px;
    }
</style>
