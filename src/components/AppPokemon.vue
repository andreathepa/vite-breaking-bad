<script>
export default {
    props:{
        myPokemon: Object
    }
}
</script>
<template lang="">
    <div class="text-center p-5">
        <img :src="myPokemon.imageUrl" class="img-fluid mb-2" alt="myPokemon.info">
        <div>{{ myPokemon.number }}</div>
        <div>{{ myPokemon.name }}</div>
        <div>{{ myPokemon.type1 }}</div>
    </div>
</template>
<style lang="scss" scoped>
    
</style>