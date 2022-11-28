<script>
import ApiSelector  from './ApiSelector.vue'

export default {
    name: 'AppMain',
    components: {
        ApiSelector,

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
    <div class="container p-3">
        <ApiSelector/>

    </div>
</template>

<style scoped>

</style>
