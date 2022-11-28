<script>

export default {
    name: 'CharacterCounter',
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
    <div class="container-fluid p-3">
       <span>Found .. Characters</span>
    </div>

</template>

<style lang="scss" scoped>
    .container-fluid {
        background-color: #212529;
    }
    span {
        color: white;
    }
</style>
